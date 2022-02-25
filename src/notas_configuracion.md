### configurar las carpetas con capas
- Remplazar las carpetas que se vayan a usar en "layers"
- Puede colocarse imagenes vacias (transparentes) con el nombre "blank2 y no van a aparecer en la data subida
- Puede manejarse la rareza de las capas colocanco /*<nombre #peso>*/ por ejemplo azul #10

# Cambiar datos en src/config.js

### Datos de la colección
En las líneas 8 al 11 cambiar los datos de acuerdo a la colección que se vaya a crear

const namePrefix = "Nombre de la colección / Your Collection";
const description = "Descripción de la colección aca /Remember to replace this description";
const baseUri = "ipfs://NewUriToReplace";

### Número de imágenes generadas
Línea 27: colocar el número de imágenes que se desea crear
Línea 28: colocar las carpetas que contienen las capas de imágenes y deben ir desde la mas lejana a la mas cercana, y coincidir con los nombres de las carpetas en "layers"

### Tamaño de las imágenes creadas
Linea 44: colocar el tamaño en pixels de las imágenes que quiero

### Crear .gif ademas de las imágenes fijas
Línea 51: true = crear .gif / false = no crear .gif

### Añadir metadata adicional para el nft
Línea 81: se puede añadir metadata con un nombre y descripción, esto será agregado a los json generados por la app