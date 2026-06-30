## Cómo usar el sistema

### 1. Preparar datos de entrada

Crear un archivo `.txt` con el siguiente formato:

- Un mensaje por línea
- Texto libre desde redes sociales, chats o reportes

Ejemplo:

AYUDA urgente familia atrapada en Valencia
Buscan a Maria Lopez CI 12345678 en Caracas
Centro de acopio en Chacao agua comida

---

### 2. Cargar archivo

Subir el archivo a Colab como:
raw_input.txt

---

### 3. Ejecutar pipeline

El sistema:
- Limpia el texto
- Extrae datos clave (cédula, tipo, ubicación)
- Genera identificadores de caso
- Produce un output en JSON y Excel

---

### 4. Resultados

Se generan:

- Archivo JSON estructurado
- Archivo Excel con los datos procesados

---

### 5. Importante

- Cada archivo procesado genera un nuevo dataset
- No reutilizar archivos anteriores
- Mantener histórico por fecha y fuente

Ejemplo:
twitter_2026-06-30.xlsx
whatsapp_2026-06-30.xlsx


-------------

## How to use the system

### 1. Prepare input data

Create a `.txt` file with:

- One message per line
- Raw text from social media, chats, or reports

Example:

Emergency family trapped in Valencia
Missing person Maria Lopez CI 12345678 Caracas
Aid center in Chacao food and water

---

### 2. Upload file

Upload the file to Colab as:
raw_input.txt

---

### 3. Run pipeline

The system:
- Cleans text
- Extracts key data (ID, type, location)
- Generates case identifiers
- Outputs JSON and Excel files

---

### 4. Output

- JSON file (structured data)
- Excel file (tabular view)

---

### 5. Important

- Each input generates a new dataset
- Do not overwrite previous runs
- Keep historical records by date and source

Example:
twitter_2026-06-30.xlsx
whatsapp_2026-06-30.xlsx
