# Instalacion de Android en Ubuntu 15.10

* **Instalando android**

**Primero checa que version de java tienes**
``` sh
java -version

javac -version


```

** Si no te aparecen las maquinas virtuales**

sudo apt-get install ubuntu-developer-tools-center

umake android --accept-license

**Tambien te pueden faltar las librerias para leer los archivos de 32 bits**

en lo siguiente es considerando que la carpeta Android de la instalacion esta en HOME, si no esta en HOME cambiar la direccion por la que tienes.

apt-get install lib64stdc++6
cd ~/Android/Sdk/tools/lib64/libstdc++
mv libstdc++.so.6 libstdc++.so.6.bak
ln -s /usr/lib64/libstdc++.so.6 ~/Android/Sdk/tools/lib64/libstdc++



**Si te muestra el siguiente error: sh: 1: glxinfo: not found**

instalar la siguiente biblioteca grafica

sudo apt-get install mesa-utils