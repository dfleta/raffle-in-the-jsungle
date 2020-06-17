Raffle in the JSungle
=====================
#### Examen JS client-side DWEC Dual Junio 2020

Jerry es un aficionado a coleccionar _sneakers_ de edición limitada. Para ello, ha de aplicar a las rifas que organizan las distintas tiendas de zapas.

Rifas hay muchas. Si no lleva la cuenta de en cuáles se ha apuntado, corre el riesgo de introducir los datos dos veces y que lo descalifiquen.

Por ello, Jerry utiliza una sencilla app en el navegador donde señala si ha participado ya en dicha rifa o no.

El comportamiento de la app es como este:

https://www.soleretriever.com/raffles/air-jordan-6-retro-hare-ct9529-062

No se exige que el maquetado de la página quede igual. **Asegúrate de que el comportamiento de la app es igual**. Haz uso del inspector del navegador para hacerte con los estilos CSS y componentes visuales de la página que necesites, si quieres.

**Se proporciona un módulo llamado `data.js` que exporta un objeto JS en notación `JSON` con los datos de la zapatilla y sus rifas**. Simula el envío de datos por parte del servidor web al hacer peticiones GET y POST.


## Instrucciones

- Crea un **repositorio privado en GitHub** y compártelo con dfleta.

- Realiza **_commits_ periódicamente** por cada unos de los items que consigas implementar en cada historia de usuario.  **Publica tu solución en el repo creado en GitHub**. **Sin estos dos requisitos, el examen no se corrige**.

- No olvides configurar git en tu equipo para que el autor de los _commits_ seas tú.

- Puedes desplegar la app en el servicio que quieras.

- Envíame tu proyecto comprimido en un **ZIP** a gelpiorama@gmail.com

- Si sabes cómo hacer luego un _bundle_ para el navegador, divide el proyecto en los módulos que estimes necesarios para garantizar la modularidad, la reutilización y el testing de los componentes.

- **NO se puede utilizar ningún framework (ni para el CSS ni para la lógica)**. Nada de VUE, ReactJS, Angular ni similares; tampoco superconjuntos de JS como Typescript y similares; tampoco Bootstrap, Tailwind para la presentación ni similares.

- **Sólo se puede usar Vanilla JS**, es decir, el que hemos visto en clase, y CSS 3.
 

## Programa principal y casos test

El _script_ principal `main.js` está compuesto por el código necesario para completar las historias de usuario.

Si sabes cómo hacerlo, este código invocará a los módulos con las funciones que necesites, de modo que al final has de generar un `bundle.js` que consuma el navegador. Puedes utilizar la herramienta que prefieras. Con `browserify` y `npm` es fácil. Puedes utilizar el sistema que conozcas y automatizar las tareas con _Grunt_, _Gulp_, _Webpack_ o el que sea que utilices en tu empresa.

**Recuerda que se proporciona un módulo llamado `data.js` que exporta un objeto JS en notación `JSON` con los datos de la zapatilla y sus rifas**.Simula el envío de datos por parte del servidor web al hacer peticiones GET y POST.

Abrevia los casos test: hazlos mediante interacción con el usuario, comprobando la gestión adecuada de los eventos. También puedes completarlos leyendo el estado del  `localStorage`.


# Historias de usuario

## Clean Code

Intenta que el código cliente JS satisfaga las buenas prácticas que hemos tratado en clase (modularidad, asincronía, gestión de eventos, etc.). 

## Visualiza la zapatilla 

Al cargar la página, se observa el modelo de zapatilla y sus datos, que provienen del `data.js` en el objeto `shoe`.

Intenta que el formato de la fuente sea parecido en tamaño.

No es necesario que metas las llamadas a la API de StockX. 


## Visualiza las rifas

Los datos se obtienen del fichero `data.js`, del objeto `raffles`.

- Al cargar la página, se observan las rifas. Significa que el `data.js` con el `JSON` ha sido parseado.
- Un **botón verde** con el texto `Open Raffle` indica las rifas que están aun abiertas, en función de la fecha del día y de la fecha en la que cierran.
- Una **etiqueta** con el texto `closed` indica las que ya han cerrado. Los botones `Open Raffle` y `Mark done` se formatean en gris.
- El **nombre de la tienda está en negrita**

Intenta que la disposición de las rifas sea lo más parecida a la de la app original. Puedes usar un flex-box o la ñapa que se te ocurra para salir del paso. **No pierdas mucho tiempo en esto**.


## Visita la tienda

- Al hacer **clic sobre el nombre y descripción de la tienda o del botón Open Raffle**, se abre una nueva pestaña del navegador con la página de la `url` indicada en el `data.js`
- Al situar el puntero del ratón encima de calquiera de estos tres botones (sin clic), el comportamiento es como el que muestra la app real (el botón cambia de color). Intenta simularlo. No es necesario que sea idéntico.

## Indica la participación

- Cuando Jerry, por su cuenta, participa en la rifa, hace clic sobre el botón `Mark done`. El **texto del componente cambia** a `Entered` y el relleno del botón cambia a gris. Al hacer clic de nuevo, cambia al texto y color original `Mark done`. Puedes obtener el icono directamente de la página original haciendo uso del inspector del navegador.

- Este dato de **configuración de la app se guarda de manera local** en el navegador de Jerry, de modo que **cuando recarga la página**, puede consultar las rifas en las que ya ha entrado y en cuáles no.


## Filtro por criterio de búsqueda

A veces hay decenas de rifas, así que Jerry necesita filtrarlas en función de ciertos criterios.

Crea un filtro que permita filtrar las rifas por:

- Envío postal (_shipping_) o recoger en tienda (_Pick-up_)
- Tipo de rifa _In-Store_, _Online_, _Social_, _In App_
- País de la tienda.


## ¡Me ha tocado!

Veamos si tu código es _Open-Closed_.
Añade una nueva funcionalidad en cada rifa que te permita indicar si has tenido suerte o no (_get an L_). Implementa un componente visual con una ele mayúscula `L` en amarillo en caso de perder la rifa o una `W` en caso de ganarla.
