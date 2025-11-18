# MISION 3: MODULACIÓN DE ONDA CONTINUA

# Fase 1: Diseño y configuración del modulador (Preparación técnica)
![Diagrama de flujo fase 1](Diagrama_de_flujo.png)
 Frecuencia de la Portadora: 433 MHz

 Tasa de Muestreo (Sample Rate): 12.5 MS/s

 Ganancia de Transmisión (TX Gain): 0 dB, para evitar daños en el puerto de entrada del osciloscopio o el analizador de espectro.
# Fase 2: Generación y Medición

   Conexión Segura: Conecte la salida de transmisión (TX1 / RX1) de su SDR al atenuador, y la salida del atenuador a la entrada del canal 1 del osciloscopio. Nota: recuerde que la amplitud maxima de la envolvente compleja debe ser menor a 0.5

  Señal senoidal:
  ![Señal senoidal modulada vista en el osciloscopio](Señal_senoidal_modulada.jpg)

  Señal senoidal con ganancia K de 1 a 1kHz de frecuencia.

   Señal cuadrada:
  ![Señal cuadrada modulada vista en el osciloscopio](Señal_cuadrada_modulada.jpg)

  Señal cuadrada con ganancia K de 1 a 1kHz de frecuencia.

   Señal de audio:
  ![Señal de audio modulada vista en el osciloscopio](Señal_audio_modulada.jpg)

  Se utilizo una señal de audio de una canción.
 
  # Fase 3: Análisis de Espectro y Comparación
### Tabla Comparativa de Señales Moduladoras

| Tipo de Señal Moduladora | Analizador de espectro | Descripción tecnica | Efecto de la Modulación |
|--------------------------|--------------------------|------------------------------------------------|--------------------------|
| Senoidal                | ![](Señal_senoidal_espectro.jpg) | |  |
| Cuadrada                | ![](Señal_cuadrada_espectro.jpg) |  |  |
| Triangular              | ![](Señal_triangular_espectro.jpg) |  |  |
| Diente de sierra        | ![](Señal_dientesierra_espectro.jpg) |  |  |
| Audio          | ![](Señal_audio_espectro.jpg) |  |  |

---
