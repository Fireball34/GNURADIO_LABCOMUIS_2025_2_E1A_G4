# Fase 1: Exploración y Descubrimiento (El Ojo Panorámico delSDR)

Se encuentra como señal más potente y estable una señal con frecuencia central de 782 MHz y unaganancia máxima de -67 dB, se considera que esta señal corresponde a una portadora de telefoníamóvil por su estabilidad y banda considerablemente amplia de aproximadamente 10 MHz.

<img width="1033" height="583" alt="image" src="https://github.com/user-attachments/assets/39891ce1-0369-4d13-aa2c-0ed5ea7c661a" />

También se captan cerca a los 643 MHz picos frecuentes con hasta -43 dB de ganancia y una bandamuy estrecha, se le asocia estas señales a interferencias.

<img width="1032" height="585" alt="image" src="https://github.com/user-attachments/assets/44d878b0-475a-4a7d-b987-ef513e1da4cf" />

Rondando los 100 MHz se encuentran múltiples señales de radio FM evidenciadas como múltiples picos estables.

<img width="1037" height="584" alt="image" src="https://github.com/user-attachments/assets/d2907ffa-ec29-4c6b-bdb2-26ff9eddff75" />

Cerca de los 475 MHz se hallan señales con un promedio de -68 dB de ganancia, asociando esta señala televisión digital con una banda de buen anchor aproximadamente 5 MHz pero no tan estable comola primera señal.

<img width="1035" height="584" alt="image" src="https://github.com/user-attachments/assets/847a5d8c-83bc-4c9a-90c2-927d7fd623ad" />

# Fase 2: Análisis de Precisión (La Lupa del Analizador)

- Frecuencia Central:
    783.007614 MHz. Se toma este parametro, ya que, se reconoce como elpunto medio entre las dos frecuencias visualizadas donde comienza y termina la señal.

<img width="1033" height="576" alt="image" src="https://github.com/user-attachments/assets/22f8789e-160b-4647-b732-336588f4c173" />

- Potencia:
    -67.52 dBm. El marcador en su modo seat to peak toma como pico este valor depotencia.

<img width="1032" height="590" alt="image" src="https://github.com/user-attachments/assets/0923305a-959c-475e-ad04-8d698f69cff8" />

- Ancho de Banda:
    9.0913 MHz. La diferencia entre los puntos donde inicia la señal y termina laseñal.

<img width="1032" height="576" alt="image" src="https://github.com/user-attachments/assets/972401cf-7907-4653-97ed-6ccc877315e3" />

- Resolución de ancho de banda (RBW):
    100 kHz. Para un RBW superior (entre 300kHz y 1MHz)no se percibe el salto entre ruido y señal. Para un RBW menor la visualización de la señalempieza a ser mejor.

- SPAN:
    12MHz. Este valor de SPAM permite visualizar todo el ancho de banda de la señal y unborde de ruido.

# Fase 3. Visualización de la Onda

Se va a tomar como referencia la señal correspondiente a la frecuencia 90.7MHz debido a que lafrecuencia usada en los puntos anteriores de 783MHz esta fuera de los limites del osciloscopio. Usandomediciones automáticas, el voltaje pico a pico medido por medio del osciloscopio fue de 8.3986mVcon una frecuencia de 5.88MHz. La señal en el dominio del tiempo presento fluctuaciones debidas a lacombinación de distintas frecuencias en esa misma señal lo cual dificulta su analisis en el dominio deltiempo, pero por medio de la FFT su comportamiento permite un mejor análisis. Aparentemente losvalores máximos y mínimos de tensión se mantienen,es decir, no se presentan picos anormales detensión a lo largo de la señal

![Osciloscopio](https://github.com/user-attachments/assets/7cc4c471-c529-4064-9abf-43e182b5e884)

# Resultados y Hallazgos

## Medición con SDR:

<img width="1033" height="578" alt="image" src="https://github.com/user-attachments/assets/074040cf-974e-499e-b8c6-522ca7cfac98" />

## Medición con analizador de espectros:

<img width="1034" height="576" alt="image" src="https://github.com/user-attachments/assets/22645a93-d48d-4c21-8900-dcce78f2a419" />

## Medición con el osciloscopio:

<img width="1035" height="659" alt="image" src="https://github.com/user-attachments/assets/729763c8-cc07-4b20-9ebb-91a16733cdf8" />

# Análisis y Discusión

## Comparativa de Equipos:

- **¿Con cuál equipo le fue más fácil encontrar la señal?**

Con el SDR se hace mucho más sencilla la tarea de búsqueda de señales debido a su interfaz, además, las señales visualizadas no tienen tanta dependencia del entorno como lo hace el analizador de espectros.

- **¿Qué ventajas y desventajas tiene cada equipo para esta tarea de reconocimiento?**
  
### SDR:
  
*Ventajas:*
  
- Ajustabilidad de parámetros para facilitar la tarea requerida.

- Permite un desplazamiento en la búsqueda de frecuencia mucho más fluido.

*Desventajas:*
                    
- Requiere una amplia configuración y conocimiento para ajustar de la mejor forma la herramienta.

### Analizador de espectros:

*Ventajas:*

- Mayor precisión para la medida de potencia de la señal
- No requiere de muchos ajustes para poder captar las señales.

*Desventajas:*
                    
- Realizar barridos de búsqueda es complejo debido a la capacidad de actualización (poca fluidez) de las medidas al desplazarse en frecuencia.

### Osciloscopio:

*Ventajas:*
                    
- Permite obtener información de amplitud y forma de onda

*Desventajas:*
                    
- Limitaciones en frecuencia (aprox freq max 600MHz)

- Menor precisión de medida en dominio de la frecuencia

## Precisión:

- **¿Cuál de los tres equipos ofrece la medida de frecuencia más confiable y precisa?**

El analizador de espectros trabajando en el dominio de la frecuencia se vuelve el equipo más preciso, ya que, posee herramientas especializadas para este dominio.

- **¿Por qué cree que es así?**

Porque al trabajar con SDR las señales en frecuencia suelen ser un poco volátiles y sus medidas de potencia no reflejan mucho los factores del entorno.

## La Conexión Tiempo-Frecuencia:

- **Explique con sus palabras que representa el pico que se observa en el analizador de espectros en relación con la onda sinusoidal que se observa en el osciloscopio.**

Lo que explica esto, es el dominio en el que trabaja cada equipo, donde el analizador de espectros trabaja en frecuencia, mostrando realmente las portadoras de las señales en dicho dominio; sin embargo, el osciloscopio toma la forma de la señal en el dominio del tiempo y justamente esta es la relación de una señal sinusoidal en el tiempo siendo un impulso en frecuencia.

## Desafíos:

- **Describa las dificultades que se encuentran especialmente al intentar visualizar la señal en el osciloscopio. ¿Cómo las resuelvo?**

Al trabajar en el dominio del tiempo y captando la señal con un antena, se debe tener en cuenta que la señal se puede encontrar modulada dependiendo de la frecuencia, este equipo no está especializado para este tipo de tareas por sí solo, de aquí surge la necesidad de usar la herramienta de FFT para una mejor visualización.

