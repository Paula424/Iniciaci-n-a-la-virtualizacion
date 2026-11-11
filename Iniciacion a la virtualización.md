# **Instalación de Ubuntu en VirtualBox**

1. **Descarga la ISO de Ubuntu 24.04 LTS desde la página oficial de Ubuntu.**
   
   Nos vamos a la página oficial, y le damos a descargar el ubuntu que nos inidca la tarea, y a esperar.

<img width="1366" height="768" alt="descargarUbintu1" src="https://github.com/user-attachments/assets/636e47a5-bbc5-4320-ada4-3c4f8decd94d" />

<img width="1366" height="768" alt="descargarUbuntu2" src="https://github.com/user-attachments/assets/3f31288c-8615-4374-ab59-83c1a6d35ac0" />


2. **Crea una nueva máquina virtual con las siguientes características recomendadas:**
    * *Nombre*: Ubuntu-DAW2DAW
    * *RAM*: 4096 MB
    * *Disco duro virtual*: mínimo 50 GB
    * *Tipo de red*: NAT

<img width="950" height="304" alt="creacionMaquinaVirtual1" src="https://github.com/user-attachments/assets/a8d7252a-9d52-4e4e-810e-9932ee3d42b6" />

<img width="902" height="248" alt="creacionMaquinaVirtual2" src="https://github.com/user-attachments/assets/ae4d8f93-da59-4956-95d5-5ef08ddeeecb" />

<img width="924" height="152" alt="creacionMaquinaVirtual3" src="https://github.com/user-attachments/assets/e6c87896-0bba-4176-a18b-c45192ddd517" />

<img width="895" height="371" alt="creacionMaquinaVirtual4" src="https://github.com/user-attachments/assets/9e9dd450-fc64-4d18-8745-d4d91286dfea" />

<img width="961" height="544" alt="creacionMaquinaVirtual5" src="https://github.com/user-attachments/assets/c7c2f491-c1cb-4ecb-a506-5364fc2276fa" />


3. **Instala las _Guest Additions_**

Esperamos a que se instale, esto se isntala nada mas entrar por primera vez a la máquina virtual

<img width="1335" height="691" alt="guestAditions1" src="https://github.com/user-attachments/assets/5d5a2bb1-7993-4396-bde0-5474df009f72" />

Ahora después que se termine la instalación, le damos a 

<img width="1365" height="727" alt="guestAditions2" src="https://github.com/user-attachments/assets/2c5b8607-2f4d-4e7b-ae89-2bfc61e1de22" />


Depués de darle a eso no hace nada, ahora le tenemos que dar al icino de disco que sale a la izquierda y nos abrirá una "explorador de archivos"

<img width="1365" height="730" alt="guestAditions3" src="https://github.com/user-attachments/assets/44f3bb2b-8dfd-4e16-bf1d-2933feccfacc" />

Ahora desde ahí abrimos una terminal

<img width="1365" height="726" alt="guestAditions4" src="https://github.com/user-attachments/assets/7952959c-69cc-4774-8ee6-b53eb8d42762" />

Ahora para comenzar a instalar las Guest Aditions ponemos este comnado
```
   sudo ./VBoxLinuxAdditions.run
```

<img width="1365" height="253" alt="guestAditions5" src="https://github.com/user-attachments/assets/53ec7d24-b585-4f82-9a2c-89bea90c422a" />

Y este no hace nada porque después ahi que poner este comando
```
      sudo reboot
```

<img width="1358" height="222" alt="guestAditions6" src="https://github.com/user-attachments/assets/5b39197f-1807-468c-aab5-54212deb0677" />

Y después de eso se reinicia la máquina, por eso no te he podido hacer una captura de cuando ejecuté los dos comandos.

Y despues pongo este comando para comprobar que las guest aditions están instaladas
```
   lsmod | grep vboxguest
```

<img width="1372" height="326" alt="guestAditions7" src="https://github.com/user-attachments/assets/6457bbd3-c5c3-4c50-aab4-e0a9a9565a74" />


4. **Toma una captura de pantalla del escritorio una vez instalado.**
<img width="1365" height="727" alt="guestAditions9" src="https://github.com/user-attachments/assets/ed457172-dbd3-4354-a79c-535bca7f91f5" />

<img width="1365" height="728" alt="guestAditions8" src="https://github.com/user-attachments/assets/c1fe067c-20be-4f04-854c-ddc22d23da53" />


# **Instalación de Docker en Ubuntu**

1. **Actualiza los repositorios:**
```
   sudo apt update && sudo apt upgrade -y
```

<img width="1368" height="176" alt="instalacionDocker1" src="https://github.com/user-attachments/assets/ff1ed3ea-7ed0-4fe3-bff7-f36f5a688708" />

<img width="1365" height="730" alt="instalacionDocker2" src="https://github.com/user-attachments/assets/d070cc9b-2928-4030-9de5-fa7b28b664c8" />

2. **Instala dependencias:**
```
   sudo apt install ca-certificates curl gnupg -y
```

<img width="1365" height="516" alt="instalacionDocker4" src="https://github.com/user-attachments/assets/aa11fd65-c84b-40f7-83d9-ac9322096f25" />

<img width="1365" height="102" alt="instalacionDocker3" src="https://github.com/user-attachments/assets/2326c7e5-a0ef-458a-8583-a2cc7e9c1290" />


3. **Añade el repositorio de Docker e instala Docker Desktop:**
```
  curl -fsSL https://get.docker.com | sudo sh
   sudo apt install docker-desktop -y
```

Este comando da error o parece porque no funciona

Yo use los soguientes comandos
```
   curl -fsSL https://get.docker.com -o get-docker.sh
   
   sudo sh get-docker.sh
```
<img width="1365" height="169" alt="instalacionDocker5" src="https://github.com/user-attachments/assets/94f23f1d-6dd6-4626-b1c1-ee7767ed109c" />

<img width="1365" height="180" alt="instalacionDocker6" src="https://github.com/user-attachments/assets/34adb26d-fd0d-4948-ad4c-cb8b07eb8561" />


4. **Verifica que Docker funciona correctamente:**
```
  docker --version
   docker run hello-world
```
<img width="1365" height="117" alt="instalacionDocker8" src="https://github.com/user-attachments/assets/2ed5880d-ac9d-4e5c-9ca7-661f2a5978c0" />

<img width="1365" height="261" alt="instalacionDocker9" src="https://github.com/user-attachments/assets/498e95c8-b410-4d53-894c-0ac00589c2ab" />

<img width="1365" height="729" alt="instalacionDocker10" src="https://github.com/user-attachments/assets/ce6f5995-c799-4624-a628-e6fdbfb01b43" />


# **Instalación de contenedores de servidor web y de aplicaciones**
## **Instalación en Docker**

1. **Buscar imágenes disponibles:**
```
   docker search nginx 
   docker search tomcat 
```

   Nginx

<img width="1365" height="171" alt="instalacionDocker11" src="https://github.com/user-attachments/assets/a4b3b3a5-69b7-46b6-b547-e27f495c6e5d" />

<img width="1365" height="728" alt="instalacionDocker12" src="https://github.com/user-attachments/assets/b5efdaa6-3538-48fe-a2fe-4623f8acd4f2" />

   Tomcat

<img width="1365" height="176" alt="instalacionDocker15" src="https://github.com/user-attachments/assets/6cf8c790-87e6-43de-88c1-6f53b2989001" />

<img width="1365" height="727" alt="instalacionDocker16" src="https://github.com/user-attachments/assets/52fb9254-1b1d-429f-bcd2-c239f38eec30" />


2. **Descargar e iniciar contenedores:**
```
   docker run -d -p 8080:80 --name webserver nginx 
   docker run -d -p 8081:8080 --name appserver tomcat
```

   Nginx

<img width="1365" height="61" alt="instalacionDocker13" src="https://github.com/user-attachments/assets/04fd3dd8-51b0-4786-b8e8-14bb510e409e" />

<img width="1365" height="405" alt="instalacionDocker14" src="https://github.com/user-attachments/assets/ec5b4baf-8b46-4872-8782-6ae3243f446b" />

   Tomcat

<img width="1365" height="65" alt="instalacionDocker17" src="https://github.com/user-attachments/assets/bfded71e-b8c0-4b05-bade-e5671b2f2e0c" />

<img width="1365" height="428" alt="instalacionDocker18" src="https://github.com/user-attachments/assets/b7ce419e-15b2-4ffa-8427-bd363b2e284d" />


3. **Verificar contenedores activos:**
```
   docker ps
```

<img width="1365" height="33" alt="instalacionDocker19" src="https://github.com/user-attachments/assets/6ceb4c04-8e70-4a60-8636-aaf573318f30" />

<img width="1365" height="188" alt="instalacionDocker20" src="https://github.com/user-attachments/assets/bd94660e-35ff-44f1-8a50-06dcc8c2f8f8" />


4. **Abrir en el navegador:**
   * _http://localhost:8080_ → **Nginx**

<img width="1365" height="440" alt="instalacionDocker21ç" src="https://github.com/user-attachments/assets/a6207fd4-148c-4873-a5bb-875f201c4f77" />


   * _http://localhost:8081_ → **Tomcat**

<img width="1365" height="357" alt="instalacionDocker22" src="https://github.com/user-attachments/assets/f16f41a3-296e-487c-baac-4760f9350978" />

Como vemos me dio error, entonces con ayda de la IA, lo pude solucionar, la verdad que bastante rapido y sencillo, con unos comandos.
 ```
Primero, en la terminal de Ubuntu, ejecuta:
docker ps

Comprueba que aparece tu contenedor appserver y que el puerto está así:
text
0.0.0.0:8081->8080/tcp

Después, ejecuta:
docker logs appserver

Esto nos permitirá comprobar si Tomcat se ha iniciado correctamente.
```

Me dijo esto primero, yo lo comprobé que todo estaba correcto como me pidió, y puse el comando que me dio, que como dice ahí era para comprobar si este se había iniciado correctamente.
```
docker logs appserver
```

<img width="1365" height="87" alt="instalacionDocker23" src="https://github.com/user-attachments/assets/dd3876a4-7a56-4d57-965a-09d0463739e0" />

<img width="1365" height="727" alt="instalacionDocker24" src="https://github.com/user-attachments/assets/36231b3a-06fa-421a-8c5b-65aef9a49462" />

Y me salía esto, que indicaba e resumidas cuentas que si se había iniciado.

Y me seguía saliendo el error, entonces me dio otro comando que era para que me enseñara por fin la imagen que me deberia de salir desde un prinicipio
```
En la terminal de Ubuntu, copia y pega este comando:
docker exec appserver sh -c 'cp -a /usr/local/tomcat/webapps.dist/. /usr/local/tomcat/webapps/'

¿Qué hace? Copia las aplicaciones de ejemplo que vienen con Tomcat a la carpeta desde la que Tomcat sirve las páginas web.
```
Que como explica ahí ese comando te copia las aplicaciones de ejemplo que vienen con la imagen y así conseguir que se viera y no diera error.
Te pongo el cmnado de nuevo
```
docker exec appserver sh -c 'cp -a /usr/local/tomcat/webapps.dist/. /usr/local/tomcat/webapps/'
```

<img width="1365" height="78" alt="instalacionDocke25" src="https://github.com/user-attachments/assets/5193602c-3490-4aea-b405-850776bbee08" />

<img width="1365" height="728" alt="instalacionDocker26" src="https://github.com/user-attachments/assets/5ac175da-a10b-404b-8007-903905212c8f" />

Y así pude yo solucionar lo de la imagen en el buscador de Tomcat.










