### Comentarios Generales

Yaneri, primero felicitarte por tu trabajo. Tu portfolio quedó muy lindo, se nota el esfuerzo por hacerlo realmente tuyo y a nivel personal me gusta mucho tu eleccion de colores, imagenes, como lo adaptaste para que te reflejara mejor. 

Entiendo que no llegaste tan bien con el tiempo, por lo que noto que algunas consignas no estan incumplidas. El responsive no funciona correctamente, en parte por algunos errores en el CSS que te voy a comentar mas en detalle. Tu repositorio no cuenta con un README, ni tu web esta deployada. No sé bien cuáles de estas cosas fueron por falta de tiempo, pero tengo que contemplar de todos modos el grado de cumplimiento de las consignas en la nota final. 

Dejo algunos comentarios generales sobre tu trabajo: 

- Tu HTML esta muy prolijo, ordenado y bien tabulado. Usas correctamente las etiquetas semánticas, no agregaste mucho código de más (algo que suele ser habitual al comenzar) y se nota el esfuerzo por dejarlo lo más claro posible. 

- Tu CSS esta bien tabulado y muy bien ordenado. Se nota que le pusiste trabajo. Aprecio que te hayas tomado el trabajo de ordenar los estilos generales arriba de todo y que tu CSS vaya siguiendo la estructura de tu web. A veces sin embargo dejas algunos saltos de linea extra que dificultan la lectura. Es decir, muchas veces dejas espacios de mas como aqui:

```css
.final-footer{
    display: flex;
    justify-content: center;
    margin-top: 40px;
    margin-bottom: 40px;
    list-style-type: none;
    color: black;
        
}
.footer li {
    margin: 20px;
    color: black
        
        
}
```

Cuando lo correcto seria hacerlo de esta manera:

```css
.final-footer {
    display: flex;
    justify-content: center;
    margin-top: 40px;
    margin-bottom: 40px;
    list-style-type: none;
    color: black;
}

.footer li {
    margin: 20px;
    color: black;        
}
```

- Tus nombres de clases son excelentes, mucho mejores de lo que se espera a esta altura. Cumplis bien el requisito de que sean descriptivos en un sentido funcional: describir que es un elemento y qué hace, no necesariamente como se ve. Quizá la única excepción sea la sección "hola". En unos meses tal vez ya no quieras que diga "Hola", pero la clase en el código seguirá siendo "hola": no es bueno depender del contenido para los nombres de clases (ni colores, o formas), sino describir funcionalidades. Esa seccion es la seccion de presentación, o la sección principal: esos nombres son más adecuados para describirla. 

- Ocasionalmente usas alturas fijas para las secciones, y eso no es buena práctica: salvo cuando se trata de elementos pequeños (como tarjetas o botones), la altura de un elemento tiene que estar dada por sus contenidos. Tambien noto que usas mucho height 100%, pero eso no tiene mucho sentido para una seccion: es una orden que no se va a aplicar. 

- La conversión a mobile tiene muchos problemas, y algunos de ellos estan relacionados a erorres en tu css. Tu Visual Studio va a marcarte estos errores subrayandolos con rojo: no dejes de prestarles atencion, ya que impiden que tu CSS funcione y pueden ser muy confusos. El mas grave es este
```css
@media(min-width: 600px) y (max-width:900px) {
  ```

  La palabra correcta para unir dos medidas en una media query es "and", en ingles. Fijate que Visual Studio te subraya ese "y". Nunca deberias tener nada subrayado en tu css, ya que eso significa que los estilos no se van a aplicar. 

- Noto tambien que tenes cierta confusion respecto del uso de archivos para subir a github. Cuando creamos un repo de git, lo incorporamos dentro de una carpeta, como en tu caso la carpeta portfolio. Cuando subamos eso a github, solo se subirán los contenidos de esa carpeta. En este caso estas usando imágenes que estan adentro de *otra* carpeta en tu computadora: la carpeta "clase 6". Ni yo, ni nadie, va a poder ver estas imagenes salvo vos, porque estan en otra carpeta de tu computadora. Siempre a partir de ahora recordá que **todos** los recursos que uses en una web tienen que estar en la misma carpeta con los demás archivos. 

- Noto que no se ve tu icono hamburguesa, y eso es porque a pesar de haber usado la etiqueta correcta <i class="fas fa-bars fa-2x"></i>, no agregaste el link a Font Awesome en el <head> de tu HTML. Te recuerdo que este link es necesario para que aparezca: 

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.0/css/all.min.css">
```

- Algo similar ocurre con la tipografia: utilizas la tipografia Segoe UI, que solo esta disponible en computadoras que usan Windows, por lo que yo no puedo ver tu diseño tal como lo esperas. Recorda que cuando trabajamos con tipografias debemos importarlas usando import en CSS. 

- Tenés solamente dos commits hechos en git. Pedimos que se acostumbren desde ahora a trabajar con muchos commits ya que son muy importantes cuando trabajamos en equipo, y en el medio laboral. Cuando compartimos el código con otras personas, muchas veces podemos cometer algunos errores o tener que volver atrás un cambio en específico: ir haciendo commits seguido, e incluir nombres descriptivos en los commits, permite encontrar rápidamente el cambio que necesitamos, facilitando así la tarea. Lo ideal es ir trabajando por secciones: "agrego header", "agrego seccion principal", "agrego los estilos para celular", "corrijo estilos para tablet", etc. 

Dejo algunos comentarios específicos a lo largo de tu código. 

Notarás, viendo esos comentarios, que comento muchisimas cosas y soy bastante quisquillosa (por no usar otra palabra no tan profesional...) con las correcciones. La idea es comentarte todo lo que vea para que puedas mejorar tu código. 


### Nota final: 7

Nota desagregada: 
✔️ Estructura correcta de documento HTML --> con observaciones. 
✔️ Respeta la consigna --> con observaciones
✅ Respeta el diseño dado 
❌ Responsive funciona correctamente
✅ Código bien indentado. 
✅ Comentarios que permiten mejorar la legibilidad del código.
✅ Uso correcto de etiquetas semánticas.
✔️ Buenos nombres de clases ---> con observaciones
✅ Reutilización de estilos.
✔️ Código CSS ordenado --> con observaciones
❌ Commits con mensajes adecuados.
