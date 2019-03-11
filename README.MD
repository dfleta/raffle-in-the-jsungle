Raffle in the JSungle
=====================
#### Examen JS client-side DWEC Dual Febrero 2019

Jerry es un aficionado a coleccionar zapatillas de edición limitada. Para ello, ha de aplicar a las rifas que organizan las distintas tiendas de zapas.

Rifas hay muchas, y si introduce los datos por duplicado, lo descalifican.

Por ello, Jerry utiliza una sencilla app en el navegador donde señala si ha participado ya en dicha rifa o no.





## Instrucciones

- Crea un **repositorio en GitHub**.

- Realiza **_commits_** periódicamente mientras avanzas en el desarrollo de la aplicación y **publica tu solución en el repo creado en GitHub**. Sin estos dos requisitos, el examen no se corrige.

- No olvides configurar git en tu equipo para que el autor de los _commits_ seas tú.

- Envíame tu proyecto comprimido en un **ZIP** a gelpiorama@gmail.com

- Divide el proyecto en los módulos que estimes necesarios para garantizar la modularidad, la reutilización y el testing de los componentes.

## Programa principal y casos test

El _script_ principal `main.js` está compuesto por el código necesario para completar las historias de usuario.

Si sabes cómo hacerlo, este código invocará a los módulos con las funciones que necesites, de modo que al final has de generar un `bundle.js` que consuma el navegador. Puedes utilizar la herramienta que prefieras. Con `browserify` (y `npm`) es fácil. 

Se proporciona un módulo llamado `data.js` que exporta un objeto JS en notación `JSON` con los datos de la zapatilla y sus rifas. Simula el envío de datos por parte del servidor web.

Abrevia los casos test: hazlos mediante interacción con el usuario, comprobando la gestión adecuada de los eventos. También puedes completarlos leyendo el estado del  `localStorage`.


# Historias de usuario

## Visualizar las rifas

- Al cargar la página, se observan las rifas. Significa que el `data.js` con el `JSON` ha sido parseado.
- Un **botón verde** con el texto **ENTER RAFFLE** indica las que están aun abiertas.
- Un **botón rojo** con el texto **CLOSED** indica las que ya han cerrado.
- Un **botón gris** con el texto **ANNOUNCED** indica que aun no se han abierto.

El color de los botones se programa mediante lógica JS.

## Indicar la participación

- Cuando 


## Filtro por criterio de búsqueda

- Crea al objeto **Jerry**. 
- Tiene un `id` con el valor `"Jerry"`. 
- Posee una **colección de 4 monedas de R2-D2** en las que figura la inscripción "R2-D2". Las monedas son `string`.
- Encapsula el acceso a la colección de monedas con una función get.
- Cuando `habla` dice `"Tengo una colección de monedas antiguas raras!"`. Vídeo 1:54.
- Asegúrate de que es único.


### Clones

- Los clones de Rick no pueden tener su mismo `id` y entre ellos ha de ser distinto.
- Cada rick-clon tiene como `id` un número mayor que 137 que se genera automáticamente.
- Cada clon de Morty ha de tener como partner a un Rick.


## Mundos y dimensiones


### El universo

Los rick-clones se mueven por los distintos mundos y dimensiones pero todos forman parte del mismo universo.

- Crea un **objeto** JavaScript `universo` al que irás añadiendo todas las dimensiones y mundos por las que pasarán Rick y Morty. Lee el epígrafe _7.11 Array-Like Objects_ del libro del rinoceronte para la cuestión de la longitud ;)  

- Por cada mundo o dimensión, crea un `Array` que contenga a todos los personajes que accedan a él (cada personaje es un objeto).

- Crea la primera dimensión, el `Array` mundo `tierra`, mete en él a los tres objetos que has creado (Rick, Morty y Jerry) y añádelo al objeto `universo`.


## The portal gun

- Cada vez que Rick `dispara` la pistola de portales, se crea el acceso a una nueva dimensión / mundo (un `Array` para nosotros). Esa dimensión se añade al `universo` (y se actualiza su longitud). Vídeo 5:41.

- Cuando Rick, Morty y sus perseguidores cruzan el portal, has de eliminarlos del mundo actual y meterlos en el nuevo `array` mundo. Recuerda que siempre están en el objeto `universo`. Vídeo 5:41.

- Posee una función `scan` que lista el historial de dimensiones por las que ha pasado su propietario de la más reciente a la más antigua. Vídeo 4:45.
  + Cada dimensión es un `string` con su nombre.
  + La función `scan` usa la función `get historial()` para obtener el array de dimensiones.  


## Cruzando dimensiones

Es necesario que programes una función `cruzarDimension` para ser reutilizada cada vez que un personaje cruza de dimensión.

Puedes situarla en aquel componente que estimes más adecuado.

## Doofus Rick
 
- Es una mezcla entre Jerry y un clon de Rick, de modo que tiene todas las propiedades
de ambos.
- Las propiedades que comparten se quedan con el valor de las de Jerry.
- Tiene el `id` `"J-19-Z7"`.