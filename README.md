![UADER LOGO](https://i.im.ge/2022/07/01/usvjHh.png)
# Proyecto de Sistemas Digitales
------------

### Docentes
- Gerard Guillermo Ariel
- Minatel Villoldo Julian
- Velazquez Eduardo Antonio
 
### Autores
- Nombre: Roldán Federico David 
- Contacto:  roldanfede96@gmail.com

- Nombre:  Marandino Juan Ignacio
- Contacto:  juan_marandino@hotmail.com

------------
**Tabla de Contenidos**

[TOC]

# Introduccion
El presente proyecto se llevo acabo con el objetivo desarrollar un dispositivo inteligente que sea capaz conectarse e integrarse a tecnologías de domótica ya existentes, como ser;  Alexa, Google Home o Smart Life. Las mismas, permiten integrar una gran cantidad de dispositivos, así como muchas aplicaciones para interactuar entre elllas.

Hoy en día, es común ver dispositivos compatibles con estas tecnologías. Por lo que se ve como un requisito necesario, la implementacion del mismo basado en dichas tecnologias, con el fin de poder competir con otros productos semejantes en el mercado de la Domótica. 

Artemis es un dispositivo inteligente, creado para el control de cultivos desde la app de un celular, el cual brinda al usuario la posibilidad de automatizar sus cultivos, de preferencia interiores, mediante el seguimiento y ajuste de las condiciones ambientales que lo afectan. El control se realiza de manera recursiva a partir de la variabilidad de las magnitudes de acuerdo a valores críticos pre-establecidos, por ejemplo, el riego de un sector es regulado, a partir de la activación de la bomba, en base al establecimiento de valores mínimos de humedad en el suelo de un sector, siendo dichos valores susceptibles de ajuste. Además, permite una mayor sustentabilidad del indoor posibilitando el acceso de manera remota desde cualquier red y facilitando el progreso de los cultivos sin necesidad de control manual, lo que le resulta mucho más ameno a el usuario.

# Objetivos
Lista de objetivos que planteamos para este proyecto :
- Facilitar la configuración del dispositivo cuando se lo añade a la red.
- Facilitar la configuración de los parametros a controlar.
- Aplicacion compatible con la mayor cantidad de dispositivos.
- Diseño de la interfaz Ux UI comprensible y atractiva.
- Compatibilidad con aplicaciones de Domotica.
- Suceptible a futuras modificaciones o mejoras.

# Desarrollo
## Hardware - EasyEDA

EasyEDA es una herramienta EDA gratuita, que no requiere instalación y esta basada en la nube. Permite un sencillo diseño de circuitos, simulación y diseño de PCB desde el navegador.
Gracias a las bibliotecas disponibles tendremos la posibilidad de dibujar estos esquemas de forma fácil y rápida, además la herramienta se actualiza automáticamente de forma transparente. 

### Esquematico

![Esquematico completo](https://i.im.ge/2022/07/02/uIMcH4.png)

#### Alimentacion

![Alimentacion](https://i.im.ge/2022/07/01/usvc1m.png)

##### Regulador 12V

![Regulador 12V](https://i.im.ge/2022/07/01/usv3A1.png)

##### Regulador 5V

![Regulador 5V](https://i.im.ge/2022/07/01/usvxaP.png)

##### Regulador 3V3

![Regulador 3V3](https://i.im.ge/2022/07/01/usvxaP.png)

#### Indicadores Led

![Indicadores Led](https://i.im.ge/2022/07/01/usv8ZW.png)

#### Modulo TUYA
##### SOC

![Modulo Tuya](https://i.im.ge/2022/07/01/usvWX0.png)

#### Arduino NANO

![Modulo Nano](https://i.im.ge/2022/07/01/uDn8ET.png)

##### Wifi-Key

![Botón para entrar al modo configuración Wifi](https://i.im.ge/2022/07/01/usvZiT.png)

##### Pines Accesibles IO Analogicas/Digitales

![IO Nano](https://i.im.ge/2022/07/01/uDngD0.png)

##### Sensores
###### DHT22 - Temperatura y Humedad Ambiente

![Temperatura y Humedad Ambiente](https://th.bing.com/th/id/OIP.zwE3KRqgSh4yIjNiBehStQHaHa?pid=ImgDet&rs=1)


###### DS18B20 - Temperatura del Agua

![Temperatura del Agua](https://denkovi.com/userfiles/productlargeimages/product_760.jpg)


###### HC-SR04 - Nivel del Agua

![Nivel del Agua](https://th.bing.com/th/id/R.b9cc78457a4ce7af0b92a9b64e072af5?rik=Bp39CHKEpp103Q&pid=ImgRaw&r=0)


###### Sensor Capacitivo v1.2 - Humedad en Tierra

![Humedad en Tierra](https://th.bing.com/th/id/OIP.zfLEAAkcJ5bKQiZ0mhly-gAAAA?pid=ImgDet&w=466&h=384&rs=1)

### PCB
###### TOP

![PCB CAPA SUPERIOR](https://i.im.ge/2022/07/01/usvKbc.png)

###### BUTTOM

![PCB CAPA INFERIOR](https://i.im.ge/2022/07/01/usvVGL.png)

## Plataforma - Tuya  IOT

Tuya IoT Development Platform facilita el desarrollo inteligente para todos los desarrolladores y/o participantes de IoT, creando estandares de Interconectividad.
La plataforma proporciona una amplia cartera de servicios que cubren herramientas de desarrollo de hardware, servicios en la nube de IoT y desarrollo empresarial inteligente.

### Métodos de conexión

Tuya IoT Development Platform le permite conectar dispositivos IoT, gateway, servicios y aplicaciones a la nube. En la etapa de desarrollo del producto,se eligen los métodos de conexión deseados para lograr una comunicación bidireccional entre el dispositivo y la nube, lo que permite que los dispositivos interactúen con los servicios y aplicaciones basados en la nube y otros dispositivos conectados.

| Métodos de desarrollo  |  Descripcion | Aplicable a  |
| :------------: | :------------: | :------------: |
|  TuyaOS  | Construido sobre RTOS, Linux y Non-OS, TuyaOS es un sistema operativo IoT distribuido e independiente de la plataforma. TuyaOS se adapta a diversas plataformas de conjuntos de chips y sistemas operativos, lo que le permite conectar dispositivos y puertas de enlace entre plataformas a la plataforma de desarrollo de Tuya IoT de la manera más fácil y rápida. Desarrollo sin código: se aplica a productos basados en SoC. Decenas de soluciones incorporan las mejores y probadas prácticas de desarrollo en dispositivos comunes y sus características típicas, como productos eléctricos y de iluminación. Desarrollo de código bajo: permite que los productos con microcontroladores incorporados se conecten a la nube. Desarrollo de código profesional: proporciona SDK personalizados específicos para diferentes funciones o productos, como redes, puertas de enlace, subdispositivos, cámaras IP, NVR y conceptos básicos de MCU.|  Tuya proporciona servicios de desarrollo de IoT integrales que incluyen los tres elementos esenciales para los productos típicos de IoT, a saber, módulos de red, aplicaciones móviles y servicios en la nube.  |
|  TuyaLink  | TuyaLink: lo ayuda a conectar los dispositivos IoT existentes a la plataforma de desarrollo Tuya IoT con procesos de desarrollo estandarizados.  |  Todos los dispositivos (no integrados con los módulos de Tuya) que se conectan directa o indirectamente a internet. Los servicios integrales que incluyen modelos de dispositivos, desarrollo y depuración, y análisis de datos lo ayudan a conectar, controlar y administrar dispositivos IoT, todo en un solo lugar.  |
| Edge gateway  | La puerta de enlace informática perimetral (puerta de enlace perimetral para abreviar) amplía las capacidades de la nube a los dispositivos perimetrales locales y permite que los dispositivos perimetrales respondan rápidamente a eventos locales con servicios informáticos locales. Estos servicios cuentan con baja latencia, rentabilidad, privacidad segura y autonomía local.  | Autonomía local o dispositivos comunicándose sobre protocolos como Modbus, BACnet, OPC UA, OPC DA, SNMP, KNX, DALI, y más. |  

### Desarrollo de SDK de MCU

La solución de interfaz MCU permite que los productos con microcontroladores incorporados se conecten a la nube. Tuya proporciona servicios de desarrollo de IoT integrales que incluyen los tres elementos esenciales para los productos típicos de IoT, a saber, módulos de red, aplicaciones móviles y servicios en la nube. Con el MCU SDK de Tuya, las aplicaciones móviles todo en uno y los paneles de control, se puede conectar el producto a la plataforma Tuya IoT fácilmente y beneficiarnos de los servicios en la nube rápidamente.

![El diagrama de bloques muestra cómo la MCU se comunica con los módulos de red de Tuya.](https://i.im.ge/2022/07/01/usvnKS.jpg)

### Solución de dispositivo Wi-Fi 

El SDK de MCU para Wi-Fi nos permite comunicar nuestro MCU (arduino) con el módulo de Wi-Fi de Tuya (WR3) a través de una comunicación en serie (UART),logrando asi, que el dispositivo pueda conectarse a la nube.

#### Protocolo puerto serie

Describiremos el protocolo serie que se utiliza para implementar la comunicación entre el módulo Wi-Fi de Tuya o el módulo combinado Wi-Fi y Bluetooth Low Energy (LE) y nuestro microcontrolador.


##### Caracteristicas de la comunicacion serial
- Baud: 9600/115200
- Data bit: 8
- Parity check: none
- Stop bit: 1
- Data flow control: none
- MCU: microcontroller unit.

##### Trama

| Campo  | Bytes  | Descripcion  |
| :------------: | :------------: | :------------: |
| Cabecera | 2   |  Se fija en 0x55aa. |
| Version  | 1  | Se utiliza para actualizaciones y extensiones.  |
| Comando  | 1  |  Tipo de Instruccion. |
|  Longitud del Dato | 2  |   |
|  Data  | N  | Datos de la entidad.   |
|  Verificacion | 1  | Comienza desde el encabezado, sume todos los bytes y luego divide la suma por 256 para obtener el resto.   |

Por ejemplo, <abbr  title="Trama de Comunicacion Serial">**55 AA 00 00 00 00 FF**</abbr>

##### Secuencia de Comunicacion

Generalmente, un comando es enviado por una parte y recibido por la otra parte sincrónicamente.

Es decir, una parte envía un comando y espera una respuesta de la otra parte. Si el remitente no recibe un paquete de respuesta correcto dentro de un período de tiempo específico, la transmisión se agota, como se muestra en la siguiente figura.

![Esquema de Comunicación Serial 1](https://i.im.ge/2022/07/01/usvGi6.md.png)

El módulo envía comandos de control y la MCU informa el estado del punto de datos (DP), que se produce de forma asíncrona. Suponga que el módulo envía un comando X y la MCU informa un comando Y. La transmisión de datos es la siguiente.
- El módulo envía un comando de control:

![Esquema de Comunicación Serial 2](https://i.im.ge/2022/07/01/usvecF.md.png)

- La MCU informa el estado:

![Esquema de Comunicación Serial 3](https://i.im.ge/2022/07/01/usvBXz.md.png)

#### Tipo de Datos 
Las unidades de datos de comando y estado de DP se definen de la siguiente manera:

| Segmento de Dato  | Bytes  | Descripcion  |
| :------------: | :------------: | :------------: |
| dpid  | 1  | El id de un DP  |
|  tipo | 1  |  El tipo de datos de un DP definido en Tuya IoT Platform. |
| len  | 2  | Los bytes de un valor.  |
|  Valor | 1/2/4/N  | Representado en formato hexadecimal. Los datos de más de un byte se transmiten en formato big-endian.  |

Descripción de los campos tipo:

| Tipo  | Tipo de Dato  |  Bytes | Descripcion  |
| :------------: | :------------: | :------------: | :------------: |
|  0x00 | Raw  | N  | Representa un DP de tipo de datos sin procesar. Los datos se pasan a través del módulo a la nube.  |
|  0x01 |  Bool |  1 |   Representa un DP de tipo de datos booleano. Los valores válidos incluyen y . 0x00 0x01|
|  0x02 |  Value |  4 | Representa un DP de tipo entero. Los datos se representan en formato big-endian.  |
|  0x03 |  String |  N |  Representa un DP de tipo cadena. |
|  0x04 |  Enum |  1 | Representa un DP de tipo enum, que oscila entre 0 y 255.  |
|  0x05 |  Bitmap |  1/2/4 |  Representa un DP de tipo de error. Los datos mayores de un byte se representan en formato big-endian. |

### Asistente de depuración de módulos

Module Debugging Assistant es un depurador todo en uno que utiliza comunicación en serie. Puede simular tanto los módulos de red como los microcontroladores y admitir una serie de protocolos como Wi-Fi, Bluetooth y Zigbee para ayudarlo a realizar una prueba integral en su sistema integrado. Esta aplicación fue la primera que utilizamos al llegar el modulo WR3 para ver si podíamos realizar la conexión del modulo y si este estaba funcionando correctamente.
El asistente de depuración se compone de las siguientes áreas:

![Partes del Asistente de Depuración de Modulos](https://i.im.ge/2022/07/01/usvAbq.png)

1. El área izquierda se utiliza para la visualización de datos del puerto serie, incluida la recepción y transmisión de información de tramas y el análisis de datos clave. Los tres botones siguientes se utilizan para mostrar, guardar y borrar los datos mostrados.
2. En el área de selección de modo, puede cambiar al modo asistente. El asistente tiene dos modos: simulación de MCU y simulación de módulo, que se pueden usar como MCU y módulo respectivamente.
3. Elementos de configuración de funciones generales. El protocolo se puede seleccionar según sea necesario, la ayuda es una función auxiliar y la configuración se refiere a la visualización de la página y la configuración de los parámetros de interacción de datos.
4. El área de operación funcional contiene tres partes: Explicación, Configuración y Operación. Muestra el protocolo seleccionado, el enlace de instrucciones y los elementos de configuración cuando comienza la depuración. Las funciones de depuración difieren según los elementos de configuración. El área de operación es para pruebas de funciones específicas.
#### Caracteristicas

El Asistente de depuración de módulos es esencialmente un asistente de puerto serie que integra los protocolos de comunicación de los módulos Tuya. Se puede elegir el protocolo correspondiente según las necesidades reales. El asistente tiene dos modos de trabajo. En la cual a nosotros nos interesa solo el modo de simulación de MCU.
El asistente simula la MCU y la computadora se conecta al puerto serie de un módulo Tuya a través de una herramienta de puerto serie. Una vez que se enciende el módulo, inicia la interacción de datos de inicialización y el asistente simula la MCU para responder automáticamente con los datos correctos. En este modo, se puede usar la aplicación Tuya Smart para emparejar el módulo y verificar el formato correcto de envío e informe de datos. Después de obtener el módulo, se prueba la interacción de datos, lo que mejora en gran medida la eficiencia del desarrollo. Si se encuentran problemas durante el proceso de depuración, nos permite localizarlo. 

#### Modo de simulación MCU

El asistente simula la MCU real. Cuando está conectado al módulo Tuya, se puede realizar la prueba de emparejamiento de red. 

Conectando el hardware.
1. Utilizamos el convertidor de USB a TTL para conectar el puerto serial del módulo Wi-Fi a la computadora.
2. Seleccionamos el protocolo de comunicación.

![Seleccion de el protocolo Asistente de Depuración de Modulos ](https://i.im.ge/2022/07/01/usvto4.png)

3. Configurar las opciones de inicio.

![Descargando el archivo de configuraciones json](https://i.im.ge/2022/07/01/usv6mY.png)

4. Apretamos en iniciar depuración y el asistente comenzará a funcionar. La sección Configuración inicial muestra los parámetros que se configuran durante la inicialización. 

![Configuración del Asistente](https://i.im.ge/2022/07/01/usvCBp.png)

5. Después que comience la depuración, se obsevrva que el asistente envía automáticamente el comando de inicialización. Si la MCU responde correctamente, completará automáticamente la interacción de datos de inicialización.

![Iniciando la Simulación](https://i.im.ge/2022/07/01/usvYHf.png)

## Codigo - Platformio
PlatformIO es un ambiente de desarrollo integrado (IDE), el cuál facilita y mucho la gestión de proyectos de software embebidos, gestión de dependencias, librerías, tests,etc.

## Aplicacion - UI Studio
UI Studio es una herramienta que facilita la creacion de aplicaciones que se enlazan a Tuya Smart y Smart Life. Sin la necesidad de escribir largas lineas de codigo. 
### Interfaz
Se busco crear una intefaz amigable y lo mas minimalista posible para no perder al usuario. Esta aplicacion consta de tres paginas que pasaremos a describir brevemente a continuacion:

#### Inicio
En esta pagina,  en el primer layout mostramos los estados de los actuadores y el historial de eventos importantes.

![Aplicacion Inicio 1](https://i.im.ge/2022/07/01/uDkRv1.gif)

Se tienen programadas alertas que se visualizaran con un simbolo en el layout correspondiente. 

En los layout que se encuentra por debajo, podemos ver las mediciones que se estan realizando. Ademas, podremos ver una tabla de graficos que guardara los valores de las mediciones en un rango de 24hs.

![Aplicacion Inicio 2](https://i.im.ge/2022/07/02/uITfsr.gif)

#### Configuraciones
Aqui podremos setear todos los valores necesarios para realizar el correcto control de nuestro indoor.  

![Aplicacion Configuraciones](https://i.im.ge/2022/07/01/uDkJDL.gif)

La humedad y la Intensidad de la Luz se podra setear por etapa. Estas seran comunicadas al dispositivo y almacenadas en la EEPROM.

#### Informacion
Pagina aun no terminada, en la que se podran ver sugerencias de cultivos, sponsors y tutoriales del proyecto.

![Aplicacion Informacion](https://i.im.ge/2022/07/01/uDkpec.gif)

# Conclusiones

Se cumplieron los objetivos y se llego a un prototipo con el que quedamos bastante conformes. Hay cosas por mejorarles en cuanto a la electrónica, pero en general se llego a un buen resultado. En el camino se utilizaron varias plataformas y tecnologías, como Firebase y ESP32, también se utilizo Android Studio para desarrollar una aplicacion en JAVA. Pero, ninguna solventaba el ideal de proyecto que teníamos en mente. 

La implementación de la plataforma Tuya, facilito varios de los objetivos con los se tenían problemas, o no quedábamos muy conformes. Uno de ellos era la configuración del dispositivo cuando se lo añade a la red. Se puede añadir el dispositivo sin muchos conocimientos del usuario. Tambien, la aplicación estaba programada en Android Studio en JAVA por lo que solo era compatible con dispositivos Android, ahora con la plataforma se mantuvo la compatibilidad con los dispositivos Android y también los IOS. Y para añadir el dispositivo a alguna aplicación de domotica se complicaba mucho y eran demasiados pasos para el usuario final.