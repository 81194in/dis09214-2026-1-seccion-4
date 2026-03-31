# sesion-03

viernes 27 marzo 2026

## operador modulo

## cursor

primero hicimos que el cursor no fuera visible cuando estuviéramos sobre la canvas, usando la función `noCursor()`. esta función la incluimos dentro de setup() para que solamente ocurra una vez y al principio del programa.

## práctica profesional de vania paredes

vania paredes es la ayudante del curso, y hoy mostró su trabajo en la práctica profesional que está desarrollando este semestre en la empresa chilena Local Variable Studio <https://www.localvariablestudio.com/>, fundada y dirigida por guillermo ,ontecinos.

esta semana vania ha estado exhibiendo en un proyecto interactivo, consistente en una cámara que detecta el movimiento de las personas y superpone varias capas de video con distintos desfases de tiempo, logrando una imagen que contiene varios momentos en uno.

este proyecto está siendo exhibido en el centro cultural gabriela mistral, como una obra inspirada la ópera splitting/absence del artista sokio, con textos de gordon matta-clark.

## primera parte de la clase

ojo este código necesita la imagen subida al proyecto.

<https://editor.p5js.org/montoyamoraga/sketches/fF0VBakX3>

```javascript
// previa solemne 1

// let es para declarar
// a continuacion viene el nombre
// de la variable
// ese nombre debe ser UNICO
let tamano;


// setup() corre solo una vez
// y al principio de los tiempos
function setup() {
  // createCanvas() necesita dos params
  // primero x o ancho
  // segundo y o altura
  createCanvas(windowWidth, windowHeight);
  
  // console.log permite imprimir en consola
  // acepta varios params separados por ,
  console.log(windowWidth, windowHeight);
  
  // noCursor();
  
  // valor maximo de tasa de refresco
  // se mide en cuadros por segundo
  frameRate(10);
  
  // condiciones de inicio del dibujo
  tamano = 10;
  
  cursor("donpancho.png");
}


// draw() ocurre despues de setup()
// en bucle y se repite hasta el fin
function draw() {
  background(255, 0, 255);
  
  // tamano aumenta
  tamano = tamano + 2;
  
  stroke(0, 255, 255);
  fill(120, 0, 0);
  // noStroke();
  strokeWeight(10);
  
  // posX, posY, anchoX, altoY
  ellipse(
    windowWidth/2,
    windowHeight/2,
    tamano,
    tamano
  );
  
  stroke(0, 0, 255);
  fill(100, 200, 10);
  strokeWeight(1);
  
    // linea que va entre arriba izquierda
  // y abajo derecha
  line(
    0, 0,
    windowWidth, windowHeight);
  
    line(
    windowWidth, 0,
    0, windowHeight);
  
  
  // https://p5js.org/reference/p5/arc/
   // arc(50, 50, 80, 80, 0, PI + QUARTER_PI, CHORD);
  arc(mouseX, mouseY, 20, 20, PI + QUARTER_PI, 0, CHORD);
  
  
  ////////////////////////////////
  // la funcion modulo
  // divide y te responde el resto
  ////////////////////////////////
  
  console.log(frameCount);
}
```

## segunda parte de la clase

ojo este código necesita la imagen subida al proyecto.

<https://editor.p5js.org/montoyamoraga/sketches/yIMUrukay>

```javascript

// solemne 1

// minimos

// 8 figuras 2D en total
// incluyendo
// 3 elipses
// 3 rectangulos

// 3 lineas

// 10 colores distintos
// al menos dos que varíen en el tiempo

// un cursor distinto al original

// cada linea de comando
// con referencia al link de la referencia de p5.js
// con explicacion textual de los parametros

// dos imagenes
// una se mueve, una no se mueve

//https://p5js.org/reference/p5/loadImage/

let javiera;

function setup() {
  createCanvas(400, 400);
  javiera = loadImage("javieraasi.jpg");
}

function draw() {
  background(220);
  image(javiera,
        0, frameCount,
        100, windowHeight);
  image(javiera,
        100, 50,
        100, windowHeight);
  image(javiera,
        200, 100,
        100, windowHeight);
}
```
