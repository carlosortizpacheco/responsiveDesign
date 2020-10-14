![](https://img.shields.io/static/v1?label=school&message=platzi&color=green)
![](https://img.shields.io/static/v1?label=course&message=CursoDeResponsiveDesign&color=green)

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
- `<link rel='stylesheet' href='css/media.css' media='screen and (max-width:768px)'>`; esta forma se agrega en el head del HTML.
- `@media screen and (max-width:768px){}`; esta forma se agrega dentro del archivo css.
- margin-collapsing; se arregla utilizando un `padding` o un `border`.

## CSS Positions
- static, relative, absolute, fixed, sticky
- Por default los elementos son `static`.
- `position:relative;` el elemento en su espacio original se mantiene aunque lo haya movido por top, left.
- `position:absolute;` el elemento se mueve respecto al padre. Aqui no se respeta su espacio. Para que respete a los padres debemos colocarle `position:relative;`
- `position:sticky`; el elemento actua como fixed, con la diferencia que hay que indicarle en que momento se vuelve fixed, por ejemplo con `top:0;`.
- Si le aplico a un elemento con position:absolute, los atributos de top:0; left:0; right:0; y bottom:0; el elemento deja de respetar el padding/margin de su contenedor y abarca toda la pantalla. Util para no modificar padding/margin.

## Videos HTML5
``` 
<video src={source} width="{width}" height="{height}" controls autoplay poster="{image.jpg}"></video>
```
- iframe; se trae video u OTRO contenido de otras plataformas (páginas). En youtube le doy compartir y hay una opción para copiar codigo HTML.

- Para centrar de manera vertical sin utilizar flex, podemos usar entonces la propiedad line-height, esta propiedad debe tener le mismo valor que la altura del contenedor para que se centre en la vertical.


## Añadiendo javascript
```
const nombreVar1 = document.querySelector('.clase')
const nombreVar2 = document.querySelector('#identificador')

nombreVar2 = addEventListener('click',nombreFuncion)

function nombreFunction () {
  if( menu.classList.contains('nombreClase') ){
    menu.classList.remove('nombreClase')
  } else {
    menu.classList.add('nombreClase')
  }
}
```
- medias queries con JS
```
const nombreVar3 = window.matchMedia('screen and (max-width:768px)')
nombreVar3.addListener(nombreFuncion)
function nombreFuncion(event){
  if(event.matches) {
    document.querySelector('{nombreClase}').addEventListener('click',{nombreFuncion})
  } else {
    document.querySelector('{nombreClase}').removeEventListener('click',{nombreFuncion})
  }
}

```

