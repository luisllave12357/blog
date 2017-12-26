+++
title = "Anuncio de Lanzamiento de Skycoin BBS v5.0"
tags = [
    "Development",
    "BBS",
    "CXO",
]
bounty = 1
date = "2017-12-18"
categories = [
    "Development Updates",
]
+++

¡Skycoin BBS v5.0 ha sido finalmente liberado con muchos cambios bajo el capó!

## Cliente Ligero

El cambio más aparente de todos es la introducción del cliente ligero. ¡Ahora ud. se puede acceder a Skycoin BBS sin configurar un nodo! Sólo diríjase a [bbs.skycoin.net](http://bbs.skycoin.net). 

En versiones anteriores, uno sólo podía (y sólo debería) acceder/enviar contenido a través de una interfaz de usuario web suministrada localmente. Dado que esta interfaz web (y la API que llama) tiene control directo sobre el propio nodo, y firma el contenido con llaves privadas que son almacenadas en el nodo (o en el servidor), no es apropiado exponerlo al público.

Por lo tanto, la introducción de un cliente ligero necesita que la administración de usuario, y el proceso de firmar contenido para su envío, sean manejados del lado del cliente. Esto requiere un punto final (o puntos finales) para envío de contenido completamente renovado, y cambios importantes en el front-end.

Los detalles del nuevo proceso de envío de contenido pueden encontrarse en la wiki BBS: [github.com/skycoin/bbs/wiki/Content-Submission-Process](https://github.com/skycoin/bbs/wiki/Content-Submission-Process).

Actualmente, el front-end carga muy lentamente. Esto es ocasionado por el uso de [GopherJS](https://github.com/gopherjs) para manejar la semilla y la generación del par clave pública/privada, así como la firma y verificación de los datos. En futuras versiones haremos uso de librerías JavaScript nativas a fin de mejorar el desempeño.

## Interfaz de Línea de Comandos

Después de la introducción de un cliente ligero visible al público, eliminamos los puntos finales de la API que manejan el control administrativo e introducimos una línea de comandos para tratar con este tipo de interacciones. 

Más información acerca de esto puede conseguirse aquí: [github.com/skycoin/bbs/tree/master/cmd/bbscli](https://github.com/skycoin/bbs/tree/master/cmd/bbscli).

## Otras Mejoras

* Mejoras en la Importación/Exportación (desafortunadamente esto no es compatible hacia atrás con la importación/exportación de BBS v4.x)
* Simplificaciones para codificar y mejoras de desempeño en el envío remoto y la interacción con Skycoin Messenger. Actualizado para emplear la última versión de Messenger.
* Desempeño mejorado para el administrador de archivos.
* Mejor manejo de raíces CXO inválidas.
* Mejor manejo de las desconexiones.

## Descargas

Para descargar BBS, diríjase a [github.com/skycoin/bbs/releases](https://github.com/skycoin/bbs/releases) (tambien debe estar el código fuente allí).

Observe que también puede acceder a BBS mediante [bbs.skycoin.net](http://bbs.skycoin.net).

## Documentación

Hemos comenzado una página wiki en [github.com/skycoin/bbs/wiki](https://github.com/skycoin/bbs/wiki).

Por favor, comprenda que aún está en desarrollo.

## Comunidad

Tenemos un canal de Telegram: [@skycoinbbs](https://t.me/skycoinbbs).
