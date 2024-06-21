# 🚀 Práctica de Electrónica: Sistema Secuencial Sincrónico con Contadores 🎛️

¡Bienvenidos a esta divertida práctica donde construiremos un Sistema Secuencial Sincrónico basado en contadores! 🌟 Utilizaremos la placa Basys2 para llevar a cabo este emocionante proyecto. ¡Vamos a ello!
**OJO:** La practica es el comprimido, solo es descomprimir y abrir el proyecto con el Xilinx (tu entiendes kkk).

## 📝➡️ Orden de la práctica ⬅️📝


El sistema tendrá **3 bloques fundamentales**, cada uno con su propio rol especial:

### Bloque 1: Generador de Frecuencia de 1 Hz 🔄

- **Objetivo:** Generar una señal de 1 Hz usando la señal del reloj de 50 MHz de la placa Basys2.
- **Detalles:** 
  - Utilizaremos contadores de 4 bits.
  - El diseño debe ser completamente sincrónico.

### Bloque 2: Contador de Segundos ⏱️

- **Objetivo:** Contar segundos basándose en la señal generada por el Bloque 1.
- **Detalles:**
  - La salida será un número entero de 0 a 9, interpretado a través de 4 señales de un bit.
  - El conteo será ascendente y se reiniciará a 0 después de alcanzar 9.
  - Este bloque también debe ser sincrónico con el Bloque 1.

### Bloque 3: Display en Pantalla de 7 Segmentos 🖥️

- **Objetivo:** Interpretar la salida del Bloque 2 y mostrar el conteo en una pantalla de 7 segmentos.
- **Hint:** Usa un decodificador de 4 entradas para cada bit del contador a 7 salidas.

## 🛠️ Pasos para Implementación

### Paso 1: Configurar el Reloj en la Placa Basys2 ⏰

Descomenta las siguientes líneas en el archivo de restricciones para utilizar el reloj del sistema:

```plaintext
NET "mclk" LOC = "B8"; # Bank = 0, Signal name = MCLK
NET "mclk" CLOCK_DEDICATED_ROUTE = FALSE;


