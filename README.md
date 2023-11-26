# Estructura de los archivos
Los archivos son de formato *csv*, pero el delimitador no es una coma, sino un *pipe* |.  
Esto con el objetivo de amenizar el tacto con las frases que utilizan coma -que no son pocas-, en vez de directamente escapar el caracter.

# Carpeta 'raw'
La carpeta *raw* contiene los títulos **sin procesar** de los videos, es decir, los títulos con los que fueron subidos a Youtube. Esta carpeta será simple referencia para tener una idea de cómo es la estructura de los títulos de los videos y posteriormente procesarla para tener un listado más homogéneo (ej: algunos títulos están en mayúsculas, otros solo mayúscula inicial; pueden haber puntuaciones incorrectas o inconsistentes, etc).

## Contenido
- servicio_al_cliente.csv: 139 frases
- index.csv: 4964 frases

El *schema* es `random_index|title|video_id`.
- `random_index` es un index de control. Está ahí únicamente porque así se llevó un control interno de conteo al momento de extraer los títulos. Es irrelevante y no tiene un significado importante (hay repetidos incluso). Se planea eliminar este index y sustituirlo con un índice incremental que identifique a las palabras, en futuras actualizaciones.
- `title` es el título del video.
- `video_id` es el id de Youtube del video.

Luego de procesar los títulos, el archivo csv procesado puede ir directamente bajo el directorio `lsec-map/`, con los mismos títulos. Lo que está en la carpeta `raw` no se borra.
