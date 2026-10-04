# Polarización afectiva en Argentina: análisis de la conversación digital en X (Twitter), 2023-2025

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mickx79/An-lisis-de-publicaciones-de-X-para-tesis-de-grado/blob/main/An%C3%A1lisis_de_posteos_Tesis.ipynb)

Repositorio con el código de análisis de datos de la tesis de grado **"Polarización afectiva en Argentina: análisis de la conversación digital en X (Twitter) 2023-2025"**, presentada para optar por el título de Licenciado en Ciencias Sociales (Facultad de Ciencias Jurídicas, Políticas y Sociales, Universidad del Norte Santo Tomás de Aquino, octubre de 2026).

Su objetivo es que el jurado pueda consultar y reproducir el procesamiento y las visualizaciones presentadas en el apartado de **Resultados** de la tesis.

## Sobre la investigación

La tesis caracteriza la conversación digital en X durante los ciclos electorales argentinos, desde la campaña presidencial de 2023 hasta la campaña legislativa de 2025, a partir del eje identitario **peronismo-antiperonismo**. Se propone identificar las emociones predominantes, las estrategias discursivas polarizantes y la manera en que cada espacio se vincula con su endogrupo, su exogrupo y sus referentes.

**Corpus y recolección**

- 390 posteos de X (15 por evento), recolectados mediante *scraping* manual entre el 18/06/2023 y el 26/10/2025.
- 26 eventos de aproximadamente una semana cada uno, definidos a partir de hitos electorales y de picos de interés identificados con *Google Trends*.
- Posteos originales en español (sin respuestas), priorizando un mínimo de 5000 likes y 400 reposts.
- Se excluyeron las publicaciones de los principales referentes de cada espacio (Javier Milei y Cristina Fernández de Kirchner).

**Períodos de análisis**

1. Campaña presidencial 2023
2. Primer año de gestión presidencial (2024)
3. Segundo año de gestión presidencial (2025)
4. Campaña legislativa 2025

**Categorías de análisis aplicadas a cada posteo**

- Posición política (peronista / antiperonista)
- Tipo de contenido (promoción o detracción)
- Destinatario (endogrupo, exogrupo, referente propio, referente contrario)
- Emoción predominante (felicidad, enojo/indignación, miedo, tristeza, sorpresa, asco y furia)
- Tipo de microargumentación (lógica o emocional)
- Uso de humor o ironía
- Uso de lenguaje populista
- Uso de etiquetas peyorativas
- Repetición de estereotipos negativos
- Uso de palabras malsonantes

La codificación de cada posteo se realizó de forma manual, y los criterios y las definiciones de cada categoría se detallan en la sección de Metodología y en el Anexo de la tesis.

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `Análisis_de_posteos_Tesis.ipynb` | Notebook de Google Colab con todo el análisis y las visualizaciones. |
| `dataframe_procesado.xlsx` | Base de datos con los 390 posteos ya codificados, que el notebook toma como insumo. |

## Estructura del notebook

1. **Carga y limpieza:** lectura de la base, normalización de los nombres de columnas y corrección puntual de errores de codificación detectados durante la revisión.
2. **División por períodos:** separación del corpus en los 4 períodos y verificación de que no se pierdan filas.
3. **Análisis transversales:**
   - cantidad de usuarios únicos y cuentas con más posteos;
   - suma y promedio de likes y reposts por espacio político;
   - caracterización de los posteos más likeados por espacio;
   - microargumentación predominante por período;
   - distribución de emociones en el total del corpus.
4. **Análisis por período:** emociones según destinatario (endogrupo, exogrupo, referente propio y referente contrario) para cada uno de los 4 períodos.
5. **Evolución temporal:**
   - emociones;
   - promoción y detracción;
   - frecuencia por destinatario;
   - estrategias discursivas;
   - emociones hacia el exogrupo, el endogrupo, el referente propio y el referente contrario.

Algunas celdas son de exploración puntual: sirven para revisar casos individuales (por ejemplo, posteos con una combinación poco frecuente de posición, destinatario y emoción) y verificar la consistencia de la codificación.

## Cómo ejecutarlo

**Opción 1: Google Colab (recomendada)**

1. Hacer clic en el botón *Open in Colab* de arriba.
2. Subir `dataframe_procesado.xlsx` al entorno de Colab (panel de archivos, carpeta `/content`).
3. Ejecutar las celdas en orden (*Entorno de ejecución > Ejecutar todo*).

**Opción 2: de forma local**

```bash
git clone https://github.com/mickx79/An-lisis-de-publicaciones-de-X-para-tesis-de-grado.git
cd An-lisis-de-publicaciones-de-X-para-tesis-de-grado
pip install pandas numpy matplotlib seaborn openpyxl jupyter
jupyter notebook
```

En ese caso, hay que modificar la ruta de lectura en la primera celda (`/content/dataframe_procesado.xlsx`) para que apunte a la ubicación local del archivo.

## Tecnologías

Python 3 · pandas · NumPy · Matplotlib · Seaborn · Google Colab

## Aclaraciones

- Se trata de un estudio descriptivo e interpretativo, de muestreo no probabilístico, por lo que los resultados caracterizan el corpus analizado y no pretenden generalizarse a toda la conversación de X.
- La recolección fue manual debido a limitaciones presupuestarias y a los cambios en el acceso a la API de X para uso académico.
- Los comportamientos *online* no son trasladables directamente al mundo análogo.

## Autor

**Miqueas**: Tesis de grado para la Licenciatura en Ciencias Sociales, Universidad del Norte Santo Tomás de Aquino (UNSTA), Tucumán, Argentina.
