# Metadatos, cabeceras y extensiones de archivos
Tu aprendiste que .jpg significa la extensión de archivos de imagen, históricamente windows tenia muy pocos bytes para la extensión, por esto la extensión normalmente era de 3 dígitos.

Existen muchas otras extensiones como .html para páginas web, .mpg4 para vídeo.

Cuando abres los archivos vas a ver su codificación binaria o dependiendo del editor puedes verlo en hexadecimal.

Un sistema operativo lee los primeros bytes del archivo para entender a que archivo corresponde, esta información se llama cabecera.

Cada sistema operativo tiene una base de datos de que programa abre que tipo de archivo.

Cuando estas transmitiendo un archivo por Internet se especifica el tipo de archivo con mime types, el cual se transmite en la cabecera de un paquete http.

- La mayoría de extensiones son de tres caracteres porque en los inicios de la computación, solo era posible asignar 3 bytes para la extensión (tipo) de archivo, y 8 para el nombre. Sin embargo todo avanzo y ya no estamos limitados a usar solo tres caracteres para denotar el tipo de archivo.

- Los Sistemas Operativos, tienen en una base de datos guardada la correspondencia de cada extensión de archivo. Es decir, en la base de datos dirá algo como: jpg = imagen, mp3 = musica, html = pagina web y así…En todo caso para llegar a esta base de datos y encontrar a que corresponde, es necesario primero identficar que tipo de archivo es. Para ello el SO lee los primeros bits de cada archivo hasta que encuentra cierto patron, esos bits de identificación se llaman la cabecera. Una vez identificado el patrón, el SO ya conoce que tipo de archivo es, con que programa se debe abrir y cómo se debe mostrar gracias a la base de datos.

- Todo esto en la web funciona a través de un estandar denominado MIME TYPES (Extensión para emails multiproposito). Eventualmente funcionaba solo con emails, pero hoy en día esta en la mayoria de protocolos de comunicación. La forma en que funciona es sencilla, en la cabecera del protocolo de comunicación (independiente de si es http, ftp…) se envían metadatos con la información del archivo. De tal forma que si es una pagina web, envía text/html, si es un video mp4 envía video/mp4 y asi se logra la identificación de los archivos
