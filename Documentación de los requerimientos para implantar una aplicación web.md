# **Documentación de los requerimientos para implantar una aplicación web**

## **Índice**

* Requisitos de hardware y software.
* Infraestructura de red.
* Configuración del servidor web y de aplicaciones.
* Seguridad y mantenimiento.


### **Requisitos de hardware y software**
Para poder instalar y ejecutar una aplicación web correctamente, necesitamos un equipo que tenga los recursos suficientes para que funcione sin problemas.

**Hardware:**
* **Procesador:** uno que tenga suficiente potencia para ejecutar el servidor y atender a los usuarios.
  
* **Memoria RAM:** como mínimo 4 GB para un entorno de pruebas, aunque es recomendable disponer de más si la aplicación es grande.
  
* Almacenamiento: espacio suficiente para el sistema operativo, la aplicación, las bases de datos y los archivos que se utilicen.

  
* Conexión a Internet para descargar actualizaciones y permitir el acceso a la aplicación cuando sea necesario.

  
**Software:**
* Sistema operativo, como Ubuntu Server.
  
* Servidor web, como Nginx o Apache.
  
* Servidor de aplicaciones, como Tomcat. 

* Docker para ejecutar aplicaciones mediante contenedores.

* Sistema gestor de bases de datos, como MySQL o PostgreSQL.


### **Infraestructura de red**

Para que una aplicación web pueda funcionar correctamente, necesita una infraestructura de red que permita la comunicación entre los usuarios y el servidor.

Algunos elementos importantes son:
* Dirección IP para identificar el servidor dentro de la red.
* Conexión a Internet para permitir el acceso desde otros equipos.
* Puertos de comunicación, como el 80 para HTTP y el 443 para HTTPS.
* Configuración del router y del firewall para controlar las conexiones.
  
En esta práctica hemos utilizado NAT en VirtualBox y hemos asignado los puertos 8080 y 8081 a los contenedores de Nginx y Tomcat.

### **Configuración del servidor web y de aplicaciones**

Para implantar una aplicación web podemos utilizar diferentes servidores dependiendo de lo que necesitemos.

En esta práctica hemos utilizado:
* **Nginx:** es un servidor web que se encarga de recibir las peticiones de los usuarios y mostrar el contenido web.
* **Tomcat:** es un servidor de aplicaciones que permite ejecutar aplicaciones desarrolladas en Java.
  
Los dos se han ejecutado mediante contenedores Docker, utilizando diferentes puertos para poder acceder a ellos desde el navegador.

### **Seguridad y mantenimiento**

La seguridad es muy importante para evitar problemas y proteger tanto el servidor como los datos de los usuarios.

Algunas medidas que debemos tener en cuenta son:
* Mantener actualizado el sistema operativo y los programas instalados.
* Utilizar contraseñas seguras.
* Configurar correctamente el firewall.
* Utilizar HTTPS para proteger la comunicación.
* Realizar copias de seguridad de los datos.
* Comprobar periódicamente que los contenedores y servidores funcionan correctamente.
* No compartir información privada ni contraseñas.
