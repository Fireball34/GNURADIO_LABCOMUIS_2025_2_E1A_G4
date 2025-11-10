# MISIÓN 2: EL ENLACE CRÍTICO

# Fase 1: Establecimiento de la Línea Base (Calibración)

- **Registro de Potencia Inicial (P_in):**

La potencia registrada es: -13.67 dBm a 150MHz

![Medición fase 1](https://github.com/user-attachments/assets/4e7866a3-84a4-4ddf-ba7d-4eaaeab79a9c)

# Fase 2: Pruebas de Campo (Medición de Componentes)

- **Potencia out cable (118 ft):** -31.63 dBm, a 150MHz.

![Fase 2 Potencia out cable (118 ft)](https://github.com/user-attachments/assets/88a6a1da-6ff5-44e9-b2f9-9eecfcb81e47)

- **Potencia out cable (118 ft) con atenuador de 30 dBm:** -66.57 dBm, a 150MHz.

![Fase 2 Potencia out cable (118 ft) con atenuador de 30 dBm](https://github.com/user-attachments/assets/fe6b811e-c81b-4f4e-87dc-dedb4d54cc31)

- **(Avanzado) Cable de 118ft a 800MHz:** -69.34 dBm.

![Fase 2 (Avanzado) -69 34 dBm, a 800MHz](https://github.com/user-attachments/assets/d3de3be3-c5bf-483f-8875-d9ecff5d6530)

- **Potencia out cable (122 ft):** -48.76 dBm, a 150MHz.

![Fase 2 Potencia out cable (122 ft)](https://github.com/user-attachments/assets/b2fe915f-4b60-40c4-a376-c9034c497080)

- **Potencia out cable (122 ft) con atenuador de 30 dBm:** -68.60 dBm, a 150MHz.

![Fase 2 Potencia out cable (122 ft) con atenuador de 30 dBm](https://github.com/user-attachments/assets/3fb0f5b2-02de-4733-9294-7688e127d48d)

- **(Avanzado) Cable de 122 ft a 800 MHz:** -78.14 dBm.

![Fase 2 (Avanzado) -78 14 dBm, a 800MHz](https://github.com/user-attachments/assets/e14c4df9-66ef-4199-8d5e-fb2d7a29650b)

# Fase 3: Diagnóstico y Análisis

## Diagnóstico

### Tabla para cable de 118 ft

| Cable | Frecuencia (MHz) | P_in (dBm) | P_out (dBm) | Atenuación teórica (dB) | Atenuación experimental (dB) |
|-------|------------------|------------|-------------|-------------------------|------------------------------|
| 118 ft | 50 | -13.67 | -14.56 | 3.776 | 0.89 |
| 118 ft | 100 | -13.67 | -16.50 | 5.31 | 2.83 |
| 118 ft | 200 | -13.67 | -20.33 | 7.55 | 6.33 |
| 118 ft | 500 | -13.67 | -32.91 | 12.5 | 19.24 |
| 118 ft | 1000 | -13.67 | -43.31 | 17.11 | 29.64 |

- Medición para cable de 118 ft a 50 MHz
![Fase 3 118 ft 50 MHz](https://github.com/user-attachments/assets/09fad8d6-95ef-4605-8e59-a371a7cea14b)

- Medición para cable de 118 ft a 200 MHz
![Fase 3 118 ft 200 MHz](https://github.com/user-attachments/assets/bcc29095-af11-486a-9546-ea2f4657772b)

- Medición para cable de 118 ft a 1000 MHz
![Fase 3 118 ft 1000 MHz](https://github.com/user-attachments/assets/9067d005-5a29-4b70-8dba-f4c01b92c182)

### Tabla para cable de 122 ft

| Cable | Frecuencia (MHz) | P_in (dBm) | P_out (dBm) | Atenuación teórica (dB) | Atenuación experimental (dB) |
|-------|------------------|------------|-------------|-------------------------|------------------------------|
| 122 ft | 50 | -13.67 | -14.57 | 3.9 | 0.9 |
| 122 ft | 100 | -13.67 | -16.85 | 5.49 | 3.18 |
| 122 ft | 200 | -13.67 | -20.66 | 7.8 | 6.99 |
| 122 ft | 500 | -13.67 | -33.16 | 12.27 | 19.49 |
| 122 ft | 1000 | -13.67 | -42.56 | 17.69 | 28.89 |

- Medición para cable de 122 ft a 50 MHz
![Fase 3 122 ft 50 MHz](https://github.com/user-attachments/assets/d5b5bf9a-0ee8-400b-892f-c39c277c74a0)

- Medición para cable de 122 ft a 200 MHz
![Fase 3 122 ft 200 MHz](https://github.com/user-attachments/assets/39889c5d-4738-4c07-8aaa-be8c78d39376)

- Medición para cable de 122 ft a 1000 MHz
![Fase 3 122 ft 1000 MHz](https://github.com/user-attachments/assets/da6136ce-29df-4168-9fc0-6839bcf77adf)

## Análisis

- Identificación de anomalias: Basado en la tabla de resultados, identifique claramente cuál es el cable "que mayor atenuación presenta" y justifique por qué su atenuación es significativamente mayor.

**R/** El cable de 122 ft presenta mayor atenuación, esto debido a la relación de atenuación según el largo del cable. Ej: Para 50 MHz => 3.2 dB/100 ft, es decir, a mayor largo del cable mayor atenuación. Sin embargo, es sólo un poco mayor porque el otro cable era de 118 ft.

- Análisis Causa-Raíz: ¿Qué posibles fallas físicas en un cable o conector podrían causar una atenuación tan alta?

**R/** Conectores dañados podrían incluso dar una atenuación de -60 dB, por experiencia en el laboratorio lo decimos, ya que, por una mala conexión de un conector una señal que debía ser de -15 dBm nos daba -60 dBm aproximadamente.

- (Si se realizó el reto avanzado): Analiza cómo cambió la atenuación de los cables al aumentar la frecuencia. ¿Es un comportamiento esperado? ¿Por qué?

**R/** La atenuación aumentó demasiado al tener un cambio de 650 MHz, esto no es nada fuera de lo normal, para altas frecuencias hay diversos fenómenos físicos que afectan la transmisión en conductores, empeorandola.

## Conclusiones

Resume tus hallazgos y la importancia de medir la pérdida en las líneas de transmisión para garantizar la integridad de un enlace decomunicaciones.

**R/** Es importante tener en cuenta y conocer los límites para las pérdidas en un enlace, esto permite interpretar mucho mejor la veracidad de la información en el receptor.
