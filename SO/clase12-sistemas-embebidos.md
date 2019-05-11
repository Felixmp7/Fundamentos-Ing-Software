# Sistemas operativos embebidos e Internet of Things

Los sistemas embebidos son dispositivos que se encuentran en una gran variedad de lugares, estos son los sistemas de procesamiento que se utilizan en dispositivos diferentes a nuestros computadores, por ejemplo el microcontrolador que tiene programadas las secuencias de tu lavadora, el sistema embebido que tiene tu vehículo y que se encarga de coordinar tareas de seguridad básicas, entre otras cosas, el microcontrolador que tiene programadas las funciones de tu horno de microondas, el sistema de control de una estufa de inducción, la computadora embebida en un cajero automático, el sistema de navegación, estabilización y seguridad de un avión y muchos dispositivos más.

Los arduinos son una herramienta que permite crear prototipos de este tipo de sistemas, desde automatizar un horno antiguo hasta controlar una cámara por IoT, por esto son tan populares.

El Raspberry Pi es un dispositivo que contiene los mismos componentes que tiene un computador y cuesta sólo 35 USD, por esto y por sus entradas y salidas de propósito general (GPIO) es un sistema que vive y controla muchos proyectos desde sistemas retro de videojuegos hasta mini-clusters de cómputo, servidores multimedia DIY y más.

Hay plataformas para poder prototipar estos sistemas embebidos, las mas populares son arduino o rapberry pi, tb hay sistemas embebidos que no crearas que son un computador como la SIM Card (En la tarjeta sim hay cpu, memoria ram, un disco, un S.O, etc…)

- Los arduinos son muy populares porque sirven para prototipar muy rapido lo que quieras.

- Las CPU ARM son un tipo de CPU especial. Las CPU normales como intel o AMD son sistemas que se llaman X86, hay otro tipo de arquitectura llamada ARM que tiene otro codigo binario para ejecutar codigo. La diferencia esta en la forma en que los transistores estan por dentro organizados y en algunos elementos fundamentales por ejemplo intel siempre a optimizado los procesadores intel y la arquitectura x86 para que estos sean ultra veloces, sin importar nada mas. En cambio ARM la velocidad es una prioridad, pero muchos mas prioritario que esta es el uso de la electricidad, ARM usa la misma energia para procesar la misma cantidad de datos que un intel, obviamente por ahora un intel siempre va a hacer mas veloz aunque ARM esta alcanzando la velocidad de este. POR ESO AMD ES TAN POPULAR COMO PROCESADOR EN SISTEMAS PEQUENOS COMO MOVILES, RELOJES, ETC… PORQUE SU PRIORIDAD ES LA ELECTRICIDAD.

- En Arduino se programa usando Sketch (Derivacion de C++, que tiene funciones ya preparadas para arduino), el programa o S.O se le sube al SoC.

El arduino recibe alimentacion por USB (5V aproximadamente).

Los arduinos no sirven para hacer produccion masiva de hardware porque son caros, aunque son muy populares porque son muy rapidas de usar, un entorno muy amigable, etc…

Lo que podemos hacer es prototipar Hardware con arduino y una vez listo mandarle a produccion.
Cuando nosotros mandamos esto a produccion nosotros hacemos un RTM (Release To Manufacture), esto es la expresion minima de funcionamiento de un hardware. Por ejemplo imagina que hacemos una maleta inteligente entonces hacemos la maleta y adentro por algun lugar le colocamos un arduino, un GPS porque queremos que esta tenga tracking, una unidad de radio para que tenga conexion por sim card de 3G, una bateria externa para cargue dispositivos con la bateria, etc… Una vez lista convierten todo esto en el circuito mas barato y pequeno posible y lo mandan en un RTM para que una fabrica genere la version prototipo que luego se va a ir a produccion eso es RTM. Arduino es muy popular por ser el justo paso anterior antes del RTM.

El S.O de arduino es lo que tu programes.

El arduino tiene un sistema basico como la bios interna que arranca un codigo pero es lo que tu programas.

Los puertos son una serie de huecos que los arduinos tienen en las partes laterales y reciben senales tanto analogas como digitales en 5V.

Los raspberry pi tiene puertos basicamente de entrada electrica por lo que se pueden mandar 2 tipos de senales, analogas o digital, son las formas que tenemos de enviar y recibir info dentro de un arduino a traves de literalmente cables.

El usb sirve para subir el S.O o para alimentar el arduino o le puedes conectar una bateria para que funcione d emanera independiente de esta manera.
Un Arduino no tiene ningun procesador grafico porque no tiene niguna salida grafica. Aunque podemos programar una pantaalla que funcione en arduino. Y los arduinos tienen RAM muy limitada, la CPU d un arduino es un SoC que tb incluye ram y otros servicios. Es un sistema muy basico que lo que hace es mandar y recibir electricidad

- Los Raspberry pi tb tienen una CPU ARM pero tienen algo particular y es que esta CPU es quad-core, esto significa que son 4 CPU realmente, esto es porque los raspberry pi no se programan directamente como un arduino, estos son un PC COMPLETO y eso es una diferencia radical en comparaccion con un arduino. Los raspberry pi tienen puertos (USB, HDMI, electrico, etc…). Una Raspberry pi tb tiene una GPU que tiene un chip llamado broadcom viedocore que hace render de cualquier cosa grafica que necesites dentro de un raspberry pi. Y de hecho una de las formas para guardar informacion dentro de un raspberry pi es a traves de un puerto SD Card (UN RASPBERRY ES UNA COMPUTADORA COMPLETA Y PODMEOS CORRER CUALQUIER S.O QUE QUERAMOS).

- Historicamente los raspberry corrian linux, una verison optimizada para estos llamada raspian, sin embargo desde hace algunos anos hay una verison especial de windows llamada windows ARM.

- Microsoft tiene una historia de S.O embebidos por eso has visto en aeropuertos, cajeros, centros comerciales, fotos de la pantalla azul en lugares inesperados como el lugar donde se ven los vuelos, como pantallas de publicidad, etc… eso es porque windows creo una version para sistemas embebidos llamada windows CE y tb tenemos otro llamado windows mobile o pocket edition que fue evolucionando hasta crear el windows phone, etc… a dia de hoy solo existe un windows desde la perspectiva de microsoft (windows 10) pero hay una version especial llamada ARM edition que corre en sistemas embebidos como el raspberry pi.

- La SIM card es un SoC que tiene un S.O, estos nacieron a partir d las smart cards. Probablemente tienes una tarjeta de credito que tiene un chip igual al que tiene una sim card, o las tarjetas para entrar al trabajo, internamente seguro tienen uno de esos chips. Todos estos tienen una CPU, una memoria RAM, memoria de solo lectura donde esta el S.O, etc…Pueden correr muchos S.O, hay uno llamado JavaCard que es el S.O que usan por ejemplo los provdeedores de internet (ISP), este esta ahi para correr Java. Cuando hacemos una llamada hay una llave especial de cifrado para que tu telefono no sea secuestrado o intervenido y para que la llamada sea segura. Para que sepamos que tu tienes tu telefono y para que el operador movil este seguro de que esa llamada va solo por 1 camino. La ENCARGADA DE CIFRAR Y DESCIFRAR ESA INFORMACION NO ES LA CPU DEL TELEFONO SI NO LA CPU DE LA SIM CARD Y USA MUY POCA ELECTRICIDAD. De hecho existen Smart Cards que usan electricidad de radio en el ambiente (por ejmplo cuando compras algo de ropa y pasas por unas barreras gigantes cuando salen de la tienda estos que cuando salen empieza a pitar para evitar robos? Y le tienen que quitar una cosa de la ropa? esa cosa es un Smart Card que tiene un S.O cuya electricidad se alimenta de una senal de radio que emiten estas barreras. Entonces no usan baterias, usan la electricidad del medio ambiente para poder funcionar y comunicarse. Son S.O real time o que arrancan super rapidos y que ejecutan la aplicacion y vuelven a morir. Prenden y ejecutan y vuelven a morir, etc… son extremadamente rapidos y muy especiales. HAY MUY POCAS PERSONAS EN EL MUNDO QUE SABEN QUE ESTO EXISTE Y MUCHAS MENOS QUE SABEN PROGRAMARLO).

Hay otros S.O para estos Smart Cards, uno de los mas famosos es MULTOS (Multi operating systems for smart cards), este no se programa en java, si no en C++ o directamente en C, aunque existen compiladores de Java. Y luego se compila a un lenguaje intermedio llamado MEL que es el que interpreta la CPU de estos sistemas. Para la mayoria de SIM Cards del mundo los operadores se unieron y crearon un standard UICC (universal integrated circuit card).

Las Smart card son un ejemplo de un chip que inicialmente puede empezar en una tabla de prototipado como un arduino o un chip que ustedes quieran y que luego se va miniaturizando y creando una version RTM.

Todos estos sistemas tienden a ser un SoC. PERMITEN A UN CREADOR DE HARDWARE CREAR COSAS INCREIBLES.
