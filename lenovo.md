<!-- TITLE: Lenovo -->
<!-- SUBTITLE: Datos sobre el servidor Lenovo -->

# Acceso principal
* url: [https://192.168.0.111:8006](https://192.168.0.111:8006)
* user: root
* pass: matafuegos

# Máquinas virtuales
## pi-hole
site: proliant
os: Ubuntu 18.04 LTS
storage: local-zfs
type: ct
id: 160
url: 192.168.0.160
user: root
pass: pihole

## campus
site: proliant
os: Ubuntu 18.04 LTS
storage: local-zfs
type: ct
id: 161
url: 192.168.0.161
uservm: root
passvm: campus

## gitea
site: proliant
os: Debian 9
storage: wdgold01
type: ct
id: 166
url: 192.168.0.166
uservm: root
passvm: gitea
pass: matafuegO$

## wiki.js
site: proliant
storage: local-zfs
type: ct
id: 200
url: 192.168.0.200
uservm: root
passvm: wikijs
userapp: itelnetworking@gmail.com
passapp: matafuegos

## guti
site: proliant
storage: local-zfs
type: ct
id: 162
url: 192.168.0.162
uservm: root
passvm: matafuegos
userapp: javier
passapp: javier

