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
