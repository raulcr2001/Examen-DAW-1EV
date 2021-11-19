# **Ejercicio 3 EXAMEN**

[Raúl Cubero Romero](https://github.com/raulcr2001)
![logo](apache.png "Logo Apache")

## **Resumen**

En este ejercicio realizaré un virtualhost a [www.ejercicio3.daw](www.ejercicio3.daw) usando Apache y mostraré en esa web un texto que contendrá mi nombre.

## **Índice**

- [Introducción](#introducción)
- [Virtualhost Paso a Paso](#virtualhost-paso-a-paso)

## **Introducción**

[Apache](https://dinahosting.com/ayuda/que-es-apache-y-para-que-sirve/) es un servidor web [HTTP](https://es.wikipedia.org/wiki/Protocolo_de_transferencia_de_hipertexto) de código abierto creado en 1996 y actualmente es el servidor web más usado en todo el mundo debido a sus seguridad y estabilidad que está desarrollado y mantenido por una comunidad de usuarios en torno a la [Apache Software Foundation](https://httpd.apache.org/docs/2.4/es/).

## **Virtualhost Paso a Paso**

En primer lugar, si no sabemos nuestra IP, una manera de consultarla y además comprobar que nuestro servidor funciona bien es realizando el siguiente comando, que nos **devuelve la IP** y la **ingresamos en el navegador para comprobarlo**.

![Virtualhost](CAPTURAS/cap1.png "Hostname")

Paramos el ***servidor Apache*** y a continuación creamos el index.html en ***/var/www/gci***, en este fichero, escribiremos nuestro nombre, el cual se mostrará cuando introduzcamos la url correspondiente.

![Virtualhost](CAPTURAS/cap2.png "Paramos el servidor")

![Virtualhost](CAPTURAS/cap3.png "Creando index.html")

![Virtualhost](CAPTURAS/cap4.png "Creando index.html")

El siguiente paso será entrar en el siguiente directorio y realizar una copia del fichero ***000-default.conf***.

![Virtualhost](CAPTURAS/cap5.png "Entramos en el directorio sites-available")

Cuando lo hayamos copiado, hacemos un **_nano_** del archivo para poder verlo y poder realizar todos los cambios que haya que hacer.

![Virtualhost](CAPTURAS/cap6.png "Visualizamos el archivo y lo modificamos")

Cambiamos el ***DocumentRoot*** a la ruta donde se encuentra nuestro archivo, y en ***ServerName*** escribimos el que nos dice en el enunciado del ejercicio.

![Virtualhost](CAPTURAS/cap7.png "gci.conf")

A continuación, iniciamos el servidor, activamos el fichero de configuración y reiniciamos el servidor para guardar los cambios.

![Virtualhost](CAPTURAS/cap8.png "Últimas configuraciones")

Con el siguiente comando, visualizaremos el fichero hosts para poder modificarlo con nuestra dirección IP y la URL deseada.

![Virtualhost](CAPTURAS/cap9.png "Visualizar fichero hosts")

![Virtualhost](CAPTURAS/cap10.png "Archivo hosts")

Escribimos el ***ServerName*** en nuestro navegador y confirmamos que va todo perfectamente, ya hemos acabado el ejercicio.

![Virtualhost](CAPTURAS/cap11.png "Confirmación en el navegador")