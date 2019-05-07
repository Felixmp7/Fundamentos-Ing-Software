#Arquitecturas

##Desktop y Laptops
1. Todas tienen un procesador central llamado CPU
    **CPU**:
    - Los producen empresas como: Intel, AMD.
    - Funcionan con _Ghz_ = Velocidad de procesamiento
    - Solemos evaluarlas tomando en cuenta los *cores* = Nro de CPUS en un chip,
      o cuantas instrucciones en paralelo se pueden hacer.
    - Los CPU están hechos de un material llamado Silicio, sin embargo ya se están haciendo en otros materiales como el Grafeno.
    - Por si solas no hacen nada, requieren que de algún lugar se le provea información para procesarla, él primer lugar del que proviene informacion que recibe el CPU es la BIOS: Pequeño SO de arranque, que arranca, entiende y percibe todo lo que está conectado al sistema y le manda la señal inicial al CPU.

    **Disco Duro**:
    - Lugar en donde se guarda la información
    - Aquí se encuentra el elemento mas indispensable para arrancar nuestro computador, el SO.
    - Antes los DD eran mas lentos ya que la cabecera que lee el disco lo hace mientras el disco va girando y dependiendo de en donde se almacenaba la información habia que esperar por n cantidad de vueltas para obtenerla por completo.

    Hace algunos años se inventó lo que son los Discos SSD (Solid State Drives)
    en los cuales ahora, existe una señal electrica que viaja hacia donde estan almacenados los datos y los envía al CPU.

    - La BIOS notifica al CPU sobre el Disco Duro y se crea una conexión "directa" entre el CPU y el Disco Duro. Realmente hay un intermediario entre ambos que es en donde los datos se mueven mas rapido que en cualquier otro lugar y es... La memoria **RAM**

    **RAM (RANDOM ACCES MEMORY)**:
    - Es veloz porque es conocida como memoria volátil = sólo funciona con electricidad
    - Está compuesta por una serie de circuitos y transistores y no guarda nada, sólo ejecuta.
    - Ésta envía la información del SO al CPU y el CPU usa esta info para arrancar el computador

    **Memristores**:
    - Es una pieza dentro de nuestro Chip que guarda la onda electromagnetica que pasó por ella aún despues de que se desconecta el sistema.
    - Es tan veloz como la memoria RAM

    Una vez el CPU obtiene la informacion del SO, comienza a activar los periféricos (Pantalla,Teclado,Mouse,Puertos)

    **Periféricos**:
    - Funcionan a traves de chips especiales, por ejemplo: El teclado, mouse y los puertos, funcionan a traves de los _Drivers_ = Piezas de software que entienden como convertir las señales electricas del hardware en bits y bytes que el CPU le manda al SO para poder funcionar.

    - La pantalla requiere de un chip único que conocemos como _GPU_ = Se encarga de comunicar la pantalla con el CPU
