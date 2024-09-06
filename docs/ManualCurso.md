[Inicio](./index.html)

* [Configurando el sistema](#configurando-el-sistema)
* [Lección 1 – LabVIEW “Hello World” LED On/Off](#lección-1--labview-hello-world-led-onoff)
* [Lección 2 – Ciclos For (For Loops)](#lección-2---ciclos-for-for-loops)
* [Lección 3 – Ciclos While (While Loop)](#lección-3---ciclos-while---while-loops)
* [Lección 4 – Estructura de Eventos (Event Structure)](#lección-4---estructura-de-eventos---event-structure)
* [Lección 5 – Números, Gráficas y Tablas](#lección-5---números-gráficas-y-tablas)
  * [Entrada Analógica (Analog Input)](#entrada-analógica-analog-input)
  * [Salida Analógica (Escribir) (Analog Output (Write))](#salida-analógica-escribir-analog-output-write)
  * [Salida Analógica (Leer) (Analog Output (Read))](#salida-analógica-leer-analog-output-read)
* [Conceptos Generales](#conceptos-generales)
  * [VIs (Virtual Instruments) (Instrumentos Virtuales)](#vis-virtual-instruments-instrumentos-virtuales)
  * [Tipos de Datos](#tipos-de-datos)
  * [Ciclos While - While Loops](#ciclos-while)
  * [Ciclos For - For Loops](#ciclos-for)
  * [Estructuras de Eventos - Event Structures](#estructuras-de-eventos)

## Configurando el sistema
[Instrucciones para tutor](./InstruccionesTutor.html)

Para usar el emulador, clona el repositorio y cargalo navegando a /root/Desktop/GettingStartedLabVIEW1-Spanish-main/3) LabVIEW Instrument Emulator/builds/HandsOn/CTIPicoVISAEmulator/

Da click derecho y selecciona ‘Open Terminal Here’

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9edd704c-c81b-4c34-a92f-416af763ec48)

Escribe lo siguiente: 

>./CTIPicoVISAEmulator.exe

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/f644fde9-b481-48f4-b450-e48bac99970a)

El emulador te pedirá elegir una subred.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/159f16c4-16f9-4530-b841-644f0cbbf5ad)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3b293499-a5ea-4dd9-b082-2c3e08ba427c)

Después simplemente esperará por una conexión. “Connecting” será mostrado en la barra de estado.

# Lección 1 – LabVIEW “Hello World” LED On/Off

**Opcional**: Configurando el Hardware 

Si tienes el hardware para este curso, necesitaras configurarlo y conectarlo como lo muestra la siguiente imagen. Si no, avanza a Instrucciones.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/19efa352-e5e0-420e-9437-6cefb5fb1a49)

## Instrucciones

El equivalente en LabVIEW de un programa “Hello World” es hacer que una pieza de hardware haga algo básico, usualmente es hacer un led parpadear (ON-Off).
Arranca LabVIEW y selecciona New VI.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4c3341c5-da7e-45ad-b18c-0185f6f0bbcf)

Acomoda las ventanas de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/7350d66a-f07d-4169-ac20-ded705dd28cd)

En LabVIEW un VI (Virtual Instrument) es el equivalente a una función o un módulo en otros lenguajes de programación. Un programa en LabVIEW esta hecho por uno o mas VIs.

En el diagrama de bloques (Block Diagram) da click derecho y navega a HandsOnPi2040 Driver Palette.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/bd6141e9-356a-44bc-8179-4b56c5abcde3)
      
Arrastra el VI Initialize.vi, WriteDO.vi y Close.vi en el diagrama de bloques como se muestra a continuacion.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/142dd1d1-fb9d-4c31-b3b4-c04780d127ff)

*Observa que la flecha para ejecutar esta rota (esta flecha está en la esquina superior izquierda), si la presionas, la ventana de errores aparecerá y vendrán todas las razones por las cuales no se puede ejecutar el código.*

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4e371803-0d24-445c-958a-ec8414309aab)

LabVIEW no le permitirá ejecutar el código fuente hasta que se solucionen estos errores. Cierre la Lista de errores y seleccione todos los Vis. (Haga clic con el botón izquierdo y arrastre el mouse).

Seleccione los tres subVIs que están en el diagram de bloques.
Presione 'Ctrl+Espacio' para abrir 'Quick Drop' y presione 'Ctrl+W' para conectar los VIs. Quick drop es una herramienta de productividad extremadamente útil que viene con LabVIEW. Le permite automatizar tareas repetitivas con algunas combinaciones de teclas. Si los subVIs no se conectan es porque no los seleccionó antes de activar 'Quick Drop'.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b09151fb-88f6-4823-922d-639e41c5ae2a)

*Si presiona la flecha Ejecutar, notará que solo hay 2 problemas enumerados, ¡buen trabajo!*

Presione Ctrl-H para abrir la ventana de ayuda contextual. Pase el cursor sobre Initialize.vi.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/2b384f7c-d2fa-4ee6-9652-e3cd71acd2af)

*Observe que algunas entradas estan en **negrita**, como **'Visa Resource Name'**. Esto significa que esta entrada es obligatoria.*

Haga clic derecho en 'VISA Resource Name' del VI Initialize.vi y seleccione 'Create Constant'.

*Si presiona la flecha Ejecutar ahora, notará que solo queda 1 error a resolver.*

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c9299b51-d207-4239-95fd-ef3d75db44e4)

Este VI necesita su cableado de salida y valor DO (verdadero). Así que creemos constantes para ellos. Utilice la flecha de la derecha para seleccionar una salida

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/1000353a-eb6f-4a4b-af81-35b8e72f4637)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e716a2d7-111b-4a47-aadd-653b44fc29bf)

Es bueno que se muestre la etiqueta constante para los booleanos.

Haga clic derecho en la constante booleana "True". Aparecerá una ventana desplegable, coloque el cursor sobre "Visible Items" y seleccione "Label".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/54096500-f600-452a-b244-107407c492ae)

Las constantes son terminales en el diagrama de bloques que suministran valores de datos fijos al diagrama. Discutiremos los tipos de datos, etc. más adelante en la sesión.

Finalmente conectemos un par de salidas.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/cf6d9b82-d9f4-432e-b8c4-a58dc475ac3e)

Haga clic derecho en IDN para Initialize.vi y seleccione "Create Indicator". Luego necesitamos eliminar un error, así que haga clic derecho en la parte inferior de Close.vi y seleccione "Create Indicator".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/52586b53-ab80-4d8b-a49f-35b1f0e1a3da)

*Observe cómo aparecen los indicadores en el panel frontal. Discutiremos los diagramas de bloques y los paneles frontales en un momento.*

¡Ahora tenemos un programa listo para ejecutar!

Sin embargo, notarás que tendremos un error.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/7908dc72-b056-470f-b530-332540ef524c)

Podemos consultar el mensaje de error para intentar obtener una pista de por qué todo salió tan mal. A veces incluso puede resultar útil.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/062e5d5b-1a24-4af7-b5aa-cdafeef3ff3d)

En este caso, lo es!

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/74f37f12-a5fd-49bd-ab48-0a0f6dd83108)

Los VIs no saben con qué hardware están vinculándose. Para solucionar este problema, los usuarios de hardware deben configurar la referencia VISA correcta en el cuadro desplegable 'VISA'. Para los usuarios del emulador, haga clic en el botón 'Copy', como se ve en la imagen a continuación y pegue la referencia, si tiene hardware apriete el botón de 'Refresh' y seleccione la referencia ASRL. 

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ff03d635-6c29-474a-83ce-bdf153fab323)

Ahora, presione 'Run' nuevamente

El indicador de error mostrará que no hay error, el indicador de identidad habrá cambiado y ahora despliega valores.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5c2570bb-2497-4d50-9b4f-670e6ed637f1)

Pero, algo mas importante es que el LED del hardware se ha encendido!

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/465b4cdf-0aa2-4014-92a6-4eab1eb42a3c)


# Lección 2 - Ciclos For (For Loops)
Opcional: Configuración de Hardware

Conecte el hardware como la imagen siguiente:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/55b91ce8-3c9b-4bb9-8082-a911e74e7275)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ab4506dc-f5f3-4008-a3b9-03123cd26ebf)

## Instrucciones

Un ciclo For ejecuta un sub-diagrama un número determinado de veces. En este caso, aprenderás a construir un programa que hace parpadear un LED 10 veces antes de detenerse.

Agrande su espacio de trabajo para dejar espacio para agregar objetos. Utilice Ctrl y luego arrastre para expandir.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/484becac-5d71-445e-90b0-37525819cead)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c7ebdddb-80e6-43cc-a645-2c6b2acd05d9)

Alternativamente, seleccione los objetos que necesita mover con la herramienta de selección y arrástrelos a donde desee con el mouse o usando las flechas.

__Nota: presione Mayús y una tecla de flecha para mover los elementos seleccionados más rápido.__

Ahora inserte un ciclo For: para hacerlo, haga clic derecho en cualquier lugar del diagrama de bloques para abrir la paleta de funciones. Seleccione 'Structures' y luego 'For Loop'.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fcb44595-01e3-49f8-ac4f-7bbb2802f783)

Sólo necesitará colocar el ciclo For alrededor del WriteDO SubVI (y las constantes adjuntas a él).

Una vez que se haya colocado el ciclo For, verá una 'N' en la esquina superior izquierda, este es el número de iteraciones que realizará el ciclo For.

Haga clic derecho en la N y seleccione "Crear una constante". Para esta tarea necesitará que el número de bucles sea 20 (10 veces activado y 10 veces desactivado).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/414e694a-ae63-41e2-a36a-63e4354bbe9b)

Para que el programa "parpadee" correctamente, necesitará saber qué se ha ejecutado en la iteración anterior, por lo que necesitará un registro de desplazamiento (Shift Register).

Haga clic derecho en el borde del ciclo For y seleccione "Add Shift Register". Conecte la constante verdadera a los registros de desplazamiento y al terminal del cable DO (valor).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e7da0c07-5417-48a3-b640-e2e671d020ad)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/28a02b6e-76f8-47d5-ac87-b2f6834763ae)

_Si ejecutara el programa en este punto, el LED se iluminaría, pero no "parpadearía"._

Para un LED parpadeante necesitarás invertir el valor booleano después de cada iteración. Para hacer esto, haga clic derecho en cualquier lugar para abrir la paleta de funciones. Pase el cursor sobre "Booleano" y luego seleccione el booleano "Not". Conecte esto al registro de desplazamiento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/790e2351-196b-4504-8a31-4beed7c9c29b)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fddc4fb2-9e21-4835-b9d7-37538c2a42da)

¡El programa ahora funcionará! Sin embargo, se ejecutará muy rápido y no podrá ver el LED parpadeando, por lo que necesitas reducir la velocidad del ciclo.

Haga clic derecho dentro del ciclo For y coloque el cursor sobre "Timing". Allí verá muchas opciones de tiempo diferentes. Para ello utilizarás la función 'Wait (ms)'. Seleccionala y coloca dentro del bucle.

Cree una constante haciendo clic derecho en el lado izquierdo de la función "Wait (ms)". La función "Wait (ms)" se ejecuta en milisegundos, por lo tanto, para ralentizar el ciclo medio segundo, escriba 500.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b4139bcd-b996-4248-a196-99a3b79d2572)

Ahora ejecute el programa. Ha utilizado con éxito un ciclo For para hacer parpadear la salida digital.

# Lección 3 - Ciclos While - While Loops

Opcional: Configuración del Hardware
Conecta el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/d5d6d0d4-3271-40d3-b116-08c1402f5202)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/de741e88-970b-4f3c-8d0d-307193177107)



## Instrucciones

El ciclo While ejecuta el subdiagrama hasta que ocurre una condición específica. Siempre se ejecutará al menos una vez.

En este caso, deseamos que el LED parpadee continuamente hasta que se presione el botón "Stop". Puede crear esto utilizando el programa creado previamente con el ciclo For.

En primer lugar, haga clic derecho en el borde del ciclo For y seleccione "Replace with While Loop".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e46e9a0c-a3d8-4d65-8921-88aa0e509a8c)

Ahora que el ciclo For ha sido reemplazado, el Loop Count (N) no está conectado. Esto no es necesario para un ciclo While y se puede eliminar.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/2d510608-2133-4bdd-b4fb-84f7318bafa7)

Para agregar un booleano 'Stop', cambie a la ventana del panel frontal y haga clic derecho donde desea colocar el botón. Aparecerá la paleta "Controls", seleccione "Boolean" y elija un botón. El ejemplo utiliza un "botón pulsador" (Push Button), pero cualquiera funcionará.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4a82db62-590e-4cb7-b686-78641c159c9a)

De vuelta en el diagrama de bloques, mueva el nuevo control booleano al ciclo While y conéctelo al terminal condicional en la esquina inferior derecha. Si se presiona el botón en el panel frontal cuando el programa se está ejecutando, el bucle finalizará y el LED "parpadeante" se detendrá.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b342eea4-0fb3-4e38-b6b3-0285ed0a56c4)

## Ejercicio - Uso de entradas digitales (DI) para detener el ciclo While
__Pista: Diagrama de cableado para entrada digital__

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5b8ede3a-05b2-4cb2-ac67-4036c2f412d3)

__Pista: VI para entrada digital (DI)__

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/54f52bc0-7a5e-4f27-b68c-5fb68d4cdade)

# Lección 4 - Estructura de Eventos - Event Structure

Opcional: Configuración de Hardware
Conecte el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3dd90791-c8ab-4f77-8387-0f2b7a896ca3)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/bfba31c3-231d-44f0-852b-3f20378f4bf3)

## Instrucciones

Una estructura de eventos espera hasta que ocurra un determinado evento y luego ejecuta el caso apropiado para manejar ese evento. En este ejemplo, queremos presionar un botón y la luz correspondiente para encenderla.

Primero, eliminemos el ciclo while y su contenido. Haga clic en el bucle While y presione la tecla Eliminar. Haga lo mismo con la constante "True". Luego retire los cables rotos con Ctrl+B

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9b7012b5-e34c-4e5f-b87e-6476fc6177fc)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/db1f0425-07d1-4ba5-97cd-6980df33df38)

Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Structures" y luego seleccione "Event Structure". Coloque la estructura de eventos en el diagrama de bloques

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/622c01a2-39d0-48ce-91f0-fa433fee8706)

Conecte el VI Initialize.vi y el VI Close.vi a través de la Estructura del Evento

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5f2b924e-e26b-452e-824d-c8fa1420b310)

Agregue un nuevo caso de evento haciendo clic derecho en la etiqueta del selector y seleccione "Add Event Case".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/eabaf06e-5cef-4096-bd08-cc7a2040c960)

Agregue WriteDO.vi abriendo la paleta de funciones, coloque el cursor sobre "Instrument I/O", "Instr Drivers", "HandsOnPi2040" y seleccione "WriteDO.vi".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ffc7cfce-a9b2-415b-9a74-0ce61016a1a6)

Arrastre el sub VI dentro de la estructura del evento y conéctelo. Haga clic derecho en la terminal de "Output" y cree una Constante.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/83968bae-93f4-404d-87b1-f2b8b2fd1b79)

Cambie la salida de "NO DO - Error" a "DO1" haciendo clic en la flecha desplegable en la constante de salida.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/46e9732c-15a8-47b2-b1e7-172c74becddb)

A continuación necesitamos agregar un botón para la Salida Digital. Vaya al Panel Frontal y haga clic derecho en cualquier lugar para abrir la Paleta de Controles. Pase el cursor sobre "Boolean" y seleccione "Push Button"

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/6f69a3fb-3296-474f-b7a6-3ab3a3e7bf20)

Conecte el nuevo control booleano al terminal 'DO Value'

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3d3a1c4a-8979-4b19-a65d-90c390ca4e29)

Haga clic derecho en el selector de etiquetas, y seleccione "Edit Events Handled by This Case", pues necesitamos editar los eventos manejados por cada caso.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/f4f668c1-ad34-45ca-be7a-d92124c4b1ba)

Esto abrirá la ventana "Edit Events". Seleccione "Boolean".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/77a94469-75c5-4d39-b9bb-dcdc7aa75e91)

Este caso de evento ya está completo. Necesitaremos 3 Casos de Eventos más, cada uno correspondiente a un LED. La forma más sencilla de hacerlo es hacer clic derecho en el selector de etiquetas y seleccionar "Duplicate Event Case".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9058f9cc-ad66-4707-a9c7-7d1d55892312)

Seleccione 'Boolean 2' en la ventana de "Edit Events" (Editar eventos).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/a6e7bdbb-ad83-40ad-b8b5-3adae35cf8f7)

Es importante cambiar la constante DO cuando el caso se ha duplicado. (DO1 para booleano, DO2 para booleano 2, etc.) Duplique este caso 2 veces más para DO3 y DO4.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/33ec6534-b6e1-4cf1-a0f9-b14acec732cb)

En este punto, su panel frontal puede verse un poco desordenado; tómese un tiempo para limpiarlo. Esto hará que sea más fácil de usar cuando haya terminado de crear el programa.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/984b7c28-6b73-4b47-a326-5f7b30bed4c2)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/03847edd-1889-430e-afbd-e0cdfda0db37)

_Podrá ejecutar el programa ahora; sin embargo, se detendrá después de seleccionar un valor booleano. Podemos hacer esto más eficiente._

De vuelta en el diagrama de bloques necesitaremos agregar un ciclo While. Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Structures" y seleccione "While Loop"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/d3604cb7-e7ce-4c32-abdd-4993d1bf80b1)

Coloque el ciclo While alrededor de la estructura del evento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/559b21af-6ef2-4398-9058-435afdab1dca)

Vaya al Panel frontal, para que podamos agregar un botón "Stop" que conectaremos a la condición del ciclo. Haga clic derecho para abrir la paleta de controles, coloque el cursor sobre "Boolean" y luego seleccione "Stop Button".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/63692026-a3d4-4e5f-8fbe-e911a3f4c46e)

También necesitaremos crear un nuevo Caso de evento para este botón de "Stop". Haga clic derecho en la etiqueta del selector y seleccione "Add Event Case".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/70c38ba9-6c0a-4dcb-b640-d057b698e3dc)

Coloque el control "Stop" dentro del nuevo caso.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/574509f2-1b65-4303-af13-b9004b119784)

Haga clic derecho en la etiqueta del selector y seleccione "Edit Events Handled by This Case"


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b850954f-9a5d-4865-ae39-305abdebcbbd)

Cuando aparezca la ventana "Edit Events", elija la opción "Stop" en la tabla de "Event Sources".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/960609b9-c1bf-4461-8a4a-72715f34399d)

Nuestro último paso es conectar una constante "True" a la condición de ciclo. Haga clic derecho para abrir la paleta de funciones, coloque el cursor sobre "Boolean" y seleccione "True Constant". 
Coloque la Constante dentro de la Estructura del Evento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/dc46242b-379b-40d7-9e69-860070f1752a)

Conecte la constante a la condición de ciclo, como se muestra en la imagen a continuación.


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/3fdd8ba7-f668-414c-a42d-b2a7b8b8797f)


El programa ahora se ejecutará exitosamente. Podrá encender y apagar los LED tantas veces como quieras. Puede utilizar el botón Stop para detener la ejecución del programa.

# Lección 5 - Números, Gráficas y Tablas

Opcional: Configuración del Hardware

Conecte el hardware de la siguiente manera:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/97fc78a9-7876-422d-b74a-c75400bb1ffb)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/4d478f5a-b4c3-4f98-84bd-672c19c3b992)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e2a09693-e729-4f72-b7af-9d67f6fa4efd)

## Instrucciones

### Entrada Analógica (Analog Input)

Hasta ahora has realizado programas usando entradas y salidas digitales, es momento de revisar las entradas y salidas analógicas. En esta lección nos enfocaremos en las entradas analógicas

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/f3772781-e5db-459d-a3c1-fc9bf1694eba)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/4bb4c9f0-a99d-4d62-ad71-b2231c1796c4)

De igual manera que las lecciones anteriores, hay que comenzar con los VIs Initialize.vi y Close.vi en un nuevo diagrama de bloques (Block Diagram).

De click derecho para sacar la paleta de funciones (Functions Palette). Revisa la siguiente imagen para ubicar el VI ReadAI.vi y coloca el VI en el diagrama de bloques.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e9606dd8-840e-4f37-aea6-ce94b8eeed83)

Hay que conectar una constante dando click derecho en el VI ReadAI.vi y seleccionando 'Create Constant'.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/0a50edff-593b-4fb6-aec7-7740e40c36f4)

Crea un indicador para el valor analógico en el lado derecho del VI.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/9f993dd9-e3f4-402b-94bf-2344cdac3703)

Escribe el programa como la siguiente imagen.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/08b24200-3beb-475f-8bd2-2212003820e8)

_El programa se ejecutará exitosamente, pero se ejecutará una sola vez, obteniendo solo una lectura del canal analógico seleccionado._

Para resolver este problema, podemos agregar un ciclo While. Da click derecho para abrir la paleta de funciones, luego navega a 'Structures' y selecciona 'While Loop'. Colócalo alrededor de el VI ReadAI.vi y deja espacio para otras funciones.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/60952926-50fc-49d2-8053-e6e6154ae2d2)

Un ciclo While no funcionara sin una condición de paro. En muchos casos se utiliza un simple botón de "Stop" boleano, da click derecho en la condición de paro del While loop y selecciona 'Create Control', esto creara un boton en el panel frontal

_Esto añadirá automáticamente un "Stop" booleano en el panel frontal._

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e0016811-c6ed-4a52-9506-641d6eff7be3)


![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/c6d726ba-6fed-4946-a9eb-ba4b943fa0ed)

Puedes ejecutar el programa ahora y, al girar las perillas analógicas, el valor se mostrará en el panel frontal.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/e9b586b6-9b3f-4b26-a7fb-a0f1f894cdc9)

_Si estas utilizando el hardware fisico, notaras que el valor analógico leído estará brincando de un valor a otro, esto es hasta cierto punto normal y está relacionado al ruido electromagnético en el equipo._

Sin embargo, también es posible reemplazar el indicador numérico por un Waveform Chart, el cual desplegará los datos de manera continua. Da click derecho en el indicador 'Value', y navega hasta la opcion de reemplazar, aparecera la paleta de controles y ahi podras elegir un Waveform Chart.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/492827a5-558b-4301-a19c-5581588ef463)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/5545396/ad605cde-82e2-493c-a794-9fafdda85b73)

### Salida Analógica (Escribir) (Analog Output (Write))

Opcional: Configuración del hardware

Conecte el hardware de la siguiente manera:

![hardware11](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/e2d09cf8-9d9a-42c6-856b-ab1556fd6501)

![hardware12](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/2a85e681-fe25-4d1a-82bb-7e160b9e881f)

Comienze con un diagrama de bloques con Initialize.vi y Close.vi. Haga clic derecho para abrir la Paleta de Funciones. Siga la imagen a continuación y agregue WriteAO.vi al diagrama.

![write1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/806f357a-c6ef-487e-a211-d32d1ecb2c60)

Conecte los 3 VIs entre sí.

Haga clic derecho en la terminal 'Analog Output' y cree una constante. Para este ejercicio, la salida analógica producirá 2 datos numéricos diferentes, por lo tanto, 2 constantes se agruparán. 

![write2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/d71933c7-da7a-4e58-bdc8-7773d214ca9b)

Necesitará crear un Paquete (Bundle). Haga clic derecho en el diagrama de bloques para abrir la Paleta de Funciones, coloque el cursor sobre 'Cluster, Class & Variant', luego seleccione 'Bundle By Name'.

![write3](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/d49d8f5d-0a68-44a1-a12f-3e17cac1d461)

Elimine el cable conectado al subVI, ya que necesita conectarse al paquete que construyó anteriormente.

![write4](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/81585f55-4a2a-4b66-9097-0ac6f67d814b)

Cablee el paquete como se muestra en la siguiente imagen.

![write5](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/c5711d42-5879-4ace-9fdb-e20bf23b98b4)

Una vez conectado el paquete, notará que el paquete tiene la etiqueta "Duty". Expanda el paquete hacia abajo para que la etiqueta "Frequency" sea visible.

![write6](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/ff8dc898-363e-48aa-a6a4-eb1a6d3dbff8)

Haga clic derecho en el borde del paquete y cree Constantes para "Duty" y "Frequency".

![write7](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/72a13f73-9f4b-482f-bc20-ad30f1928b17)

El panel frontal debería verse como la imagen a continuación. Sin embargo, aún necesita algunos ajustes.

![write8](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/d9268383-5320-4de1-bf40-1e675201983b)

_Usar el "Control numérico" (Numeric Control) puede resultar un poco complicado cuando se ejecuta el programa, por lo que en este caso los cambiará por "Desplazamientos de puntero vertical" (Vertical Pointer Slides)._

Haga clic derecho en el control "Duty" y coloque el cursor sobre "Replace". Seleccione "Numeric" y luego "Vertical Pointer Slide". Haga lo mismo con el control "Frequency".

![write10](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/00963db7-38ae-4916-96ec-c074afe94d62)![write9](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/33b8cfdb-92c3-4b5b-9cdc-c89ddb3aba57)

Deberá cambiar la escala del control deslizante "Frequency". Haga clic derecho en el control deslizante, seleccione "Scale", "Mapping" y luego "Logarithmic".

![write11](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/e097f68b-d8e1-4144-856a-cf09751952cd)

_Una escala logarítmica es útil cuando los datos que se muestran son mucho menores o mucho mayores que el resto de los datos, o cuando las diferencias porcentuales entre valores son importantes._

El control deslizante "Duty" puede permanecer como una escala lineal.

![write12](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/5c6eb014-cdea-4bc6-a8fc-3baad338e7fb)![write13](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/0f4d6492-d187-4df0-a581-0b68276cf47c)

Ahora necesita configurar los puntos superiores e inferiores en los controles deslizantes. Sólo necesitará cambiar el punto más alto por 'Duty'. Configúrelo en '1'.
Para "Frequency", el punto más bajo debe ser "10" y el más alto "500,000".

_Ahora volvamos al diagrama de bloques y terminemos de construir el programa._

Abra la paleta de funciones haciendo clic derecho en el diagrama de bloques, coloque el cursor sobre 'Structures' y seleccione un ciclo For. Coloque el ciclo For alrededor de WriteAO.vi.

![write14](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/e207a1ad-bc2b-40c0-9651-b2b032caa5fe)

Un ciclo For necesita un 'Conteo de ciclos'. Elija un número que le permita usar los diales y ver cómo se ejecuta en el Waveform Chart.

![write15](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/7fcf0539-ec42-4861-bbb5-87d72b85ffa3)

Necesitará reducir la velocidad del programa antes de ejecutarlo. Abra la paleta de funciones, seleccione "Timing" y coloque la función "Wait (ms)" dentro del ciclo For.

![write16](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/3fa4a826-595b-4207-8842-1a3ccf7fdd91)

Haga clic derecho en la terminal izquierda en la función "Wait (ms)" y cree una Constante. Escriba "100". Esto ralentizará el programa lo suficiente como para que pueda ver los resultados.

![write17](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/79899d6c-3548-468b-aacc-bfba6d7678bc)

Ahora puede ejecutar su programa. Mueva los controles deslizantes hacia arriba y hacia abajo y los resultados se mostrarán en el emulador.

![write18](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/92fa3eaa-9ea6-4e79-aa5a-8f9eeaa4b309)


### Salida Analógica (Leer) (Analog Output (Read))

Si desea una representación más precisa de los controles deslizantes "Duty" y "Frequency", puede utilizar ReadAOs.vi.

Coloque ReadAOs.vi dentro del ciclo For repitiendo el mismo proceso que aprendió al comienzo de la lección 'Analog Ouput (Write)'.

![read1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/7f04b95c-2b29-44c6-91de-59639af2ac97)

Conecte el subVI como se muestra en la imagen a continuación. Haga clic derecho en la terminal 'AnalogOutput' y cree una constante, luego cree un indicador para 'AnOutValues'.

![read2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/531043f8-d2c0-4c48-a370-1b3f8ae97365)

Ahora puede ejecutar el programa y verá los valores de "Duty" y "Frequency" en el Panel Frontal.

![read3](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/72a8623e-cab4-4cb7-a0bb-db045d896c4b)

_Si está utilizando el Simulador, los valores de ambos aparecerán en el Emulador._

![read4](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/ad7fac14-7f47-4e37-ac02-209410818c0f)


# Conceptos Generales

## VIs (Virtual Instruments) (Instrumentos Virtuales)

Los programas en LabVIEW se denominan VI (Instrumentos virtuales). En otros lenguajes de programación, un VI es similar a una función o una subrutina. Un VI incluye un Panel Frontal y un Diagrama de Bloques, el ícono del VI y su Panel de Conectores.

### Panel Frontal

La ventana del panel frontal es la interfaz de usuario del VI. Usted crea la ventana con controles e indicadores, estos son los terminales interactivos de entrada y salida del VI.

### Diagrama de Bloques

El diagrama de bloques es donde creará el código para su programa. El diagrama de bloques implementará representaciones gráficas de funciones para controlar los objetos en el panel frontal. Los objetos en el panel frontal aparecerán como terminales en el diagrama de bloques.

### Íconos, Panel de Conectores, y SubVIs

El ícono y panel de conectores le permite usar y ver el VI en otro VI. Esto se llama SubVI; para utilizar un SubVI debe crear un panel conector. Se recomienda personalizar el ícono para ayudar a leer y comprender el programa.

* El ícono se muestra en la esquina superior derecha del VI, es una representación gráfica del VI. El ícono se puede personalizar con texto e imágenes para ayudar a identificar lo que hace el VI.

* El panel de conectores es un conjunto de terminales en el ícono que corresponde a los controles e indicadores del VI.

Ícono

![icon1](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/565f97eb-39d3-45c6-a4e7-9859697ebd75)

Panel de Conectores

![icon2](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/2b383660-8e69-492e-b5f2-3a9884b9e0ba)

## Tipos de Datos

Cada variable de un programa debe tener un tipo de datos. Los tipos de datos determinan qué tipo de valor contendrá la variable.

Los tipos de variables son los siguientes:

* Numéricas:
  * Entera (int) - números enteros (por ejemplo, -700, 0, 700).
  * De punto flotante (float) - números con fracciones o decimales (por ejemplo, 700.0, 0.7).
* Booleana - representa dos estados (por ejemplo, verdadero o falso, 1 o 0).
* Texto (String) - secuencia de caracteres, dígitos y símbolos - siempre tratado como texto (por ejemplo, 'hola').
* Tipo enumerado - valores únicos predefinidos (pueden ser números o textos) (por ejemplo, rock (0) jazz (1)).
* Carácter - una sola letra, dígito, signo de puntuación, símbolo o espacio en blanco.
* Arreglo - almacena múltiples elementos en un orden específico. Nota: negro significa que no se seleccionó ningún tipo de datos. Coloque otro tipo de datos en la matriz para crear una matriz de ese tipo de datos.

![data_types](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/e5dabf86-4dfb-4ac6-b5a6-ddcc5a4d5e2f)

_Nota: haga clic derecho en un terminal de tipo de datos y seleccione 'Ver como icono' según su preferencia. (La segunda fila muestra los terminales como iconos)._

## Ciclos While

Los ciclos While permiten que partes de un programa se ejecuten repetidamente hasta que se cumpla una determinada condición.

![whileloop](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/bcdcfa2e-3570-403c-ace4-bf011538f566)

1. Terminal de Iteración - la terminal de iteración provee la iteración del ciclo actual
2. Terminal Condicional - evalúa un valor de entrada **booleano** al final de cada iteración del ciclo, si la terminal condicional se cumple entonces el ciclo termina.

## Ciclos For

Un ciclo For ejecuta un subdiagrama un determinado número de veces. Este valor está conectado al terminal de conteo (N).

![forloop](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/db48ddca-3500-4775-86c7-40626695c42d)

1. Ciclo de Iteración - indica el número de iteraciones completadas
2. Terminal de Conteo - Especifíca el número de veces que se ejecutará el código dentro del ciclo For

## Estructuras de Eventos

Una estructura de eventos espera a que un evento ocurra, y luego ejecuta el caso apropiado para manejar ese evento.

![eventstr](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Spanish/assets/170447709/7793640a-caf6-46ca-918a-ee7bfc2b0f08)

1. La etiqueta del selector de eventos especifica qué eventos hacen que se ejecute el caso mostrado.
2. Las terminales de tiempo de espera especifican el número de milisegundos que se deben esperar por un evento antes de que se agote el tiempo.
3. El Nodo de Datos del Evento identifica los datos que LabVIEW devuelve cuando ocurre un evento.



























