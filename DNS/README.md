 ### DNS ###

## Resolucion
- **Resolución directa:** Se consulta un nombre de dominio para obtener su dirección IP correspondiente (por ejemplo, introducir "www.ejemplo.com" y obtener "192.168.1.1").

- **Resolución inversa:** Consiste en consultar una dirección IP para obtener el nombre de dominio asociado (por ejemplo, introducir "192.168.1.1" y obtener "www.ejemplo.com").

## Nombre de dominio
Un nombre de dominio es una cadena de texto que se asigna a una dirección IP numérica, que se utiliza para acceder a un sitio web desde el software cliente.
El DNS (Domain Name System, Sistema de Nombres de Dominio) es un conjunto de protocolos y servicios que permite a los usuarios utilizar nombres en vez de tener que recordar direcciones IP numéricas. Ésta es ciertamente la función más conocida de los protocolos DNS: la asignación de nombres a direcciones IP.

## Niveles de dominio
-**El primer nivel** (TLD, Top Level Domain o Dominio de Nivel Superior) es el que hay a la derecha del todo. Como por ejemplo “.es” en “www.aspl.es”.
-**El segundo nivel** (dominio), es el TLD mas el nombre que hay al lado. En “www.aspl.es” sería “aspl.es”.
-**El tercer nivel** (nombre de máquina o subdominio) se forma con los 3 niveles juntos. En el ejemplo de “www.aspl.es” sería “www.aspl.es”.

## Zonas de busqueda
Zonas de búsqueda directa: Contienen las asignaciones de los nombres de dominio con sus respectivas direcciones IP. Cuando un usuario introduce un nombre de dominio, la zona de búsqueda directa recupera la dirección IP asignada en el registro DNS.

## Tipos de servidores
-**Servidor DNS recursivo (resolver):** Actúa como intermediario entre el cliente y los servidores autoritativos, haciendo todo el trabajo de búsqueda para obtener la dirección IP solicitada.

-**Servidor DNS autoritativo:** Tiene la información final sobre un dominio específico, como los registros DNS de ese dominio. Es el servidor que devuelve la respuesta definitiva en una consulta de DNS.

-**Servidor DNS raíz:** Es el primer paso en la resolución de nombres de dominio, dirigiendo las consultas a los servidores TLD (Top Level Domain). Hay un número limitado de servidores raíz a nivel global.

-**Servidor TLD (Top Level Domain):** Almacena información sobre dominios de nivel superior, como ".com", ".org" o ".es", y redirige a los servidores autoritativos de los dominios correspondientes.

## Registros
Son instrucciones radicadas en servidores DNS autoritativos que proporcionan información sobre un dominio, como la dirección IP asociada con este y cómo gestionar solicitudes dirigidas a dicho dominio.

-**Registro A:** registro que contiene la dirección IP de un dominio.
-**Registro AAAA:** El registro que contiene la dirección IPv6 de un dominio (a diferencia de los registros A, que enumeran la dirección IPv4).
-**Registro CNAME:** reenvía un dominio o subdominio a otro dominio, NO proporciona una dirección IP. 
-**Registro MX:** dirige el correo a un servidor de correo electrónico.
-**Registro TXT:** Permite que un administrador pueda almacenar notas de texto en el registro. Estos registros se suelen utilizar para la seguridad del correo electrónico.
-**Registro NS:** almacena el servidor de nombres para una entrada DNS.
-**Registro SOA:** almacena la información del administrador sobre un dominio.
-**Registro SRV:** especifica un puerto para servicios específicos.
-**Registro PTR:** proporciona un nombre de dominio en búsquedas inversas.

# Funcionamiento


        - Consulta recursiva : Una búsqueda de DNS recursivo es cuando un servidor DNS se comunica con otros servidores DNS para buscar una dirección IP y devolverla al cliente.

        - Consulta iterativa : Una consulta iterativa indica que el servidor aceptará una referencia a otro servidor, en lugar de una respuesta definitiva a la consulta.
