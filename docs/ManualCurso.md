# Manual del curso

[Inicio](./index.html)


# Tabla de contenido
* Configurando el sistema
* Lección 1 – LabVIEW “Hello World” LED On/Off
* Opcional: Configurando el Hardware
* Lección Instrucciones
* Lección 2 – Ciclos For (For Loops)
* Opcional: Configurando el Hardware	
* Lección Instrucciones	
* Lección 3 – Ciclos While (While Loop)
* Opcional: Configuración de Hardware	
* Lección Instrucciones	
* Exercise – Uso de entradas digitales para detener un ciclo	
* Lección 4 – Estructura de Eventos (Event Structure)	
* Opcional: Setting up the Hardware	
* Lección Insrucciones	24
* Lección 5 – Numeros, Graficas y Charts	
* Opcional: Configurando el Hardware (Analog input)	
* Lección Instrucciones	
* Entrada Analógica	
* Salida Analógica (Write)	
* Opcional: Configuración del Hardware (Salida Analógica)	
* Analog Output (Read)	
* Conceptos Generales
* VIs (Instrumentos Virtuales - Virtual Instruments)	
* Tipos de Datos	
* Ciclos While - While Loops	
* Ciclos For - For Loops	
* Estructuras de Eventos - Event Structures	

Configurando el sistema
[Instrucciones para tutor](./InstruccionesTutor.html)
* Si estas usando el emulador, cargalo navegando a /root/Desktop/GettingStartedLabVIEW1-Spanish-main/
Emulador de instrumento en LabVIEW/builds/HandsOn/CTIPicoVISAEmulator/
* Da click derecho y selecciona ‘Open Terminal Here’
    ![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/9edd704c-c81b-4c34-a92f-416af763ec48)

* Escribe lo siguiente: 
./CTIPicoVISAEmulator.exe
![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/f644fde9-b481-48f4-b450-e48bac99970a)

* El emulador te pedirá elegir una subred.
![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/159f16c4-16f9-4530-b841-644f0cbbf5ad)
![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/3b293499-a5ea-4dd9-b082-2c3e08ba427c)


* Después simplemente esperará por una conexión. “Connecting” será mostrado en la barra de estado.

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

* En el diagrama de bloques (Block Diagram) da click derecho y navega a HandsOnPi2040 Driver Palette.
    ![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/bd6141e9-356a-44bc-8179-4b56c5abcde3)
      
* Arrastra el VI Initialize.vi, WriteDO.vi y Close.vi en el diagrama de bloques como se muestra a continuacion.
    ![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/142dd1d1-fb9d-4c31-b3b4-c04780d127ff)

*Observa que la flecha para ejecutar esta rota (esta flecha esta en la esquina superior izquierda), si la presionas, la ventana de errores aparecera y vendran todas las razones por las cuales no se puede ejecutar el codigo.*

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/4e371803-0d24-445c-958a-ec8414309aab)

__LabVIEW no le permitirá ejecutar el código fuente hasta que se solucionen estos errores. Cierre la Lista de errores y seleccione todos los Vis. (Haga clic con el botón izquierdo y arrastre el mouse).__

Presione Ctrl+espacio para abrir 'Quick Drop' y presione 'Ctrl+W' para conectar los VIs. Quick drop es una herramienta de productividad extremadamente útil que viene con LabVIEW. Le permite automatizar tareas repetitivas con algunas combinaciones de teclas.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b09151fb-88f6-4823-922d-639e41c5ae2a)


Si presiona la flecha Ejecutar, notará que solo hay 2 problemas enumerados, ¡buen trabajo!

Presione Ctrl-H para abrir la ventana de ayuda contextual. Pase el cursor sobre Inicializar.vi.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/2b384f7c-d2fa-4ee6-9652-e3cd71acd2af)


Observe que algunas entradas estan en negrita como 'Visa Resource Name'. Esto significa que esta entrada es obligatoria.

Haga clic derecho en 'VISA Resource Name' del VI Initialize.vi y seleccione crear constante.

Si presiona la flecha Ejecutar ahora, notará que solo queda 1 problema.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c9299b51-d207-4239-95fd-ef3d75db44e4)

Este VI necesita su cableado de salida y valor DO (verdadero). Así que creemos constantes para ellos. Utilice la flecha de la derecha para seleccionar una salida.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/1000353a-eb6f-4a4b-af81-35b8e72f4637)
![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e716a2d7-111b-4a47-aadd-653b44fc29bf)

Es bueno que se muestre la etiqueta constante para los booleanos.

Haga clic derecho en la constante booleana "Verdadera". Aparecerá una ventana desplegable, coloque el cursor sobre "Visible Items" y seleccione "Label".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/54096500-f600-452a-b244-107407c492ae)

Las constantes son terminales en el diagrama de bloques que suministran valores de datos fijos al diagrama. Discutiremos los tipos de datos, etc. más adelante en la sesión.

Finalmente conectemos un par de salidas.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/cf6d9b82-d9f4-432e-b8c4-a58dc475ac3e)

Haga clic derecho en IDN para Inicializar.vi y seleccione "Create Indicator". Luego necesitamos eliminar un error, así que haga clic derecho en la parte inferior de Close.vi y seleccione "Create Indicator".

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/52586b53-ab80-4d8b-a49f-35b1f0e1a3da)

Observe cómo aparecen los indicadores en el panel frontal. Discutiremos los diagramas de bloques y los paneles frontales en un momento.

¡Ahora tenemos un programa listo para ejecutar!

Sin embargo, notarás que tendremos un error.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/7908dc72-b056-470f-b530-332540ef524c)

Podemos consultar el mensaje de error para intentar obtener una pista de por qué todo salió tan mal. A veces incluso puede resultar útil.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/062e5d5b-1a24-4af7-b5aa-cdafeef3ff3d)

En este caso el problema es...

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/74f37f12-a5fd-49bd-ab48-0a0f6dd83108)

__Los VIs no saben con quién están hablando. Para solucionar este problema, los usuarios de hardware deben configurar la referencia VISA correcta en el cuadro desplegable 'VISA'. Para los usuarios del emulador, haga clic en el botón 'Copiar', como se ve en la imagen a continuación y pegue la referencia, si tiene una actualización de hardware. y seleccione la referencia ASRL.__

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ff03d635-6c29-474a-83ce-bdf153fab323)

Ahora, presione 'Run' nuevamente

El indicador de error mostrara que no hay error, el indicador de identidad habra cambiado y ahora despliega valores.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/5c2570bb-2497-4d50-9b4f-670e6ed637f1)

Pero, algo mas importante es que el LED del hardware se ha encendido!

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/465b4cdf-0aa2-4014-92a6-4eab1eb42a3c)


# Lección 2 - Ciclos For (For Loops)
Opcional: Configuración de Hardware

Conecte el hardware como la imagen siguiente:

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/55b91ce8-3c9b-4bb9-8082-a911e74e7275)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/ab4506dc-f5f3-4008-a3b9-03123cd26ebf)

## Instrucciones

Un ciclo For ejecuta un sub-diagrama un numero determinado de veces. En este caso, aprenderás a construir un programa que hace parpadear un LED 10 veces antes de detenerse

Agrande su espacio de trabajo para dejar espacio para agregar objetos. Utilice Ctrl y luego arrastre para expandir.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/484becac-5d71-445e-90b0-37525819cead)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/c7ebdddb-80e6-43cc-a645-2c6b2acd05d9)

Alternativamente, seleccione los objetos que necesita mover con la herramienta de selección y arrástrelos a donde desee con el mouse o usando las flechas.

__Nota: presione Mayús y una tecla de flecha para mover los elementos seleccionados más rápido.__

Ahora inserte un ciclo For, para hacerlo, haga clic derecho en cualquier lugar del diagrama de bloques para abrir la paleta de funciones. Seleccione 'Estructuras' y luego 'For Loop'.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fcb44595-01e3-49f8-ac4f-7bbb2802f783)

Sólo necesitará colocar el bucle For alrededor del WriteDO SubVI (y las constantes adjuntas a él).

Una vez que se haya colocado el ciclo For, verá una 'N' en la esquina superior izquierda, este es el numero de iteraciones que realizará el ciclo For.

Haga clic derecho en la N y seleccione "Crear una constante". Para esta tarea necesitará que el número de bucles sea 20 (10 veces activado y 10 veces desactivado).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/414e694a-ae63-41e2-a36a-63e4354bbe9b)

Para que el programa "parpadee" correctamente, necesitará saber qué se ha ejecutado en la iteración anterior, por lo que necesitará un registro de desplazamiento (shift Register).

Haga clic derecho en el borde del ciclo For y seleccione "add shift register". Conecte la constante verdadera a los registros de desplazamiento y al terminal del cable DO (valor).

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/e7da0c07-5417-48a3-b640-e2e671d020ad)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/28a02b6e-76f8-47d5-ac87-b2f6834763ae)

Si ejecutara el programa en este punto, el LED se iluminaría, pero no "parpadearía".

Para un LED parpadeante necesitarás invertir el valor booleano después de cada iteración. Para hacer esto, haga clic derecho en cualquier lugar para abrir la paleta de funciones. Pase el cursor sobre "Booleano" y luego seleccione el booleano "Not". Conecte esto al registro de desplazamiento.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/790e2351-196b-4504-8a31-4beed7c9c29b)

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/fddc4fb2-9e21-4835-b9d7-37538c2a42da)

¡El programa ahora funcionará! Sin embargo, se ejecutará muy rápido y no podrá ver el LED parpadeando. Entonces necesitas reducir la velocidad del ciclo.

Haga clic derecho dentro del ciclo For y coloque el cursor sobre "Time". Allí verá muchas opciones de tiempo diferentes. Para ello utilizarás la función 'Wait'. Seleccionala y coloca dentro del Loop.

Creea una constante haciendo clic derecho en el lado izquierdo de la función "Wait". La función "Wait" se ejecuta en milisegundos, por lo tanto, para ralentizar el ciclo 5 segundos, escriba 500.

![image](https://github.com/LabVIEWCommunityTraining/GettingStartedLabVIEW1-Espanish/assets/5545396/b4139bcd-b996-4248-a196-99a3b79d2572)

Ahora ejecuta el programa. Ha utilizado con éxito un ciclo For para hacer parpadear la salida digital.








