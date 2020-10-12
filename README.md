# responsiveDesign
curso de Platzi para mejorar en el responsive design

## Patrones en Reponsive Design:
- Mostly Fluid (cuando llegue a cierto tamaño empieza a ser responsive, sino se mantiene constante).
- Colocación de columnas (utiliza todo el tamaño de la pantalla).
- Layout shifter (navbar en el lado izquierdo, en mobil el navbar parasá a la parte superior).
- Tiny tweaks (diseño queda igual, cambia el tamaño de los elementos -texto,imágenes,etc.-).
- Off canvas (tipo carrusel, hay elementos fuera de lo que vemos).
- **viewport**, área visible del navegador.
- **Mobile first**, empezar un website desde la menor resolución soportada.
- **Desktop first**, empezar un website desde la mayor resolución soportada.
- utilizar google analytics para saber si llegan mas a mobile o a desktop y a partir de ahi mejorar el diseño en esa vista.
- soporte minimo que debe de tener el responsive design 320px
-`<meta name='viewport' content='width=device-width, initial-scale=1'>`

## Unidades relativas de medida
- Porcentaje, longitud referente al tamaño de los elementos padre.
- em, unidad relativa al tamaño de fuente especificada más cercana.
- rem, unidad relativa al tamaño de fuente especificada en el ancestro mas lejano (html o body)
- vw/vh, unidad relativa con respecto al viewport.


## Media Queries
- `@media {mediaType} and ({max-width:768px}) {}`
- mobile first queries
  - `@media screen and (min-width:320px) {}`
  - `@media screen and (min-width:480px) {}`
  - `@media screen and (min-width:768px) {}`
  - `@media screen and (min-width:1024px) {}`
- desktop first queries
  - `@media screen and (max-width:1024px) {}`
  - `@media screen and (min-width:768px) {}`
  - `@media screen and (min-width:480px) {}`
  - `@media screen and (min-width:320px) {}`

### Formas de incluir media queries
- `<link rel='stylesheet' href='css/media.css' media='screen and (max-width:768px)'>`; esta forma se agrega en el head del HTML
- `@media screen and (max-width:768px){}`; esta forma se agrega dentro del archivo css

- margin-collapsing; se arregla utilizando un `padding` o un `border` 
