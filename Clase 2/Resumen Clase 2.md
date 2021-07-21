# **Resumen Clase 2**

En la clase #2 Vimos los comandos necesarios para instalar el docker en ubuntu.
1. Lo primero que realizamos fue iniciar las maquinas virtuales de ubunto.
2. Debido a que no se puede copiar y pegar los comandos de instalacion de Docker, descargamos Mobax para conectarnos con la maquina.
3. Una vez descargado el programa ejecutamos el comando sudo apt-get install openssh-server.
4. Luego nos conectamos por medio de la Ip

Ahora, una vez conectados empezamos con los comandos para instalar los paquetes necesarios.

1. El primer comando sudo apt-get update lo realizamos para actualizar los paquetes de la maquina.
2. Luego los instalamos con sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release.
3. Luego agregamos la llave de Docker con el siguiente comando curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg.
4. Luego descargamos Docker con el siguiente comando echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
5. Instalamos Docker con  
sudo apt-get update 
sudo apt-get install docker-ce docker-ce-cli containerd.io
6. Una vez instalado lo corremos sudo docker run hello-world
7. Para verificar que Docker este instalado correctamente, ejecutamos el siguiente comando.
sudo docker run hello-world

Ahora procedemos con la instalacion del Docker Compose

1. Para eso ejecutamos el siguiente comando sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose.
2. Y le damos permisos sudo chmod +x /usr/local/bin/docker-compose.
3. Clonamos el repositorio donde esta la aplicacion git clone https://github.com/jsgiraldoh/Codimd.git
4. Iniciamos el contenedor con sudo docker-compose up -d
5. y lo abrimos en el puerto que nos indica, en este caso es el 3000 junto con la ip de la maquina. Y listo
