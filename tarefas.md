## Preparación
Dentro de la carpeta `task` encontrará un Playbook de Ansible para aprovisionar un nuevo servidor
Esta tarea fue preparada para ser ejecutada usando Virtualbox o Parallels.

### Imagen del servidor base
- Debian 8

### Servicios a lanzar
- nginx
- PHP7.0
- MySQL5.6

### Setup
1. cd devops-asignación / tareas
2. `vagrant up --provision`

Para ejecutar o aprovisionar nuevamente, ejecute `vagrant provision`
Acceda a la instancia a través de https (s) en `http://myplay.local`

## Tareas
### Parte 1: Fundamentos de Linux y Ansible
01. Hay uno o más errores en el Playbook ansible. Es necesario corregir los errores para que el playbook ejecute completamente.
02. Cree un rol que bloquee los puertos TCP de la máquina para permitir solo los puertos 80, 443 y 22 desde cualquier fuente
03. Configure nginx para que la página http redirija a la página https
04. Nginx no debe devolver en los encabezados la versión de Nginx. Configure el servidor para que este campo no se llene en el encabezado de respuesta
05. Crear un nuevo rol que crea usuarios en el servidor. Este rol debe crear los usuarios `dev1` y` dev2`, y los usuarios no deben tener una contraseña, sino que deben ser una autenticación de clave pública. Las claves públicas de los usuarios se pueden encontrar en el directorio `pubkeys`


### Parte 2: Docker (opcional)
06. Cree un directorio llamado `docker`
07. Migre los servicios que se ejecutan en la máquina virtual para ejecutar en los contenedores de Docker. Cada servicio debe ejecutarse en un contenedor diferente
08. Especifique el proceso para iniciar el ambiente docker creado en el punto anterior


### Parte 3: Preguntas

09. ¿Qué falta para este sistema puede ser considerado como producción? ¿Qué puntos deben revisarse?

10. Supongamos que la aplicación web ya se está ejecutando y a la vez ha comenzado a recibir una gran cantidad de tráfico. ¿Qué técnicas utilizarías para garantizar el rendimiento del sitio?

11. ¿Qué tendría que hacer si desea configurar más de un host virtual en este servidor nginx?

12. Explique brevemente: ¿Cómo haría para promover el código de entorno DEV a producción? ¿Cuántos entornos crees que necesitas y qué proceso harías para la promoción entre entornos?

13. ¿Qué es el Auto Scaling? ¿Cómo implementar? ¿Es posible tener auto escalado con contenedores?

14. ¿Qué es CI? ¿Qué es el CD? ¿Qué herramientas conoces?

15. Describa cuál sería el ideal en su opinión con respecto al monitoreo del sitio que acabamos de subir. ¿Qué debemos monitorear y qué herramientas se pueden utilizar?

16. ¿Con qué nubes públicas has trabajado?
