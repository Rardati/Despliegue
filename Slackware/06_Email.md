## Email under Linux

**Exercise 6.1 Sending email using mail**

- Primero me aseguro de tener los paquetes necesarios para enviar el email. Instalaremos el paquete mailutils y el de sendemail.

![C1.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C1.jpg)
![C1a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C1a.jpg)

-  Creamos el archivo message.txt con algún mensaje.
![C2.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C2.jpg)

- Me da error
![Error.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/Error.jpg)

- Instalamos el paquete postfix
![C1b.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C1b.jpg)

- Vuelvo a crear un archivo llamado message.txt con un mensaje para Bob
![C3.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C3.jpg)

- Modifico el mensaje 
![C3nano.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C3nano.jpg)

- Enviamos el correo con el siguiente comando
![C3b.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C3b.jpg)




**Parte 2**
- echo "Welcome to Network Computer Systems" → Imprime el mensaje en pantalla y lo pasa como entrada al siguiente comando.
- | → Redirige la salida del comando echo como entrada para mail.
- mail -s "Hello world" → Envía un correo con el asunto "Hello world".
- bob@anglia.bryant → Destinatario principal del correo.
- -c smith@anglia.bryant → Envía una copia (CC) a Smith.
- -b root@anglia.bryant → Envía una copia oculta (BCC) a Root.



**Exercise 6.2 Checking email**

- Comando mail
![C4.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C4.jpg)
![C4_1.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C4_1.jpg)


**Exercise 6.3 Exploring mail**
- Responder a un mensaje:

Para responder a un mensaje, estando dentro de mail, escribe r y luego el número del mensaje.
Escribe tu respuesta, luego presiona Ctrl+D para enviarla.

- Enviar un mensaje:

Desde dentro de mail, escribe m para componer un nuevo mensaje.
Ingresa la dirección de destino, el asunto y el cuerpo del mensaje.
Luego presiona Ctrl+D para enviar el correo.

- Eliminar un mensaje:

Para eliminar un mensaje, estando en la lista de correos en mail, escribe d seguido del número del mensaje a eliminar y presiona ENTER.

- Listar los correos:

Cuando estés en mail, si deseas ver la lista de correos, simplemente escribe h y presiona ENTER.

- Guardar un mensaje:

Para guardar un mensaje en un archivo, usa s y luego especifica el nombre del archivo al que guardarás el mensaje.

- Ayuda:

Para ver las opciones de ayuda dentro de mail, simplemente escribe ? y presiona ENTER.


![C4a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C4a.jpg)
![C4b.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C4b.jpg)


**Parte 2 What is contained in /var/spool/mail/? What are the security implications ofthis?**
- /var/spool/mail/
Esta carpeta contiene los buzones de correo de los usuarios en el sistema. Cada usuario tiene un archivo con su nombre en este directorio, como /var/spool/mail/bob, donde se almacenan los correos recibidos. 

- Implicaciones de seguridad:

Si un atacante obtiene acceso a este directorio, podría leer los correos de cualquier usuario.
La carpeta debe tener permisos restrictivos para proteger la privacidad de los usuarios, asegurándose de que solo el usuario y el administrador tengan acceso.
El directorio debe tener permisos 700 (solo lectura, escritura y ejecución para el propietario).

**Parte 3**

**Parte 4**

**Parte 5**


**Parte 6. What ports are used by SMTP and POP3?**




**Exercise 6.4 Optional exercises**
1. What is IMAP? List the differences between POP3 andIMAP.

- IMAP (Internet Message Access Protocol) es un protocolo estándar de acceso a correo electrónico que permite a los usuarios gestionar sus correos en el servidor en lugar de descargarlos a su dispositivo. Es muy útil para quienes necesitan acceder al correo desde múltiples dispositivos (como teléfonos, computadoras, tabletas, etc.), ya que los mensajes permanecen en el servidor y no se descargan permanentemente a un solo dispositivo.

- Las diferencias:
POP3 es más adecuado para usuarios que solo usan un dispositivo y desean descargar y almacenar sus correos localmente.
IMAP es más adecuado para usuarios que acceden a sus correos desde diferentes dispositivos, ya que mantiene los correos en el servidor y permite una sincronización completa.


2. What is PGP encryption? How does it work?
PGP (Pretty Good Privacy) es un sistema de cifrado que asegura la privacidad, la autenticidad y la integridad de las comunicaciones electrónicas, utilizando un par de claves públicas y privadas para cifrar y verificar los mensajes.
Su principal función es garantizar que el contenido de un mensaje sea confidencial y que el remitente sea quien dice ser.

