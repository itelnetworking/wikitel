<!-- TITLE: Servidores -->
<!-- SUBTITLE: Información y tips en relación a la gestión de servidores -->

#Agregar discos a Proxmox
Podemos agregar discos extras en Proxmox para se empleados por las máquinas virtuales o bien como espacio de almacenamiento. 

Para poder agregar elementos de _storage_ primeramente tendremos que realizar algunas acciones empleando la terminal. 


En primer lugar, listamos los discos disponibles:

```apache_conf
fdisk -l
```

Veremos que los discos del sistema se verán con el siguiente formato `/dev/sdX` donde `X` corresponde a una letra (a, b, c, d, etc) y que dependerá de la cantidad de discos físicos instalados en el equipo. 

