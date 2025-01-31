## Email under Linux

**Exercise 6.1 Sending email using mail**

- Primero me aseguro de tener los paquetes necesarios para enviar el email. Instalaremos el paquete mailutils y el de sendemail.

![C1.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C1.jpg)
![C1a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C1a.jpg)

-  Creamos el archivo message.txt con algún mensaje.
![C2.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/C2.jpg)

- Me da error
![Error.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasE/Error.jpg)

**Parte 2**
- echo "Welcome to Network Computer Systems" → Imprime el mensaje en pantalla y lo pasa como entrada al siguiente comando.
- | → Redirige la salida del comando echo como entrada para mail.
- mail -s "Hello world" → Envía un correo con el asunto "Hello world".
- bob@anglia.bryant → Destinatario principal del correo.
- -c smith@anglia.bryant → Envía una copia (CC) a Smith.
- -b root@anglia.bryant → Envía una copia oculta (BCC) a Root.





