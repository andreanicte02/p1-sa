# Aplicación web node-js + express
```sh
$ cd app;

# Installar dependencias
$ npm install;

# Ejecutar pruebas unitarias
$ npm test;

# Levantar la aplicación
$ node app;
```
La aplicación estará disponible en el puerto 3000.



# Instalacion de jenkins ubuntu 20.04 lts

```sh
$ wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

$ sudo apt update

$ sudo apt install jenkins

#levantar el servicio

$ sudo systemctl start jenkins
```



# Deployed

```sh
#en el servidor de ubuntu se cambia al usuario de jenkins

$ su - jenkins
 
#se exporta la siguiente ruta para que jenkis pueda tener acceso 
#n-1 es la configuracion de node 
$ export PATH=${PATH}:/var/lib/jenkins/tools/jenkins.plugins.nodejs.tools.NodeJSInstallation/n-1/bin

#dentro de la carpeta /var/lib/jenkins/tools/jenkins.plugins.nodejs.tools.NodeJSInstallation/n-1/bin

$pm2 start app.js
```

