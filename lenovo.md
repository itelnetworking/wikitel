<!-- TITLE: Lenovo -->
<!-- SUBTITLE: Datos sobre el servidor Lenovo -->

# Acceso principal
* url: [https://192.168.0.111:8006](https://192.168.0.111:8006)
* user: root
* pass: matafuegos

# Máquinas virtuales
### service: pi-hole
site: proliant
storage: local-zfs
type: ct
id: 160
url: 192.168.0.160
user: root
pass: pihole

site: proliant
storage: local-zfs
type: ct
id: 161
url: 192.168.0.161
uservm: root
passvm: campus

site: proliant
storage: wdgold01
type: ct
id: 166
url: 192.168.0.166
uservm: root
passvm: campus

site: proliant
storage: local-zfs
type: ct
id: 200
url: 192.168.0.200
uservm: root
passvm: wikijs
userapp: itelnetworking@gmail.com
passapp: matafuegos

