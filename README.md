# DESAFÍO TÉCNICO - SOTO N.
## Procesamiento de Archivos

Este documento detalla el proceso llevado a cabo para transformar los archivos propuestos, cumpliendo con las especificaciones dadas. El objetivo fue limpiar y formatear los datos de acuerdo a los modelos proporcionados.

## 1. Procesamiento de "hurl.csv TRABAJAR.xlsx"

### Pasos Realizados

1. **Apertura del Archivo**:
   - Abrí el archivo CSV utilizando Google Sheets para facilitar la edición y el procesamiento de datos.

2. **Limpieza de la Base de Datos**:
   - Realicé una revisión exhaustiva para identificar celdas vacías y datos duplicados.

3. **Adición de Encabezados**:
   - Agregué encabezados a las columnas para que coincidan con el formato del modelo.

4. **Concatenación de Información**:
   - Utilicé la función `CONCATENAR` para unificar la información de las columnas "Descripción" y "Descripción2" en una sola columna.

5. **Eliminación de Filas Vacías/Redundantes**:
   - Eliminé filas vacías y redundantes, incluyendo la fila que contenía información irrelevante.

6. **Reemplazo de Caracteres No Legibles**:
   - Identifiqué y reemplacé caracteres no legibles (como Á y Ñ).

7. **Formateo de la Columna Precio Final**:
   - Utilicé la función `REDONDEAR` para ajustar la columna de "Precio Final", asegurando que tuviera el mismo formato que el modelo.

8. **Formato y Estilo**:
   - Seleccioné toda la tabla, apliqué formatos de colores alternos y elegí una paleta de colores que coincidiera con el modelo.

### Herramientas Utilizadas

- Google Sheets: Para la apertura, edición y procesamiento de los datos.
- Funciones de Google Sheets: Como `CONCATENAR`, `REDONDEAR`, y herramientas de formato.

---

## 2. Procesamiento de "ford TRABAJAR.xlsx"

### Pasos Realizados

1. **Configuración Regional**:
   - Configuré la hoja de cálculo en Google Sheets para que utilizara la región Argentina.

2. **Navegación de Datos**:
   - Revisé todos los datos para identificar filas o columnas vacías y datos duplicados.

3. **Eliminación de Espacios en Blanco**:
   - Utilicé la función de "Buscar y Reemplazar" para eliminar todos los espacios en blanco.

4. **Formateo de Precios**:
   - Para el precio, revisé que la cantidad de dígitos fuera correcta. En caso de que fuera diferente, eliminé los últimos 4 ceros y añadí una coma antes de los últimos dos dígitos.

5. **Eliminación de Símbolos No Deseados**:
   - Utilicé la siguiente fórmula para eliminar los símbolos no deseados de la lista:
     ```plaintext
     =REGEXREPLACE(A1, "[╝┤\xE2\x96\x84\xE2\x96\x92]", "")
     ```

6. **Revisión Final**:
   - Hice una revisión final del archivo para asegurarme de que no hubiera errores.

### Herramientas Utilizadas

- Google Sheets: Para la edición y procesamiento de los datos.
- Funciones de Google Sheets: Como `REGEXREPLACE`, y herramientas de formato.

---

## 3. Procesamiento de "LP_RASA_001 (1).txt TRABAJAR.xlsx"

### Pasos Realizados

1. **Descarga y Apertura del Archivo**:
   - Descargué el archivo TXT y lo abrí en Excel para manipular y llevar los datos a columnas generado utilizando "de ancho determinado"

2. **Guardado y Carga**:
   - Guardé el archivo en formato XLS y lo subí a Google Drive para continuar con el formateo.

3. **Preparación de los Datos**:
   - Configuré la región en Google Sheets.

4. **Eliminación de Columnas y Filas Redundantes**:
   - Eliminé columnas y filas redundantes y/o vacías.

5. **Formateo del Código**:
   - Utilicé la siguiente fórmula para asegurarme de que la columna A fuera un número entero:
     ```plaintext
     =SI(ESNUMERO(VALOR(A2)); A2; REGEXREPLACE(A2; "[^\d]"; ""))
     ```

6. **Limpieza y Concatenación**:
   - Apliqué la función `LIMPIAR` a las columnas A y B, y luego concatené ambas columnas utilizando:
     ```plaintext
     =CONCATENAR(A2; " "; B2)
     ```

7. **Cálculo del Precio**:
   - Formulé el precio con la siguiente función para ajustarlo a los valores del modelo:
     ```plaintext
     =I2/100
     ```

8. **Copia de Encabezados**:
   - Copié el encabezado de la tabla anterior para que quedara igual al modelo.

### Herramientas Utilizadas

- Google Sheets: Para la edición y procesamiento de los datos.
- Funciones de Google Sheets: Como `LIMPIAR`, `REGEXREPLACE`, y herramientas de formato.

---

## 4. Procesamiento de "Anaerobicos trabajar.xlsx"

### Pasos Realizados

1. **Configuración Regional**:
   - Cambié la configuración regional seleccionando en el menú: `Archivo > Configuración > Configuración Regional`.

2. **Navegación de Datos**:
   - Revisé la planilla para identificar qué datos había.

3. **Eliminación de Filas Vacías**:
   - Creé un filtro, seleccioné las filas vacías y las eliminé.

4. **Recorte de Espacios Vacíos**:
   - Recorté los espacios vacíos en la columna "Producto".

5. **Eliminación de Datos Duplicados**:
   - Eliminé datos duplicados para asegurar la unicidad.

6. **Corroboración de Información**:
   - Verifiqué que la información en la Hoja 1 y Hoja 2 fuera la misma; la primera incluía un porcentaje de variación y la segunda no.

7. **Creación de Columnas de Código y Descripción**:
   - Utilicé las siguientes funciones para extraer el código y la descripción:
     ```plaintext
     =REGEXEXTRACT(producto; "^\d+")
     =REGEXEXTRACT(producto; "\D.*")
     ```

8. **Control de Encabezados**:
   - Revisé y aseguré que los encabezados fueran correctos.

9. **Ordenación de Precios**:
   - Seleccioné la tabla, fui a `Datos > Ordenar Intervalos > Opciones Avanzadas`, seleccioné las columnas con precios y activé la opción de encabezado, ordenando de mayor a menor.

10. **Eliminación de Columnas Redundantes**:
    - Eliminé la columna "Variación", la columna "Producto" y la columna "Código de Barras", ya que no eran necesarias.

11. **Reemplazo de Fórmulas por Valores**:
    - Reemplacé las columnas con fórmulas copiando y pegando solo los valores.

### Herramientas Utilizadas

- Google Sheets: Para la edición y procesamiento de los datos.
- Funciones de Google Sheets: Como `REGEXEXTRACT`, y herramientas de formato.

---

## Conclusión

Los archivos `HARD.csv`, `1_ford TRABAJAR.xlsx`, `RASA.txt`, y `ANAEROBICOS.xlsx` fueron procesados y transformados de acuerdo a las especificaciones requeridas, resultando en archivos limpios y formateados, listos para su uso en el sistema.
