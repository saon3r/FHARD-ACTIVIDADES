**ESCAPE ROOM 2026**  					grupos 2 personas

Manual de placa base: Gigabyte Z690 AORUS PRO / Z690 AORUS PRO DDR4 (PDF partes 1 y 2). Las respuestas se refieren a la variante **Z690 AORUS PRO DDR4**.  
***Trabajo con IA y documentos (manual Placa Base) como contexto (Skill)***

**FASE 1: Identificación del Factor de Forma (El Tamaño Sí Importa)**  
**El problema:** El cliente ha comprado una caja de ordenador ultra compacta para el salón, pero la placa base que ha intentado meter dentro es demasiado grande y no encaja en los anclajes del chasis.

* **El Reto en el Manual:** Id a la primera página de especificaciones generales o al índice del manual, donde se describen las características físicas de la placa (*Hardware Installation* / *Introduction*).

* **Pregunta / Desafío:**  
  1. Según el manual de esta placa base, ¿cuál es su **factor de forma** o tamaño exacto (por ejemplo: *ATX*, *Micro-ATX*, *Mini-ITX*, etc.)?   
**Respuesta.** El factor de forma es **ATX** y la placa mide **30,5 × 24,4 cm** (parte 1, pág. 12 del manual).

* *Código para avanzar:* **ATX**.

**FASE 2: El Zócalo de la CPU (Cuidado con los Pines)**  
**El problema:** Un compañero va a instalar el procesador en el zócalo y os pregunta cómo debe orientarlo correctamente para no doblar ningún pin ni forzar el anclaje metálico.

* **El Reto en el Manual:** Buscad en la sección de instalación del procesador (*CPU Installation*) el nombre del zócalo. 

* **Pregunta / Desafío:**  
  1. ¿Cómo se denomina exactamente el **modelo de socket o zócalo** de esta placa base (por ejemplo: *LGA 1700*, *AM5*, *LGA 1151*, etc.)?   
  2. ¿Los pines de conexión están en este zócalo de la placa o en la parte inferior de la CPU? 

**Respuestas**

1. El zócalo se denomina **LGA1700**.
2. Los pines están en el **zócalo de la placa base**. La cara inferior del procesador tiene contactos planos. Para orientarlo, hay que hacer coincidir las muescas con las guías del zócalo y alinear las dos marcas triangulares del pin 1 (parte 1, pág. 13 del manual).

* *Código para avanzar:* **LGA1700**.

**FASE 3: Los Puertos de Vídeo Traseros (La Gráfica Integrada)**  
**El problema:** El cliente enciende el ordenador por primera vez sin tarjeta gráfica dedicada y conecta el cable del monitor directamente a la placa base, pero no ve imagen en pantalla. Queréis comprobar qué salidas de vídeo físicas ofrece la placa de serie.

* **El Reto en el Manual:** Buscad el diagrama del **Panel de E/S Trasero** (*Back Panel Connectors* / *I/O Back Panel*), donde se detallan todos los puertos de la parte posterior.

* **Pregunta / Desafío:**

¿Qué **puertos de vídeo** integrados (como *HDMI*, *DisplayPort*, etc.) incluye esta placa base en su parte trasera para usar con la gráfica integrada del procesador?

**Respuesta.** El panel trasero tiene una única salida de vídeo, **DisplayPort 1.2**. Admite hasta **4096 × 2304 a 60 Hz**, según el procesador con gráfica integrada y el monitor (parte 1, págs. 9 y 18 del manual).

* *Código para avanzar:* **DisplayPort**.

**Parte 2 del ejercicio**

**Instrucciones:***Sois un equipo de técnicos de soporte de nivel 2\. Un cliente os ha enviado un ordenador de alta gama recién montado que **no arranca**, se queda la pantalla en negro y los ventiladores giran de forma extraña. Tenéis el manual oficial de la placa base en la pantalla y 3 fases que superar para descifrar el error y levantar el sistema. ¡El tiempo corre\!*

**FASE 4: El Diagnóstico del Panel Frontal (Los "Front Panel Connectors")**  
**El problema:** El cliente intentó cambiar la caja del PC y ahora, al pulsar el botón de encendido (*Power Button*) de la torre, **absolutamente nada se enciende**. No hay corriente ni chispa.

* **El Reto en el Manual:** Buscad en el manual de la placa el apartado dedicado a las conexiones del panel frontal (suele llamarse *Front Panel Header*, en los manuales de Gigabyte suele estar en la sección de instalación de hardware bajo la etiqueta **F\_PANEL**).

* **Pregunta / Desafío:**

  1. ¿En qué pines exactos del bloque F\_PANEL debe ir conectado obligatoriamente el interruptor de encendido (**PWR\_BTN** / Power Switch)?  
  2. Si por error el alumno hubiera conectado los pines del Power Switch en los pines de *Reset* o en los de los LEDs del disco duro, ¿por qué el ordenador no muestra ninguna señal de vida?

**Respuestas**

1. El interruptor de encendido se conecta a los pines **6 (PW+)** y **8 (PW−)** del bloque **F_PANEL** (parte 2, pág. 29 del manual).
2. Al pulsar el botón, el interruptor cierra el circuito del par al que está conectado. Si se conecta a **RES**, acciona la entrada de reinicio. El par **HD** está destinado al LED de actividad del disco. En ambos casos la placa se queda sin la señal de encendido que debe recibir por **PW**.

* *Código para avanzar:* **Página 29 del manual**, apartado 13, **F_PANEL (Front Panel Header)**. Es la segunda página del PDF de la parte 2.

**FASE 5: El Laberinto de la Memoria RAM (Canales y Slots)**  
**El problema:** Tras solucionar el botón de encendido, el ordenador por fin da señal de vídeo, pero la pantalla se queda congelada mostrando un código de error de memoria y la placa base emite una secuencia de pitidos cortos continuos. El cliente ha colocado los dos módulos de memoria RAM DDR4 en los zócalos AMC\_1 y AMC\_2 (los dos primeros empezando desde el socket del procesador).

* **El Reto en el Manual:** Buscad en el manual el apartado de **Installation / Recommended Population for 2 DIMMs** (Instalación de memoria en arquitectura de doble canal).

* **Pregunta / Desafío:**  
  1. Según el fabricante de esta placa, si solo se van a instalar **dos módulos de RAM**, ¿en qué ranuras específicas (por nombre de slot, ej. *A2 y B2* o *DDR4\_1 y DDR4\_2*) deben colocarse obligatoriamente para activar el *Dual Channel* y evitar el fallo de arranque?

**Respuesta.** Gigabyte recomienda instalar los dos módulos en **DDR4_A2** y **DDR4_B2**, uno en cada canal. Los dos primeros zócalos desde el procesador se llaman **DDR4_A1** y **DDR4_A2** y pertenecen ambos al canal A (parte 1, págs. 5 y 16 del manual).

* *Código para avanzar:* **DDR4_A2 y DDR4_B2**.

**FASE 6: El Enigma de la UEFI y la Actualización de la BIOS (*Q-Flash*)**

**El problema:** El PC ya arranca y entra al sistema, pero al montar un procesador de decimotercera o decimocuarta generación en esta placa Z690, el sistema no reconoce la CPU correctamente o se cuelga en el logo inicial. Necesitáis actualizar la BIOS/UEFI. Lo fascinante es que esta placa cuenta con un botón físico trasero para actualizarla **sin necesidad de tener CPU ni RAM instaladas**.

* **El Reto en el Manual:** Buscad en el manual el apartado de la tecnología de actualización sin procesador (en Gigabyte se llama **Q-Flash Plus**).

* **Pregunta / Desafío:**

  1. ¿Cómo se llama exactamente el **puerto USB trasero de color especial** (o serigrafiado) donde obligatoriamente se debe conectar el pendrive USB con el archivo de la BIOS para usar esta función?

  2. ¿Qué nombre exacto debe tener obligatoriamente el archivo de la BIOS dentro del pendrive para que la placa lo reconozca al pulsar el botón *Q-Flash Plus*?

**Respuestas**

1. El puerto se identifica como **USB 3.2 Gen 2 Type-A Port (Red) (Q-Flash Plus Port)** (parte 1, pág. 19 del manual). El esquema del manual sitúa el botón **QFLASH_PLUS** en la propia placa (parte 1, págs. 5 y 20 del manual).
2. Los PDF facilitados no indican el nombre exacto del archivo de la BIOS. El apartado de Q-Flash Plus remite a la sección *Unique Features* de Gigabyte para más detalles (parte 1, págs. 19 y 20 del manual).

* *Código para avanzar:* **Q-Flash Plus Port**.

