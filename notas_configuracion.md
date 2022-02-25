# Algunas notas para la configuración del este programa

## carpetas con las capas de las imágenes

### configurar las carpetas con capas
- Remplazar las carpetas que se vayan a usar en "layers"
- Puede colocarse imagenes vacias (transparentes) con el nombre "blank2 y no van a aparecer en la data subida
- Puede manejarse la rareza de las capas colocanco /*<nombre #peso>*/ por ejemplo azul #10

## Cambiar datos en src/config.js

### Datos de la colección
En las líneas 8 al 11 cambiar los datos de acuerdo a la colección que se vaya a crear

*const namePrefix = "Nombre de la colección / Your Collection";*
*const description = "Descripción de la colección aca /Remember to replace this description";*
*const baseUri = "ipfs://NewUriToReplace";*

### Número de imágenes generadas
Línea 27: colocar el número de imágenes que se desea crear
Línea 28: colocar las carpetas que contienen las capas de imágenes y deben ir desde la mas lejana a la mas cercana, y coincidir con los nombres de las carpetas en "layers"

### Tamaño de las imágenes creadas
Linea 44: colocar el tamaño en pixels de las imágenes que quiero

### Crear .gif ademas de las imágenes fijas
Línea 51: true = crear .gif / false = no crear .gif

### Añadir metadata adicional para el nft
Línea 81: se puede añadir metadata con un nombre y descripción, esto será agregado a los json generados por la app, se debe revisar los nombres usados en las plataformas para que coincidan

## Usando NFTport

### 1 obtener la API de NFTport
Desde el sitio NFTport.xyz ir obtener api key gratis, resguardar

### 2 crear contrato NFT ERC721
- Desde el sitio ir a contracts > Deploy an NFT contract
- Owner address para la prueba 0xe53cc759f8b4ea9b655f777d2105518503f678f4
- Red para la prueba rinkerby (metamask chrome)
- código para crear contrato
*{
  "chain": "rinkeby", <cadena de deployment>
  "name": "Prueba Ubikalo", <Nombre de la coleccion/contrato>
  "symbol": "Pubk", <ticker del contrato>
  "owner_address": "0xe53cc759f8b4ea9b655f777d2105518503f678f4", <Wallet del creador>
  "type": "erc721" <tipo de contrato>
}*

==> respuesta del contrato generado
*{
  "response": "OK",
  "chain": "rinkeby",
  "transaction_hash": "0xf93025d7f12174a5de41ee743dda33747c233b9748f0f1074259f25d29aedcdb",
  "transaction_external_url": "https://rinkeby.etherscan.io/tx/0xf93025d7f12174a5de41ee743dda33747c233b9748f0f1074259f25d29aedcdb",
  "owner_address": "0xe53cc759f8b4ea9b655f777d2105518503f678f4",
  "name": "Prueba Ubikalo",
  "symbol": "Pubk"
}*


