# Instalacion de Android en Ubuntu 15.10

* ##Instalando android

**Primero checa que version de java tienes**
``` sh
java -version

javac -version


```

**Instalar Ubuntu Developer Tools Center**

Ubuntu Developer Tools Center es un proyecto que servirá para facilitar a los desarrolladores que utilicen Ubuntu y derivadas el acceso a las herramientas de programación más demandadas, como por ejemplo son Android Studio y Android SDK.

En esencia, Ubuntu Developer Tools Center no es más que un repositorio dedicado y con vistas de mantenerse constantemente actualizado en lo que a herramientas de desarrollo se refiere. Así, comienzan por Android, pero seguirán con otros palos, como desarrollo web o lenguajes y/o plataformas diferentes.

Se trata, pues, de hacer más sencilla la instalación de este tipo de aplicaciones, muchas de las cuales no suelen estar presentes por defecto en los repositorios oficiales de la distribución.


```sh
sudo apt-get install ubuntu-developer-tools-center

```

Ahora solo queda instalar Android Studio y Android SDK: usaremos el Ubuntu Developer Tools Center. ``` udtc android ```

En caso que no funcionara lo anterior utilizar el siguiente comando. 
``` umake android --accept-license ```

-------------------------------------------

* ##Maquinas virtuales

Para poder crear las maquinas virtuales primero abriremos nuestro android studio y seguir lo siguiente

**Tools>Android>SDK Manager>Launch Standalone SDK Manager**

ahora solo queda instalar las herramientas y los Android para las maquinas virtuales.

En **Tools** lo que se recomienda es instalar
* Android SDK Tools
* Android SDK platform-tools
* Android SDK Build-tools 25

Los Android elige dependiendo de para que sistema Android desea desarrollarlo. Las versiones mas avanzadas pueden soportar las anteiores pero no aplica a la inversa.

En **Extras** se recomienda lo siguiente
* Android Support Repository
* Android Auto Desktop Head Unit emulator
* Google Play services
* Google Market Apk Expansion
* Android Auto API Simulators

**Nota**

----------------------------------------------------------

* ##Error

Mas adelante se agregaran las explicaciones de que hace cada tool o extra.

**Si no te aparecen las maquinas virtuales al ejecutar**


Puede que te falten las librerias para los archivos de 32 bits

En lo siguiente se considera que la carpeta Android de la instalacion esta en HOME, si no esta en HOME cambiar la direccion por la que tienes.

apt-get install lib64stdc++6
cd ~/Android/Sdk/tools/lib64/libstdc++
mv libstdc++.so.6 libstdc++.so.6.bak
ln -s /usr/lib64/libstdc++.so.6 ~/Android/Sdk/tools/lib64/libstdc++



**Si te muestra el siguiente error: ```sh: 1: glxinfo: not found```**

instalar la siguiente biblioteca grafica

sudo apt-get install mesa-utils