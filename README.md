# Reporte Técnico de Configuración de Laboratorio

## 1. Fundación: VirtualBox y Red Aislada

Para la máquina virtual se configuró la red en modo **NAT**. Esta configuración permite que la máquina virtual tenga acceso a Internet utilizando la conexión del equipo anfitrión, sin quedar expuesta directamente como un dispositivo independiente dentro de la red local.

La utilización de NAT permite realizar las prácticas y descargar actualizaciones manteniendo un nivel de aislamiento respecto del equipo Host.

### Evidencia – Configuración de red en VirtualBox

> Archivo: `capturas/01-red-nat.png`

---

## 2. Capa de usuarios y actualizaciones

Para las prácticas se utilizó un entorno Linux basado en Debian. Se creó y utilizó un usuario sin privilegios administrativos para las tareas habituales, evitando trabajar permanentemente como usuario `root`.

También se realizó la búsqueda de actualizaciones de los paquetes del sistema mediante la terminal, manteniendo el sistema preparado para las prácticas.

### Evidencia – Usuario del sistema

> Archivo: `capturas/02-usuario.png`

### Evidencia – Actualización del sistema


> Archivo: `capturas/03-apt-update.png`

---

## 3. Capa Linux: Permisos y Gestión

Se creó un archivo dentro del sistema y se utilizó el comando `ls -l` para visualizar sus permisos.

Este comando permite comprobar quién es el propietario del archivo y qué permisos poseen el propietario, el grupo y los demás usuarios del sistema. La gestión adecuada de permisos ayuda a evitar accesos o modificaciones no autorizadas.

### Evidencia – Permisos de archivo mediante `ls -l`


> Archivo: `capturas/04-permisos-ls-l.png`

---

## 4. Red de Seguridad: Snapshot Inicial

Como último paso se creó una instantánea de la máquina virtual denominada **"Hardening Inicial"**.

El Snapshot permite conservar el estado de la máquina en este punto y recuperar esta configuración en caso de que durante futuras prácticas se produzca algún problema o se realicen modificaciones que afecten el funcionamiento del sistema.

### Evidencia – Snapshot "Hardening Inicial"


> Archivo: `capturas/05-snapshot-hardening-inicial.png`

---
