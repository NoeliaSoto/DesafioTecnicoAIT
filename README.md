# README - Procesamiento de 1_ford TRABAJAR.xlsx

## Introducción

Este documento describe el proceso llevado a cabo para transformar el archivo `1_ford TRABAJAR.xlsx` de acuerdo a las especificaciones dadas. El objetivo fue preparar los datos para que cumplan con el formato requerido y asegurar su calidad.

## Pasos Realizados

1. **Configuración Regional**:
   - Configuré la hoja de cálculo en Google Sheets para que utilizara la región Argentina. Esto asegura que los formatos de número y moneda sean correctos.

2. **Navegación de Datos**:
   - Revisé todos los datos para identificar filas o columnas vacías y datos duplicados, asegurando que el archivo estuviera limpio antes de realizar modificaciones.

3. **Eliminar Espacios en Blanco**:
   - Utilicé la función de "Buscar y Reemplazar" para eliminar todos los espacios en blanco. Esto se realizó buscando el espacio y reemplazándolo con nada, asegurando que no hubiera espacios entre los códigos.

4. **Formateo de Precios**:
   - Para el precio, revisé que la cantidad de dígitos fuera correcta en comparación con el modelo. En caso de que el formato fuera diferente, eliminé los últimos 4 ceros y añadí una coma antes de los últimos dos dígitos, utilizando una fórmula personalizada para realizar esta tarea.

5. **Eliminación de Símbolos No Deseados**:
   - Utilicé la siguiente fórmula para eliminar los símbolos no deseados de la lista:
     ```plaintext
     =REGEXREPLACE(A1, "[╝┤\xE2\x96\x84\xE2\x96\x92]", "")
     ```
   - Esta fórmula se aplicó a toda la columna de datos, asegurando que todos los símbolos especificados fueran eliminados.

6. **Revisión Final**:
   - Hice una revisión final del archivo para asegurarme de que no hubiera errores y que todos los datos cumplieran con las especificaciones.

## Herramientas Utilizadas

- Google Sheets: Para la edición y procesamiento de los datos.
- Funciones de Google Sheets: Como `REGEXREPLACE`, `BUSCAR Y REEMPLAZAR`, y formateo de celdas.

## Conclusión

Los datos del archivo `1_ford TRABAJAR.xlsx` fueron procesados y transformados satisfactoriamente, cumpliendo con todas las especificaciones requeridas. El archivo resultante ahora está listo para su uso en el sistema.
