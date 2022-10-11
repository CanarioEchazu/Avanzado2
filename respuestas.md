## Respuestas al Test de JavaScript

Recuerda que estas respuestas (o al  menos la mayoría) NO SON ABSOLUTAS. Es completamente válido (en la mayoría de casos) si tienes otras respuestas. Recuerda que podemos discutirlo en la sección de comentarios del curso. :D


## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve? 

Cajitas (espacios en memoria) donde podemos guardar informacion (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre tal. Mientras que inicializar (o reinicializar) es asignarle un valor a esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?

En caso de variable number, el signo + suma.
Si es string el signo + agrega a la cadena de string.

- ¿Cuál operador me permite sumar o concatenar?

+

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre string
- Apellido string
- Nombre de usuario en Platzi string
- Edad number
- Correo electrónico string
- Mayor de edad boolean
- Dinero ahorrado number    
- Deudas number



### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.
```js
let nombre = 'Dario';
let apellido = 'Echazu';
let usuario = 'darioechazu';
let edad = 52;
let correo = 'darioechazu@hotmail.com';
let mayorEdad = true;
let dineroAhorrado = 270000;
let deudas = 38000
```


### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```js
let nombreCompleto = (nombre +" "+apellido);
let dineroReal = dineroAhorrado - deudas;
```


## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

Es un método que vamos a reusar en cualquier instante que se llame, y entrega una respuesta.
```js
function nombreCompleto (name,lastname){
    return name+" "+lastname;
}

```


- ¿Cuándo me sirve usar una función en mi código?
para llamar instrucciones que reiteramos.

Nos sirve cuando tenemos variables o bloques de código muy parecidos ( con cambios que podrían ser parámetros y argumentos) que podemos encapsular para resultar más de una vez en el futuro.

También nos sirve para ordenar y mejorar la legibilidad de nuestro código.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

las funciones reciben parámetros cuando las creamos. Y les enviamos arguentos cuando las ejecutamos.


### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name +" "+ lastname;
const nickname = "juandc";

function saludo(completeName,nickname){
    return console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
}
saludo(completeName,nickname);
saludo('Dario Echazu','Canario');

function saludo2(name,lastname,username){
        return console.log("Mi nombre es " + name + " " + lastname + ", pero prefiero que me digas " + username + ".");
}
saludo2('Dario','Echazu','Canario');

```


## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?

Son las forma en que ejecutamos un bloque de codigo u otro dependiendo de alguna condición o validación.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

if (else y else if),switch.

Las diferencias entre if y switch:
El condicional IF (con else y else if) nos permite hacer validaciones completamente distintas (si así queremos) en cada vallidación o condicional.

En cambio en SWITCH todos los cases se comparan con la misma variable o condición que definimos en el switch.

- ¿Puedo combinar funciones y condicionales?

Si. Las funciones puede encapsular cualquier bloque de código, incluyendo condicionales.


### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```
```js
function suscripcion (tipoDeSuscripcion) {
    if (tipoDeSuscripcion == 'Free'){
        console.log("Solo puedes tomar los cursos gratis");
        return;
    } else if(tipoDeSuscripcion == 'Basic'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        return;
    } else if (tipoDeSuscripcion == 'Expert'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    } else if (tipoDeSuscripcion == 'ExpertPlus'){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
    }
}

```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏


## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?

Es la forma de ejecutar un mismo bloque de codigo, hasta que cummpla una condicion.

- ¿Qué tipos de ciclos existen en JavaScript?

While, for, do while.

For nos obliga a cumplir una condicion para poder ejecutar el bloque.
While, se ejecuta desde el incio y despues se fija la condicion para terminar el bloque.


- ¿Qué es un ciclo infinito y por qué es un problema?

Es cuando nunca llega a la condicion de cierre.

- ¿Puedo mezclar ciclos y condicionales?

Si.
Aunque los ciclos son una especie de condicionales, nada nos impide agregar más condicionales dentro del código.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```

```js

let i = 0;
while (i<5){
    console.log("El valor de i es: " + i);
    i++;
}

let i = 10;
while(i >= 2){
    console.log("El valor de i es: " + i);
    i--;
}


```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```js

let respuesta = prompt('cuanto es 2 + 2? ');
while (respuesta != '4' ){
   let pregunta = prompt ('Cuanto es 2 + 2?');
   respuesta = pregunta;
}
alert('Felicitaciones !!! ');

```

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?

Es una lista de elementos.

```js
const array = [1, 'letras', true, false,];
```

- ¿Qué es un objeto?

Es una lista de elementos PERO cada elemento tiene un nombre clave.
 ```js
 const objeto = {
    nombre: 'Dario',
    edad: 52,
    comidasFavoritas: ['Pollo frito','vegetales'],
 };
 ```
 o

 ```js
Object.values(objeto);
 ```

 Entonces como convertir un objeto en array?

 ```js
 const arr = Object.values(objeto);   
 // aqui los valores de las propiedades
 // del objeto en valores del array arr. 
 ```

- ¿Cuándo es mejor usar objetos o arrays?

Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demás (la regla se puede incumplir). Mientras que en un objeto cuando los nombres de cada elemento, son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Sí.
Los arraays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js

function mostrarPrimero (array){
   console.log(array[0]);
}
```


### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).
```js
function mostrarTodos (array){
    for (let i=0; i<array.length ; i++  ){
        console.log(array[i]);
    };
};

```


### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
```js
 const objeto = {
    nombre: 'Dario',
    edad: 52;
    comidasFavoritas: ['Pollo frito','vegetales'],
 };
function mostrarObjetos(objeto){
    for (i=0;i<objeto.length){
        
    }
}

/** 
 * Ahora voy a crear una nueva funcion 
 * para que muestre en un array, 
 * todos los valores del objeto.
*/

function mostrarTodosObjeto (objeto){
    const arr = Object.values(objeto);
    for (let i=0; i<arr.length ; i++  ){
        console.log(arr[i]);
    };
};

```

```js
/***
 * VIENE DE LA LINEA 135
 * EJERCICIO BONUS
 * 
 * */

function suscripcion (tipoDeSuscripcion) {
    if (tipoDeSuscripcion == 'Free'){
        console.log("Solo puedes tomar los cursos gratis");
        return;
    } else if(tipoDeSuscripcion == 'Basic'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        return;
    } else if (tipoDeSuscripcion == 'Expert'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    } else if (tipoDeSuscripcion == 'ExpertPlus'){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
    }
}

// Tenemos la siguiente funcion

function () {
    if (){

    }else if (){

    }
        // ...
}

// entonces si tenemos una respuesta valida

function () {
    if (basic){
        // queremos aqui temine la funcion
        return;
            // y si no econtro la respuesta, va a los
            // siguientes else if
    }else if (){

    }
        // ...
}

```

Entonces el ejercicio bonus queda asi.

```js
function conseguirTipoSuscripcion(suscripcion) {
    if (suscripcion == 'Free'){
        console.log("Solo puedes tomar los cursos gratis");
        return;
    }  
    
    if(suscripcion == 'Basic'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        return;
    }
    
    if (suscripcion == 'Expert'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        return;
    } 
    
    if (suscripcion == 'ExpertPlus'){
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        return;
    }

    console.warn ('Este tipo de suscripcion no existe');
}

conseguirTipoSuscripcion('Basic')

```
* * * * * * * * * 
BONUS, viene desde 175
* * * * * * * * *
Con un solo condicional.

Para hacerlo, hay que hacer una clase de objeto,
asi repetimos las veces que fuera necesario

```js

const tiposDeSuscripciones = {
    free: "Solo puedes tomar los cursos gratis",
    basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
    expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
    expertPlus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año",
};

tiposDeSuscripciones.free;
tiposDeSuscripciones['free']; // ambos funcionan igual.

tiposDeSuscripciones.basic;

tiposDeSuscripciones.expert;

tiposDeSuscripciones.expertPlus;

// podemos crear otra variable

const ejemploSuscripcion = 'free';

tiposDeSuscripciones[ejemploSuscripcion];

```

Ahora entonces vamos a crear la FUNCION

```js
function conseguirTipoSuscripcion (suscripcion){
    if (tipoDeSuscripciones[suscripcion]) {
        console.log(conseguirTipoSuscripcion[suscripcion]);
    }

    console.warn ('Este tipo de suscripcion no existe');

