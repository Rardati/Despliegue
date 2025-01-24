## Exercise 4.1 Exploring currently running processes
- instalar openbsd-inetd
![C1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/C1.png)


- ps aux 
![Cpsaux1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cpsaux1.png)

- top
![Ctop2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Ctop2.png)

-  Presionamos q para salir.
 ![Cq3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cq3.png)

- Ver imagen:
![C4.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/C4.png)

Explicacion de 5 procesos: 
Systemd es un sistema de inicialización y gestión de servicios para sistemas Linux.
kthreadd su función principal es crear y gestionar otros hilos de kernel. 
rcu_gp (Read-Copy-Update Graceful Preemption)  se encarga de la sincronización de datos compartidos en el núcleo. 
rcu_par_gp es similar a rcu_gp .
netns (network namespaces) es un proceso que permite aislar y organizar redes dentro del mismo sistema. 


## Exercise 4.2 Exploring network processes
- nmap localhost
![Cnmap.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cnmap.png)

ssh:  es un protocolo de red que permite una comunicación segura y cifrada entre dos sistemas, como un cliente y un servidor remoto.
Proporciona una forma segura de acceder y gestionar servidores desde cualquier lugar.
domain: es un nombre único y exclusivo que identifica un sitio web o dirección de correo electrónico en la red. Son clave para 
la identificación y accesibilidad de sitios web y direcciones de correo electrónico en Internet.

- ps aux | grep nombre_proceso
![Cgrep.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cgrep.png)

-

![Cinetd.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cinetd.png)


## Exercise 4.3 Exploring UNIX signals

- Comando kill -l
![Ckill1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Ckill1.png)


**Explica qué hace este comando y resume los resultados**
1 SIGHUP Hang up detectado en la terminal de control 
2 SIGINT Interrupción desde el teclado 
3 SIGQUIT Salir del teclado 
4 SIGILLInstrucción ilegal 
5 SIGTRAP Trampa de seguimiento 
6 SIGABRT Abrt de la función abort() 
7 SIGEMT Ejecución de instrucción emulada 
8 SIGFPE Excepción de punto flotante 
9 SIGKILL Matriz el proceso (no puede ser capturado ni ignorado) 
10 SIGUSR1 Senal definida por el usuario 1 
11 SIGSEGV Referencia de memoria inválida 
12 SIGUSR2 Senal definida por el usuario 2 
13 SIGPIPE Escribir en un tubo con ningún lector 
14 SIGALRM Tiempo de reloj expiró 
15 SIGTERM Senal de terminación de software

## Exercise 4.4 Processes and networking


![Cinstalltelnet.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cinstalltelnet.png)
![Cnano.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapturasD/Cnano.png)




