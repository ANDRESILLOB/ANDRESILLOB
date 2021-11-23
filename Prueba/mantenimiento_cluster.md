# Mantenimiento del Cluster ECCI

Para realizar el amntenimiento al cluster lo primero es que tipo de uso se le esta dando:

- Conexión remota grafica (anydesk)
- Conexión remota consola (Putty)


## Conexión remota grafica ( Anydesk )

La conexión remota consume recursos de la tarjeta grafica, es por consiguiente tener actualizado los controladores con los que se encuentra trabajando y tener cuidado al momento de instalar y desinstalar programas de ubuntu, para ello se recomienda que al instalara o desinstalar, realizarle una actualización automatica del sistema

```shell
sudo apt update

sudo apt upgrade
```
## No hay conexión con Anydesk

El no haber conexión de anydesk deja sin acceso a traves del entorno grafico al equipo, pero la conexion por consola va a existir, un opcion es entrar por consola a realizar la reparación, sino se puede obener el acceso por consola, se debera entrar a anydesk a otro equipo y desde alli realizar el proceso de reparación de consola.

El daño para el acceso puede ocurri por una de las siguientes causas:

* Instalación de programas donde se modifique las librerias del entorno grafico
* Instalación de programas y no realizar una actualización previa, y por ello genere conflictos o bucles, se recomienda antes de instalar cualquier programa actualizar el sistema antes
* La no actualización periodica del equipo
* Dejar corriendo codigos o pruebas que generen bucles o bugs, donde el usuario este cerrado

Para resolver lo anterior tenemos los siguientes pasos

```shell
sudo ubuntu-drivers autoinstall

```

Este código generara una revisión automatica del sistema e instalara los controladores que se necesitan para funcionar , ya sean porque se borraron o fueron cambiados

```shell
sudo apt-get dist-upgrade

```

Esta línea de código permite instalar los paquetes que no se dejan instalara mediante el *sudo apt update* y *sudo apt upgrade* 

## Conexión remota consola ( Putty )

La conexión remota se trabaja a traves de terminal, es una conexion eficiente y muy rapida, problemas no genera y desde la misma consola se puede arreglar cualquier problema, no genera fallos, a diferencia de una conexion remota por los recursos, para ello se puede realizar periodicamente cada semana la actualizacion :

```shell
sudo apt update

sudo apt upgrade
```
