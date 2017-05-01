---
layout: post
title: Qué es Ardour?
description: "Introducción"
comments: false 
tags: [01 INTRODUCTION]
comments: false
image:
  feature: Ardour_5_background.png
  credit:  
  creditlink:  
---

### Haz clic [aquí]({{ site.url }}/tags) para saltar directamente a la Tabla de contenidos

Basado en el manual de Ardour2, http://en.flossmanuals.net/Ardour 
Traducido del original al inglés por Roman Muñoz, intxixu@gisa-elkartea.org 
Actualizado a la versión 5 y adaptado por Daniel Schär, schaerdaniel@gmail.com
Para ver la lista de créditos y la Licencia ir a http://brunoruviaro.github.io/Ardour4-tutorial/credits

# 1. Introducción
## Ardour 5 y sus características
### Qué es "Ardour"
Ardour es un grabador a disco duro completo, libre, de codigo abierto y un puesto de audio digital adecuado para uso profesional. 
Presenta ilimitadas pistas de audio y buses, edición no-destructiva, no-lineal con deshacer ilimitado, y enrutamiento de señal desde y hacia cualquier lugar. 
Soporta formatos de fichero estándar, tales como MIDI, BWF, WAV, WAV64, AIFF y CAF, y puede usar formatos de Plugins LADSPA, LV2, LinuxVST (en GNU/Linux), VST (en Windows) y AudioUnit (en mac OS).
Se ejecuta en Linux, mac OS y Windows (oficialmente a partir de la versión 5), y usa ALSA o el Jack Audio Connection Kit (JACK) para interactuar con la tarjeta de sonido del ordenador, así como con otras aplicaciones de audio ejecutándose en el mismo sistema. 

Se puede encontrar más información sobre Ardour y descargar el programa para las varias plataformas en http://ardour.org. En este momento (Abril 2016) la versión mas reciente es 5.8. 
Hay muchas características y correcciones de fallas en esta versión por lo cual te recomiendo actualizar si tienes una versión anterior. Este manual de referencia solo es valido para las versiones 5+ de Ardour. 

### Por qué se llama "Ardour"
El nombre "Ardour" surgió a partir de consideraciones acerca de cómo debería pronunciarse el acrónimo HDR (Hard Disk Recorder). El intento más obvio suena como un "harder" sin vocales y entonces fue un paso pequeño cambiarlo a una palabra no relacionada pero que sonaba parecido.
  Ardour n 1: sentimiento de fuerte impaciencia (normalmente en favor de una persona o causa); 
  "estaban imbuídos de un ardor revolucionario"; "sentía un tipo de celo religioso" [syn: ardor, impulso, celo] 
  2: intenso sentimiento de amor [ syn: ardor] 
  3: sentimientos de gran calidez e intensidad; "habló con mucho ardor" [syn: ardor, fervor]"
Años después, apareció otra interpretación de "Ardour", esta vez basada en escuchar a hablantes no-nativos de inglés intentando pronunciar la palabra. En lugar de "Ardour" se convirtió en "Our DAW", lo cual parecía ajustarse poéticamente a una Digital Audio Workstation cuyo código fuente y diseño pertenece a un grupo de colaboradores.

### ¿Por qué escribir otro DAW?
Existen ya un buen número de excelentes estaciones de trabajo de audio digital. Para mencionar unas pocas: ProTools, Nuendo, Samplitude, Digital Performer, Logic, Cubase (SX), Sonar y otras. Cada uno de estos programas tiene sus puntos fuertes y débiles, aunque en los últimos años la mayoría de ellos han convergido en un grupo muy similar de características principales. Sin embargo, cada uno de ellos sufre dos problemas cuando se les ve desde la perspectiva del grupo de desarrollo de Ardour:
No todos son mulitplataformas y funcionan en GNU/Linux
No están disponibles como código fuente, con lo cual es imposible modificarlo, mejorarlo o corregir fallos por parte de los usuarios con conocimientos técnicos y los informáticos que se puedan emplear.

### ¿Que sistema operativo es recomendado para usar Ardour?
Inicialmente Ardour fue creado como DAW solamente para el Sistema GNU/Linux. El autor principal de Ardour usa GNU/Linux y quería un DAW que pudiera ejecutarse ahí. A partir de la versión 4 se hizo una versión para mac OSX. Hubo muchas personas que preguntaron en el foro de la pagina de Ardour cuando si y cuando va a salir una versión para Windows. En Abril 2015 los desarrolladores sacaron una versión Nightly Build para Windows pero sin ningún soporte. A partir de la versión 5 que salió en Agosto 2016 se consideró que la versión para Windows es suficiente estable para lanzarla oficialmente. Como el sistema operativo Windows aún ocupa el primer lugar mucho es probable que va a ganar mucho mas usuarios.

Las ventajas de usar GNU/Linux:
- Puede permanecer en pie durante meses (incluso años) sin problema.
- Es infinitamente configurable hasta el más pequeño detalle.
- No es propiedad de ninguna entidad corporativa, asegurando que su vida y la dirección que toma están a salvo de la intervención de esa corporación.
- Es rápido y eficiente.
- Se ejecuta prácticamente en cualquier plataforma hardware jamás creada, incluyendo viejos y "lentos" sistemas.
- Es uno de los sistemas operativos más seguros "por defecto"

Las ventajas de usar Windows
- Seguro que tu interfaz audio trae un driver para Windows
- se puede usar los plugins WindowsVST que es uno de los formatos de plugin estándar en el mundo profesional 

Las ventajas de usar mac OS
- Seguro que tu interfaz audio trae un driver para macOS
- Se puede usar los plugins AU que es uno de los formatos de plugin estándar en el mundo profesional  

### Requerimientos 
Computadora
- Cualquier computadora con un chip Intel de 32 or 64 bit. La velocidad del CPU limita la cantidad de procesamiento.
Sistema Operativo 
- Cualquier versión de Linux con un kernel mas reciente que #3 y versión de libc #25 o arriba.
- Cualquier versión de Windows XP, 7 o arriba.
- Cualquier versión de mac OS de 10.6 (Snow Leopard) hasta 10.11 (El Capitan)
RAM
- 2GB son recomendados, más es siempre mejor
Disco Duro
 - Mínimo de 350MB de espacio libre para instalar Ardour. Para grabar se necesita mas espacio. No es necesario tener un disco separado pero esto puede facilitar un rendimiento mayor.

### ¿No es un programa muy complicado?
No tiene sentido pretender que Ardour es un programa sencillo y fácil de manejar. El grupo de desarrollo ha trabajado duro intentando hacer las cosas sencillas razonablemente fáciles, las tareas comunes rápidas, y las cosas difíciles o inusuales posibles. Al mismo tiempo, la edición de audio multipista, multicanal, no-lineal y no-destructiva, está lejos de ser un proceso sencillo. 
Este trabajo no sólo requiere un buen oído, sino también un conocimiento sólido de los conceptos básicos de audio y un modelo mental/metáfora robusto de lo que se está haciendo. Ardour no es un simple "grabador de audio", aunque ciertamente se pueda usar para grabar material estéreo (incluso mono) en una sola pista, sino un programa que se ha diseñado para ser capaz de mucho más que esto. Si nunca has trabajado con un grabador de audio multipista es mejor que empieces a trabajar con un editor mas sencillo como por ejemplo Audacity para familiarizarte con este concepto. 

## Convenciones de formateo
### Tipografía
Este manual usa unas pocas convenciones para indicar atajos de teclado, elecciones de menú y otras interacciones del usuario.
Atajos de teclado como [Ctrl + A] significan "Mantén pulsada la tecla Ctrl y pulsa la tecla A”
Los nombres propios, términos técnicos, términos en inglés aparecen en cursiva: Ardour, Hydrogen, master
El nombre de una opción de menú aparecerán como **Menú → Sub-Menú**.

### Botones del ratón
Puede que estés acostumbrado a términos como "botón izquierdo" y "botón derecho del ratón". Ardour se usa normalmente con un ratón equipado con al menos 2 botones que pueden ser remapeados para usuarios diestros y zurdos, lo cual hace difícil definir sin ambigüedades "derecho" e "izquierdo" de un modo útil. 
Si eres diestro y usas un ratón convencional, entonces Clic se corresponde con el botón izquierdo y Clic derecho se corresponde con el botón derecho. Si eres zurdo o usas un ratón no convencional, esta nomenclatura se aplica de manera espejada. Si ves instrucciones como [Ctrl + Clic], significan "Mantén pulsada la tecla Ctrl y pulsa Botón izquierda."

### Avisos
Los avisos aparecen aparte del texto principal y se pretende que atraigan su atención hacia ciertos fragmentos de información. Según lo crítica que es la información para el usuario, pueden ser

`Nota. Típicamente, una nota es información que necesitas para comprender la conducta de Ardour.` 

Importante. Se usa para atraer la atención hacia partes del interfaz que pueden ser pasadas por alto o hacia ciertos ajustes que son vitales para determinar el comportamiento de Ardour.
Peligro. El aviso de peligro se usa cuando una acción puede tener consecuencias no deseadas o permanentes, como cambios a la sesión que no se pueden deshacer o borrado de archivos.

## Elementos básicos del interfaz
Aunque Ardour tiene un interfaz gráfico de usuario bastante convencional, similar a otros Digital Audio Workstations (DAW, estación de trabajo para audio digital) como ProTools. A partir de la versión 5 el Interfaz gráfico se puede adaptar en algunos aspectos (cambiar el tema, ventanas, colores, escalar el interfaz, etc). Para este manual se hicieron las capturas de pantalla con el tema de color “Unastudio” que se puede seleccionar en Editar → Preferencias → Tema.
Hay unos pocos elementos que son únicos y que probablemente te resultarán nuevos. Este capítulo proporciona una guía para usar esos elementos.

### Clics del ratón
Cuando decimos "haz clic en" sin especificar el botón, queremos decir que uses el botón izquierda para hacer clic en algún elemento del interfaz (botón, Fader, menú, etc).

Como en la mayoría de los interfaces gráficos actuales, un "clic derecho" en muchos de los elementos del interfaz, mostrará un menú que dependerá del contexto específico, permitiendo ajustar parámetros o realizar operaciones. Hay un montón de ejemplos de esto, pero hacer la prueba en una región de audio, en un botón "mute" del mezclador y en una banda del mezclador mostrará la idea general.

También existe el clic con el botón central (la rueda del ratón) que permite activar o desactivar funciones en algunos elementos (por ejemplo activar/desactivar un Plugin en la banda de mezcla)

### Relojes
En el interfaz de Ardour hay varios relojes, algunos de ellos son visible siempre, otros están en ventanas que sólo se muestran a petición del usuario. Todos estos relojes son idénticos en cuanto a funcionalidad, aunque algunos pueden ser editados por el usuario y otros sólo pueden ser visualizados.
Un clic contextual en un reloj mostrará un menú que te permitirá modificar el modo de visualización de ese reloj. Las opciones son:
a) Frames de audio, 
b) BBT (Bars, Beats, Ticks - Tiempo basado en tempo y métrica musical ) 
c) SMPTE
d) Min:Sec
Cada modo de reloj tiene un número de campos diferente. Por ejemplo, SMPTE tiene horas, minutos, segundos y frames de video.
Para editar el valor de un reloj en particular, haz clic en el campo más a la izquierda de los que quieras modificar. Puedes meter un nuevo valor para ese campo usando el teclado numérico, así como el carácter '.' donde sea apropiado. La edición saltará automáticamente al campo siguiente una vez que hayas introducido el número máximo de dígitos en un campo. Para moverte al campo siguiente sin necesidad de introducir el número máximo de dígitos, pulsa [Tab]. Para terminar la edición, pulsa [Intro] o usa [Tab] para saltar todos los campos restantes.

### Barras de control
Una barra de control es un elemento del interfaz que funciona de un modo bastante diferente a cualquier elemento estándar encontrado en la mayoría de programas. Se usan para proporcionar un método combinado de mostrar y modificar un parámetro.
Para editar gráficamente el valor del parámetro representado por una barra de control, pulsa y arrastra la barra de control hacia la derecha o la izquierda, arriba o abajo, según resulte apropiado. Para editar el valor con mayor precisión, haz un doble clic en la barra de control y se transformará en un diálogo de entrada de datos. Puedes meter un valor exacto para el parámetro, o usar las flechas para aumentar/disminuir el valor mostrado. Cuando hayas terminado de editar, las teclas [Intro] o [Tab] transformarán de nuevo el diálogo de entrada de datos en una barra de control.

## Qué es diferente en Ardour?
Si ya has usado otros programas de audio, sobre todo DAW, (estación de trabajo para audio digital), entonces hay un cierto número de cosas en Ardour que pueden parecer raro las primeras veces que uses el programa.

### „No hay sesión por defecto!“
Es necesario crear explícitamente una Sesión antes de poder hacer nada, y si escoges no usar una de las esquemas predefinidas, también tendrás que crear las pistas y Buses necesarias para grabar y/o editar el material existente.

### „¿Dónde van los Plugins y los envíos?“
Ardour no tiene un número fijo de "ranuras" para Plugins, envíos o insertos: en cada pista puedes tener tantos como permita la potencia de tu máquina. Las dos cajas negras encima y debajo del control de volumen en la tira del mezclador correspondiente a la pista son listas de redirección en las cuales puedes añadir, reordenar, eliminar y -generalmente- controlar los Plugins, envíos e insertos, tanto antes de controlar el volumen como después.

### Un conjunto de herramientas más pequeño
La mayoría de DAWs han evolucionado hacia proveer la llamada "herramienta inteligente" que te permite usar el ratón para realizar diversos tipos de operaciones sin necesidad de cambiar a una herramienta diferente. Ardour ha usado esta orientación desde el principio, de modo que la herramienta "Objeto" de hecho te permite realizar muchas operaciones diferentes dependiendo de cómo y dónde se usa el ratón. Ardour no proporciona una herramienta "Lápiz" destructiva como hacen otros DAW, por razones técnicas básicas. La necesidad de una herramienta "Lápiz" para reparar la forma de la onda, casi siempre indica que hay un problema con el ajuste de la sesión y/o el hardware de grabación. Las diferentes herramientas que Ardour sí ofrece incluyen la herramienta "Objeto", la cual tiene muchos usos diferentes incluyendo copiar/mover/recortar regiones, editar la automatización, y otros; una herramienta "Rango" para definir rangos de tiempo; una herramienta "TimeFX" para ajustar el tiempo; una herramienta "Gain", usada exclusivamente para editar las envolturas de ganancia de una región; y una herramienta "Zoom" para manipular el zoom temporal. Muchas otras operaciones son accesible vía menú contextual o por atajos de teclado.

### Configuración sin restricciones de las entradas y salidas de las pistas
Las pistas y los Buses de Ardour no vienen con configuraciones predeterminadas. Puedes crear una pista mono, y convertirla en pista estéreo en cualquier momento. Puedes convertirla en una pista con 3 entradas y 7 salidas si quieres, ya que Ardour no restringe las configuración de entradas y salidas a un grupo fijo de mono/estéreo/5.1/7.1, etc. También puedes conectar cualquier pista a cualquier número de otras pistas y Buses. En Ardour, la única diferencia entre una pista y un Bus es que una pista puede reproducir material pre-grabado desde el disco duro y puede grabar al disco duro. Tanto las pistas como los buses pueden tener plugins, envíos, insertos, automatización y más.

### Uso de JACK
Es extremadamente importante comprender que Ardour no interactúa directamente con la tarjeta de sonido. En vez de eso, todas las señales de audio que Ardour recibe y genera son enviadas hacia y desde un sistema de audio. Estos enrutan el audio entre la tarjeta de sonido y las aplicaciones de audio, en tiempo real. Hay un sistema de audio que fue portado de GNU/Linux a mac OS y también a Windows que se llama Jack Audio Connection Kit (JACK). 
Tu sesión no está limitada a recibir y enviar audio desde/hacia tu tarjeta de sonido. Puesto que Ardour usa JACK, una pista con una entrada de hecho puede recibir datos de muchas localizaciones diferentes. Tradicionalmente, la mayoría de las fuentes de audio que querías grabar, así como un montón de los efectos más significantes, vivían fuera del ordenador. Por tanto uno de los mayores problemas para integrar un ordenador en el flujo de trabajo de un estudio de grabación es cómo meter y sacar los datos de audio del ordenador.
Sin embargo, cada vez es más común que los estudios usen fuentes de audio y procesado de efectos hechos completamente por software, a menudo ejecutándose en la misma máquina, como un secuenciador de MIDI o un sintetizador virtual. En estas situaciones surge un nuevo problema, porque mover datos de audio de un lado a otro ya no involucra a tu tarjeta de sonido. En vez de eso, los datos deben ser llevados de un programa a otro, preferiblemente con el mismo tipo de sincronización. Por medio de JACK Ardour puede enviar y recibir señales de audio de cualquier otra aplicación que se ejecutan en otro ordenador. Por una parte, esto hace un poco más complejo comprender las opciones de Entrada/Salida de una pista o un Bus, pero también proporciona a Ardour una potencia increíble, como veremos más adelante. 

Si quieres usar este sistema de audio te recomendamos estudiar la pagina de cual también lo puedes bajar el programa para tu sistema operativo: http://jackaudio.org 

Si quieres instalar y usar JACK
- en Windows hay un tutorial en: http://www.jackaudio.org/faq/jack_on_windows.html

- en GNU/Linux es recomendable descargar la versión de JACK de tu distribución por medio del instalador de paquetes. Los dos paquetes se llaman jackd y qjackctl. Ademas es recomendado leer el tutorial de JACK en Linux de la siguiente pagina: https://radioslibres.net/article/el-poderoso-e-incomprendido-jack/

- en mac OS te recomendado leer el tutorial de JACK de la siguiente pagina: http://www.jackosx.com/about.html

JACK no tiene interfaz gráfico para ejecutar y controlar. Sin embargo, hay aplicaciones como qjackqtl en GNU/Linux o JackPilot en mac OS que son aplicaciones que empaqueta JACK en un interfaz gráfico que es a la vez agradable de ver y útil. Necesitas ejecutar qjackctl (en Linux), Jack Control (en Windows) o JackPilot (en mac OS) que controla JACK antes de abrir Ardour. Deberías de ser capaz de abrir este programa desde el menú principal de tu sistema, que normalmente se encuentra en el panel/appbar/dock o como se llame en alguno de los márgenes de tu pantalla. Haz clic en el triangulo verde (Start) en la ventana principal de qjackctl. Hasta ahora puedes arrancar Ardour. 

Nota: Antes de la versión 4 de Ardour siempre necesitaba JACK como sistema de audio. A partir de la versión 4 ya no. Si no usas programas o dispositivos externos (sintetizadores, baterías electrónicas, varias tarjetas de sonido, etc.) puedes usar Ardour perfectamente sin JACK.

## Hacer funcionar la tarjeta de sonido
En un mundo perfecto solo hay que conectar tu interfaz de audio con la computadora y tu sistema operativo la reconoce automáticamente. Puedes determinar si estás en esta situación ideal haciendo unas pocas pruebas sencillas en tu máquina. La prueba más obvia es reproducir audio por un reproductor y escuchar si salga de tu tarjeta o interfaz de audio. Si es así, puedes saltar a la sección "Seleccionar la fuente de captura".

### Probar el interfaz de audio
Conseguir que funcione la tarjeta de sonido puede ser algo difícil al configurar tu ordenador para ejecutar Ardour. El nivel de dificultad al que te enfrentas dependerá del tipo de tarjeta de sonido que tengas, de la versión del sistema operativo que uses, y de tu propia comprensión de cómo funciona todo esto. Si no consigues reproducir audio correctamente, primero comprueba que todos los cables están en su sitio, que los altavoces están encendidos, etc. Después sigue las instrucciones recomendadas dependiendo de tu sistema operativo:

ASIO en Windows:
Aunque tengas un driver especifico para tu interfaz audio vale la pena echar un vistazo a ASIO4ALL, un proyecto que tiene como finalidad de ofrecer un driver de audio ASIO de baja latencia para cualquier tipo de tarjeta de sonido que funciona con WDM (un estándar para tarjetas de sonido). Es freeware (gratis) y se puede descargar de la pagina: http://asio4all.com (La versión mas reciente es #13 y existe en español).

Para instalar ASIO4ALL haz doble clic en el instalador y en **Siguiente**, dando clic en **Acepto los términos de la licencia** y otra dos veces en **Siguiente**. Al final deberías de ser capaz de ver el símbolo de ASIO4ALL en la barra de menú a la hora de abrir el programa. 

En la pestaña Dispositivos WDM vemos la
en primer lugar los dispositivos WDM, pues si tuviéramos más de una tarjeta de sonido, podemos activar o desactivar cada una de ellas dando clic en el símbolo a su izquierda.
Después, podemos hacer clic en el expansor **(+)** a la izquierda para ver las entradas y salidas de las tarjetas para activar/desactivarlas individualmente.

Para saber mas de ASIO te recomendamos leer la pagina https://www.wikiwand.com/es/Audio_Stream_Input/Output 

ALSA en GNU/Linux:
Entra en el sistema como root y ejecuta el programa alsaconf. Puedes hacerlo pulsando [ALT+F2] y escribiendo alsaconf en la ventana de diálogo que aparecerá. Alsaconf es un asistente que intentará configurar tu tarjeta de sonido. Si todo va bien, no tendrás más que ir aceptando lo que te proponga. Una vez ejecutado alsaconf, intenta reproducir de nuevo un archivo de audio. Si consigues escucharlo correctamente, todo va bien.
Si alsaconf no termina con un mensaje de éxito, probablemente el problema es que la tarjeta de sonido no es reconocida correctamente o no existe un driver ALSA para ella. En este caso, una visita a la página ALSA matrix card puede confirmarte si existe un driver para ella o no. Este es una pagina de ALSA-Project donde usuarios evaluaron el funcionamiento de tarjetas de sonido en GNU/Linux: http://www.alsa-project.org/main/index.php/Matrix:Main.

Si cuando entras como root escuchas el audio y cuando entras como usuario no, tienes un problema de permisos. En este caso, vuelve a entrar como root, abre una consola o [Alt+F2] y usa este comando:

**adduser tu-usuario audio**

Con eso estás metiendo tu usuario en el grupo audio, y por tanto le das permiso para usar el hardware de audio. Cuando vuelvas a entrar como usuario, deberías poder reproducir el archivo de audio sin problemas. Sustituye "tu-usuario" por el nombre de usuario que realmente usas para entrar en el sistema. Este comando debería funcionar en cualquier distribución basada en Debian (es decir, una que use paquetes .deb)
Como alternativa puedes descargar el paquete ubuntustudio-controls con el siguiente comando: 
**sudo apt-get install ubuntustudio-controls**

Luego lo abres como root y puedes realizar la misma tarea de añadir tu usuario al grupo audio de manera gráfica.

Core Audio en mac OS
El estándar Core Audio ha sido introducido con la versión 10.3 de mac OS. La mayoría de los interfaces de audio profesionales de hoy en día son compatibles con Core Audio, así que no necesitas instalar ningún driver extra. Sin embargo es una buena idea echar un vistazo a la pagina web del de tu interfaz de audio para verificar si es compatible con tu versión de mac OS. 

### Seleccionar la fuente a capturar
Muchas tarjetas de sonido ofrecen modos de conectar tanto micrófonos como instrumentos u otro hardware de audio para grabar su señal. La pregunta surge de inmediato: ¿cómo sabe Ardour (o cualquier otro programa) qué señal debe grabar, la que viene de la entrada del micrófono o la que llega por la entrada "line"? La misma cuestión surge cuando trabajamos con tarjetas de sonido caras, aunque en este caso el problema se presenta de diferentes maneras. La respuesta rápida es: Ardour no lo sabe. En lugar de eso, eres tú quien debe hacer la elección usando un programa que sabe cómo controlar el mezclador hardware de la tarjeta de audio. Cada uno de ellos ofrece una manera de seleccionar cuál de las señales posibles será usada como "fuente a capturar". El cómo seleccionar la señal en cuestión varía de programa a programa. De modo que tendrás que consultar la documentación del programa que elijas. 

También puedes buscar la opción Tamaño del buffer Esto nos permite aumentar o bajar la latencia. Debe estar hacia la izquierda si queremos trabajar con prioridades de tiempo real. Tiempo real quiere decir que la señal será procesada como máximo cada X mili-segundos. Cada vez que nuestro sistema sea incapaz de procesar la señal de audio en el intervalo de tiempo especificado en "Latencia", tendremos un corte, que se reflejará en la grabación y reproducción de audio como un „retraso“. Si lo conseguimos y la latencia es de 5 mili-segundos o menos, tendremos un sistema de audio profesional. Si la latencia está entre 5 y 7 mili-segundos, tendremos un sistema semiprofesional. Para trabajar en tiempo real necesitamos una computadora suficiente poderosa sino probablemente tendremos muchos cortes. Un corte de más de cinco mili-segundos es perceptible por el cerebro humano. Es inaceptable tener estos cortes mientras capturamos audio.

Ahora estas listo para descargar, instalar y configurar Ardour.  

#  2. Iniciar tu primera sesión
## Instalar Ardour
Este capítulo cubre las bases para descargar, instalar, configurar y comenzar un nuevo proyecto en Ardour, incluyendo cómo ajustar una sesión.

### Descargar y instalar 
Desde la pagina https://community.ardour.org/download puedes descargar la versión actual del programa para GNU/Linux, Windows y mac OS. El código fuente es libre y gratis. Para obtener el programa ejecutable necesitas dar clic en el botón Ready-to-Run Program, seleccionar tu sistema operativo y pagar al mínimo 1 USD con una tarjeta de crédito o con PayPal. 

El desarrollador principal vive de estos ingresos. Sea generoso! 
Antes de descargarlo revisa si tu sistema corre en 32 o 64 bit para descargar la versión adecuada a tu sistema.
Mejor registrarte para que vayas recibiendo todas las versiones de 5.X gratis. Ademas puedes usar el enlace tres veces para descargar el programa. Después de descargarlo, busca el instalador del programa y sigue los pasos dependiendo de tu sistema operativo:

en GNU/Linux:
Verifique en las propiedades que el instalador (termina con “.RUN”) sea ejecutable. Cierra y ejecuta el archivo como usuario (sin necesidad de ser root). Si no sabes como ejecutar un archivo, abre un terminal con [Alt + F2] y entra a la carpeta donde se descargó el instalador de Ardour, por ejemplo: 
**cd /Descargas**
Ejecuta el instalador escribiendo “./” antes del nombre del instalador (por ejemplo: 
**./Ardour_64bit-##0.run**
Sigue las instrucciones: Ingresar tu contraseña, confirmar las preguntas, etc. Ardour se instala en la carpeta **/opt**. Si ya tienes una versión anterior de Ardour instalado, te pregunta si quieres desinstalar esta. 

    Nota: Necesitarás obtener privilegios root para instalar el programa. 

en mac OS
Después de descargar el instalador (termina en .DMG) con tu navegador, el Finder debería mostrar el Programa Ardour con su logotipo en tu escritorio. Puedes arrastrarlo en cualquier lugar en tu disco duro y arrancarlo desde allá. 

Importante: La versión 64bit ya no soporta los plugins Carbon Audio-units de 32bit. Si usas solamente 32bit plugins, favor usar la versión 32bit (que también funciona en mac OS de 64bit).

en Windows:
Para instalar haz doble clic en el instalador y sigue las instrucciones dando clic en **I Agree, Next** y **Install**

Si ya tienes una versión anterior de Ardour instalado, te pregunta si quieres desinstalar esta.
Para arrancar Ardour 5 buscalo en el menú de Windows. 

## Configurar una nueva sesión
Cuando arrancamos Ardour por primera vez aparece automáticamente el diálogo para crear una nueva sesión. Si trabajaste en sesiones anteriormente les va a mostrar en Sesiones recientes. 
Si hay una nueva versión de Ardour disponible aparece en la misma ventana arriba un mensaje (ver en la pantalla al lado).

Dando clic en Nueva sesión nos permite dar nombre a la nueva sesión. Puedes usar los caracteres que quieras como parte del nombre, pero conviene que sepas que casi cualquier cosa que no sea alfanumérica (letras del alfabeto y números) será convertida a guión bajo para formar el nombre de la carpeta de la sesión.

Necesitas especificar dónde quieres guardar la nueva carpeta de sesión. Si no quieres guardarla en el directorio actual, haz clic en el botón Crear carpeta de sesión en para abrir el selector de archivos. Si las opciones que aparecen aún no te convienen, haz clic en Otro… y a continuación navega hasta el lugar que quieras.
Ahora Ardour crea una nueva carpeta llamada igual que la sesión, y almacena diversos tipos de archivos y sub-carpetas en ella. La carpeta más importante es sounds, la cual contiene todo el audio grabado o importado en la sesión.

### Opciones avanzadas
Si quieres tener más control, por ejemplo en el caso cuando no quieras usar el Bus master, haz clic en el triángulo junto a Opciones avanzadas para ver todas las opciones disponibles: Esto es útil si vas a pasar la salida de Ardour por una mesa de mezclas o si quieres por ejemplo crear sonido surround de 8 canales -7.# Pero si no sabes que eligir es recomendado que no hagas ningún cambio.

Buses
Normalmente se va crear un Bus master estéreo con las salidas conectadas a las dos primeras salidas de tu tarjeta de sonido. Un Bus master es un Bus al que todas las pistas y Buses (o la mayoría) envían su señal. Es conveniente porque proporciona un punto de control único para la salida de Ardour, y es una localización típica para efectos globales. Por esto, el uso de un Bus master está activado por defecto, y el Bus master está configurado como estéreo (2 entradas, 2 salidas). Todas las pistas nuevas tendrán sus salidas enviadas al Bus master todas las pistas nuevas tendrán las entradas conectadas a lo que Ardour crea que es la entrada(s) de tu tarjeta de audio.
En tal caso, desactívalo haciendo clic en el botón junto a Crear Bus master. También puede ocurrir que quieras usar otra configuración de canales en la salida master (por ejemplo, sonido surround de 8 canales 7.1). En ese caso, tendrás que hacer clic en el clickbox para poner el número de canales del Bus master en el valor que quieras.

Entradas
Hay dos opciones disponibles para configurar las entradas de las pistas: la primera, Conectar a entradas físicas automáticamente, por defecto viene activada. Si lo dejas así, las entradas de las nuevas pistas serán conectadas a las entradas de tu tarjeta de sonido. Si la desactivas, será asunto tuyo configurar las entradas para cada pista. 

Salidas
Por defecto veremos que está activada la opción Conectar salidas automáticamente, lo que significa que Ardour conectará automáticamente las salidas de las pistas que se creen. A continuación hemos de optar entre que esa conexión automática sea hacia el Bus master (activada por defecto) o hacia las salidas físicas. Esta segunda opción se usa si no queremos usar el Bus master (evidentemente), por ejemplo porque estemos enviando la salida de Ardour a una mesa de mezclas externa. Si activamos la opción Usar solo X salidas físicas, Ardour creará en cada pista tantas salidas como le indiquemos; si la dejamos desactivada, hará lo que le parezca más adecuado.

### Configurar el audio 
Antes de empezar a usar Ardour, necesitarás tener las entradas y salidas de tu ordenador correctamente configuradas para trabajar o con el sistema de audio preferido (JACK, ALSA, CoreAudio o PortAudio). Selecciona tu dispositivo de entrada y salida. Por medio del botón Device Control Panel se puede abrir el controlador (driver) de tu interfaz audio para configurar el interfaz audio.
Si estas listo, haz clic en Start y espera hasta que se va la palabra roja Parado y cambia a Running. Mientras, Ardour realiza las conexiones y carga los Plugins. Esta ventana se cerrará pero si quieres puedes mostrarla otra vez cuando vas en el menú Ver → Configuración Audio/MIDI.

Nota: Si quieres usar JACK en GNU/Linux pero recibes un error que no se puede abrir el sistema de audio puede ser que te ayude parar JACK en un terminal [Alt + F2] y entra el comando: 
**jack_control exit **

## Visión general de la interfaz
Cuando Ardour arranca con una sesión por defecto, hay una sola ventana visible llamada con la barra de transporte y el Editor. Sin embargo, el programa tiene muchas más ventanas que se pueden visualizar para diferentes propósitos. 
Ardour proporciona dos maneras de ver una sesión: El Editor y el Mezclador. El Editor muestra la sesión representando las pistas como líneas de tiempo horizontales, con el material contenido en las pistas (audio, MIDI, video, datos de automatización, etc.) ordenado a lo largo del eje horizontal (tiempo). El Mezclador muestra la sesión representando las pistas como tiras de mezcla verticales, con controles de ganancia, activado de grabación, solo, etc. En abstracto, el Editor representa los aspectos de la sesión basados en tiempo, mientras que el Mezclador representa el flujo de la señal. En seguido te presentamos los tres áreas:

### La barra de transporte
Esta barra proporciona control completo sobre todas las funciones de transporte de Ardour a la izquierda, los relojes al centro y los botones para mostrar las ventanas del Editor, Mezclador y las Preferencias. Inicialmente está incluida en la ventana Editor, pero también se muestra si vamos en la ventana Mezclador o Preferencias.

Ir al Inicio Bucleo  Play   Activar Grabar   Reloj primario y secundario Botones para cambiar la ventana

Claqueta   Ir al Final      Detener   Activar que el curso vuelve después de parar   Desactiva todos los solos

Hay dos relojes las cuales pueden mostrar el tiempo en una cantidad de formatos: **Timecode (Código de tiempo), Bars:Beats (Compases:Pulsos), Minutos:Segundos y Samples (Muestras)**. Clic derecho para cambiar el formato de los dos relojes.

### Ventana Editor
Esta es la ventana principal de Ardour. Contiene la linea de tiempo, con sus varias reglas, así como las pistas de audio y MIDI. Es perfectamente posible controlar todos los aspectos de flujo de señal desde el Editor, sin la vista general que proporciona el Mezclador. Si acudimos al menú **Ver → Mostrar Mezclador** en Editor o usamos el atajo [Mayusc.+ E], aparecerá una sola banda de mezcla en el extremo izquierdo de la ventana Editor. Al hacer clic en cualquiera de las pistas en el área de visualización de las pistas, la tira de mezcla de la izquierda pasará a reflejar los valores correspondientes de esta pista. Por eso, sobre todo durante las fases iniciales, el Editor puede ser la única ventana que necesites.


#### Modos de edición, 

Los controles de Modo de edición y Modos de cursor definen el comportamiento de lienzo principal y las diferentes funciones que el cursor puede tener. Hay tres modos de edición en el menú desplegable:
**Deslizar
Rizado (o Ripple)
Bloquear** (ningún objeto se puede mover)
Tras el menú desplegable están los modos de cursor:
**Smart / Modo inteligente** - suma las funciones del modo objeto con el modo de rango. Si está activado el ratón se comporta como el modo rango en la mitad superior de una región y en la mitad inferior funcionará como en modo objeto. [ Y]
**Seleccionar/Mover objeto** – permite seleccionar un objeto [ G]
**Seleccionar/Mover rango** – permite seleccionar y mover un rango [ R]
**Recortar** – permite dividir una región [ C].
**Estirar/Contraer regiones** – permite cambiar el tempo de una región manteniendo el tono [ T]
**Modo Audición** - permite escuchar las regiones o pistas marcadas
**Automatización** – permite dibujar regiones, notas, curvas directamente en la pista (por ejemplo notas MIDI o curva de ganancia) [ D] 
**Modo edición interna** - para editar automatización de ganancia o notas [ E]
La mayoría de estos modos de ratón se analizan más ampliamente en el capítulo Trabajando con las regiones. Los dos últimos modos de cursos se discuten en el capítulo Automatización.

#### Modo de zoom 
Entre los Modos de cursor y Modo de ajuste están las opciones de Zoom. Aquí puedes definir el comportamiento de las operaciones de zoom. Tiene dos botones, uno zoom in y otro zoom out, más uno tercero llamado Zoom a la sesión (útil para tener una visión general de toda la sesión: Hace un zoom para que se ajuste al espacio disponible en la pantalla).
Importante: Utilice los atajos del teclado:  = (signo igual en el teclado principal) para acercar o zoom +, y - (guión la tecla en el teclado principal) para alejar o zoom -

El siguiente menú desplegable controla el foco del zoom. Es decir, define el punto de enfoque de las operaciones de zoom, desde dónde comienza a ampliar o reducir. Por ejemplo, escoger la marca activa causará que el zoom se comporte en relación a la posición de la marca activa. Si lo dejamos en ratón,  tomará la posición actual del ratón como la referencia, y así sucesivamente. El siguiente menú desplegable y los dos últimos botones son el control zoom vertical. Permiten ampliar y reducir el tamaño de todas las pistas y Buses verticalmente. Utilice el menú desplegable para elegir un determinado número de pistas que desee para que quepa en la pantalla. Utilice los botones para reducir o aumentar todas las pistas (o pistas seleccionados, si se ha realizado una selección).

#### Modo de ajuste
Los menús **Modo de ajuste** se encuentran justo bajo los relojes. Controlan la cantidad de Subdivisión de la rejilla de tiempo, por ejem.: la cantidad de "ajuste" que una Región de audio tiene para el tipo de rejilla que hayas escogido.

Cuando se selecciona **Sin Rejilla**, las Regiones pueden ser movidas alrededor libremente dentro de las Pistas. Cuando se selecciona Rejilla, las Regiones se ajustarán a Punto de Rejilla más cercano. Cuando se selecciona Magnético, las Regiones pueden moverse libremente pero se ajustarán a un Punto de Rejilla cuando se muevan muy cerca de uno. El menú de Unidades medias se utiliza para seleccionar qué serán los puntos de Rejilla, tales como Pulsos, Compases, Marcas, Minutos, Segundos, varios aspectos del Código de tiempo SMPTE, o los bordes de las Regiones.

#### Las reglas

Debido a que diferentes usuarios querrán utilizar Ardour para diferentes tareas, el modo en que el tiempo es medido en puede ser cambiado. Los usuarios que crean obras de audio, documentales, reportajes o paisajes sonoros pueden desear utilizar Minutos y Segundos, por ejemplo, mientras aquellas bandas que graben o produzcan música pop o  electrónica utilizarán lo mas probablemente Compases y Pulsos. Los productores de vídeo encontrarán útil un Timecode (Código de tiempo) de cuadros-por-segundo, mientras que aquellos que deseen precisión extrema puede incluso querer usar Samples (Muestras). Todos estos pueden ser vistos en Ardour y utilizados como medios para organizar vuestras regiones y ediciones.

    Nota: Para ver/ocultar reglas en la línea de tiempo haz clic en el menú Ver→ Reglas o clic derecho en la linea de tiempo y (de)selecciona la que (no) necesitas.

En las reglas Métrica y Tempo es posible de poner una métrica y tempo para la sesión entera de Ardour, así como cambiarlos en puntos diferentes en la misma sesión. 
Para trabajar con el Timecode (Código de tiempo) de vídeo, primero necesitas establecer las fps del Código de tiempo (Cuadros por segundo). Esto puede encontrar en la pestaña de Timecode de las Propiedades de Sesión en el menú principal de Ardour bajo Sesión → Propiedades [Alt + O].

#### Pistas y Buses
Justo bajo las reglas es donde las pistas y los Buses son mostrados. En el ejemplo a la derecha, puedes ver un Bus llamado master debajo de una pistas llamadas "01_Kick". Esta pista de Audio también contiene una región, la cual representa un fichero de audio con un dibujo de su forma de onda. Más información sobre las Pistas y Buses puede encontrarse en el capítulo Crear una Pista o un Bus.

#### Mezclador del Editor
El Mezclador del Editor está ubicado a la izquierda de la Ventana del Editor. Muestra la Banda de Mezcla de la pista o Bus actualmente seleccionado. Controla el volumen, los Plugins y enrutamiento para esa pista o Bus al que corresponde. Puedes cambiar de mostrar a ocultar el Mezclador del Editor pinchando en el menú Ver → Mostrar Mezclador del Editor [Mayús. + E]. Este mezclador se cubre en el capítulo La Banda de Mezcla.

###7. Regiones, Pistas/Buses, Capturas, Grupos de edición, Trozos
A la derecha del Editor se puede mostrar la Ventana del Editor de Ardour que tiene cinco funciones diferentes, dependiendo de que pestaña esté actualmente seleccionada: Regiones, Pistas/Buses, Capturas, Grupos de edición, y Trozos. Aparece desde Ver → Mostrar vista de Editor. Regiones es la pestaña seleccionada por defecto. Esta parte de la Ventana del Editor se denomina comúnmente como Lista de Regiones. Más información sobre Regiones puede hallarse en el capítulo Trabajar con Regiones. La pestaña de la Pista se cubre en el capítulo Organizar Pistas.

Nota: Las Regiones representan ficheros de audio almacenados en el disco duro las cuales pueden ser arrastradas desde la lista de Regiones directamente sobre el lienzo principal. 

### Controles de la Ventana del Mezclador
La ventana del Mezclador completo se abre aparte yendo al menú Ventana → Mostrar Mezclador [Alt + M].
La función principal de la Ventana del Mezclador es mostrar todas las bandas de mezcla para cada una de las pistas. Esta ventana se utiliza principalmente durante el proceso de Mezcla, y también proporciona acceso a Plugins y otras características de Enrutamiento. Mira los capítulos de Comprender el enrutado, Mezcla y Utilizar Plugins para los detalles.

Esta ventana también contiene un listado de las Bandas de mezcla disponibles en la esquina superior izquierda. Las cajas de marcado en este área pueden utilizarse para mostrar y ocultar las Bandas de Mezcla de las diferentes Pistas. Encima de las Bandas de Mezcla hay un área para gestionar Grupos.

### Cambiar entre ventanas, pegar y despegar ventanas
Ya sabes que puedes utilizar la combinación de teclas [Alt + M] para poder conmutar cual ventana esté encima: del Editor o del Mezclador. Si usas dos monitores tal vez quieres tener en un monitor el Editor y en el otro el Mezclador. En este caso necesitas despegar una de las ventanas. Esto se hace por medio del menú Ver. Busca la ventana que quieres despegar y vas en → Desacoplar. El menú despegado será una ventana separada de tu pantalla. Para acoplar vas otra vez al menú Ver, buscas la ventana y vas en  → Acoplar.

## Crear una Pista o un Bus
Que es una Pista?
Una Pista es un lugar donde puedes donde puedes grabar sonidos que procedan de una fuente externa nueva (por ejemplo de tu interfaz audio) o arrastrar una Región desde tu Lista de Regiones. 

Que es una Región?
Una Región representa un fragmento de audio, por ejem.: uno de tus ficheros de sonido o justo una porción del fichero de sonido. En la imagen al lado, el área marcada "01_Kick" es una Pista, y la información de audio dentro de aquella Pista es una Región.

Que es un Bus?
Un Bus es similar a una pista exceptuando que no contiene regiones propias. No puedes grabar directamente en un Bus o arrastrar regiones a él. En Ardour el área marcada "master" es un Bus, como puedes ver en la imagen arriba.  Normalmente cada sesión tiene un Bus master. Todo el audio para ser exportado de tu Sesión será enviada al Bus master sumando las diferentes pistas en una sola.

### ¿Cómo se utilizan las Pistas y los Buses?
Las Pistas de Audio pueden ser enrutadas a Buses. De hecho, se pueden enrutar simultáneamente muchas Pistas a un Bus. Los Buses se utilizaban tradicionalmente como un modo conveniente para aplicar cualquier tipo de señal a muchas Pistas al tiempo. Por ejemplo, podrías encontrar útil enrutar todas las Pistas que contienen sonidos de tambor a un sólo Bus que podrías llamar 'Bus de Batería'. Entonces, si decides que todas tus Pistas de tambor son demasiado sonoras, puedes ajustar rápidamente el nivel del 'Bus de Batería' más que ajustar cada pista separada que llegue a él.
Otro uso de un Bus sería el tener un Plugin Reverberación común, tal que cualquier Pista de audio que requiera el efecto de Reverberación podría enrutarse a un solo Bus.
Entonces, Plugins y Automatización pueden ser aplicados tanto a Pistas como Buses.

### Añadir Pistas y Buses
Para grabar audio o MIDI hay que añadir primero las pistas que van a contener la información audio o MIDI. Hay 4 maneras de como añadir pistas o Buses.  
1) Clic derecho en el área vacía de la izquierda, debajo de la última pista o Bus añadido
2) Clic en el menú Sesión → Añadir Pista/Bus/VCA.
3) Clic en el menú Pista → Añadir Pista/Bus/VCA
4) Con [Ctrl + Mayus. + N].

En la ventana que aparece puedes encontrar los siguientes opciones:
Añadir permite especificar cuántas Pistas o Buses querrías crear al mismo tiempo.
Escoge Pistas o Buses para especificar si quieres crear Pistas o Buses. O si quieres crear pistas para música digital MIDI o Audio+MIDI.
Coloca un nombre a tu pista y en el menú desplegable Configuración te permite especificar cuántos canales de audio querrías que manejara la nueva Pista o Bus o si quieres que sea Mono o Estéreo. Esta opción afectará posteriormente el tipo de fichero de audio que puedan ser importados a la Pista.
La siguiente opción, Modo grabación, te da una opción entre el Modo Normal y Modo de Cinta. El Modo Normal crea una nueva Región para cada Toma  de Grabación, y se sugiere para los principiantes. El Modo de Cinta graba destructivamente. En otras palabras la Toma previa de una Pista es eliminada con cada nueva Toma.
Finalmente, pincha el botón Añadir para crear las Pistas o Buses que justo acabas de configurar. Los verás aparecer como nuevas filas en el Área de trabajo principal al final o al inicio de la selección en función de lo que eligieras en la ventana en el desplegable Insert.

### Grabar Audio
Para grabar nuevo audio puedes usar la fuente de las entradas de línea o de micrófono de tu interfaz de audio, o incluso podría ser sonido originándose desde otras aplicaciones en tu ordenador las cuales hayan sido conectadas a Ardour. Por favor mira la sección sobre Enrutamiento en Ardour para mayor detalle.
Esta sección te mostrará cómo grabar audio desde una fuente externa (por ejemplo, un micrófono) en una pista de Ardour.

# Tendrías que comprobar que las entradas apropiadas han sido enrutadas a la pista a la que deseas grabar.
# Selecciona la pista pinchando en el espacio vacío justo bajo su nombre y el deslizador de volumen. La Pista queda destacada.
# La Banda de Mezcla vertical ubicada en la parte izquierda de la Ventana del Editor tendría que mostrar ahora la pista que justo has seleccionado (01_Kick en este ejemplo).
Importante: Si no puedes ver el canal o banda de mezcla usa el atajo de teclado [Mayus. + E] o ve al menú principal en Ver → Mostrar Mezclador en Editor. 
# Justo bajo el nombre de la Pista en la Banda de Mezcla encontrarás un botón que te deja editar el Enrutamiento.
# Pincha en ese botón y selecciona Editar para investigar el Enrutamiento.

#### Armar la Pista
"Armar la Pista" es sencillamente dejarla preparada para grabar. Una vez hayas comprobado que las entradas de captura apropiadas han sido enrutadas a la Pista, puedes armar la Pista para grabar pinchando en el icono rojo pequeño en la banda de pista horizontal (no el grande de los controles de Transporte) o el botón Grabar en la Banda de Mezcla. Cuando esté correctamente armada, el icono rojo pequeño quedará destacado, y serás capaz de ver la señal de entrada mirando en el Medidor de Picos en la Banda de Mezcla o en la banda de Pista horizontal.

Nota: a no ser que hayas dicho a Ardour que actúe de otro modo, la entrada que se graba será monitorizada (en otras palabras, oída) vía la salida Escucha. Si no estás utilizando auriculares para controlar el proceso de grabación, ¡puede que consigas alguna fuerte retroalimentación llegando a este punto!

#### Armar Ardour e Iniciar la grabación
Ahora que has armado la Pista para grabarla, tienes que armar Ardour mismo para grabar pinchando en el botón rojo grande en la barra de Transporte.El botón parpadeará en rojo, indicando que Ardour está listo para grabar. Para empezar a grabar, pincha en el botón Play del menú de Transporte, o pulsar la barra espaciadora de tu teclado de ordenador. Pinchar el botón Play de nuevo (o pulsar la barra espaciadora) parará la grabación.
Mientras que grabe, la Pista armada capturará los sonidos de la entrada. Cualquier sonido existente en otras pistas se reproducirá normalmente durante la grabación. Esto de permite reproducir, cantar o hablar junto con otras Regiones y pistas que ya hayas grabado o incrustado en tu Sesión.
Mientras que grabe, serás capaz de ver los Niveles (la amplitud en decibelios) del sonido entrante, así como ver los Picos de la Forma de onda que aparezcan según se esté grabando.

Importante: ¿Mencionamos lo importante que es guardar el trabajo con frecuencia? Haz clic en [Ctrl + S] en este momento. Adquiere el hábito de teclear [Ctrl + S] cada pocos minutos.

#### Evitar Saturación
El audio en la captura de pantalla abajo fue grabado demasiado fuerte y produjo Saturación (en otras palabras, la señal grabada estaba fuera de los límites de lo que podría ser representado digitalmente), lo cual resulta en una pérdida de información y en distorsión audible. Los picos saturados en la forma de onda se marcan en blanco, y el Medidor de Picos en la Banda de Mezcla ha registrado un nivel de señal máximo sobre el límite de cero decibelios.
La manera mejor y más fácil para evitar la Saturación es tener algún control sobre el volumen de la señal de audio entrante antes de que llegue a la tarjeta de sonido. Por ejemplo, puedes mover el micrófono más lejos del sonido grabándose o utilizar un mezclador para reducir el volumen de la señal entrante.

La señal de audio debe ser grabada dentro de límites apropiados. No debe haber Picos rojos, y el medidor de nivel debe dejar una distancia cómoda hasta el punto de Saturación.
El rango de decibelios entre el Pico máximo de la región y el punto de Saturación es generalmente referido como Margen. Es práctica común de grabación el mantener aproximadamente de tres a seis Decibelios de Margen entre el máximo de tu señal y el Punto de Saturación, siendo este Punto de truncamiento representado como 0dB (cero Decibelios). En otras palabras, una región de audio con una cantidad cómoda de Margen tendría sus Picos Máximos entre −6dB y −3dB.

El audio grabado aparece como una Región nueva en la Pista de grabación. Como todas las Regiones, esta nueva región grabada estará disponible en la Lista de Regiones (mostrar en el menú  Ver → Mostrar lista de Editor) , de donde la puedes arrastrar-y-soltar a otras Pistas si se necesita.

La región que acabas de grabar automáticamente recibirá el nombre de la pista en la que se grabó, con diferentes tomas numerados de forma automática. En la pantalla al lado, "Guitar 2-1" y "Guitar 2-2" representan dos diferentes grabaciones realizadas en una pista llamada "Guitar 2".

Puedes planificar con anticipación y organizar tu sesión de grabación dando los nombres apropiados a las diferentes pistas. Por ejemplo, una Pista utilizada sólo para grabar cantos puede ser llamada "Guitar". De este modo, los archivos de sonido grabados serán nombrados consiguientemente, y las diferentes tomas aparecerán en la Lista de Regiones identificadas como "Guitar-1", "Guitar-2", etc, en vez de los nombre genéricos por defecto, como "Audio 1".
Para renombrar una Pista, pincha justo en su nombre (antes de que armes la pista para grabar) y escribe el nombre nuevo.

#### No capto ninguna señal cuando grabo...
El problema más común para los usuarios de audio novatos en GNU/Linux es intentar grabar algo y no obtener ninguna señal en absoluto, o una señal muy baja. El problema de la señal baja típicamente surge de una de las siguientes causas:
Un micrófono conectado a la toma line de la tarjeta de sonido. Los niveles de la señal producida por un micrófono son muy bajos y necesitan ser amplificados antes de poder ser empleados en la mayoría de circuitos de audio. En los estudios de grabación profesionales, esto se hace mediante hardware dedicado llamado "pre-amplificador". Si tu tarjeta de sonido tiene un entrada mic, entonces tiene su propio pre-amplificador integrado en la tarjeta, aunque probablemente no será muy bueno. Si por error conectas un micro en la entrada line, la señal que obtengas será inaudible o muy baja.
Se has seleccionado la fuente de captura equivocada en el mezclador de la tarjeta de sonido.
La ganancia del canal "captura" en el mezclador de la tarjeta de sonido se ha ajustado a un nivel demasiado bajo. Necesitarás ajustarla a un nivel adecuado.
Nota: En Ardour, notarás que la tira del mezclador para cada pista permite cambiar la selección de monitorear entre input/pre/post. Ajustar el Fader mientras se controlan los niveles "input" NO tendrá ningún efecto en los niveles. Como se ha dicho antes, Ardour depende de los ajustes del mezclador externo.
Por ultimo revisa la ventana de Conexiones de audio [Alt + P] , o a través de la ventana de menú Ventana → Conexiones de audio. Al lado izquierda están los Orígenes y en la parte inferior derecha están los Destinos. Revisa si el hardware (tu tarjeta de sonido) esta conectado al Bus master. Cada punto verde representa una conexión. Sino, haz clic en la matriz para realizar la conexión manualmente. Ver el capitulo siguiente para entender mejor el enrutamiento de Ardour.

## Comprender el enrutamiento
Enrutar una señal de audio es enviarla desde algún sitio a algún otro sitio más. Además de conseguir señales de audio a y desde Ardour, el enrutamiento juega una parte importante dentro de Ardour mismo. Ejemplos de utilizar enrutamiento dentro de Ardour incluyen audio desde Pistas al Bus master o a otros Buses, crear 'envíos', enrutar las salidas desde los Buses al Bus master, etc. (mira el capítulo Crear una Pista para una explicación sobre Pistas y Buses). 

### Enrutamiento en Ardour
El enrutamiento estándar de entradas, pistas y Buses en Ardour se determina cuando una Sesión nueva es creada en las Opciones Avanzadas de la caja de diálogo Sesión Nueva (mira el capítulo Iniciar una Sesión). Por defecto, el enrutamiento es como sigue:
Las entradas del dispositivo de audio son enrutadas a las entradas de Pistas.
Todas las salidas desde las Pistas y Buses son enrutadas a las entradas de Bus Master (ver imagen al lado: La Pista 1 out L va a la pista Master in L, la Pista 2 out L va al Master in R).
Las salidas del Bus Master son enrutadas a las salidas del dispositivo de audio.
Esta configuración de enrutamiento es básica y tiene sentido para las sesiones que contienen sólo Pistas, pero para hacer uso de los Buses (que no sea el Bus Master) o para ser creativo con las señales de audio dentro de Ardour, tenemos que ser capaces de cambiar el enrutamiento.

La ventana de Conexiones de Audio es la principal manera de hacer conexiones hacia, desde y dentro de Ardour. Puede abrir esta ventana con el atajo [Alt + P] , o a través de la ventana de menú Ventana → Conexiones de audio.

El área de control o presenta dos grupos de puertos; un conjunto de fuentes llamadas Orígenes, y uno de Destinos. Las orígenes y los destinos son organizadas por pestañas. Las fuentes-orígenes disponibles se visualizan verticalmente en el lado izquierdo, y los destinos se visualizan horizontalmente en la parte inferior.

En la pantalla al lado, observa que la pestaña hardware se selecciona en la parte superior izquierda (que es una fuente u origen), y el Pistas Ardour se selecciona como destino en la parte inferior. Esto significa que la matriz muestra las conexiones de las fuentes de sonido del hardware disponible (por ejemplo, un micrófono), para las pistas de Ardour existentes.
Los puntos verdes representan una conexión. La imagen anterior nos dice que los sonidos entrantes de "sistema: capture_1" (la primera fuente de entrada de la tarjeta de sonido, o el micrófono incorporado del equipo portátil) están entrando en la pista Ardour llamada "Audio 1 in", y también que los sonidos entrantes de "sistema: capture_1" y "sistema: capture_2" van respectivamente a las entradas izquierda y derecha de la pista Ardour nombre "Audio #"

Nota: Recuerda que "Audio 1" es una pista mono. Lo vimos en la pantalla anterior que "Audio 1" sólo tiene una ranura de entrada. Pero ahora en la pantalla de arriba se ve que "Audio 1" tiene dos salidas (izquierda y derecha). Esto es normal: definimos que una pista es mono o estéreo por su número de entradas, no de salidas. Las pistas mono sostendrán un solo canal de audio, pero aún así se puede optar por colocar el sonido al altavoz izquierdo o al derecho (o en cualquier lugar o en el medio).

Por último, vamos a explorar un par de pestañas en la Ventana de Conexiones de audio para ver el sonido que va desde el Bus Master a las salidas de hardware reales (tus altavoces o auriculares):
Como se puede ver, en Origenes está seleccionado es ahora Buses Ardour y la pestaña de Destinos es hardware. En esta sesión se pasa a tener un único Bus, el Master que como dijimos es el seleccionado por defecto. Los puntos verdes muestran que todos los sonidos que salen del Bus Master van a la reproducción del sistema 1 y 2, que son las salidas de la tarjeta de sonido.

Importante: Para realizar una conexión, haz clic en el cuadrado vacío deseado que se encuentra en la matriz; un punto verde aparecerá para indicar que se realizó la conexión. Para deshacer una conexión, simplemente haz clic en un punto verde existente y este desaparecerá.

### Ejemplo práctico de enrutamiento a Buses
A veces puede ser útil para controlar el volumen de varias pistas con un solo Fader. En la siguiente sesión de ejemplo, hay dos pistas de guitarra y un Bus no utilizado que se llama “Guitar-Bus”, todo estéreo.
Supongamos que deseas enviar la salida de las dos pistas de guitarra al Guitar Bus en lugar de enviar al Bus Master. Esto te permitirá controlar el volumen de las dos guitarras con un solo Fader (en este caso el Fader será el “Guitar-Bus”). A continuación, la salida del Guitar-Bus, que es la suma de las dos guitarras, va directamente al Bus Master.
En la imagen que tienes a continuación se muestra el enrutamiento que se debe realizar para el caso expuesto anteriormente. Selecciona las Pistas Ardour en las pestañas verticales donde están las Origen y elige Ardour Buses en los Destinos que se encuentran en las pestañas inferiores horizontales. Lo primero es deshacer con un clic las conexiones existentes que probablemente lleven las guitarras al Bus Master. A continuación, con un clic sobre los cuadros para que aparezcan las conexiones verdes, crea las conexiones entre las dos pistas de la guitarra (“Guitar1 out” y “Guitar2 out”) con el “Guitar-Bus”. El resultado final sería el siguiente:

Ahora ambas pistas de guitarras están enrutadas al Guitar-Bus y ya no se conectan directamente al Bus Master. A continuación, nos aseguramos de que el Guitar-Bus es, por su parte, encaminada al Bus Master (el direccionamiento de salida de un Bus se edita en la misma forma que para una pista), de modo que aún podemos oír el sonido de ambas pistas de guitarra. Y podemos controlar el volumen de ambas pistas juntas al cambiar el deslizador del “Guitar-Bus”. Lo que es más, ahora podemos añadir Plugins para el “Guitar-Bus” para procesar el sonido de las dos pistas de guitarra juntos.

A veces abrir la Ventana de Conexiones audio no es necesario si lo que se desea es sólo cambiar rápidamente el encaminamiento de una sola entrada o salida de la pista. Ardour permite acceder a un subconjunto importante de conexiones cuando se hace clic directamente en el botón de entradas o salidas de una pista o Bus en el mezclador.
El botón de entradas está en la parte superior, y el botón de salidas es similar y se encuentra en la parte inferior del mezclador. Al hacer clic en cualquiera de los dos se mostrará un menú de opciones de conexión. En la pantalla abajo, por ejemplo, tendrías que hacer clic en el botón "1" justo debajo del nombre de la pista "Guitar 1" con el fin de acceder a este menú:

Puedes seleccionar una conexión en ese mismo menú, o elije Routing Grid para ver una versión más sencilla del gestor de conexiones de audio que contiene sólo las entradas o salidas de la pista o el Bus seleccionado.

En este capítulo, cubrimos cómo gestionar el Enrutamiento dentro de Ardour, o entre Ardour y la tarjeta de sonido. Aun así, uno de las fortalezas de utilizar el sistema JACK es que también pueda gestionar conexiones entre aplicaciones en el mismo ordenador. Para obtener un mejor entendimiento de cómo funciona esto, por favor continúa al capítulo Enrutamiento entre Aplicaciones. Si preferirías trabajar sólo con Ardour, entonces salta adelante hasta la sección Usar MIDI.

### Enrutamiento entre Aplicaciones
Es posible que en algún momento necesites registrar la salida de audio de otro programa en Ardour (por ejemplo, el sonido de un vídeo de YouTube en Firefox, o la salida de SuperCollider o Hydrogen). En este capítulo se muestra cómo lograr eso.
Los ejemplos de esta página fueron creados en un equipo con Ubuntu. Ten en cuenta que las cosas pueden funcionar de manera diferente en tu GNU/Linux. Los principios generales son siempre los mismos, sin embargo los procedimientos pueden cambiar.

#### Grabar el sonido de una aplicación no JACK en Ardour
Los navegadores web (Firefox, Chromium, etc.) son aplicaciones no JACK. Afortunadamente, los sistemas operativos como KXStudio y UbuntuStudio vienen con una aplicación de puente entre el sistema regular de audio (como PulseAudio) y también JACK. En este tutorial se supone que estás utilizando un equipo con este puente que ya se está ejecutando y trabajando.
Los pasos generales para grabar audio de un navegador (por ejemplo un video) en Ardour son:
1. Crear una pista estéreo en Ardour
2. Desconecta las fuentes de entradas de pista (recuerda, debajo del título, en este caso Firefox, clic en ese botón y selecciona "Desconectar". Aparece un c.
3. Conectar PulseAudio Jack Sink a las entradas de la pista. (tendrías que usar el gestor de conexiones de tu sistema, Cadence, por ejemplo, en GNU/Linux)
4. Inicia la grabación en la pista
5. Inicia la reproducción del sonido (por ejemplo del navegador Firefox)
Para este ejemplo, ...
1. se ha creado una nueva sesión con una pista estéreo llamada "Firefox":
2. se ha seleccionado la pista y en la Tira de la Mezclador como fuente de entrada el guión (= significa que con esta pista todavía no tiene un conexión)
3. Después de desconectar la matrix para la pista “Firefox” debería mostrarse así (sin los puntos verdes)
4. El próximo paso es de cambiar la pestaña en esta ventana: Selecciona Otras. Allí encuentras todas las aplicaciones activas que pueden servir como fuente para Ardour. Si usas PulseAudio Jack bridge, vas a ver PulseAudio JACK Sink como fuente. Haz clic en los rectángulos vacíos para establecer la conexión (círculos verdes) para  “front-left” y “front-right” a la izquierda y la derecha de la pista “Firefox”. Debería mostrarse así.

#### Grabar de aplicaciones con soporte JACK en Ardour
Otros aplicaciones de audio como SuperCollider o Hydrogen funcionan con JACK. Esto significa que van a aparecer con entradas y salidas en las en la ventana Conexiones de audio en Ardour. No necesitas de usar PulseAudio / Jack bridge como en el ejemplo anterior. El procedimiento es muy parecido:  
1) Crear una o varias pistas en Ardour para grabar el audio.
2) Conectar la entrada de la pista con la fuente como te muestra la captura de pantalla siguiente:


La captura de pantalla de arriba muestra la grabación de un patrón de batería de Hydrogen directamente a una pista llamada “from Hydrogen” en Ardour. La ventana de Hydrogen está a la derecha. La ventana de conexiones de audio en Ardour está abierta para mostrar las conexiones: Nota que Hydrogen aparece como fuente en la pestaña Otras. Está conectada directamente a la entrada de la pista. Nota también que SuperCollider (aplicación con soporte JACK) está abierta. SuperCollider tiene 8 salidas por defecto, cuales se muestran como fuentes posibles en la ventana de conexiones de Ardour.

3) Ahora listo para empezar. Solamente sigues el mismo procedimiento como explica el capitulo Grabar audio.
4) Empieza la reproducción de la aplicación: En este caso haz clic en play en Hydrogen y se graba tu patrón de batería a la pista audio en Ardour.

##  Usar MIDI
### Que es MIDI?
MIDI (abreviatura de Musical Instrument Digital Interface) es un estándar tecnológico que describe un protocolo que permite que varios instrumentos musicales electrónicos, computadoras y otros dispositivos relacionados se conecten y comuniquen entre sí. Una simple conexión MIDI puede transmitir hasta dieciséis canales de información que pueden ser conectados a diferentes dispositivos cada uno. MIDI lleva mensajes de eventos que especifican notación musical, tono y velocidad; señales de control para parámetros musicales como lo son la dinámica, el vibrato, paneo y señales de reloj que establecen y sincronizan el tempo entre varios dispositivos. 
Ardour puede 
importar y grabar datos MIDI para mandarlo a un instrumento virtual como “información musical” y se puede procesar esta información (editar, aplicar efectos, etc.). 
en el caso de un hardware externo de MIDI, recibir datos de este (por ejemplo un teclado MIDI), o mandar datos MIDI (cambio del volumen, del balance o estado de Plugins, etc.) de modo que un controlador MIDI motorizado externo puede reflejar los estos cambios causados por la automatización como por ejemplo el Presonus Faderport. También con otros controladores MIDI externos que no son motorizados es probable que Ardour puede enlazar todos sus Faders, panners, botones y todos los parámetros de los Plugins mediante el protocolo MIDI Machine Control (MMC), MIDI Continuous Controller (CC) o mensajes Note On/Off.

### Reproducir notas MIDI con un instrumento virtual: Helm
Vamos a cargar un instrumento virtual dentro de Ardour para reproducir datos MIDI. Por defecto Ardour solo viene con un instrumento virtual que se llama Reasonable synth, pero hay una multitud de instrumentos virtuales disponibles que se pueden instalar. Ver el capitulo Plugins.

En este ejemplo vamos a usar un sintetizador. Sintetizadores son muy importante para la música electrónica. Reciben datos MIDI y devuelven una señal de audio. El modo en que crean una señal de audio varía un poco de uno a otro. Un sintetizador contará con una fórmula u onda geométrica para crear sonido. Los sonidos típicos de un sintetizador comienzan con una onda cuadrada u onda diente de sierra. 

Usamos un sintetizador que se llama Helm, es multi-plataforma Linux/mac OS/Windows y usa la técnicas síntesis sustractiva. Aparte de la síntesis añade una sección de efectos de procesado. Helm es muy fácil de usar: viene con un montón de presets listos para usar de todo tipo de instrumentos, y por otro lado, permite la experimentación con un número enorme de parámetros y estrategias de síntesis. Puedes descargar el sintetizador en la pagina web: http://tytel.org/helm/downloads/
Instala el programa y reinicia Ardour. 
Nota: Para Windows tambien tienes que verificar que esta instalado Microsoft Visual C++ 2015 Redistributable Update 3 RC en tu sistema.
Los pasos para añadir una pista MIDI con un instrumento virtual es (igual como añadimos una pista de audio): 
1) Damos clic en el menú Pista → Añadir pista o Bus
2) En la ventana que aparece seleccionamos Añadir 1 Pistas MIDI y abajo donde dice Instrumento: Helm.
3) Damos clic en el botón Añadir
4) Ahora vamos a insertar notas MIDI con el ratón: Seleccionamos el lápiz (Tecla D) en las herramientas.


5) Dibujamos un rectángulo de algunos compases en la pista MIDI. Pulsamos en la pista y arrastramos el cursor hacia la derecha. Se muestra una región MIDI donde vamos a insertar las notas.  
6) Vamos a alargar la pista pulsando en y arrastrando hacia abajo. Ahora se muestra el Piano-Roll, las teclas blancas y negras de un teclado. 
7) Insertamos las notas con el mismo lápiz, pulsando y arrastrando hacia la derecha en la nota que queremos. Ardour siempre te muestra el nombre de la nota que estas insertando.
8) Reproduzca las notas con el botón Play (o la tecla espaciadora)

### Grabar notas MIDI con un teclado externo
Insertar notas MIDI con el ratón consume bastante tiempo. Si dispones de un teclado MIDI externo puedes grabar estas notas en tiempo real. Ardour reconoce por defecto los dispositivos MIDI genéricos gracias a ALSAMIDI. Conecta tu dispositivo y prueba si aparece en la lista en la banda de mezcla debajo de donde dice MIDI. La pantalla a la izquierda muestra que está conectado un teclado Keystation (de M-Audio).
Haz clic en el botón al lado para que se activa la entrada de datos MIDI a esta pista. Prueba si suena el instrumento virtual. Ahora para grabar arma tu pista MIDI para grabar y haz clic en el botón grabar. Deberías ver como se dibuja las notas MIDI en la pista. 
Para editar notas MIDI usa la herramienta de edición interna [ E]. 


Para eliminar, transponer, crear legato, cuantificar, eliminar solapamiento o transformar notas MIDI solo selecciona las notas y haz clic derecho (en una de las notas seleccionadas) para editarlas todas a la vez. 

### Usar controladores externos de MIDI
Ya explicamos que Ardour puede recibir datos MIDI (cambio del volumen, del balance o estado de Plugins, etc.) no solo de un teclado sino también de un controlador externo, o mandar datos MIDI a este controlador MIDI que va a reflejar los estos cambios. Esto puede ser muy útil en el momento de la edición y mezcla. 
Para usar controladores externos de MIDI en Ardour necesitas ir a la ventana Preferencias y Buscar en la lista a la izquierda la opción Superficies de control 

Si aparece tu controlador en la lista: Perfecto! Seleccionalo. Sino 
1) intenta con Generic MIDI
2) Conecta el puerto MIDI de Ardour llamado control a tu hardware
3) Haz clic CENTRO (con el botón del centro de tu ratón) en un Fader, parámetro de Plugin, botón etc. que quieres controlar. Una pequeña ventana aparece que dice Operate Controller now
4) Mueve el botón/Fader de tu controlador o presiona el botón.
5) Se completó el enrutamiento. Si mueves el botón Fader de tu controlador externo, Ardour debería reflectar este cambio.

### Sistema de MIDI en Linux
Las entradas y salidas de MIDI Ardour se controla por el misma “motor” como las entradas y salidas de audio. Se puede usar JACK o el soporte nativo MIDI del sistema operativo para recibir y mandar datos MIDI. ALSAMIDI es el estándar para MIDI en GNU/Linux. Mientras, si usas JACK, la aplicación QjackCtl muestra los puertos ALSAMIDI en la pestaña ALSA. QjackCtl es el mismo programa que es recomendado para controlar JACK que incluye un excelente gestor de conexiones MIDI. Si tienes un interfaz MIDI genérico también es probable que en la ventana Configuración Audio/MIDI del menú Ver aparece y puedes calibrarlo allí. 


# 3. Editar Sesiones
## Organizar Pistas
Organizar tus pistas puede ahorrarte mucho tiempo a la hora de los procesos de editar y mezclar audio. Por esto te recomendamos seguir los siguientes pasos. 

### Renombrar y Reorganizar
Es recomendable renombrar las pistas si no tienen un nombre significativo, lo que te ayudará encontrar una pista mas rápido después. En vez de tener una serie de pistas audio llamados “Audio 1”, “Audio 2”, “Audio 3” es mejor renombrarlas según su contenido, por ejemplo: “Bombo”, “Caja”, “Tom1”, Tom2”, etc. 
Haz doble clic en el nombre de la pista para editarlo. 

También puedes desear reorganizar el orden de las pistas de arriba a abajo. Esto se hace en la Ventana del Editor. Hazlo pinchando la pestaña Pistas/Buses en la extrema derecha de la Ventana del Editor y arrastrando-y-soltando las pistas en el orden que prefieras. En el mismo orden como aparecen en la Ventana del Editor (de arriba hacia abajo) van a aparecer también en la Ventana del Mezclador.

Nota: También puedes usar las cajas de marca en esta pestaña para ver u ocultar las Pistas en el Lienzo principal. 

### Configurar la métrica
La métrica determina la velocidad musical del pasaje que estamos componiendo, cuando medimos en pulsos por minuto (beats per minute en inglés). Si estamos componiendo algo que es rítmico, ello determinará también las longitudes de las muestras de sonido que utilizamos hasta cierto punto. Así que es importante ser capaz de configurar la Métrica antes de que continuemos.
Para ver la Métrica de nuestra sesión, podemos hacer clic derecho en cualquier parte del "cabezal" de la línea de tiempo y hacer clic en las siguientes opciones: Métricas, Compases:Pulsos y Tempo en el menú que aparece.

Es posible de poner una Métrica y Tempo para la sesión entera, así como cambiarlos en puntos diferentes en la misma sesión. Para esto, localiza la sección de la Métrica de la Barra de la Línea temporal en la Ventana del Editor, y haz clic-derecho en la primera marca roja pequeña para abrir el Diálogo de Métrica.

Aquí puedes introducir valores nuevos para los Pulsos por compás así como el Valor de Nota. Pincha Aplicar para aplicar los cambios de manera global a tu sesión.
En el Diálogo de Tempo puedes introducir un nuevo valor de Pulsos Por Minuto, lo cual afectará la sesión entera.
Si la Métrica o Tempo de tu sesión cambia más tarde en la canción o composición, sencillamente añade un marcador nuevo haciendo clic-derecho en la sección de Métrica o Tempo y seleccionando un Tempo Nuevo o Métrica Nueva e introduciendo el tempo nuevo o métrica en el diálogo resultante.

### Utilizar Rangos
Un Rango es una selección del la Línea temporal que puede incluir una o más Pistas. La herramienta de Rango se ubica justo bajo el Menú de Transporte en la Ventana del Editor.

Cuando hayas seleccionado la herramienta de rango, tu puntero de ratón se verá como una línea vertical:

Puede ser útil crear selecciones de rango que se alineen con los bordes de las regiones en tu línea temporal. Para esto selecciona los Rejilla y Bordes de Región para los menús de Rejilla y Punto de Rejilla respectivamente hace esto fácil.

Para hacer una selección de rango, arrastra doquiera en la Línea temporal. Las opciones actuales de Rejilla y Punto de la Rejilla determinan exactamente cómo se comporta la selección de rango. Una vez un rango ha sido seleccionado, si haces clic derecho sobre él se abre un menú con operaciones específicas de rango.
Rango de Bucle, por ejemplo, configura los Marcadores de Bucle del Rango actual y empieza una reproducción cíclica. Los puntos de Inicio de Bucle y Fin de Bucle pueden ser cambiados moviendo los triángulos verdes qué corresponden a cada punto.
Otras opciones útiles aquí para editar te permite Duplicar el rango, Seleccionar Todo dentro del rango o Cortar el rango.

### Configurar un Bucle
Si queremos oír el pasaje que estamos componiendo como bucle, tenemos que crear un rango para escuchar dentro de nuestra sesión, de modo que podamos regresar exactamente a este punto de la Sesión una y otra vez:
1) Alejar la imagen si es necesario (acceso directo "-") para ver las barras completas en la línea de tiempo. 
2) Utilizar la herramienta de rango para seleccionar un compás entero con la ayuda de las configuraciones de la Rejilla,
3) Hacer clic derecho dentro de ese rango para Definir bucle según selección.

Probablemente querrás poner la Rejilla de modo que tus acciones se ajusten a ciertos elementos métricos de la sesión. 

Esto configurará un rango de bucle que puedes reproducir utilizando el botón de Reproducir Bucle en el Menú de Transporte o pulsando en la tecla L. Mientras el rango esté ciclando, puedes utilizar el botón Solo en cada pista para escuchar individualmente a cada instrumento.

### Trabajar con Regiones
En Ardour las secciones de audio se conocen como Regiones. Para componer el tipo de pasaje rítmico en que hemos estado trabajando, necesitaremos conocer cómo Seleccionar, Mover, Dividir y Recortar estas regiones, así como conocer cómo Intensificar (fundido de entrada) o Atenuar (fundido de salida) su volumen y crear Fundidos cruzadas (Crossfades) entre ellas. Algunas de estas opciones puede necesitar ocurrir en Puntos de edición específicos de la composición, o según la Métrica musical podemos también definir con la Línea temporal y la Rejilla.

Seleccionar Regiones
El modo Seleccionar/Mover objetos [G] está ubicado justo bajo el menú de Transporte en la Ventana del Editor. Utilizarás mucho esta herramienta en tu trabajo de Ardour.
Cuando esté activo, tu puntero de ratón se verá en el lienzo principal como una pequeña mano:

Realiza las siguientes operaciones para practicar: 
Haz clic en la forma de onda de la región para seleccionarla. Haz clic y arrastra en una región para moverla por distintos lados (izquierda y derecha en la misma pista, sino también hacia arriba y hacia abajo sobre otras pistas).
Usa [Ctrl + Clic] para crear y arrastrar una copia de la región.
Puedes seleccionar varias regiones manteniendo pulsada la tecla "Mayus." mientras seleccionas.
Mover varias regiones al mismo tiempo, después de seleccionarlas.
Se pueden seleccionar varias regiones secuenciales en una pista a la vez, manteniendo pulsada la tecla Mayus. mientras se selecciona la primera y la última Región de la secuencia (copiar unas pocas regiones en la misma pista para probar esto).
Cuando se selecciona una sola región, asegúrese de hacer clic en la par de con el dibujo de forma de onda de su rectángulo. La banda inferior con el nombre de la región se utiliza para una acción diferente (véase Recorte de regiones más abajo).
Utiliza la tecla "Supr" para eliminar regiones seleccionadas.
Las operaciones estándar de copiar [Ctrl + C], cortar [Ctrl + X], y pegar [Ctrl + V] también funcionan con las regiones.
También puede arrastrar un cuadro de selección a través de múltiples regiones para seleccionarlos todos.

### Mover Regiones
Cuando se mueve una Región, un Timecode (Código temporal) aparecerá en números amarillos sobre la pantalla. Este Timecode es el punto de partida de la Región en la Línea de tiempo. Puedes mover Regiones horizontalmente (de lado) a un punto diferente en el tiempo sobre la misma Pista, o puedes mover la Región seleccionada verticalmente (arriba o abajo) a una Pista diferente.
Cuando un conjunto de una o más Regiones es seleccionado, puedes mover el conjunto completo arrastrándolo con el ratón.
Nota: asegúrate de seleccionar la Región en su sección de forma de onda, porque seleccionando el área de barra de título inferior se utiliza para un acción diferente (mira Recortar Regiones abajo).
Consejo: si pulsas y mantienes la tecla Alt mientras que arrastras una Región entre Pistas, la Región será copiada a la Pista nueva en vez de movida.

### Duplicar Regiones
Utilizar la herramienta Seleccionar/Mover Objetos para seleccionar un conjunto de Regiones, y utilizar la función Duplicar para hacer una copia del conjunto. Está en el menú Regiones → Duplicados Región [Alt + D]. 
Los Duplicados aparecerán inmediatamente después (y en la misma pista que) los originales.
En la siguiente captura de pantalla, se ha duplicado una región utilizando los métodos explicados:

### Utilizar Puntos de Edición
Otro modo de copiar regiones es utilizando los comandos estándar Copiar [Ctrl + C] y Pegar [Ctrl + V]. La ubicación exacta donde la Región copiada será pegada está determinada por el menú desplegable de Punto de Edición.
Si se selecciona Ratón como el Punto de Edición, la Región copiada será pegada en la posición actual del ratón.
Si se selecciona Playhead (Marca activa) como el Punto de Edición, la Región copiada será pegada en la línea roja de Marca activa en la misma Pista donde está la Región original.

Finalmente, si se selecciona Marcador como el Punto de edición, entonces la Región copiada se pegará inmediatamente tras el Marcador de ubicación actualmente seleccionado.

### Marcadores
Cuando se crea una nueva sesión, dos marcadores de ubicación se agregan automáticamente de forma predeterminada. Estos son los marcadores de inicio y fin. Si no ve el marcador final, aléjese lo suficiente y lo encontrará.

Pero es muy útil de etiquetar diferentes ubicaciones en una sesión para su uso posterior durante la edición y mezcla. Ardour ofrece varias maneras de hacer esto. El método más común es usar las Marcas de posición, que definen las posiciones específicas en el tiempo.
Los Marcadores pueden añadirse a la Línea temporal haciendo clic derecho en la banda de Marcadores de posición y seleccionando Añadir nueva marca de posición. También pueden ser seleccionados con el ratón y movidos a posiciones nuevas.

#### Dividir Regiones
Para Dividir una Región sencillamente significa dividir una sola Región en dos Regiones independientes. Hay dos maneras de realizar esta acción:
Puedes utilizar el Modo de corte [ C] para hacer clic en cualquier lado que quieras dividir; y,
si el ratón está seleccionado como tu Punto de edición actual, selecciona una Región y coloca el cursor en el punto te gustaría dividir. Pincha en Editar → Dividir Región [ S]. 
Tras ser dividido, la Región única original se transforma en dos regiones independientes, con un nuevo nombre por cada cual:

Las dos nuevas Regiones son ahora enteramente independientes. Puedes mover y editarlas separadamente.
Las Regiones pueden ser divididas Utilizando la Marca activa o un Marcador como el punto de Edición.

#### Recortar regiones
Si mueves el cursor hasta la banda inferior de la Región, donde su nombre aparece, verás que el puntero se torna como una flecha doble. Pincha y arrastra hacia adentro desde cualquier cabo de la Región, y la Región se acortará consiguientemente. Esto se denomina Recortar la Región. Las regiones pueden ser recortadas desde el inicio de la Región (arrastra de izquierda a derecha en el borde) o desde el fin (arrastra de derecha a izquierda).

Esta acción es no destructiva: ningún audio de hecho está siendo eliminado. Es como si justo "escondieras" aquellas porciones de la Región que no quieres o que ya no necesitas más. Después, puedes "des-recortar" la Región (p. ejem.: extenderla otra vez a su medida original total), incluso si ha sido movida o copiada a una Pista nueva. Una región recortada recibirá un nombre derivado del nombre original de su Región fundamental, y verás ésta reflejada en tu Lista de Regiones. 

    Importante: El recorte obedecerá a la configuración de la rejilla. Si no quieres que el recorte se limite a la rejilla, simplemente escoge la opción No rejilla.

#### Eliminar regiones
Una región puede eliminarse de una pista de cuatro formas distintas:
Seleccionar la Región y utilizar la tecla [Supr] (no la tecla de borrar "backspace") para sacarla.
Selecciona la Región y utiliza el atajo [Ctrl + X] para Cortarla (para más tarde pegarla).
Selecciona la Región y utiliza la opción Editar → Cortar en el menú principal para cortarla (para más tarde pegarla).
Otra vez, porque Ardour es no destructivo, las Regiones no son eliminadas de la Sesión y pueden ser accedidas desde la pestaña de Regiones en el lado extremo derecho de la Ventana del Editor.

#### Crear Fundidos de entrada y de salida en las Regiones
Un fade (fundido) es un cambio en el volumen de una Región, bien cuando la Región comienza o bien cuando esta se acaba. Un fade-in al comienzo de la Región es un fundido de entrada, y al final de la Región es un  fundido de salida. Cada Región tiene dos pequeños manipuladores a lo largo de la parte superior, los cuales pueden ser arrastrados hacia adentro desde cualquier borde para crear un fundido de entrada o de salida, como se muestra en la siguiente imagen.

Nota: De hecho, cada región ya tiene un fundido de entrada y de salida por defecto. El fundido de región es muy corto, y sirve para evitar clics en las transiciones al inicio y al final de la región. Mediante el ajuste de las regiones permiten una transición más gradual.

Haciendo clic derecho en las áreas sombreadas azules, se puede ajustar la velocidad del fundido.

#### Crear Fundidos cruzados (Crossfades) entre dos Regiones
Cuando una Región se atenúa mientras otra se intensifica, esto se denomina una Fundido cruzado (Crossfade). Si las dos Regiones están en Pistas diferentes, puedes utilizar el método descrito encima con los manipuladores de atenuación.
Aun así, si ambas Regiones están en la misma Pista, entonces Ardour automáticamente creará un fundido cruzado cuando una Región se mueva sobre otra. No hay necesidad de crear un fundido cruzado específicamente como en otros editores de audio. Cuando una región se superpone con otra Ardour las trata como capas. Esto significa que una región es una capa que está encima de la inferior. Lo importante es entender que: El fundido de entrada o de salida de la región superior representa el fundido cruzado entre las dos regiones.
Una vez que entiendas este principio es sencillo crear y controlar fundidos entre regiones. Aquí hay un ejemplo. Las dos regiones separadas que vemos aquí abajo se superpondrán para crear un fundido cruzado.

    Nota: no hemos agregado ningún fundido extra a la primera región, pero agregamos un fundido más largo a la segunda región. Luego arrastramos la segunda región sobre la primera, superponiéndolas parcialmente:

El fundido de entrada de la segunda región funcionará como el fundido cruzado entre las dos regiones. En otras palabras, la primera región se desvanecerá y a la vez que la segunda región se intensifica.
Para que esto ocurra necesitamos asegurarnos de que la región que queremos que sea la "superior" en el sistema de capas de Ardour. Para cambiar las opciones de capa, selecciona una región y ve al menú Región - Capas.

#### Utilizar Configuraciones de Rejilla
Experimenta con la configuración de la Rejilla, como se habló en el capítulo Configurar la Línea temporal, para dar clases diferentes de Subdivisión - en otras palabras, para limitar las fronteras de cada Región a ciertos puntos de rejilla. Aquí, la Rejilla ha sido activada y puesta a Pulsos/4, para subdividir las Regiones a negras dentro de cada compás. Puedes desear Recortar los extremos de algunas de las muestras, como se habló antes, para que quepan dentro de la estructura métrica has configurado.


## Más operaciones de región
Hacer clic derecho en una Región seleccionada revela un menú contextual. El primer elemento del menú (etiquetado con el nombre de la Región) contiene un gran sub-menú. Esta sección describe unas cuantas de las operaciones más generalmente utilizadas accesibles desde este menú.
El menú de clic derecho de la región encuentras
Reproducir
Reproduce desde el principio hasta el final de la región.
Bucle
Reproduce la región en bucle.
Editar
En este submenu puedes cambiar el tono de la region, revertirla o 
Audition (Escucha)
Más abajo en el menú, la opción Escucha reproduce la Región vía el Bus de Escucha. 
Bloqueo
La caja conmutadora Bloquear bloquea la Región de modo que no pueda ser Movida o Recortada. Todavía puede ser dividida, sin embargo, y las Regiones resultantes serán desbloqueadas.
Normalize (Normalizar)
La función Normalizar aumenta no-destructivamente el nivel de la Región seleccionada de modo que los Picos estén en 0dB. En otras palabras, hace la región tan sonora como fuera posible mientras evita Saturación. El aumento aplicado cuando una Región ha sido normalizada puede ser invertido seleccionando el ítem Desnormalizar de menú.
Análisis espectral
Pinchar esta función abre una nueva ventana la cual exhibe el contenido de frecuencia global de la Región.
Invertir
La función Invertir invierte la región seleccionada de audio, causando en efecto que se reproduzca hacia atrás. Invertir una región crea un archivo de audio nuevo 'entre bambalinas'.
Recortar
La función Recortar recorta la Región en varias maneras, incluyendo desde el Inicio al punto de edición y Punto de edición hasta el fin (mira el capítulo anterior para un debate de Puntos de Edición).
Hacer Regiones Mono
La función Hacer Regiones Mono divide una región estéreo en dos regiones mono las cuales pueden ser accedidas vía la pestaña de Regiones al extremo derecho de la Ventana del Editor.
Duplicar, Multi-duplicar, Llenar Pista
Duplicar, Multi-Duplicar y Llenar Pista son métodos para Duplicar la Región. Por favor mira el capítulo Crear Secciones Cicladas para una discusión detallada de estos.
Eliminar
La función Eliminar borra la Región seleccionada de la Pista. La región permanece disponible en la Lista de Regiones al extremo derecho de la Ventana del Editor, tal que se puede recuperar arrastrándola y soltándola a una pista en cualquier momento.
Siéntete libre de explorar otros sub-menús que no hayamos mencionado en esta sección. Muchos de ellos son opciones que encontrarás en el menús de Regiones de Ardour. A continuación detallaremos las funcionalidades más útiles. 

Cambio de tono
La función de cambio de tono cambia el tono de una región sin cambiar su duración. La función aplica un algoritmo de desplazamiento de afinación para crear un nuevo clip de audio basado en el clip de origen.
La ventana de cambio de tono al usuario especificar la cantidad y dirección de la transposición deseada. La ventana incluye un botón Preserve formantes. Cuando cambio de tono por grandes cantidades, la opción Conservar formantes puede dar resultados que suenan un poco más natural, especialmente cuando se utiliza en el material vocal.

Normalizar
La función Normalizar [Alt + 3] aumenta el nivel de la región seleccionada de manera que los picos estén a 0 dB o menos. Cuando normalicemos a 0,0, la región será tan fuerte como sea posible, evitando recortes. A veces puede resultar útil para normalizar una región a un valor inferior a 0, como -#0, -#0, -#0 o decibelios, para que no llegue a ser demasiado alto.

Invertir
Esta función invierte la región de audio seleccionada, en efecto, haciendo que se reproduzca de atrás para adelante. Invertir una región crea un nuevo archivo de audio.
Operaciones en dos o más rangos seleccionados
Si se selecciona más de un rango, la operación se aplicará a todos ellos (por ejemplo, Normalizar, Invertir, etc.)

Combinar
Algunas operaciones desde el menú contextual sólo estarán disponibles cuando se seleccionen dos o más regiones. Por ejemplo, echa un vistazo a la función "Combinar", bajo el submenú "Editar".
En primer lugar seleccionamos dos regiones adyacentes:

Luego elegimos "combinar" en el menú contextual que se despliega haciendo clic derecho en alguna de las regiones seleccionadas, o desde el menú "Regiones/Editar/Combinar":

Como resultado, las regiones seleccionadas se combinarán en una sola. Esto es particularmente útil cuando se ha encontrado una secuencia exacta de las regiones que trabaja del mismo modo que desee y que, a continuación, te gustaría copiar y/o mover toda la secuencia como grupo.

Nota: Ten en cuenta que la región combinada resultante tiene la palabra "compuesto" unido a su nombre:

## Cambiar Modos de Edición
Ya hemos aprendido un poco sobre las herramientas Seleccionar/Mover y Rango. En este capítulo conseguiremos una visión general de todo los Modos de edición y Modos de Cursor disponibles en aquella parte de la Ventana de Editor.

Estos controles definen el comportamiento del Lienzo principal y las diferentes funciones del cursor.
El menú desplegable Modo de Edición contiene tres opciones. Deslizado es el modo estándar. Te permite arrastrar regiones alrededor horizontalmente (dentro de la misma pista) y verticalmente (entre pistas). Rizado no te permite arrastrar regiones, pero todavía te deja ejecutar operaciones de corte (como cortar,pegar y dividir). El espacio entre las regiones se mantendrá constante tras cualquier operación que lo afecte. Si eliminas la segunda mitad de una región, por ejemplo, cualesquier regiones subsiguientes en la misma pista se moverán automáticamente atrás en la rejilla de tiempo. Bloquear es similar a la Edición Rizado, pero las regiones quedarán en sus posiciones originales a pesar de cualquier operación de edición ejecutada.

Seleccionar/Mover Objeto [ O]
Este Modo de Cursor te permite seleccionar o mover objetos tales como regiones y puntos de ruptura (en una curva de automatización). Cuando este Modo de Cursor se selecciona, tu puntero de cursor se verá así:

Rango [ R]
Este Modo de Cursor te permite pinchar y arrastrar para definir o redimensionar Rangos. Cuando este Modo de Cursor está seleccionado, tu puntero de cursor se verá así:

Modo Cortar [ C]
Usa este curso para dividir regiones en regiones más pequeñas. El cursor se verá como unas pequeñas tijeras. Esto te permitirá cortar donde hagas clic con el cursor. 
Consejo: puedes cortar regiones directamente desde el Modo Seleccionar/arrastrar objeto también (algunas veces puede resultar más práctico). Sin dejar el Modo Seleccionar objeto, simplemente coloca el cursor en la ubicación deseada de corte y aprieta la tecla [S] (de split, dividir en inglés). Importante: tu punto de edición (a la derecha de la configuración de la grilla) debe estar puesta en "Mouse".

Expandir/Encoger Regiones [ T]
Este Modo de Cursor te permite arrastrar y redimensionar la duración de una Región entera sin cambiar el Tono. Esto es a veces llamado “Timestretching” o “expansión de tiempo”, por ello el tecla [T].

Escuchar Regiones específicas
Este Modo de Cursor te permite pinchar en cualquier Región existente sobre cualquier pista y reproducirla inmediatamente. La reproducción para al final de la Región. Cuando este Modo de Cursor se selecciona, tu puntero de cursor se verá así:

Nota: También puedes escuchar rápidamente una región seleccionada sin salir del modo Seleccionar/arrastrar objeto. Simplemente selecciona una región y aprieta la tecla "H". 

Dibujar Automatización de Ganancia [ G]
Utiliza este Modo de Cursor si quieres dibujar la Automatización del volumen de una región específica. La curva de automatización creada de este modo no abandonará la región sobre la que fue creada, incluso cuando la Región se mueva alrededor Este tipo de Automatización de ganancia se dibuja directamente en la Región misma, lo cual lo hace diferente de la Automatización utilizada en la región desplegable de Automatización (mira el capítulo Automatización).

Modo de edición
Use este modo para editar puntos de automatización de ganancia existentes. El cursor parece una mano y se convierte en una pequeña cruz cuando se está en la parte superior un punto existente. Haga clic en (mantenga el clic apretado) y arrastre con el fin de mover los puntos.

MIDI
Los dos últimos botones citados anteriormente también se utilizan para crear y editar la información MIDI. Para aprender mas acerca de MIDI favor leer el capitulo Usar MIDI

Zoom horizontal y opciones de vista
Los principales atajos que probablemente uses todo el tiempo son [-] y [=] (disminuir el zoom y aumentarlo, respectivamente). La ampliación o disminución sucederá en relación con el punto de edición actualmente seleccionada (ratón, marcador o cursor de reproducción). En caso de duda sobre qué punto de edición elegir, selecciona Mouse.
El botón de Zoom a la Sesión [_] se acerca o aleja, según sea necesario, para que puedas ver el inicio y fin de los marcadores de tu proyecto.

Todas las opciones de zoom discutidos anteriormente controlan la cantidad de contenido horizontal que vas a ver en la pantalla. Una vez que tengas una sesión con varias pistas, también tendrás que controlar la cantidad de contenido vertical, que eres capaz ver en la pantalla. Hay varias formas de hacer esto:
Utiliza el "Número de pistas visibles" del menú desplegable para seleccionar el número de pistas que deseas ver para que quepan en la pantalla.
Utiliza el botón "Encoger pistas"  para que todas las pistas seleccionadas quepan.
Utiliza el botón "Expandir pistas" para que todas las pistas seleccionadas de vean más grandes.
También puedes cambiar el tamaño de una pista individual arrastrando su borde inferior, o haciendo clic derecho en la cabecera de la pista y la seleccionando de la "Altura" deseado.

Herramienta de navegación
Puedes usar la herramienta de navegación que se encuentra abajo de todo en la ventana de edición, para subir y bajar la sesión y ajustar el zoom vertical y horizontal, achicando o agrandando el tamaño de la ventana.

Crear sesiones en bucle (loop)
Puedes repetir secciones de audio fácilmente en tu sesión de Ardour. Aquí, tomamos el pasaje rítmico de audio que creamos en Trabajar con Regiones y lo duplicamos para hacer un bucle.
Antes de duplicar el pasaje o sección de audio, es una buena idea combinar las distintas regiones de la misma pista en una sola: es más fácil el traslado si lo hacemos de esta manera, y se impide que se mueva accidentalmente una sola parte fuera de lugar, por ejemplo. Hay dos maneras de hacer esto: Combinar Regiones (te permite descombinar) y Consolidar Rango ( no permite separar más adelante).
Si todavía están pensando en hacer alteraciones en el ritmo (añadir, eliminar o mover regiones individuales), puede ser mejor usar la opción Combinar regiones. Si te gusta la secuencia de la manera que es y no quieres o no te importa tener la capacidad para separarlos más tarde, utilice la opción Rango Consolidar.

Combinar Regiones
Sólo tiene que seleccionar todas las regiones que desea combinar:
A continuación, ve al menú Región → Editar → Combinar (o hay clic en las regiones seleccionadas y encontrar la misma opción a través del menú contextual, como se muestra a continuación):
Las regiones combinadas se verá como esta (nota que la palabra "combinado" se ha añadido al nombre):
Si tiene que separarlos de nuevo en el futuro, sólo tienes que seleccionar la región compuesto e ir al mismo menú y elegir la opción "Uncombine".

Consolidar el rango
Cuando hayas arreglado tus Regiones en un solo "ciclo de bucle" y quedado satisfecho con el sonido, estas a punto para crear un Rango con todas las regiones que harán el bucle. Primero, asegúrate de que se seleccione cada Pista utilizada en el bucle. Las pistas deseleccionadas son grises, y las seleccionadas azules. Si ninguna de las Pistas que utilizaste no está seleccionada, mantén pulsada la tecla de Mayúsculas mientras pinchas en ellas para añadirlas al grupo seleccionado. Finalmente, utiliza la herramienta de Rango para seleccionar el bucle entero. 
Una vez más, la configuración de la Rejilla te ayudará a poner precisamente el rango al punto de inicio y fin de tu barra métrica. Una vez que tengas seleccionado el bucle entero, haz clic-derecho en el rango y selecciona Consolidar rango. Si te gustaría que cualquier efecto de Automatización o Plugin que hayas añadido al bucle fuera incluido, selecciona Consolidar rango con procesamiento.

Cuando el rango o intervalo seleccionado se consolida, aparecerá nuevas regiones en cada Pista, cada cual conteniendo todas las repeticiones de las muestras que hayas configurado en pasos anteriores.
Recuerda, una vez que el rango se consolida, no hay manera de deshacer la operación. En cualquier caso, si encuentras que necesita para alterar el ritmo de cualquier manera, siempre se puede recuperar las muestras individuales originales de la lista de regiones y reconstruir el patrón con ellos.

Duplicar el Rango
Después de haber fusionado regiones individuales que forman el patrón (usando la función Combinar o consolidar), es el momento de duplicar el patrón para formar un bucle o loop.

La función Multi-Duplicar (visto en el trabajo con el capítulo Regiones) es una buena manera de lograr esto. Volver a modo Grab [ G], selecciona todas las regiones, y pulsa [Mayus. + D]. Elegir el número de veces que deseas duplicar el patrón, por ejemplo: 1# Después duplicar nuestra sesión se ve algo como esto:

Sólo para su revisión, otras opciones que se pueden usar para la duplicación son:
El comando Rellenar la pista desde el menú Región → Duplicar → Rellenar pista. Esto llenaría toda la pista con las copias de las regiones seleccionadas, todo el camino hasta el marcador de final.
El comando Duplicar en el mismo menú [Alt + D]. Esto le permite hacer una sola copia a la vez.
La única acción duplicado con [Ctrl + clic] en la región + arrastrar una copia.

Expandir/Encoger Regiones
Las regiones pueden ser expandidas o encogidas en longitud sin cambiar su Tono utilizando la herramienta Expandir/Encoger Regiones. Un ajuste pequeño a la longitud de una Región puede no causar Artefactos notorios de sonido. Aun así, cuanto más extremo el cambio en longitud, más obvio el efecto de procesado en el sonido.

Para utilizar Expandir/Encoger Regiones, sitúa tu cursor encima de la región, y entonces pincha-arrastra a izquierda o derecha. Mientras arrastres, verás una área destacada, que representa la nueva duración a la cual la Región será encogida o expandida cuando liberes el ratón en la posición actual.

Esto es útil cuando añadamos una Región a una Pista nueva y la longitud de esta nueva Región no coincide con el ritmo existente que hemos ya creado. Es demasiado largo para ser un compás y demasiado corto para ser de dos compases. Selecciona la región que deseas corregir, y arrastra la nueva longitud hasta el final de la segunda barra, de nuevo con la asistencia de la configuración de cuadrícula. 
Al soltar el botón del ratón, aparecerá el cuadro de diálogo Ampliación de tiempo de audio. Puedes experimentar con diferentes ajustes para la operación de ampliación de tiempo. Cada ajuste afectará al sonido de diferentes maneras. Es una buena idea experimentar con unos pocos ajustes diferentes de estiramiento para averiguar lo que le da el resultado mas adecuado para tu gusto. Cuando la operación de ampliación de tiempo se ha completado, la región será exactamente largas, y debe encajar con el ritmo que ya creaste.

# 4. Mezcla
Mezclar es el proceso de convertir Pistas múltiples a una Mezcla estéreo dónde todo los instrumentos puedan ser oídos claramente. Niveles, Panoramización, Ecualización (EQ), y Compresión son las principales herramientas utilizadas para conseguir una buena Mezcla. Además de estas herramientas básicas, también se puede utilizar una amplia gama de efectos para mejorar el sonido, como efectos de Espacio (Reverb o Delay), Efectos de Modulación (Flanger, Chorus, Phaser, etc). Estos efectos vienen en forma de Plugins, es decir pequeños programas adicionales que son desarrollado independientemente de Ardour y que vienen en diferentes formatos. Mas acerca de Plugins en el capitulo Utilizar Plugins.

## Presentar la Banda de Mezcla. 
La Banda de Mezcla es la columna vertical que contiene varios controles relacionados con el flujo de la señal. Cada Pista y Bus en Ardour tiene su propia Banda de Mezcla. La Banda de Mezcla es también una herramienta básica que utilizaremos en el proceso de mezcla de nuestras pistas. En este capítulo, conseguiremos una visión general de la Banda de Mezcla, con cada sección descrita. También proporcionaremos referencias a los capítulos que contienen la información específica a cada aspecto de la Banda de Mezcla. 

Las Bandas de Mezcla pueden ser accedidas tanto desde la Ventana del Editor como desde la Ventana del Mezclador [Alt + M] para alternar entre los dos. Las Bandas de mezcla en cualquier ventana (del Editor o del Mezclador) son espejo una de la otra: cualesquier acciones hechas en una Banda de Mezcla en la Ventana del Mezclador serán reflejadas en la correspondiente Banda de Mezcla en la Ventana del Editor, y viceversa. 

### La Banda de Mezcla desde arriba hasta abajo 
En la ventana del editor, se puede ver la banda de mezclador de la pista seleccionada en la parte izquierda de la ventana. Si no lo ve, pulsar [Ctrl + E] para mostrarla.

Modos regulares y estrechas
Con el botón arriba a la izquierda la banda de mezclador se puede cambiar entre el ancho regular y una anchura más estrecha para conservar espacio. La parte superior de la banda de mezclador, se muestra a continuación, cambia entre los modos regulares y estrechos utilizando el botón izquierdo. El botón derecho oculta la banda de mezclador del todo.

Nombre de la pista y el botón de enrutamiento
Continuando desde arriba hacia abajo, la siguiente sección de la banda de mezclador contiene tres regiones. La primera de estas regiones muestra el nombre de la pista (esa es la palabra Audio 1 en la imagen al lado). La siguiente región, es el 1 en la imagen al lado, es un botón que permite acceder al enrutamiento, es decir, seleccionar qué entrada de la tarjeta de audio asignamos a esa pista. En la sección de Enrutamiento tienes toda la información. También en los capítulos de grabación de audio se habla del enrutamiento de entrada. El último botón sirve para el cambio de fase de la pista que es una opción avanzada sólo para aspectos musicales.

Procesador
La gran región de negro en la parte inferior de esta sección es la caja del procesador. Aquí es donde se pueden añadir Plugins, por ejemplo. La caja del procesador siempre contendrá el Fader en azul. Esto indica dónde se encuentra el atenuador principal del canal. El Fader se muestra en la mitad inferior de la tira. Por favor, consulta el capitulo Utilizar Plugins para más detalles. 

La siguiente parte de la banda de mezclador incluye controles para la toma panorámica, Record, Mute y Solo, entre otros.

Paneo
Paneo tiene que ver con la colocación de los sonidos en cualquier lugar entre los altavoces izquierdo y derecho. Por favor, consulte el capítulo Utilizar el Panning para obtener más información.

Solo
Cuando una pista o el Bus está en Solo, todas las otras pistas o Buses que no son del mismo modo en solitario no puede oírse a través del master de Bus o de la audición. También podemos encontrar un botón Solo en miniatura del mezclador de pistas. Tenga en cuenta que el aislamiento de una autobús no silenciará las pistas y viceversa.
Cuando cualquier pista o el Bus está en Solo, el indicador Solo en el menú de controles auxiliares se pondrá roja. Al hacer clic en el indicador de Solo mientras parpadea, se desactivarán todos los Solo, en la Sesión.

Mudo
Cualquier pista o el Bus de Silencio no puede oírse a través del Bus master o de la audición. El mezclador de pistas también contiene un botón de silencio en miniatura, entre el botón de grabación del brazo y el botón Solo. Haga clic en el botón Mute le ofrece opciones avanzadas para el comportamiento del botón de silencio.

Preparar la grabación
El botón Rec de la pista la prepara para la grabación, como se ve en el capítulo de grabación de audio. Pero haciendo clic no inicia la grabación, sólo la selecciona para cuando hagamos clic en el Rec general, en esa pista se graben las fuentes de entrada.

Fader, fundidos y medidores de pico
El control más importante presente en una banda de mezclador es el Fader, que se utiliza para ajustar la ganancia total para el correspondiente pista o el Bus. El medidor de pico muestra el valor máximo de la pista seleccionada, y se encuentra justo a la derecha del Fader. Estos medidores de nivel consiste en un gráfico de barra en el caso de una pista mono, y dos gráficos de barras en caso de una pista estéreo. El pequeño campo rectangular por encima de los medidores muestra el mayor valor de pico que se ha jugado en esa pista hasta el momento.

Al hacer clic en el botón de la derecha en la parte inferior de la banda de mezclador (se lee "post" en la imagen al lado), puedes seleccionar el punto de medición, por ejemplo, el directo "In" de la tarjeta de sonido, el "pre" señal de Fader, o el "post" señal Fader. Es decir, seleccionas antes o después del Fader. 

Como se puede ver en la imagen de abajo, hay una versión más pequeña de la banda de mezclador en cada pista, llamado el mezclador de pistas, que contiene un atenuador horizontal, un Medidor vertical, así como botones de miniatura para Rec, Mute y Solo . Todos ellos son similares a los encontrados en la banda de mezclador para esa pista.

Enrutamiento
Por último, llegamos a la parte inferior de la banda de mezclador. Aquí encontramos el botón de enrutamiento de salida, marcado como "master" en la captura de pantalla anterior, que se discute en el capítulo Descripción del enrutamiento.

## Niveles de Mezcla
Los Niveles son los volúmenes que cada Pista tiene relativamente a las demás. Si no puedes oír una línea de graves por encima de los otros instrumentos, la elección obvia sería alzar el volumen de línea de graves. Los niveles pueden ajustarse en la Banda de Mezcla de cada Pista bajo su nombre de Pista. El primer paso en la Mezcla es escuchar a todo aquello que ha sido grabado y ajustar los niveles de todas las Pistas de modo que puedas oír todo claramente, pero en una manera que es apropiada para la canción. Por ejemplo, la pista vocal es normalmente más fuerte que la guitarra rítmica porque la voz es el punto focal de la canción.

##1 Utilizar el Atenuador (Fader)
El Atenuador es el control primario de niveles por cada pista. El valor exacto de los niveles de la Pista se muestran en el pequeño campo rectangular por encima del Atenuador. Puedes cambiar los niveles bien arrastrando el deslizador o bien escribiendo un nuevo número directamente en el rectángulo con la cantidad. Por defecto el Atenuador está puesto a −0.0 dB, que significa que los Niveles de la Pista no se cambian mientras se reproduce.

Una otra tarea importante en la Mezcla es evitar Saturación. El Valor de Pico en la Banda de Mezcla se vuelve rojo cuando la señal ha hecho pico por encima de 0.0dB. Puedes utilizar esta herramienta para controlar los Niveles más altos de tu Pista mientras Mezclas. Pincha encima para reiniciarlo.
Ya que Ardour utiliza internamente Números de coma flotantes, las señales no son necesariamente Saturación mientras que la información permanezca dentro de Ardour. Así que puede estar OK si una pista o Bus ocasionalmente se pone rojo. Pero tendrías que asegurarte de que cualquier cosa que envíes a tu tarjeta de sonido o que finalmente exportes como archivo de sonido (como para masterizar un CD) nunca vaya por encima de 0.0dB para evitar Saturación real.

Si se produce el recorte en un sonido muy percusivo y es casi imperceptible, que puede ser capaz de ocultarlo por la disminución de la ganancia (por ejemplo, Normalizar la región a 0,0, o un número menor como -1,0). Sin embargo, a menudo los resultados de recorte en la distorsión audible del sonido grabado. La mejor solución en este caso es simplemente grabar de nuevo con los niveles más bajos.

### Utilizar el Panning (Panorámica o Paneo)
Una vez te ha establecido un equilibrio bueno de niveles en todas las Pistas, puedes empezar para pensar sobre Panoramización. La panoramización ayuda a establecer un Campo estéreo, un espacio relativo entre los altavoces en el qué colocar tus pistas de instrumentos.

La interfaz de Panoramización
El Deslizador de Panoramización en Ardour está ubicado en la Banda de Mezcla y puede ser ajustado moviendo la línea vertical verde a izquierda o derecha. Una Pista Mono tendrá un deslizador de panoramización como lo de arriba, mientras que una Pista Estéreo tendrá uno como en la de abajo:

Panear una pista mono
El valor por defecto Mono distribuye 1 entrada para 2 salidas. Su comportamiento es controlado por un solo parámetro que es la posición donde coloquemos el paneo. Por defecto, se centra el panorámico de audio al medio. Puede cambiar la posición haciendo clic y arrastrando directamente en el panorámico de audio mono hacía izquiera o derecha. Haga clic en el panorámico de audio para acceder a otras opciones.

Panear una pista estéreo
El paneo estéreo por defecto distribuye 2 entradas 2 salidas. Su comportamiento es controlado por dos parámetros, anchura y posición. Por defecto, el panorámico de audio se centra en el ancho total, es decir, en la mitad. 
Haz clic y arrastra los botones izquierda o derecha para cambiar el ancho. Por ejemplo, si los lleva más juntos que se verá así:

Con una anchura más estrecha, también puedes arrastrar el asa superior para cambiar la posición central relativa.

Si hacemos que los botones Izquierda y Derecha se superpongan por completo (es decir, el ancho se reduce a cero), ambos botones se convierten en un solo indicador y la señal de marca cambiar a "M" (de mono):

Como regla general práctica, las guitarras tienden a ser panoramizadas a la izquierda y derecha. Las voces y el bajo tienden a ser colocados en el centro. Si quieres crear un equilibrio de modo que un lado no sea más fuerte que el otro. Los auriculares pueden ser útiles para determinar cómo tendrían que ser panoramizados los instrumentos y si un lado es demasiado sonoro y hace que la mezcla parezca torcida.

Dos otras herramientas que son útiles para crear un Campo estéreo o "espacial" son Reverberación (Reverb) y Retraso (Delay). Estos efectos puede ser utilizados junto con envíos para crear un envío de tambor que quedaría más lejano en la mezcla cuanta más Reverberación, y un envío de voz que podría tener un poco más Retraso pero sonar más cercano que los tambores. Por favor mira el capítulo Utilizar Plugins de efectos y Crear y utilizar Envíos para más información.

Nota: ¡Mantén siempre un ojo en tus Niveles mientras panoramizas pistas! Panoramizar una pista a un canal aumenta el Nivel de aquel canal. Esto puede cambiar el equilibrio de Niveles que configuraste en el capítulo anterior, y en los casos extremos pueden resultar en Saturación. Cuando esto suceda, reduce los Niveles globales de aquella pista y comprueba de nuevo cómo sienta el cambio a la Mezcla.

## Utilizar Plugins de efectos
Hay dos grandes categorías de Plugins: instrumentos virtuales y efectos. En este capitulo nos referimos a los efectos. Los Plugins pueden ser utilizados para transformar el sonido de pistas individuales, o a un grupo de Pistas vía un Envío. Más tarde hablaremos de algunos Plugins específicos al proceso de Mezcla, como Compresores, Limitadores, Ecualizadores, Reverberaciones y otros.

Nota: Por defecto Ardour solo trae una pequeña cantidad de Plugins. Pero hay muchísimos Plugins de varios formatos disponible en Internet. Hay varios sitios web donde hay Plugins gratis para diferentes formatos. Vease Plugins.

### Formatos de Plugin
LADSPA (Linux Audio Developers Simple Plugin API)
Los Plugin LADSPA son el formato "nativo" de Plugin para Ardour. Fueron inicialmente desarrollados para Linux, pero desde entonces han sido portados a mac OS también. Cada vez mas van a ser reemplazado por LV# 
Puedes encontrar mas información acerca de LADSPA en: https://www.wikiwand.com/es/LADSPA

LV2
Los LV2 son los extensibles sucesores de los LADSPA, los cuales pueden usarse para exhibir características sonoras de una manera gráfica. Los Plugins LV2 pueden ser utilizados en Linux y también en mac OS. Puedes encontrar mas información acerca de LV2 en: www.wikiwand.com/es/LV2

VST (Virtual Studio Technology)
Los VST son el formato de Plugin común para Windows, inicialmente desarrollado por la empresa alemana Steinberg. Los Plugins VST compilados para Linux pueden ser utilizados en Ardour (se muestran como LXVST).
Puedes encontrar mas información acerca de VST en: http://www.wikiwand.com/es/Virtual_Studio_Technology

A menudo se encuentra un plugin en la dos versiones, de 32bit y de 64bit. Descarga y instala el plugin correspondiente a tu versión de Ardour, es decir si tienes una versión de Ardour de 32bit descarga los plugins de 32bit. Los plugins de 64bit solo cargan en una versión de Ardour de 64bit (si no usas una bridge como Jbridge).

Plataforma
Windows
mac OS
Linux

Soporta Formatos de Plugins
(Extensión de archivo)
Windows VST en la versión #4 (.dll)
AudioUnit (.component) y mac VST en la versión #4 (.vst)
LinuxVST en la versión #4, LADSPA y LV2 (.so)
Directorio donde se guarda 
A menudo una sub-carpeta con el nombre VST2 o VST3 dentro de la carpeta Archivos de Programma 
Macintosh HD/Library/Audio/Plug-Ins/
usr/lib/lxvst o usr/lib64/lxvst (para LinuxVST) /usr/lib/lv2 (para LV2)
o /usr/lib/ladspa (para LADSPA)
Si un directorio no existe hay que crearlo, por ejemplo con sudo mkdir /usr/lib/lxvst

Después de la instalación de nuevos Plugins es necesario de reiniciar Ardour y actualizar la lista de los Plugins. Para que Ardour encuentre Plugins VST hay abrir el menú Editar → Preferencias y buscar en la lista  VST y hacer clic en VST Path para introducir directorio donde Ardour debe buscar para plugins VST. 
													
Si usas Ubuntu Linux puedes instalar el meta-paquete ubuntustudio-audio-plugins con el gestor de software o en un terminal: 
sudo apt-get install ubuntustudio-audio-plugins 
Este comando te instalará una multitud de Plugins de diferentes categorías, entre ellos la seria de Calf y los de Invada que dan muy buenos resultados y vienen con una interfaz atractiva. 

Más información acerca de utilizar Plugins LADSPA, LV2 y VST con Ardour, se puede encontrar aquí: http://manual.ardour.org/working-with-plugins/

### Procesar efectos
En la terminología de Ardour, un procesador es cualquier cosa que conectado a una banda de mezclador trata la señal de alguna manera. La disposición de los procesadores es arbitraria, es decir, la eliges vos, y no hay límite para el número no puede haber. El espacio principal de color negro que se muestra en la imagen de arriba es la caja del procesador. El cuadro azul Fader es en realidad un Plugin que viene por defecto dentro de la caja. Representa el atenuador que se utiliza para controlar el volumen de la pista. 
Todos los procesadores se muestran como rectángulos de color, con una LED pequeña de color al lado de ellos que se ilumina cuando se activa el Plugin. 
Los procesadores se añaden por defecto después del Fader, es decir pos-Fader. 
Nota: Puedes cambiar esto arrastrando el procesador soltándolo arriba del procesador “Fader”.

### La adición de un Plugin de efecto para una pista
Los Plugins se pueden añadir haciendo con un doble-clic en la caja del procesador de la pista o el Bus. Se presenta el administrador de Plugins: En esta lista, se pueden buscar por tipo (formato),categoría o creador. En este ejemplo, vamos a añadir el Plugin de reverberación llamado Gverb:

Una vez seleccionado, haz clic en Añadir (o doble clic) y el Plugin se mostrará en la lista de Plugins que va a conectarán. A continuación, haga clic en Insertar Plugin(s) y se mostrarán en la caja del procesador.

### Editar los parámetros de un Plugin
Haz doble clic en un Plugin para editar sus parámetros. En este ejemplo, hacemos doble clic en el cuadro "Gverb" y se abre la siguiente ventana:

En este caso se pueden controlar los parámetros de reverberación tales como el tamaño de la sala (Roomsize), amortiguación (Damping), la cantidad de señal seca (Dry) y húmeda (Wet), etc. 

Puedes usar Añadir para guardar esta nueva configuración como un preset propio. Coloca un nombre y así lo podrás usar en futuras ocasiones de la misma forma sin tener que configurar de nuevo. 

Puentear
Para omitir el Plugin, pulsa el botón Puentear en la ventana de parámetros del Plugin, o simplemente haz clic en el LED del Plugin en la caja del procesador y se "apaga". Esto deja el Plugin fuera y permite que la señal pase por ella sin ser afectada. Esto es útil cuando se desea comparar cómo suena una pista con y sin el Plugin.
Los Plugins anulados se muestran en gris y con el LED desactivado.

Clic derecho sobre el Plugin muestra un menú con varias opciones, incluyendo Suprimir o Borrar el Plugin. 

Pre- versus Pos-Fader
Tienes una elección entre si te gustaría añadir tu Plugin antes o tras del Fader. Por defecto se insertarán pos-Fader, es decir se insertan tras el Fader: En este caso el Fader controla el nivel de señal que entra en el Plugin, mientras si lo pones en pre-Fader se insertan en el camino de la señal antes del Fader, de modo que el Fader controla el nivel de la señal que sale del Plugin. Para ciertos Plugins, la colocación pre- o pos-Fader no importa. Para otros, la diferencia es sutil. Para otros de todos modos, insertarlos en el lugar correcto es absolutamente esencial.

### Crear y Utilizar un Envío
Un envío es sólo una salida adicional para una pista o un autobús con su propio Fader propio, que se puede utilizar para dirigir la señal a otros puntos de Ardour. También conocido como envíos auxiliares o AUX, que aprovechan la señal en un punto específico en el flujo de señal (pre-Fader, post-Fader, antes o después de ecualizadores y otros Plugins, etc.) y envía una copia de esa señal a otro lugar, sin afectar la señal normal fluya hacia el atenuador de canal. En Ardour, se pueden agregar fácilmente envíos a pistas y buses a través de la banda de mezclador. 

¿Cuando es útil un envío?
Si tienes en tu proyecto una batería con cuatro pistas: bombo, caja, platillos y redoblantes y digamos ahora que deseas añadir una reverberación a la batería, se podría, por supuesto, añadir un Plugin independiente para cada pista individual, y ajustar las configuraciones por separado. Pero este método aumenta innecesariamente la cantidad de trabajo: Cada vez que desee cambiar un ajuste de reverberación a través del tablero para todos los tambores, se tendría que abrir los cuatro Plugins de reverberación y cambiarlos de la misma manera. Aquí es donde el envío puede venir muy bien: se puede utilizar para añadir un efecto particular a un conjunto de pistas sin crear varias instancias de la misma Plugin.

Aquí está el resumen de cómo crear un efecto envío:
1) Crear un nuevo bus: seleccionar Pista → Añadir Pista o Bus → Buses de audio
2) Ir a la Banda de mezcla de este nuevo Bus y añadir un Plugin en esta Banda.
3) Enrutar un envío para cada pista de batería a la que deseas aplicar el efecto.

Antes de encaminar un envío a este Bus, primero asegúrate de que las salidas de buses se dirigen al bus master, como se muestra a continuación (botón en la parte inferior dice master).
También, abra la ventana del Plugin (doble clic sobre el rectángulo Gverb) y ajuste la señal de la mezcla a 1,0 Nivel Wet y en Dry 0.0 Nivel. Esto asegura que el Bus lleva toda la señal procesada (la señal 'Wet - húmeda') del Plugin, y ninguna de la señal sin procesar (la señal 'Dry-Seca') al Bus master. Recuerda, las señales 'limpias', sin procesar, están todavía disponibles desde sus pistas originales, así que no hay ninguna necesidad de duplicarlas en este bus.

Crear Envíos en las otras Pistas y enrutarlos a las entradas del Bus.
Para crear Envíos en las diferentes pistas haz clic-derecho en el área pos-Fader bajo el Atenuador en una de las Pistas de Audio y selecciona Nuevo Envío y selecciona Bus # Hazlo en la banda de cada pista a cual quieres aplicar el efecto (en nuestro ejemplo al bombo, la caja, los platillos y a los redoblantes). 
Deberías ver ahora esto en el procesador de la pista:
El pequeño Send es un control deslizante que aparece justo debajo del rectángulo verde y controla la cantidad de sonido que se envía desde esta pista al Bus. Para controlar el nivel de cada envío, simplemente haz clic y arrastra el Fader para aumentar o disminuir su volumen.

El Bus que creamos recibe la suma de todas las pistas que seleccionamos y aplica el efecto. Un solo Plugin aplicado al Bus controla el efecto de la mezcla de los sonidos de toda la batería enviados ahí. De esta manera, tienes un control independiente sobre el sonido "seco (Dry)" de la reverberación de las pistas originales, y el sonido "húmedo/ )(Wet)" del efecto de salida en el Bus.
El Envío se comporta como cualquier otro Plugin en la caja del procesador. Puedes desactivar temporalmente haciendo clic en el LED pequeño y puedes hacer clic en el rectángulo para acceder a otras opciones, incluyendo "Borrar".

Nota: Es importante de considerar si quieres crear un Envío pre-Fader o pos-Fader. Generalmente esto depende de el tipo de Plugin de efecto utilizado y el resultado deseado. En envíos pre-Fader, el nivel de Envío es controlado solo por el deslizante de control, independientemente del Fader de la pista. En Envíos pos-Fader, el nivel de Envío es controlado tanto por el Fader de Pista como por el atenuador de Envío. Esto significa que el nivel de Envío pos-Fader es siempre proporcional al nivel de Pista/Bus, el cual controla la señal 'Seca'.

## Efectos de Dinámica
Uno de los problemas que puedas encontrar en una Mezcla es que las partes sonoras son demasiado fuertes, pero las partes silenciosas lo son demasiado. Este tipo de problema no puede ser fácilmente resuelto utilizando solamente Atenuadores para ajustar los Niveles. Puede que pongas los Niveles tan alto que saturen, o que añadas ruido de fondo indeseado por sencillamente incrementar los Niveles. Estos son todo problemas de lo que se llama Rango Dinámico, esto es, la diferencia entre las partes más fuertes y más tranquilas de tu Sesión. Hay varios tipos de herramientas para ajustar el Rango Dinámico disponible en Ardour incluyendo Limitativo (Limiting), Compresión (Compression) y Apertura (Gating).

### Limitación
Un Limitador es una herramienta que impide que el volumen de una Pista supere un cierto Nivel, normalmente el Nivel de Pico (0dB) o algo cercano. Muchos Limitadores tienen la opción para aumentar los Niveles de la señal entrante antes de que están Limitados, y de este modo puedes "cerrar el vacío" entre las partes más sonoras y las más silenciosas de tu mezcla. Un Limitador puede utilizarse en el Bus master para impedir la Mezcla global sature. Los Limitadores se utilizan casi siempre pos-Fader.

El "Limitador de oteo rápido (Fast Lookahead Limiter)" puede ser encontrado entre los Plugins LADSPA. Para poner cuánto limita el limitador de oteo rápido, sencillamente ajusta el deslizador de "Límit (dB)". El Limitador de oteo rápido literalmente "mira adelante" en la señal por unos cuantos mili-segundos, y cuando ve que la señal está a punto de superar el límite que has puesto, automáticamente decrementa los Niveles.

El deslizador de Input Gain (dB) determina cuánto se incrementan los Niveles antes de que alcancen el Limitador, y el medidor de Limit (dB) en el lado derecho muestra a que Nivel máximo se reduce. Mientras la reducción en volumen es casi-instantánea, el deslizador del Release time determina cuánto tiempo le toma al Limitador regresar a 0 dB.
Nota que cuanto "más duro" uno maneje el Limitador (incrementando la Ganancia de entrada y/o decrementando el Límite de Pico máximo permitido), más reducción se fuerza a hacer al Limitador, y más probablemente es que ocurran artefactos del procesamiento (como Distorsiones o cambios erráticos en volumen). En el Bus master, es generalmente mejor evitar Limitación excesiva.
Al lado se muestra una captura de pantalla de un Limiter similar del paquete de Plugins Calf:

### Compresión
Un Compresor impulsa el volumen global de un sonido, pero entonces "lo" aprieta dependiendo de cuán sonoro sea. Esto puede hacer que las voces suenen más incluso o que los tambores suenen más llenos y más fuertes. El efecto final es similar a cómo un Limitador puede reducir el rango entre el más silencioso y el más fuerte de los sonidos, aun así el efecto es más selectivo cuando se utiliza un Compresor.

El Compresor en su forma más sencillo tiene los siguientes controles: El "Umbral (Threshold)" establece el Nivel en qué el Compresor empezará a actuar, y la "Proporción de Compresión" controla cuánto "aprieta" el sonido el Compresor. Los parámetros "Ataque" y "Decaimiento" controlan cuán deprisa el Compresor afecta al sonido.

Un Compresor más complejo, el Plugin LADSPA SC1 Compresor, puede encontrarse entre los Plugins de Ardour.
El SC1 Compresor tiene tres botones principales: Nivel de Umbral (Thresold level) (dB), Proporción (Ratio) (1:n) y Ganancia (Makeup gain) (dB).
El Thresold level pone el Nivel al cual el Compresor comprimirá o apretará el sonido. El Ratio controla cuánto apretará cuando se alcance el Umbral. El Makeup gain aumenta la señal entera después de ocurrir la Compresión. 

Los otros tres controles Tiempo de Ataque (Attack time)(ms), Tiempo de Liberación (Release time)(ms) y Radio (Knee radius) (dB), te permiten controlar la forma de la Compresión. Para una Compresión vocal suave, querrías un Tiempo de Ataque semi-rápido de modo que el Compresor coja el principio de cada palabra, un Tiempo de Liberación más lento para dejar que suene la voz, y un suave Radio (Knee) para crear una forma moderada de compresión que no es demasiado notoria. Si quieres hacer que los tambores suenen grandes, podrías probar un Tiempo de Ataque lento de modo que no Comprimas el pop del tambor, un Tiempo de Liberación rápido de modo que el Compresor pueda coger el próximo golpe del tambor, y una Proporción grande para hacer las Dinámicas entre el principio y el fin del golpe de tambor similares.

Al lado se muestra una captura de pantalla de un compresor similar del paquete de Plugins Calf.


### Puerta Umbral (Pasa Ruido)
La clase más sencilla de Puerta deja pasar una señal a través cuando es superior a un cierto Nivel, y bloquea la señal cuando es menor que aquel. Las puertas son a menudo utilizadas como un tipo de reducción de ruido. Por ejemplo, la Puerta en un canal de micrófono podría abrirse solamente mientras la cantante está cantando, impidiendo que otros ruidos de fondo vengan a través también cuando no esté cantando. Las puertas de los tambores son también un viejo truco de estudio de producción para hacer su sonido "más afilado".

Aquí, el Plugin LADSPA "Gate" muestra un parámetro de control único, el "Threshold" en qué la Puerta abrirá y dejará pasar la señal. 

La mayoría  de Puertas de ruido, como el Calf Gate Plugin, tienen un control independiente sobre cuan deprisa la Puerta abre (el "Ataque") y cierra (el "Decaimiento"), así como otros parámetros bastante similares a aquellos descritos para el Compresor arriba.

## Ecualización
A menudo, incluso después de ajustar Niveles y Panoramización, puede ser difícil de discernir pistas diferentes con contenido de frecuencia similar (por ejemplo, una guitarra de graves y un bombo) en la Mezcla. Una herramienta buena para resolver este asunto es un Ecualizador (o EQ). Esencialmente, un ecualizador te permite controlar por separado la ganancia de diferentes rangos de frecuencia de un sonido. Esto puede ser útil no solo para esculpir el timbre de un sonido aislado (por ejemplo, para hacer un sonido 'mas acusado' o 'más suave'), sino también para hacer que sonidos de varios timbres se integren mejor en la mezcla. 

### Ecualizador de 3-Bandas.
La clase más sencilla de Ecualizador es el que nos es familiar de mezcladoras analógicas. Tiene tres parámetros, los cuales ajustan los Niveles de tres Bandas, o rangos de frecuencia: uno para el Graves (frecuencias bajas), uno para las frecuencias de gama medias y uno para el Agudo (frecuencias altas). El Plugin LADSPA "DJ EQ" es justo el dicho EQ: Tiene tres controles para subir/bajar los Graves (Lo gain), los Medios (Mid gain) y los Agudos (Hi gain)

### Ecualizador Multi-Banda (o Gráfico)
Un ecualizador Multi-Banda (o Gráfico) más complejo a menudo tiene entre ocho y treinta y dos Bandas. Cada Banda está centrada en una frecuencia, y el Nivel de cada Banda puede ajustarse independientemente. En algún EQ Multi-Banda, como el Plugin LADSPA TAP Equalizer mostrado al lado, la frecuencia central de cada Banda puede ser definida por el usuario. Esto te permite bien atenuar (o sacar) una frecuencia indeseada, o bien reforzar (incrementar) una deseada.

La curva "global" de las Bandas también puede utilizarse para determinar el tono general de tu Pista o Mezcla. En el ejemplo encima, la parte más baja de las frecuencias de rango-medio ha sido "disminuida" un poco (nota cómo las Bandas 1 y 8 quedan intactas en 0 dB, mientras que las Bandas intermedias de 2 a 7 dibujan una curva de atenuación, con las Banda 4 en -13 dB como el punto más bajo). 

### Ecualizador paramétrico
El Ecualizador Paramétrico es el tipo más versátil de EQ utilizado para Mezclar debido a su extenso control sobre todos los tipos de EQ parámetricos. En Ardour hay un ecualizador paramétrico llamado el “Triple Band Parametric with Shelves”. También hay una similar desde el paquete de Calf Plugins, como se ve en la pantalla al lado: El Calf Equalizer 5 Band. Explicamos su interfaz: 

Parametrics
Hay tres botones para cada banda de frecuencia. Cada una de las tres bandas tiene un control Freq (Hz) que sirve para seleccionar la frecuencia central, un Level (dB) para cortar o aumentar las frecuencias y un ajuste Q que determina el ancho de la gama de frecuencias a ser afectada.

Highshelf, Lowshelf
A la izquierda y a la derecha hay dos filtros para cortar por encima o por debajo de una frecuencia determinada. Por ejemplo, un filtro bajo (Lowshelf) se puede utilizar para eliminar Ruidos sonidos no deseados, y un alto se puede utilizar para reducir silbidos. El control de Frequency determina la frecuencia de corte. Por ejemplo, un Lowshelf con frecuencia de corte 200 Hz significa que el ecualizador atenuará todo por debajo de esa frecuencia. La cantidad de atenuación es controlada por el mando de nivel (level). Lo contrario aplica al Highshelf. A partir de la frecuencia seleccionada atenuará todo por arriba de esa frecuencia.

#### Un ejemplo de uso de un Ecualizador
Para conseguir una mejor separación de dos instrumentos en la mezcla a través del uso de EQ, primero necesitas descubrir donde se solapan los dos instrumentos. Asumimos que tienes una pista de bajo eléctrico y una pista de guitarras con distorsión. 
1) Ponlas en SOLO para escuchar las dos. 
2) Inserta el Plugin Calf Equalizer 5 Band en tu banda del bajo.
3) Activa el primer filtro de los Parametrics.
4) Activa el Analyzer para que muestra el espectro de frecuencias del señal
5) Selecciona el punto del filtro en la pantalla y sube la "ganancia" a 10dB,
6) Incrementa el "Q" de modo que sea un rango más estrecho hasta 1,
7) Desplaza arriba y abajo la "frecuencia". Oirás el tono subir y bajar. 
8) Entonces desplázalo abajo despacio hasta que oigas el rango de frecuencia donde los dos instrumentos se superponen o una frecuencia de la son
9) Ahora sencillamente reduce la "ganancia" a unos dB, y esperemos que oigas los instrumentos un poco más claros.
Luego, aplica el mismo proceso al otro instrumento.

Hay muchos enfoques a la ecualización. Esperemos que esto proporcionará un ejemplo de cómo comenzar ecualizando pistas en tu mezcla. Pero muy en particular, en cuanto a lo que se refiere a EQ, es mejor utilizar de menos que de más, a no ser que conscientemente estás utilizando ecualización extrema como parámetro composicional.


## Automatización
Si quieres que cambien los parámetros de tus Atenuadores, Panoramización o Plugins en el tiempo, entonces querrás explorar este capítulo Utilizar la Automatización. Si no, salta adelante para aprender cómo Exportar Sesiones en la siguiente sección.

La automatización es la manera de representar y especificar cambios en los parámetros de procesado de audio en el tiempo. Hasta ahora, se han usado valores fijos para diversos parámetros de nuestras canciones (por ejemplo, un conjunto de la pista Fader y -3,0 dB, o un panorámico de audio mono se ajusta al 100%, izquierda; etc.) Estos valores fijos se aplicarían para toda la pista a lo largo de toda la sesión.
Pero, por ejemplo, es posible que desees tener la ganancia de una pista para disminuir gradualmente durante veinte segundos y que encima se escucha una voz. O es posible que desees hacer un movimiento sonido de izquierda a derecha sobre dos segundos. Para esto se usa la automatización.

Se pueden automatizar el Atenuador (Volumen), la Panoramización y cualesquiera de los parámetros de los Plugins utilizados en esa Pista. Un parámetro automatizado se muestra debajo de la pista padre en su propia Pista de Automatización. Los datos de automatización son representado visualmente como una Línea de Automatización, hecha de una cantidad de Puntos de Automatización. Aquí tienes cómo se ve una pista con automatización del Fader:

En la imagen al lado, la Pista de Automatización llamada Fader (Volumen) está asociada a la Pista llamada Gtr1Amp# La ganancia de controles de línea de automatización cambian con el tiempo. 

### Crear una Línea de Automatización
Para añadir Automatización a una Pista, pincha el botón A o haz clic-derecho en el área de la Pista. Aparecerá un menú, donde puedes seleccionar el parámetro que te gustaría Automatizar o puedes mostrar toda la Automatización. Para nuestro ejemplo tomamos el parámetro Pan (paneo):
Aparecerá entonces una Pista de Automatización. Con la herramienta Dibujar activa, se pueden crear Puntos de Automatización haciendo clic en cualquier parte de la pista de automatización. Una línea de automatización se une a los puntos de automatización que añada. El número en la imagen al lado indica el estado del panorama actual en la pista de automatización seleccionada.
Para que se aplica la pista de automatización debes cambiar la pista del modo Manual al modo Reproducir. Este botón está ubicado en el área de cada parámetro de automatización.
A la hora de reproducir la pista vas a ver como se mueve el pan según la pista de automatización. A la hora de la subido el botón del paneo se mueve hacia la izquierda y cuando baja va hacia la derecha.

### Modos de Automatización
El modo Reproducir aplicará los datos de Automatización existentes durante la reproducción. En este modo no se grabarán datos de Automatización. 

El modo Manual le dice a Ardour que ignore los datos de Automatización durante la reproducción. 

El modo Escribir graba continuamente los cambios de usuario al parámetro Automatizado según se reproduzca el Transporte, creando una Línea de Automatización. Por ejemplo, puedes empezar la reproducción y entonces hacer cambios de tiempo real en la ganancia utilizando el Atenuador en la banda de mezcla de tu Pista. Todos los cambios que hagas serán escritos (grabados) como una Línea de Automatización, la cual entonces puedes reproducir más tarde cambiando el Modo de Automatización otra vez a Reproducir. El proceso de "grabación en directo" de Líneas de Automatización es igual para Plugins. Abre un Plugin existente haciendo doble-clic sobre él vía la banda de mezcla. Mientras la interfaz de Plugin esta abierta, inicia la reproducción. Cualesquier cambios que hagas moviendo los controles del parámetro Automatizado en la interfaz de Plugin serán escritos como una Línea de Automatización. 

¡Aviso: Dejar la Automatización en modo Escribir durante la reproducción puede sobre-escribir cualquier Automatización anterior que hayas creado! 

El modo Tocar es similar al de Escribir. aun así a diferencia del modo Escribir, el modo de Tacto no grabará sobre datos de Automatización existentes a no ser que el parámetro esté siendo cambiado.

### Crear Automatización de un Plugin
Puede agregar automatización a cualquier Plugin que ya ha sido añadido a una pista. En el siguiente ejemplo, tenemos un AM pitchshifter Plugin añadió a una pista.

Para seleccionar un parámetro de este Plugin y automatizarlo haz clic en el botón A de la pista marcada y aparecerá un menú. En la sección Automatización procesador encontrará una lista de los Plugins que se han añadido para esa pista. Dentro de cada efecto es posible elegir el parámetro que deseas automatizar. En el ejemplo, hemos elegido el parámetro Pitch shift del AM pitchshifter. Aparece una pista de automatización para ese parámetro. Ten en cuenta que al abrir varias pistas de automatización, aparecerán uno tras otro por debajo de la pista principal.

Dibujar una curva de automatización para ese parámetro. No te olvides de establecer el estado de automatización en Reproducir.

En la imagen de arriba, el pitch shift está cambiando controlado por la curva creada.

Importante: Puede ocultar una pista de automatización haciendo clic en la "X" en la esquina superior izquierda de la pista de automatización. Tenga en cuenta que una automatización de pista oculta sigue funcionando incluso cuando no es visible.

### Trabajar con Puntos de Automatización 
Se puede conseguir mayor precisión vertical mediante el aumento de la altura de la pista de automatización. Mover el cursor cerca del borde inferior de la pista de automatización. El puntero se convierte en una doble flecha vertical. Arrastra hacia abajo para aumentar la altura de la pista de automatización. Ten en cuenta que la altura de la pista "padre" principal y la alturas de automatización de pista son independientes, por lo que mientras se trabaja en sus curvas de automatización es posible configurarlos así:

Nota: Recuerda que puedes ampliar la resolución del eje horizontal con el Zoom In y Zoom Out.

Hay varias maneras de maneras de ajustar puntos de automatización, dependiendo del modo de edición se encuentra en:
Un punto de automatización se puede arrastrar en cualquier dirección con el ratón (funciona en modos de ratón seleccionar, dibujar y modo de edición).
[Ctrl + clic + arrastrar] mueve el punto actual en cualquier dirección, y también todos los puntos subsiguientes sólo horizontalmente (funciona en seleccionar, dibujar y modos de edición).
Modo de edición única: cualquier segmento de la línea de automatización entre puntos de automatización puede ser arrastrado verticalmente, que afecta a los dos puntos finales a la vez, sin afectar a su posición horizontal. Simplemente haga clic en algún lugar de la línea entre dos puntos, y arrastre hacia arriba y hacia abajo.
Para eliminar un punto de automatización, mantenga presionada la tecla Mayus., mientras que haciendo clic derecho sobre ella (trabaja en seleccionar, dibujar y modo de edición).
Cómo eliminar varios puntos de automatización a la vez (modo seleccionar y el modo de edición solamente): seleccionar varios puntos de automatización arrastrando un cuadro a partir de la pista de fondo en torno a los puntos, sería como dibujar un cuadrado seleccionando con el ratón. A continuación, los puntos seleccionados se pueden eliminar presionando [Supr]".

Después de terminar una curva de automatización, su valor se mantendrá en ese nivel para todas las regiones posteriores, aunque no aparezca dibujada. Ese mismo nivel se mantiene durante el resto de la pista, a pesar de que la línea no se dibuja hasta el final.

### Automatización en movimiento
Si desplazamos una región a una nueva ubicación se moverán automáticamente los datos de automatización que podrían ser alineados con él, como podemos ver en las siguientes capturas de pantalla. Es decir, se mueve la pista con la línea de automatización completa y los puntos que hicimos en ella. 
Puede cambiar este comportamiento si lo deseas. Si quieres curvas de automatización que no estén ancladas y permanezcan donde están aunque se desplace la región, vas a Edición → Preferencias → Editor y desactivas la casilla Mover la automatización relevante al desplazar las regiones de audio.

Región específica automatización de ganancia
Hay una manera de crear una automatización de ganancia directamente unido a una región. Cuando se selecciona el modo de dibujar, debería ver una línea plana en la mitad superior de cada rectángulo Región:

Haz clic directamente en esa línea para crear puntos de automatización. Estos se pueden dibujar directamente en la propia región, en vez de en las pistas de automatización. 

Al igual que con las pistas de automatización, un punto de automatización de ganancia se puede arrastrar en cualquier dirección con el ratón o eliminar, presionanda la tecla Mayus., mientras que haces clic derecho sobre el.

Desactivación y eliminación de automatización de ganancia
La automatización de ganancia - se denomina también como envolvente - puede reiniciarse o desactivado en el menú contextual Región, al que se accede pulsando el botón derecho en la Región (solo funciona en modo Seleccionar y Audición) y después en Ganancia.
Restablecer Envolvente elimina los punto de automatización que has dibujado en la Región. Envolvente activa activa o desactiva la automatización de ganancia. 

###¿Cuándo debo utilizar automatización en la región o una pista de automatización?
Como se ha visto anteriormente, ambos son muy similares. Con la práctica te darás cuenta de las situaciones en las que una es más conveniente que la otra. He aquí dos ejemplos:

Si todo lo que necesita hacer es un poco de retoque (corte o realce de ganancia) en una parte específica de una región, y estás satisfecho con el nivel para el resto de la pista completa, utiliza la automatización específica de cada región.
Si tienes una pista más compleja con fundidos sobre las regiones, y / o la necesidad de dar forma a una curva dinámica de la mayoría de las regiones de esa pista, el uso de atenuadores de automatización es lo recomendado: 

Si hay un simple desvanecimiento gradual a partir de la primera región de la pista, y terminando en la última región, es muy sencillo de hacer esto con atenuador de automatización, pero sería mucho más difícil de hacerlo mediante la automatización específica de la región.


# 5. Exportar y Guardar
Guardar una sesión te permite guardar tu proyecto para que puedes trabajar en el con Ardour mas adelante mientras que exportar es el proceso de guardar una región, pista o sesión a un fichero de tu ordenador al cual puedas escuchar, compartir, quemarlo como un CDR o convertirlo a un MP3/OGG. Exportar una región NO exporta todos los cambios que querrías haber hecho a la región. Para exportar ediciones con Atenuación, Efectos, Paneo, y Automatización, debes exportar bien un rango o la sesión entera.

## Guardar Sesiones
Hay varias maneras de guardar Sesiones en Ardour, de modo que cada sesión se puede utilizar más adelante. La forma más sencilla es salvar toda la sesión al igual que salvas cualquier tipo de documentos: En el menú Sesión - Guardar [Ctrl + S]. De todas formas, siempre que inicias una sesión se crean todas las carpetas necesarias. Recomendamos SIEMPRE GUARDAR CON FRECUENCIA mientras estás trabajando. Es recomendable adquirir el hábito de hacer [Ctrl + S] cada poco minutos. 

Importante: Evitar el uso de caracteres que no sean letras y números al nombrar a su sesión. Evitar los espacios en blanco, letras acentuadas,! @ # $% * (+), Puntos, comas, Ñ, etc. Use guiones o guiones bajos si lo desea. Por ejemplo, en lugar de "Mi gran sesión!", es mejor "Mi_Gran_Sesion", o "MiGranSesion", o "mi-gran-sesión". 

### Ardour y formato del archivo de carpetas
El contenido de una carpeta típica de la sesión en el disco duro podría ser algo como esto:
Si el nombre de esta sesión es mi_sesion:
El archivo de sesión principal se llama mi_sesion.ardour. El archivo de sesión está respaldado periódicamente por Ardour con una extensión mi_sesion.bak.
El archivo .history mantiene un registro de los cambios que has realizado durante tu período de sesiones, y también está respaldado periódicamente.

La carpeta de exportación es donde los archivos exportados se guardan de forma predeterminada.
La carpeta interchange contiene los datos reales de audio de todas las regiones utilizadas en tu sesión. Se llaman por ejemplo:  Audio #wav,  Audio 1-1%R.wav . 
Si ya has renombrado cada pista antes de grabar audio en ella tienen los nombres de las pistas correspondientes: cymbal-#wav, highhat-#wav, kick-0-bounce.wav, etc, lo que te ayuda a la hora de Buscar el archivo que necesitas por si acaso quieres importarlo en otro programa. 
Y finalmente, la carpeta peaks contiene los datos que Ardour utiliza para exhibir gráficamente los Picos de tus ficheros de sonido.

Importante: Si haces doble clic en el archivo de sesión no se inicia Ardour, utiliza el método estándar de la primera apertura de la propia aplicación, a continuación, elegir una sesión desde el cuadro de diálogo de configuración de sesión.
### Moviendo una sesión a otra computadora o disco
Si tiene que mover tu sesión de Ardour a otro equipo, o si desea hacer una copia de seguridad en un disco duro externo, debe copiar TODA LA CARPETA  que contiene todos los archivos mencionados anteriormente. No basta simplemente copiar el archivo  *.ardour.

Importante: Al copiar una carpeta a otro equipo o unidad, no cambies manualmente el nombre o el nombre de cualquiera de los archivos internos.

### Guardar y Retomar capturas (Snapshots)
Guardar una captura de sesión en Ardour es similar a guardar tu sesión a un fichero nuevo. Se utilice este comando para evitar sobrescribir el fichero de sesión original. Una captura contiene el estado actual de tu trabajo, a la par que comparte todo el audio y ficheros de datos de la sesión.

Puedes guardar una captura vía menú: Sesión → Captura de sesión [Ctrl + Mayus.+S]. Por defecto el programa nombrará la nueva captura según la fecha actual y fecha de tu sistema. Si deseas, puedes cambiar el nombre a uno con más sentido que corresponda a la Sesión con la estás trabajando.

Puedes retomar una captura guardada vía la pestaña Capturas de sesión en el área en la derecha:
Ahí ves la captura nueva “Lacuna-3001” que justo creamos, y la entrada “Lacuna” representa el estado original de nuestra sesión.

Nota: A veces es útil de tener un punto de partida por defecto para tus Sesiones más que una captura de los cambios que hayas hecho. Para aprender cómo para hacer esto, por favor continua a la siguiente sesión llamada Guardar Plantillas.

### Guardar plantillas
Si a menudo te toca configurar la misma información en cada nueva sesión que crees, como el número de entrada y Canales de producción, el número y nombres de Pistas o Buses, o el Enrutamiento, entonces puedes desear crear una Plantilla de aquella información en su lugar.
Con una Plantilla, puedes recrear tu Sesión de trabajo actual sin todos los ficheros de información de Región. Las plantillas son útiles si, por ejemplo, estás haciendo un extenso enrutamiento en Pistas y Buses y quieres guardar lo  para uso en otras Sesiones. Un ejemplo podría ser una Plantilla para grabar Pistas de batería, bajo, guitarra y voces, cada cual con su entrada propia en la tarjeta de sonido, lo cual lo podrías utilizar como base para cada Sesión que crearas en esa situación. 

Puedes guardar una nueva plantilla desde el menú principal: Sesión → Guardar Plantilla... 
Cuando se crea una nueva Sesión, puedes también cargar una plantilla previamente guardada con la opción Usar esta plantilla:

Tus plantillas se van a guardar en la carpeta /opt/ y en esta en Ardour-5.5.0/share/templates o dependiendo de la versión de Ardour.
En mac OS se encuentra en la carpeta usr/tunombre/.Ardour. 

## Exportar una sesión
Recordamos que exportar es el proceso de guardar una sesión a un solo fichero estéreo de tu ordenador que puedes compartir y reproducir con un reproductor de audio.

Antes de todo tienes que echar un vistazo a toda la sesión. La forma más sencilla es:
1) Seleccione “Todos” del menú "Número de pistas visibles":
2) Haz clic en el botón "Zoom a la sesión" (tercer botón en las Opciones de zoom):
Ahora debería tener una buena visión general de toda la sesión, así:
Escucha la producción por última vez y asegúrate de que se oye todo de la manera deseada y que no se te olvido desactivas algún Mute o Solo. Todo lo incluido entre los Marcadores de Posición "inicio" y "fin" en la línea temporal será exportado, así que tienes que establecer primero los marcadores si no están en la posición correcta.
Si el marcador de final está demasiado después del final de la pieza, haz clic y arrastra hacia la izquierda hasta que esté bastante cerca del final de la última región de la composición. En el caso contrario todo eso se exporta como espacio en blanco sin sonido. 

Importante: Puesto que exportar se maneja mediante el Bus master, todas las pistas dentro del rango que seleccionas se exportan conjuntamente, exactamente como se reproducen en tu sesión. A diferencia de la orden Exportar Región, este tipo de exportación incluye cualquier Atenuación y Panoramización, y Automatización o Plugin que hayas creado, junto con las ediciones individuales hechas a las Regiones también. Si cualquier pista tiene los botones de enmudecer o de solo activados, esto afectará a qué pistas se oirán en el fichero exportado. 

Ahora para exportar una sesión, utiliza el menú superior: Sesión → Exportar → Exportar sesión a fichero audio.

Preset: Aquí NO se escribe el nombre del archivo. Es sólo para guardar "preset" predefinidas para guardar archivos, por ejemplo, si siempre guardas en uan calidad de audio determinada tus audios creas una preset y al elegirla se cargan los parámetros definidos. No te preocupes por este campo ahora.
Formato: permite elegir el formato de archivo (WAV, OGG, FLAC, etc.). El valor predeterminado es de CD, que crea un archivo WAV. 
Nota: Si usas GNU/Linux NO viene para exportar en MP3, pero puedes exportar a WAV y luego usar un conversor de audio.
Añadir otro formato: si desea exportar en más de un formato, al mismo tiempo, haz clic en esta pestaña.
Posición: Este es el lugar donde se encuentra el archivo después de guardarlo. De forma predeterminada, se encuentra en la carpeta de "Export" que está dentro de la carpeta principal de la sesión. También puedes hacer clic en "Examinar" y seleccionar otra ubicación, como el escritorio, por ejemplo.
Construir el nombre: Aquí es donde se escribe el nombre para el archivo. Ardour añadirá automáticamente el nombre de sesión para el archivo exportado, por lo que si no se escribe nada aquí el nombre puede terminar algo genérico como "mi-sesion.wav".
Después de haber elegido las opciones, haz clic en Exportar. Una vez finalizada la operación, se puede encontrar el archivo en la carpeta “Export” o en la elegida. 

### Opción: Upload to SoundCloud 
Por medio de la página web SoundCloud puedes compartir tus sonidos en privado en publico (por ejemplo en las redes sociales o incluirlas en tu sitio web propio). Usar SoundCloud es gratis. Para poder conectarse tienes que ingresar tus datos de la cuenta. Si todavía no tienes una cuenta lo puedes crear gratuito en la pagina web: www.soundcloud.com
Entonces si tienes una cuenta puedes seleccionar esta opción “Upload to SoundCloud“ dentro de la ventana de Exportación que permite la subida de tu audio exportado a la pagina web de SoundCloud. Después de terminar la exportación Ardour se conecta directamente a tu cuenta SoundCloud y sube tu audio. 

### Opción: Analizar audio exportado
Esta opción te permite ver la Waveform, la representación visual de un sonido en el dominio temporal incluyendo los momentos de Saturación y un análisis del espectro audio, los picos, el rango de Loudness, la Loudness integrada y  LUFS. También puedes ver los datos generales del archivo como la duración, el Timecode, la frecuencia de muestreo, los canales, el formato. Si necesitas mas información acerca de estos términos técnicos, hay una pagina interesante acerca de la Loudness en ingles: http://www.tcelectronic.com/de/loudness/loudness-explained/



## Exportar Regiones
Puedes querer exportar solo una región de tu sesión, quizás para utilizarla como ejemplo en otra aplicación, o para editarla en un programa de edición diferente.

Para Exportar una región, selecciónala (para que se torne azul), y entonces haz clic-derecho en Exportar o utiliza el menú Sesión → Exportar → Exportar regiones seleccionadas a fichero de audio.

Esto abrirá el mismo cuadro de diálogo Exportar explicado en el capítulo Exportación de una sesión. Elige las opciones y haz clic en Exportar. Sólo se exportará la región seleccionada!

Por favor ten en cuenta que cuando se exporta una región, no todos los parámetros y ediciones son exportados. Las Regiones recortadas, divididas, extendidas e invertidas pueden ser exportadas, pero ediciones tales como la Normalización, Atenuación y Panoramización, y Automatización NO se exportan. También, el volumen de la misma pista de audio o del Bus master no afectará al fichero exportado. Para exportar estas ediciones, por favor mira los capítulos Exportar un Rango y Exportar una Sesión.

### Exportación Diversas Regiones a la vez
Si estás construyendo una colección de muestras para usar después y las muestras son, básicamente, recortando y editando Regiones, al final del proceso tendrás que exportar todas ellos. Si el número es grande, la exportación de forma manual puede ser tediosa. He aquí una manera de exportar varias regiones a la vez.
En el modo Seleccionar objeto [ G], selecciona todas las regiones que deseas exportar. No es necesario que estén en la misma pista.

Ir al menú Región → Rangos selecciona Agregar marcador para un intervalo de Región. (Región →  Rangos Añadir → Marca de rango por región.)

Ardour crea ahora sólo Rangos de marcadores que se ajustan exactamente al comienzo y al final de sus regiones seleccionadas (ver los rectángulos verdes en la regla Marcas de rango):

Ve al Menú de Sesión → Exportar y selecciona Exportar a archivo de audio (s) [Alt + E).
En el cuadro de diálogo Exportar, haz clic en la pestaña Intervalo de tiempo. Verás todos los rangos de nueva creación que allí se indican. También hay un rango predeterminado que representa toda la sesión.
En Intervalo de tiempo, haz clic en Seleccionar todo, y de-seleccionar el primer rango (el rango de "sesión"). La razón es porque queremos exportar los rangos cortos, no toda la sesión completa.
Volver a la pestaña principal (Formato de archivo).
Haz clic en Exportar.
Tus regiones se habrán exportado a archivos de audio individuales.

Importante: Este método exporta todo lo que cae en cada intervalo de tiempo definido. En otras palabras, si tienes otras regiones en otras pistas que suenan simultáneamente con la región que deseas exportar, serán mezcladas entre sí. Otra forma de verlo es la siguiente: la operación de exportación exportará todo lo que juega bajo los rangos de tiempo definidos. Si eso no es lo que quieres, se puede utilizar en solitario o botones de silencio en seleccionar las pistas para garantizar exportar sólo lo que quieres.

## Exportar Rangos
Según hemos aprendido previamente, exportar una Región no exporta todos los cambios que querrías haber hecho a la región. Para Exportar ediciones tales como Normalización, Atenuación y Panoramización, y Automatización, debes exportar bien un Rango o la sesión entera que también vimos con anterioridad.

¿Qué es exactamente un rango?
Un rango es simplemente un área específica con un punto de inicio y final. La pantalla de selección a la derecha del reloj secundaria muestra el tiempo de inicio y fin del rango seleccionado, así como su duración. El área creada por el método anterior desaparecerá tan pronto como se hace clic fuera de ella.

Para Exportar un rango, selecciona la herramienta Seleccionar/Mover rangos , entonces haz clic-derecho en Exportar rango o utiliza el menú superior: Sesión → Exportar → Exportar rangos seleccionadas a fichero de audio. Vamos por partes:

1. Haz clic en el botón de modo de rango [ R)
2. Marca el rango que quieres exportar
3. Haz clic derecho en el área de distribución y elige la opción Exportar intervalo en el menú: Esto abrirá el cuadro de diálogo Exportar que explicamos en el capitulo Exportar una sesión. Elige las opciones y clic en Exportar. El rango se exportará y se guarda como un archivo de audio.

Nota: El comando Intervalo de exportación exportará todo lo que se escucha en el Bus Master, tal y como se reproduce en la sesión. Si alguna de las pistas tienen los botones de Silencio y solo participan, esto también afectará a la que las canciones se escuchan en el archivo exportado.

¿Qué es un marcador de intervalo o rango?
Marcadores de rango son esencialmente dos marcadores de ubicación para marcar el inicio y el final de una sección.
Aquí están algunas maneras de crear marcadores de rango o intervalo:
A partir de una selección, clic derecho sobre él y seleccione Añadir Marca de rango.
Desde la línea de tiempo, clic en el espacio horizontal Marcas de rango y elegir la opción Nuevo Rango.
A partir de una o más regiones seleccionadas, clic derecho en la Región y elegir la opción Añadir Marca de rango simple (si se seleccionas una sola región), o Añadir Marca de rango por región (si se seleccionan varias regiones).

Nota: Puedes borrar todos los marcadores existentes haciendo clic derecho en el área de distribución de marcadores de la línea de tiempo y seleccionando Borrar todos los rangos.

## Exportar Audio a Video
Aunque Ardour no es un editor de video se puede añadir una pista audio a un archivo de video. Ardour usa ffmpeg, una herramienta de video muy potente. Aún así las opciones de exportar en Ardour solo ofrece unas opciones limitadas lo cual implica que es para el uso básico de exportación de video. 

Output: Aquí puedes entrar el nombre del archivo que vas a exportar.

Entrada de Video: Dando clic en Explorar puedes seleccionar la fuente (el archivo de video a cual quieres añadir la pista audio). 

Audio: Por defecto se va usar el audio que sale del Bus Master y añadir a tu video, pero puedes seleccionar otras fuentes.  

Para saber más acerca de los demás opciones de video ver la pagina de ffmpeg: http://ffmpeg.org/documentation.html

Dando clic en exportar inicia la exportación. 

## Intercambiar con otro DAW
Nunca ha sido muy fácil de mover sesiones creado en un DAW a otro DAW. Hay dos estándares que existen para esto y que gozan un apoyo bastante amplio. 
OMF (Open Media Framework), también conocido como OMFI. Fue desarrollado y controlado por la empresa Avid 
AAF (Advanced Authoring Format), desarrollado por un consorcio de corporaciones de medias.
Pero en practica los dos de estos “estándares” tienen un especificaciones tan complejas o incompletas que diferentes DAWs solo lo soportan parcialmente, diferentemente o no. 

Entonces para mover sesión Ardour a otro DAW tienes 3 maneras:
Exportar los Stems – significa exportar las pistas audios y MIDI consolidados - con sus efectos de insert -   completas de inicio al final de la sesión. Esto es la manera recomendada y tal vez más rápida. La ventaja es que asi se puede importar todos los archivos audio en una DAW
Copiar la sub-carpeta “interchange” de la sesión de Ardour. La desventaja es que esto copia TODOS los archivos audio, también los que no son utilizados, sin sus efectos insert. Los archivos MIDI no se copian. Si quieres hacer esto, es recomendable usar ANTES el comando Sesión → Purgar → Bring all media files into one folder y también Purgar archivos no usados en el mismo menú para que se limpie tu sesión de los archivos que grabaste pero al final no usaste. 
Usa AATranslator. Es un complemento comercial que permite a exportar la sesión en otro DAW y guardarla en formato de Ardour. Mas información: http://www.aatranslator.com.au/

Y para mover una sesión de otro DAW a Ardour hay también las 3 maneras:
Importar los Stems (archivos de audio que contienen las pistas individuales con sus efectos). 
Si trabajaste con ProTools puedes importar una sesión de este DAW. Abre la sesión por el menú Sesión → Importar sesión PT. Esto NO importa la sesión 100% correcto ya que el formato de una sesión ProTools no es un formato abierto y se desconoce como funciona completamente. 
Usa AATranslator. Es un complemento comercial que permite a exportar la sesión Ardour para usarlo en otra DAW. Mas información: http://www.aatranslator.com.au/

En la próxima sección, los Apéndices, hemos incluido alguna información adicional que creemos que sería de utilidad para los nuevos usuarios de Ardour, incluyendo cómo conseguir Más Ayuda, un Glosario de términos técnicos utilizados en este manual, algunos Enlaces para más información acerca de Ardour en Internet.

¡Felicitaciones, has logrado llegar al fin del manual Ardour 5! Esperamos que este manual te haya sido útil para aprender las funciones clave de Ardour.

# 6. Appendix
Sigue unas tablas con los atajos de teclado principales. Es recomendable familiarizarte con ellos ya que esto te permite trabajar mas rápido y fluido. Para ver todos los atajos y cambiarlos puedes ir al menú Ventana - Bindings editor o pulsando el atajo [Alt + K]. 
#1 Atajos de teclado 

### Atajos generales
Atajo
Acción
Mayus. + E
Cierra cualquier ventana de diálogo excepto los avisos de error
Alt + E
Abre la ventana para exportar 
Alt + M
Cambia entre las ventanas del Editor y del Mezclador
Alt + O
Abre la ventana “Propiedades de la sesión”
Alt + P
Abre el gestor de conexiones audio
Alt + C
Abre el reloj grande
Ctrl + l
Importar medios existentes
Ctrl + S
Guarda la sesión
Ctrl + Q
Salir
Ctrl + O
Abre una sesión
Mayus. + Ctrl + O 
Abre una sesión reciente


### Atajos de transporte
Atajo
Acción
Espacio
Activa/desactiva el transporte
Alt + Espacio
Reproduce selección
*
Activa/desactiva el botón de grabación del transporte
Inicio
Mueve la cabeza de reproducción al principio
Fin
Mueve la cabeza de reproducción al final
C
Activa/desactiva la claqueta


### Atajos en la ventana Editor
Atajo
Acción
Mayus + Ctrl + N
Crea una nueva Pista/Bus/VCA 
Ctrl + Z
Deshace
Ctrl + R
Rehace
Supr 
Elimina el objeto seleccionado
Ctrl + C
Copia el elemento seleccionado
Ctrl + V 
Pega el elemento seleccionado
Ctrl + X
Corta el elemento seleccionado


### Atajos de selección de herramientas
Atajo
Acción
R
Selecciona modo Rango
G
Selecciona modo Seleccion (atrapar)
C
Selecciona modo Recortar
T
Selecciona modo Estirar (Time-stretch)
E
Selecciona modo Edición interna
D
Selecciona modo Dibujo
Y
Activa/Desactiva la función SMART


### Atajos en la ventana Mezclador
Atajo
Acción
Flecha derecha
Avance rápido/más rápido
Mayus. + flecha derecha + espacio
Avance muy rápido
Ctrl + flecha derecha
Avance rápido lento
Flecha izda
Rebobinar/rebobinar más rápido
Mayus. + flecha izda
Rebobinar rápido
Ctrl + flecha izda
Rebobinar despacio


### Mover la cabeza de reproducción
Atajo
Acción
P
Mover la cabeza a la posición del puntero
Intro
Mover la cabeza al cursor de edición
Tab
Mover la cabeza al inicio de la siguiente región
Ctrl + Tab
Mover la cabeza al final de la siguiente región
`
Mover la cabeza al inicio de la región anterior
Ctrl + `
Mover la cabeza la siguiente marca
| (numérico)
Mover la cabeza a la marca anterior


##7. Mover el cursor de edición
Atajo
Acción
E
Mover el cursor a la posición del puntero
Alt + Intro
Mover el cursor a la posición de la cabeza de reproducción
[
Mover el cursor al inicio de la región anterior
Ctrl + [
Mover el cursor al final de la región anterior
]
Mover el cursor al inicio de la región siguiente
Ctrl + ]
Mover el cursor al final de la región siguiente
””’
Mover el cursor al sync de la región siguiente
;
Mover el cursor al sync de la región anterior
F1
Mover el cursor al comienzo de la selección de rango (si está definida)
F2
Mover el cursor al final de la selección de rango (si está definida)


##7. Cambiar la visualización
Atajo
Acción
Flecha izquierda
Mover línea de tiempo hacia atrás
Ctrl-b
Mover línea de tiempo hacia atrás
**Flecha derecha
Mover línea de tiempo hacia delante
**Ctrl-f
Mover línea de tiempo hacia delante





## Ayuda y enlaces utiles
### Foro oficial Ardour
En el sitio oficial de Ardour hay el manual (http://manual.Ardour.org/) y un foro oficial en ingles de puedes navegar o publicar preguntas. Muchas cuestiones comunes sobre configuración y uso de Ardour ya han sido contestadas allí. Publicar en este foro requiere registrarse en el sitio web http://community.Ardour.org/community
Puedes acceder también por el menú Ayuda - Foros de usuarios y se abre tu navegador con el sitio web del foro. 

### Conseguir ayuda vía listas de correo
Para los que prefieren las listas de correo al chateo por IRC, la lista de correo de Usuarios de Ardour es también un sitio bueno donde los usuarios y algunos desarrolladores hablan de todas las clases de problemas e ideas relacionaron con utilizar Ardour. Esta es una lista activa, con muchos usuarios solícitos y enterados alrededor para ayudar a guiar a gente menos experimentada. Hay a veces discusiones más generales sobre temas como técnica de grabación, selección de interfaz de audio, etc.
http://lists.Ardour.org/listinfo.cgi/Ardour-users-Ardour.org

### Centro de Ayuda LiberaTuRadio.org
La Red de Radios Comunitarias y Software Libre tiene en su web un centro de ayuda con videos, manuales y recursos sobre distinto software libre para radio: 
https://liberaturadio.org/centro-de-ayuda/programas-libres/editor-audio-Ardour
https://liberaturadio.org/centro-de-ayuda-menu
http://vimeo.com/2867399

### Configuración JACK:
Cadence
https://liberaturadio.org/category/tutorial-jack-cadence
Jack Audio Connection Kit
http://jackaudio.org

### Plugins:
http://www.audiopluginsforfree.com (instrumentos y efectos) en varios formatos (WindowsVST, LinuxVST,  AU y LV2) y que son gratuitos.
http://www.guitarix.com es un amplificador virtual de guitarra (hay la versión LV2 que se puede instalar en Ubuntu con “sudo apt-get install guitarix-lv2”)
http://wootangent.net/2011/06/lv2-synths-for-Ardour-3-a-list/ o 
http://linux-sound.org/linux-vst-Plugins.html

### Enlaces relacionados a la producción musical
http://www.futuremusic-es.com/
Noticias, guías, pruebas/evaluaciones de equipos, descarga de software gratis, paquetes de samples y Plugins.

http://produceaudio.net/
Cursos, guías y asesoramiento para la producción (acústica, grabación, mezcla, masterización), ofrece un paquete incluyendo 2 libros gratis por suscripción de correo. 

www.audioproduccion.com
Tutoriales gratis y cursos premium para la producción audio ofrece un libros gratis por suscripción de correo. 

http://www.hispasonic.com/
Noticias, guías, pruebas/evaluaciones de equipos, descarga de software, paquetes de samples y Plugins.

www.doctorproaudio.com
Noticias, Calculadores de Audio e Iluminación, listas muy completas de organizaciones, ferias, importadores de diferentes marcas, etc.

## Glosario
AIFF 
Un formato de fichero de sonido desarrollado por Apple y generalmente utilizado para audio sin pérdida y sin compresión. Los ficheros AIFF son compatibles con sistemas operativos Linux, mac OS y Windows.
ALSA (Linux)
Advanced Linux Sound Architecture (Arquitectura de sonido avanzada de Linux). ALSA proporciona funcionalidad de audio y MIDI al sistema operativo Linux.
Arm (Armar) Pistas para grabar/ Ardour para grabar]
Acción que hace que Ardour esté preparado para grabar. Antes de grabar en Ardour, una o más pistas necesitan ser armadas primero, y entonces Ardour mismo necesita ser armado.
Artefacts (Artefactos) [de sonido]
Disminución o distorsión perceptible de calidad de sonido generada como subproducto de ciertas operaciones de procesamiento de señal. Los artefactos son normalmente vistos como resultados indeseables o inesperados de la transformación de sonido de otro modo intencionada.
Attenuation (Atenuación)
Reducir el nivel de una señal de audio, normalmente medida utilizando una escala logarítmica. Ver también gain (ganancia). 
Audition (Escucha)
El auditor es una banda de mezcla oculta a través de la cual se reproducen las regiones escuchadas. Escuchar (Auditioning) una región reproducirá sólo esa región, sin procesar envíos o Plugins.
Automation (Automatización)
La Automatización es el ajuste automático de parámetros varios tales como la ganancia, la panoramización o las configuraciones de Plugins. Los cambios pueden ser hechos una vez y luego repetidos cada vez que la mezcla se repita. La automatización en Ardour está controlada por lineas de automatización unidas a cada pista o Bus.
Auxiliary Controls (Controles Auxiliares)
Los botones en el lado superior derecho de los controles sitos en la Ventana de Editor: Pinchar/Despinchar (Punch in/out), Auto Reproducir, Auto Entrada, Click, Solo y Escucha.
Amplitude (Amplitud) 
El nivel o magnitud de una señal. Las señales de audio con una amplitud más alta normalmente suenan más fuertes.
Bands (Bandas) [ecualización]
Las particulares regiones de frecuencia a ser aumentadas o atenuadas en el proceso de Ecualización.
Bars (Compases) [música]
Igual que 'medida', un compás es una unidad métrica. En notación Occidental, es el espacio comprendido entre dos líneas verticales dibujadas a través del pentagrama La duración específica de un compás depende de su Time signature (Compás) y el actual Tempo de la música.
Bass (Graves) [Frecuencias]
Una manera genérica de referirse a las frecuencias más bajas del Espectro de un sonido.
Beat (Pulso)
El pulso básico subyacente una pieza de música.
Beats per Minute (Pulsos por Minuto) 
Pulsos por Minuto (BPM) es una medida del Tempo en música. Un índice de 60 pulsos por minuto significa que cada segundo habrá un pulso; 120 bpm significa dos pulsos por segundo, y así. Las indicaciones BPM normalmente aparecen al inicio de una notación musical tradicional como una marca de metrónomo (por ejemplo, "la negra equivale a 60", significa una nota negra por segundo).
Bit 
Un bit (binary digit o dígito binario) es un número único con un valor de 1 ó 0. 
Bit Depth (Profundidad de Bits)
Se refiere al número de bits utilizado para escribir una muestra. En el CD estándar, cada muestra de audio está representada por un número de 16-bit. Esto da 2^16 (dos elevado a la potencia de dieciséis = 65,536) valores posibles que una muestra puede tener. Una profundidad de bits más alta significa un mayor rango dinámico posible. Las grabaciones de estudio son normalmente primero hechas grabar con una profundidad de bits de 24 (o incluso 32) para preservar tanto o más detalle antes de que se transfiera a CD Los DVDs están hechos a 24 bits, mientras videojuegos de los '80 son famosos por su "sonido de 8 bits" característicamente áspero. A la profundidad de bits también se le dice como word length (Tamaño de palabra). 
Buffer Size (Tamaño de buffer o tampón)
El buffer o tampón es una sección de memoria específicamente dispuesta para los datos de señal provisionales. Bufferes tampón pequeños permiten una latencia más baja y así son necesitados cuando se utilizan aplicaciones de audio que requieren interacción en tiempo real. La desventaja es que el consumo de CPU para el sistema es mayor con tamaños de buffer menores. Los bufferes grandes (como de 512 o 1024) pueden ser utilizados cuando no hay tal requisito.
Built-in Input and Output (Entrada y Salida incorporada)
Estos son los interfaces por defecto para conseguir meter y sacar sonido de tu ordenador si no tienes una tarjeta de sonido externa. En un portátil, son las conexiones comunes de entrada (mic) y salida (auriculares).
Bus 
Un Bus es similar a una Pista excepto que no contiene sus propias regiones. No puedes grabar directamente en un Bus o arrastrar regiones a él. La banda de mezcla vertical representa el flujo de señal de un Bus, mientras que el lienzo principal horizontalmente exhibe información en función del tiempo para cada Bus (tales como líneas de automatización).
BWF
Broadcast Wave Format o Formato de onda de difusión (BWF) es una extensión del popular formato de audio Microsoft WAVE y es el formato de grabación de la mayoría de grabadoras digitales no-lineales basadas en ficheros utilizadas para producción de películas y televisión. Este formato de fichero permite la inclusión de metadatos para facilitar el intercambio perfecto de datos de sonido entre plataformas de ordenador diferentes y aplicaciones.
CAF
CAF (Core Audio Format o Formato de audio central) es un formato de fichero para almacenar audio, desarrollado por Apple. Es compatible con mac OS 10.4 y superiores. El formato Core Audio está diseñado para superar las limitaciones de los viejos formatos, incluyendo AIFF y WAV. Justo como el formato de fichero .mov de QuickTime, un formato de fichero .caf puede contener muchos formatos de audio, pistas de metadatos, y muchos más datos diferentes.
Center Frequency (Frecuencia Central)
En algunos Plugins de EQ (ecualización), el usuario tiene la posibilidad de elegir la frecuencia central para cada una de las Bandas de Frecuencia. La frecuencia central de una Banda será la que más se atenúe o refuerce por el ecualizador para esa banda específica. Las frecuencias que rodean a la frecuencia central serán menos afectadas. 
Clipping (Saturación)
La Saturación ocurre cuando una señal es demasiado alta en nivel para ser reproducida. Cualesquier muestras demasiado altas en nivel sencillamente serán truncadas, resultando en distorsión, pérdida de detalle de audio, y frecuencias artefacto que no estaban presentes en el sonido original. 
Clipping Point (Punto de Saturación) 
El punto de saturación de un sistema digital se refiere a 0 dB, y el nivel de cualquier sonido está medido en cuán lejos éste está por debajo del punto de saturación (-10 dB, -24 dB, etc). 
Clocks (Relojes)
Los dos grandes visualizadores numéricos cerca de la Ventana de Editor. Pueden exhibir el tiempo en varios formatos: Timecode (Código de tiempo), Bars:Beats (Compases:Pulsos), Minutos:Segundos, y Samples (Muestras).
Compile (Compilar)
Las aplicaciones FLOSS están distribuidas como código fuente, el cual es humanamente legible pero no puede ser ejecutado como una aplicación real. Para tornar este código fuente en una aplicación de ejecutable, primero debe ser Compilado. Cuando descargas una imagen de disco para mac OS o un paquete de software de tu distribución (Ubuntu, Debian o Fedora), ya ha sido compilado para ti. Aun así, si deseas añadir características (como soporte para Plugins VST) que tu distribución no proporciona, entonces tienes que compilar la aplicación con el código de fuente tu mismo. 
Compression (Compresión) [DSP]
Esencialmente, la compresión hace que las partes silenciosas de una señal sean más sonoras sin cambiar el nivel de 
las partes más fuertes. Esto conlleva una reducción del rango dinámico real: un sonido comprimido es menos dinámico (tiene una rango más pequeño de niveles) 
Compression (Compresión) [datos]
Como cualesquier otros datos, los datos de audio pueden ser comprimidos de modo que utilicen menos espacio de disco duro. La compresión tal como FLAC, ALAC, o MLP reduce el tamaño de ficheros de audio comparados con WAV o AIFF sin cambiar los datos, lo que se suele llamar compresión sin pérdida. El audio puede ser comprimido a un tamaño menor utilizando compresión con pérdida tal como MP3, Ogg Vorbis o AAC pero esto se consigue eliminando datos lo que puede tener un efecto audible. 
Cursor Modes (Modos de cursor)
Estos son los seis botones justo bajo las órdenes de Transporte en la Ventana de Editor. Las seis funciones diferentes que el puntero de ratón puede tener en Ardour son: Seleccionar/Mover Objetos, Seleccionar/Mover Rangos, Selecciona Rango de Ampliación (Zoom), Dibujar Automatización de Ganancia, Extender/Encoger Regiones, Escuchar Regiones Específicas.
Decibels (Decibelios) 
El decibelio es una escala logarítmica utilizada para medir muchas cantidades, incluyendo la ganancia, nivel o volumen de una señal. El decibelio es normalmente abreviado a dB y en el audio digital normalmente denota cuan lejos por debajo 0 dBFS (el punto de clipping [saturación] de un sistema) está una señal. 
Delay (Retardo) [efecto]
La cantidad de tiempo entre un evento y otro. Como efecto de audio, un retardo toma una señal de sonido entrante y la retarda durante una cierta cantidad de tiempo. Cuando se mezcla con el sonido original, se oye un "eco". Utilizando la retroalimentación para retornar la señal tratada de nuevo al retardo (normalmente después de bajar su ganancia), producirá ecos múltiples con un decaimiento.
Destructive Editing (Edición destructiva) 
Las acciones destructivas son las que modifican o borran permanentemente los datos originales (ficheros de sonido) en el transcurso de la edición o grabación. 
Distortion (Distorsión) 
La distorsión ocurre cuando una señal de audio está cambiada de alguna manera que produce frecuencias no presentes en la original. La distorsión puede ser deliberada o indeseada, y puede ser producido por conducir la señal a un punto de clipping (saturación) , o por utilizar transformaciones matemáticas para alterar la forma (o "waveform") de la señal (normalmente referido como "waveshaping").
Driver (Controlador) [JACK]
Software escrito para controlar hardware. CoreAudio es el controlador de sonido de Mac. ALSA es el controlador más común de Linux.
DSP
Digital Signal Processing (Procesamiento de señal digital).
Dynamic Range (Rango dinámico)
Utilizado para referirse a la diferencia entre el sonido más fuerte y el más silencioso que posiblemente pueda grabarse, así como la cantidad de detalle que pueda ser oído en entre aquellos extremos. Los sonidos que son demasiado silenciosos para ser grabados se dicen de estar bajo el noise floor (umbral de ruido) del sistema de registro (micrófono, grabador, tarjeta de sonido, software de audio, etc).  Los sonidos que son demasiado fuertes serán distorsionados o saturados. 
Edit Modes (Modos de edición)
Los tres Modos de edición disponibles (Deslizar, Rizado o Bloquear) controlan el comportamiento de las operaciones de edición en el Lienzo Principal. 
Edit Point (Punto de edición)
El punto en el Lienzo Principal donde tiene lugar una acción como Pegar. Este puede ser el Ratón, la Marca activa o un Marcador.
Editor Window (Ventana de Editor)
Ardour proporciona dos modos de ver una sesión: el Editor y el Mezclador. El Editor representa los aspectos temporales de una sesión: muestra pistas y Buses como exhibiciones horizontales de línea de tiempo, con material dentro de las pistas (audio, MIDI, vídeo, datos de automatización, etc.) colocado a lo largo del eje horizontal (tiempo).
EQ / Equalization (Ecualización) 
La Ecualización (EQ) es el proceso de ajustar los niveles relativos de diferentes frecuencias en una grabación o en una señal. En otras palabras, es el proceso de aumentar o atenuando las varias bandas de frecuencia de un sonido según una meta artística escogida.
Filter (Filtro)
Un tipo de procesamiento de señal que suprime algunas frecuencias. 
Floating Point Numbers (Números de coma flotante)
Es sencillamente un número con un coma decimal. "Coma flotante" se refiere a a la técnica específica que el ordenador utiliza para representar un mayor rango de valores enteros y no enteros.
FLAC
Un formato open source de audio sin pérdida generalmente compatible con Linux, mac OS y Windows. A diferencia de AIFF y WAV, FLAC es un formato comprimido, que permite reducir los tamaños de fichero. 
FLOSS
FLOSS significa Free Libre Open Source Software. Los Manuales FLOSS son una colección de manuales sobre software libre y open source junto a las herramientas utilizadas para crearlos y la comunidad que utiliza esas herramientas. Incluyen autores, editores, artistas, desarrolladores de software, activistas y muchos más.
Format (Formato) [fichero de audio]
Los tipos de fichero de sonido como se guardan los sonidos Entre el más común están AIFF, WAV, FLAC, mp3 y Ogg Vorbis. 
fps
Frames Per Second (Cuadros por segundo). La ratio de Cuadros, o la frecuencia de cuadros (ratio) a la cual un dispositivo de imagen produce imágenes únicas llamadas cuadros.. El término se aplica igualmente bien a gráficos de ordenador, cámaras de vídeo, cámaras de película, y sistemas de captura. La Ratio de cuadros se expresa lo más a menudo en cuadros por segundo (FPS). 
Frequency (Frecuencia)
Se refiere al numero de veces que una oscilación ocurre por segundo. La frecuencia se mide en Hercios (Hz), y está correlacionada con el tono de un sonido. La frecuencia es una escala lineal, mientras que el tono es logarímico. El tono 'La' (A) sobre el 'Do' (C) medio tiene una frecuencia de 440 Hz. El 'La' (A) una octava por encima de aquella es dos veces aquella frecuencia (880 Hz).
Gain (Ganancia)
Aumentar el nivel de una señal de audio, normalmente medida utilizando un escala logarítmica. Ver también atenuación.
Grid (Rejilla)
La rejilla es un sistema de puntos al que una región se puede ajustar cuando se edita. LA rejilla puede estar "Sin Rejilla", "Rejilla" o "Magnética". 
Grid Points (Puntos de rejilla)
Los puntos en la Rejilla a los cuales las regiones se ajustarán cuando esta esté activa. Los Puntos de Rejilla pueden ser minutos, segundos, cuadros de vídeo, compases, pulsos o algún múltiplo de pulso. 
Hertz (Hercio)
Un término utilizado para describir el número de veces que algo ocurre en un segundo. En el audio digital, se utiliza para describir la sampling rate (frecuencia de muestreo), y en acústica se utiliza para describir la frecuencia de un sonido. Mil hercios se describen como KHz (Kilo Hercio). 
High Shelf (Estante Alto) 
En un Ecualizador, un Shelf (Estante) corta o aumenta todo por encima (High Shelf o Estante Alto) o por debajo (Low Shelf o Estante Bajo) de una frecuencia específica.
Headroom (Margen) 
El rango de Decibelios entre el Pico máximo de región y el Punto de Saturación es generalmente referido como Margen. Es práctica común de grabación mantener aproximadamente de tres a seis Decibelios de Margen entre el máximo de tu señal y el Punto de Saturación.
Jack Audio Connection Kit (JACK) 
JACK es un sistema de audio de baja latencia qué gestiona conexiones entre Ardour y la tarjeta de sonido de tu ordenador, y entre Ardour y otros programas de audio JACK en tu ordenador.
Jack Server (Servidor Jack) 
El servidor Jack es el "motor" o "backend" del juego de conexión Jack Audio Connection Kit. 
Jack Router (Enrutador Jack) 
El Enrutador Jack Router permite enrutar el audio de una aplicación a otra utilizando el Servidor Jack. 
LADSPA Plugins 
Linux Audio Developer Simple Plugin API (LADSPA) es el estándar que permite a los procesadores de audio y efectos ser enchufados a un amplio rango de paquetes de síntesis de audio y grabación. Por ejemplo, permite al desarrollador escribir un programa de reverberación y empaquetarlo en una "biblioteca de Plugins" LADSPA. Entonces los usuarios ordinarios pueden utilizar esta reverberación dentro de cualquier aplicación de audio compatible con LADSPA. La mayoría de aplicaciones de audio en Linux soporta LADSPA.
Latency (Latencia)
La latencia es la cantidad de tiempo necesario para procesar todas las muestras que vienen desde aplicaciones de sonido en tu ordenador y enviarlas a la tarjeta de sonido para reproducción, o para reunir muestras desde la tarjeta de sonido para grabación o procesado. Una latencia más breve significa que oirás los resultados más rápido, dando la impresión de un sistema que responde mejor.. Aun así, con latencia más breve también correrás un riesgo mayor de fallas en el audio porque el ordenador podría no tener bastante tiempo para procesar el sonido antes de enviarlo a la tarjeta de sonido. Una latencia mayor significa menos fallas, pero al precio de un tiempo de respuesta más lento. La Latencia se mide en milisegundos.
Amplitude (amplitud) [mezcla]
La fuerza de una señal de audio. La escala de amplitud es logarítmica, ya que expresa la proporción física de potencia entre un sonido y otro. Los niveles en sistemas de audio digital son normalmente representados como la cantidad de decibelios bajo el punto de saturación de 0 dB. Véase también loudness (volumen). 
Limiting (Limitación)
El proceso por el cual se previene que la amplitud de salida de un dispositivo exceda de un valor predeterminado. 
Linear (Lineal)
Una escala de números qué progresa de manera aditiva, tal como por añadir uno (1, 2, 3, #..), dos (2, 4, 6, 8...) ó diez (10, 20, 30, 40...). Multiplicar una señal de audio, por ejemplo, bien por una escala lineal o bien por una escala logarítmica producirá resultados muy diferentes. La escala de frecuencia es lineal, mientras que la escala de tono y ganancia son logarítmicas.
Lock Edit (Edición de Bloqueo o Bloquear)
Uno de los tres Modos de Edición disponibles, la Edición de Bloqueo (o Bloquear) es similar a la Edición de Trozo (o Reunir), pero las regiones quedarán en sus posiciones originales a pesar de cualquier operación de edición ejecutada.
Logarithmic (Logarítmica)
Una escala de números qué progresan según una cierta proporción, tal como exponencialmente (2, 4, 8, 16, 25#..). Ambas escalas de tono y ganancia son logarítmicas, mientras que la escala de frecuencia es lineal.
Lossless/Lossy (Sin/con pérdida)
Véase Compression (Compresión) [datos] 
Loudness (Volumen)
A diferencia de la amplitud, la cual expresa la potencia física de un sonido, el volumen es la fuerza percibida de un sonido. Tonos en frecuencias diferentes pueden ser percibidos como que estén a diferentes volúmenes, incluso si son en la misma amplitud.
LV2
LV2 es un estándar abierto para Plugins y a juego con aplicaciones anfitrionas, principalmente apuntados al procesamiento y generación de audio. LV2 es un sencillo pero extensible sucesor de LADSPA, pretendido para hacerse cargo de las limitaciones de LADSPA el cual muchas aplicaciones han sobrepasado.
Lienzo principal
En la Ventana de Editor de Ardour, el Lienzo Principal es el espacio justo bajo las reglas de línea de tiempo donde las pistas y Buses se exhiben horizontalmente. 
Master Out (Salida Master)
Una salida maestra es un Bus al cual todas (o la mayoría) de las pistas y otros Buses envían sus salidas. Proporciona un conveniente punto único de control para la producción de Ardour, y es una ubicación típica para efectos globales. El uso de la Salida Master está activado por defecto, y el Bus de salida maestra está configurado para ser estéreo.  
Meter (Métrica) 
La agrupación de pulsos fuertes y débiles en unidades mayores llamadas compases o medidas. En Ardour hay un marcador para cada cambio de métrica que se puede ver en la barra de  
Mixing (Mezcla)
La Mezcla de audio es el proceso por el cual una multitud de sonidos grabados son combinados en uno o más canales, más generalmente estéreo bicanal. En el proceso, los niveles, el contenido de frecuencia, las dinámicas y posición panorámica de las señales de origen se manipulan en común y se puede agregar efectos tales como la reverberación. 
MIDI
MIDI (abreviatura de Musical Instrument Digital Interface) es un protocolo estándar industrial definido en1982 que permite a instrumentos electrónicos musicales tales como Controladores de teclado, ordenadores y otro equipamiento electrónico comunicarse, controlarse, y sincronizarse entre sí. MIDI permite que los ordenadores, sintetizadores, controladores MIDI, tarjetas de sonido, samplers y cajas de ritmos se controlen unos a otros, e intercambien datos de sistema. MIDI no transmite señales de audio, sino sencillamente mensajes como el número de nota (tono), velocidad (intensidad), nota-pulsada, y nota-soltada,  señales de control para parámetros musicales como lo son la dinámica, el vibrato, paneo y señales de reloj que establecen y sincronizan el tempo entre varios dispositivos. 
Mixer Strip (Banda de Mezcla)
Cada pista y Bus se representa en la Ventana de Mezclador por una Banda de Mezcla verticalque contiene varios controles relacionados con el flujo de señal. Hay dos sitios en Ardour en qué puedes ver Bandas de Mezcla. La ventana de mezclador es el obvio, pero también puedes ver una sola banda de mezcla en la parte izquierda del Editor (Mayús. + E para esconder/mostrar) 
Mixer Window (Ventana de Mezclador)
El Mezclador muestra la sesión representando pistas verticalmente como Bandas de Mezcla, con controles para ganancia, habilitar grabación, solo, Plugins, etc. El Mezclador representa el flujo de señal de Pistas y Buses en una sesión de Ardour. La ventana de mezclador proporciona una vista que imita una consola de mezcla de hardware tradicional
Monitoring (Monitorización)
Monitorizar es el proceso de enrutamiento de una mezcla o submezcla específica de tu sesión a salidas separadas (como auriculares). Por ejemplo, un músico siendo grabado puede querer escuchar el material existente mientras actúa. Ardour y JACK hacen fácil configurar salidas de monitor ya que cualquier señal entrante entonces puede ser enviada de nuevo a cualquier salida, opcionalmente mezclada junto con otras señales y con cualquier clase de procesamiento de sonido añadido.
Mono
Un fichero de sonido monoaural contiene solo un canal de audio al contrario de un fichero de sonido estéreo. Una pista monoaural de Ardour tiene solo una entrada y maneja ficheros de sonido monoaurales. 
MP3
Un Formato de fichero de sonido comprimido con pérdida y no-libre. Una alternativa libre al MP3 es OGG/Vorbis.
Graphic Equalizer/Multi-Band Equalizer (Ecualizador gráfico/Ecualizador multibanda)
Un Ecualizador Gráfico (o Multibanda) consta de un banco de deslizadores para aumentar o atenuar diferentes frecuencias de un sonido. 
Non-destructive Editing (Edición no destructiva)
Esto es una forma de editar donde el contenido original no se modifica en el curso de la edición. Detrás de las bambalinas, el fichero de sonido original se mantiene intacto, y tus ediciones son de hecho una lista de instrucciones que Ardour utilizará para reconstruir la señal desde la fuente original cuando lo reproduzcas otra vez. Por ejemplo, crear fade-ins (intensificaciones) y fade-outs (atenuaciones) en tus Regiones es un tipo de edición no-destructiva. 
Normalize (Normalizar)
Normalizar una señal de audio significa ajustar su Ganancia de modo que haga pico a lo máximo que la tarjeta de sonido permita antes de Saturar.
Normal Mode (Modo Normal)
Véase Track Mode (Modo de Pista). 
Note value (Valor de Nota)
La duración proporcional de una nota o silencio en relación a una unidad estándar. Por ejemplo, una 'negra' tiene una duración relativa de un cuarto de una 'redonda'. 
Octave (Octava) [música] 
Una distancia de 12 semitonos entre dos notas. En Hercios, la proporción de una octava es 2:# Por ejemplo, la nota 'La' (A) por encima del 'Do' (C) medio tiene una frecuencia de 440 Hz. La nota 'La' (A) una octava por encima son 880 Hz, y una octava por debajo son 220 Hz. 
Ogg Vorbis
Un formato de fichero de sonido open source comprimido y con pérdida.  
Panning (Panoramización)
La Panoramización es la ubicación de sonidos en el Campo estéreo (izquierda/derecha). 
Parametric Equalizer (Ecualizador paramétrico)
El Ecualizador paramétrico es el tipo más versátil de EQ utilizado para Mezclar debido a su extenso control sobre todos los parámetros de filtrado.
Peaks (Picos)
Los Picos son una representación gráfica de los Niveles máximos de una Región. 
Peak Meters (Medidor de Pico) 
Los Medidores de Pico son una representación en vivo de los Niveles máximos de una Región, y están localizados próximos al Atenuador en la Ventana del Mezclador, y también en el Mezclador de Pista, de cada Pista. 
Pitch (Tono)
El tono representa la frecuencia fundamental percibida de un sonido. Es uno de los tres atributos principales de los sonidos junto con el volumen y el timbre. En MIDI, el tono se representa por un número entre 0 y 127, representando cada número una tecla de un teclado MIDI. La relación del tono a la Frecuencia es Logarítmica. Esto significa que un sonido que se escuche como una Octava (+12 notas MIDI) sobre otro es del doble de frecuencia en Hz, mientras que un sonido una octava por debajo (-12 notas MIDI) es de la mitad de la frecuencia.
Playhead (Marca Activa)
En Ardour, la Marca activa es la línea roja que se mueve en el tiempo (esto es, de izquierda a derecha) para indicar la posición de reproducción actual. 
Plugin
En computación, un Plugin consiste en un programa de ordenador que interacciona con la aplicación anfitriona (en este caso, Ardour) para proporcionar una cierta función "bajo demanda", normalmente una muy específica. Reverberación, filtros, y ecualizadores son ejemplos de Plugins que pueden ser utilizados en Ardour en asociación con las Pistas o Buses.
Portaudio
Un conjunto de controladores de audio libre y de código abierto.
Post-Fader (Plugin or Send) / (Plugin o Envío) Post-Atenuador
En la Banda de Mezcla, el área post-atenuador es el espacio negro bajo el deslizador de ganancia, a los qué los Plugins o envíos se pueden añadir. La entrada de estos Plugins y envíos será la señal después de que cualquier cambio de ganancia manual o automatizada (por tanto "Post-Atenuador"). 
Pre-Fader (Plugin or Send) / (Plugin o Envío) Pre-Atenuador
En la Banda de Mezcla, el área pre-atenuador es el espacio negro sobre el deslizador de ganancia, al que los Plugins o envíos se pueden añadir. La entrada de estos Plugins y envíos será la señal entrante antes de que está sea afectada por cualesquier cambios de ganancia manual o automatizada controlados por el deslizador (por tanto "pre-Atenuador").
Quantization (Subdivisión) 
En procesamiento de señal, la subdivisión puede referirse a la profundidad de bits (véase la definición de Bit depth (Profundidad de bits). En MIDI, la subdivisión se refiere al proceso de alinear notas a una rejilla temporal precise. Esto resulta en notas establecidas por pulsos o fracciones exactas de pulsos. Los secuenciadores MIDI típicamente incluyen algún tipo de función de subdivisión.
Range (Rango)
Un segmento de tiempo. Los rangos se crean con la herramienta Seleccionar/Mover Rangos y pueden incluir una o más pistas. Los rangos de bucle y de pinchado son tipos especiales de rangos que se crean y manipulan con el medidor de rangos de bucle/pinchado.
Real-time System (Sistema de tiempo real) 
En un sistema de tiempo real, el núcleo de Linux está normalmente recompilado (reconstruido) con nuevos parámetros, y otras configuraciones en el sistema están optimizadas lo que acelera el uso de aplicaciones audio en el sistema.
Regions (Regiones)
Las regiones son los elementos básicos de edición y composición en Ardour. Cada región representa todo o una parte de un fichero de audio. Eliminar una región de la pista no elimina el fichero de audio del disco.
Region List (Lista de regiones)
La lista de región está ubicada en el lado derecho de la Ventana de Editor y muestra todas las regiones asociadas con la sesión. 
Reverberation (Reverberación)
La reverberación es la persistencia del sonido en un espacio particular tras eliminar la fuente original del sonido. Una reverberación, o reverb, se crea cuando un sonido se produce en un espacio cerrado causando que se agrupen una gran cantidad de ecos y que luego decaigan lentamente mientras el sonido es absorbido por las paredes y el aire. La reverberación Digital se puede añadir a un sonido en Ardour por medio de la utilización de Plugins. 
Routing (Enrutamiento) 
El enrutamiento es mandar una señal de audio desde algún sitio a doquiera. Las señales pueden ser enrutadas no solo desde el mundo exterior a Ardour y viceversa, pero también dentro de Ardour mismo (por ejemplo, desde una pista a un Bus).
Rulers (Reglas)
Las reglas están en las delgadas barras horizontales que exhiben la línea temporal, ayudando a ver cuando una región o sonido comienza o acaba exactamente. Exhibidos también con las reglas están los marcadores de métrica y tempo, los marcadores de ubicación, los marcadores de rango y los rangos de bucle/ pinchado. 
Sample (Muestra) [datos]
En audio digital, una muestra es el segmento más pequeño posible de un sonido grabado. En audio-CD, por ejemplo, se necesitan 4#100 muestras para hacer un segundo de sonido grabado, y así podemos decir que la frecuencia de muestreo es de 4#100 Hercios. Las muestras también tienen una profundidad de bits la cual determina el rango dinámico que se puede grabar y reproducir. Profundidades de bits comunes son de 16 (para audio-CD), 24 (para grabación de estudio y DVDs) o 32 (para sonidos dentro del ordenador).
Sample (Muestra) [música] 
En música electrónica, la palabra muestra puede significar cualquier porción de sonido extraído de una pieza existente de música para ser reutilizada en una nueva composición. 
Sampler
Un instrumento o software de música electrónico qué reproduce un sonido grabado (o muestra) siempre que se envíe un mensaje de nota- El tono de la nota determina cuan rápida o lentamente se reproduce la muestra, lo que emula los cambios de tono en otros instrumentos. Las muestras pueden ser cicladas (reproducidas una y otra vez) y one-shot (reproducida una vez).
Sampling Rate (Frecuencia de muestreo)
La frecuencia a la cual un ordenador graba y reproduce sonido, que se mide en Hercios que representan el número de muestras por segundo. Un audio-CD se graba y reproduce a 4#100 Hz (o 44,1 KHz), mientras que un audio-DVD va a 9#000 Hz (96 KHz) y aparatos baratos de consumidor como grabadoras de voz, videojuegos, teléfonos móviles, juguetes y algunos reproductores de MP3 a menudo utilizan una frecuencia de 2#050 Hz (22,05 KHz) o incluso menos. La frecuencia de muestreo determina la frecuencia más alta que puede ser grabada o reproducida, la cual se expresa por el número de Nyquist (la mitad de la frecuencia de muestreo). Reproducir sonidos a una frecuencia de muestreo diferente que a la que fueron grabados resultará en la escucha de un sonido a la "velocidad incorrecta".
Send (Envío) 
Una salida auxiliar opcional para una pista o Bus
Session (Sesión)
Una sesión es toda la información que constituye un proyecto en Ardour. Cada sesión se guarda en su propia carpeta que contiene todo el audio, datos paramétricos y de región, y un archivo maestro con la extensión '.Ardour'.
Shelf (Estante) 
En un Ecualizador, un Shelf (Estante) corta o aumenta todo por encima (High Shelf o Estante Alto) o por debajo (Low Shelf o Estante Bajo) de una frecuencia específica.
Slice Edit (Edición de trozo o Reunir)
Uno del tres Modos de edición disponibles, la edición de trozo (o Reunir) no permite arrastrar regiones alrededor, pero todavía te permite operaciones de trozo (como cortar, pegar, y dividir. El espacio entre las regiones se mantendrá constante tras cualquier operación que lo afecte. Si eliminas la segunda mitad de una región, por ejemplo, cualesquier regiones subsiguientes en la misma pista se moverán automáticamente atrás en la rejilla de tiempo.
Slide Edit (Edición de desliz o Deslizar)
Otro del tres Modos de Edición, la edición de desliz (o deslizar) es el modo por defecto. Te permite arrastrar regiones alrededor horizontalmente (dentro de la misma pista) y verticalmente (entre pistas).
SMPTE timecode (Código de tiempo SMTP) 
Un conjunto de estándares cooperando para etiquetar cuadros individuales de vídeo o película con un timecode (código temporal) definido por la Sociedad de Ingenieros de Cine y Televisión. Los Timecodes (códigos de tiempo) se añaden al material de película, vídeo o audio, y también han sido adaptados para sincronizar música. Proporcionan una referencia de tiempo para la edición, sincronización e identificación.
Snap Mode (Modo de Ajuste)
Los menús de Modo de Ajuste se encuentran justo debajo de los Relojes. Controlan la cantidad Subdivisión de la Rejilla de tiempo, p. ejem.: la cantidad de "ajuste" que una Región audio tiene para el tipo de rejilla que has escogido.
Snapshots (Capturas)
Guardar una captura en Ardour es similar a guardar la sesión a un nuevo fichero para evitar sobrescribir el fichero de sesión original. Una captura contiene el estado actual de tu trabajo, mientras que comparte todo los ficheros de audio y datos de la Sesión. Si estuvieras probando a encontrar una función "guardar como" en Ardour, guardar una captura es probablemente lo que estarías Buscando. 
Solo
Interruptor de conmutación en controles de pista y Bandas de mezcla. Cuando esté encendido, únicamente las pistas en solo enviarán la salida. Se pueden marcar varias pistas como solo al tiempo. El botón general de Solo (fila superior de los controles en la Ventana de Editor) puede utilizarse para quitar el solo de todas las pistas en solo de un único gesto.
Spectrum (Espectro)
La representación de una señal en términos de sus componentes de frecuencia. 
Stereo (Estéreo o Binaural)
Un fichero de sonido estéreo contiene dos canales de audio (normalmente conocidos como canales Izquierdo y Derecho). Una pista estéreo en Ardour tiene dos entradas y salidas, para grabar y reproducir ficheros estéreo.
Stereo Field (Campo estéreo)
El campo estéreo es la percepción de la ubicación espacial de sonidos basada en un sistema de reproducción de sonido de 2 canales (Izquierdo y Derecho).
Take (Toma) [grabación]
Una secuencia de sonido grabada continuamente de una vez.
Tape Mode (Modo de cinta)
Véase Track Mode (Modo de Pista). 
Tempo (música)
La frecuencia a la que un pulso ocurre. Indicaciones Precisas de Tempo se miden en bpm (pulsos por minuto), aunque las indicaciones subjetivas son también comunes en las partituras clásicas (Allegro, Adagio, etc). 
Terminal (Consola) 
Una "terminal" es la interfaz basada en texto que permite operar un ordenador escribiendo órdenes en ella. La mayoría de usuarios de ordenador hoy confían solamente en una interfaz gráfica para controlar sus sistemas. Tanto mac OS como Linux aun así, incluyen una terminal la cual puede hacer algunas tareas más fáciles para algunos usuarios.  
Timecode (Código de tiempo)
Un código de tiempo es una secuencia de códigos numéricos generados a intervalos regulares por un sistema de cronometraje. la familia SMPTE códigos de tiempo es casi universalmente utilizado en producción de películas, vídeos y producción de audio.
Time Signature (Compás) [música] 
Una señal colocada al inicio de una pieza de música (después de la clave y la armadura de clave) o durante el curso de la pieza, indicando el métrica de la música.
Track (Pista) 
Una Pista es el sitio a dónde puedes arrastrar una Región de tu Lista de Regiones y donde puedes grabar los sonidos que provienen una fuente exterior. La Banda de Mezcla representa verticalmente el flujo de señal de una pista, mientras que el Lienzo Principal exhibe horizontalmente información basada en tiempo para cada pista. 
Track Mode (Modo de Pista)
El Modo de Pista te da la oportunidad de escoger entre Modo Normal y Modo de Cinta. El Modo Normal crea una nueva Región para cada Toma de Grabación, mientras Modo Cinta graba destructivamente--en otras palabras la toma previa de la pista es eliminada con cada nueva Toma.
Transport (Transporte) 
Los botones ubicados en la esquina izquierda superior de la Ventana de Editor, con controles como Rebobinar, Reproducir, Paro. 
Treble (Agudo) [frecuencias]
Manera genérica de referirse a las altas frecuencias del Espectro de sonido.
VST (Virtual Studio Technology) [Tecnología de estudio virtual] 
VST es una interfaz para integrar sintetizador audio de software y Plugins de efectos con editores de audio y estaciones digitales tales como Ardour. VST y tecnologías similares utilizan procesamiento de señales digitales para simular aparatos de estudio de grabación tradicional con el software. Existen miles de Plugins, tanto comerciales como freeware. VST fue creado por Steinberg. 
WAV
Un formato de fichero de sonido desarrollado por Microsoft e IBM y comúnmente utilizado para audio sin pérdida y no comprimido. Los ficheros WAV son compatibles con sistemas operativos Linux, mac OS y Windows. <br>
Waveform (Forma de onda)
La representación visual de un sonido en el dominio temporal. Las Waveforms se dibujan dentro de los rectángulos colorados que representan Regiones en el Lienzo Principal.
