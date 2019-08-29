<!-- TITLE: Servidores -->
<!-- SUBTITLE: Información y tips en relación a la gestión de servidores -->

#Agregar discos a Proxmox
Podemos agregar discos extras en Proxmox para se empleados por las máquinas virtuales o bien como espacio de almacenamiento. 

Para poder agregar elementos de _storage_ primeramente tendremos que realizar algunas acciones empleando la terminal. 


**Listamos los discos físicos**

```apache_conf
fdisk -l
```

Veremos que los discos del sistema se verán con el siguiente formato `/dev/sdX` donde `X` corresponde a una letra (a, b, c, d, etc) y que dependerá de la cantidad de discos físicos instalados en el equipo. 

**Particionamos los discos**
Recurriremos para este paso al comando `cfdisk`, seguido de la unidad de disco a la cual queremos dar formato: 

```apache_conf
cfdisk /dev/sdc
```

Y nos aparecerá un menú interactivo para crear las particiones. En mi caso, solo crearé una partición, por lo tanto, quedará designada de la siguiente manera: `/dev/sdc1` (ésta será la denomación que usaremos de ahora en más en este ejemplo para referirnos a la partición creada). Para aplicar los cambios en el disco, debermos elegir la opción "Write".

**Usando LVM**
Para convertir un disco al formato LVM, deberemos indicar que el mismo pasará a ser un PV (Pyshical Volume):

```apache_conf
pvcreate /dev/sdc1
```

Luego, crearemos un grupo de volumenes, procedemos: 

```apache_conf
vgcreate WDGOLD01 /dev/sdc1
```

Donde "WDGOLD01" es el nombre que se me ocurrió darle al grupo de volúmenes. 


