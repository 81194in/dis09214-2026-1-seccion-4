# sesion-02

viernes 20 marzo 2026

## sistemas de coordenadas 2D

en p5.js se usa por defecto un sistema de coordenadas cartesianas, donde el punto (0, 0) está en la esquina superior izquierda de la pantalla.

el eje x aumenta hacia la derecha y el eje y aumenta hacia abajo.

## obra de vania paredes que mostró en clases

aquí el código en javascript para copiar y pegar, y también en mi croquera de p5.js

<https://editor.p5js.org/montoyamoraga/sketches/wf_g0bNRg>

```javascript
// let es para declarar
let x = 0;
let direccion = 1;

function setup() {
  //página de 600 de ancho y 400 de alto
  createCanvas(1000, 400); 
  noCursor();
}

function draw() {
   background(135, 206, 235);
  // = es para asignar valor
  // cada vez que draw corra, sumale 1 al valor de x
  x = x + 1 * direccion;
  //Cielo azul
  if (x > 400) {
      direccion = -1;
    background(0, 0, 0)
  }
  if (x < 0) {
    direccion = 1;
     background(0, 0, 0)
  }
  
  background(135, 206, 235);
  //sol a la derecha arriba
  //Sol amarillo con orilla naranja
  fill("yellow");
  stroke("orange");
  strokeWeight(20);
  
   circle(300, x, 100);
  //Pasto
  stroke(0);
  strokeWeight(0);
  fill("green");
  rect(0, 250, 600, 150);

  
  textSize(75)
  text("🐛", mouseX, mouseY);
  text("🌷", 150, 250);
  
  textSize(250)
  text("🏡", 300, 250)
}
```

## código de primera mitad de la clase

<https://editor.p5js.org/montoyamoraga/sketches/aTgiP97wG>

```javascript
let x = 0;

function setup() {
  // el primer parametro
  // es la coordenada X
  // el segundo es Y
  createCanvas(400, 400);
}

function draw() {
  x = x + 1;
  background(220, 150, 0);
  noStroke();
  ellipse(x, 100, 20, 20);
}


// function limpiarCasa()  {
  // trapear();
  // encerar();
  // alimentarRingo();
  // barrer();
// }

```

## segunda parte de la clase

<https://editor.p5js.org/montoyamoraga/sketches/obUKbIOOK>

```javascript
// let es para declarar
// declarar en lenguaje actual
// la gente lola le llama manifestar
// despues de let viene el nombre
// puedo hacer el nombre que quiera
// despues viene = que es para asignar valor
let nombreBacan;
let x = 0;
let y = 100;
let direccion = 1;

function setup() {
  // el primer parametro
  // es la coordenada X
  // el segundo es Y
  createCanvas(400, 400);
}

function draw() {
  // = es para asignar valor
  // nombre = valor
  // esto sobreescribe el valor
  // olvidate todo
  // deja tu vida anterior atras
  // y ahora solamente hay un presente
  // el valor de la derecha
  x = x + 10 * direccion;
  y = x/2;
  
  if(x > 400){
     direccion = -1;
    background(
      random(255),
      random(255),
      random(255)
    );
  }
  if (x < 0) {
     direccion = 1;
    background(
      random(255),
      random(255),
      random(255)
    );
  }
  
  // background(220, 150, 0);
  noStroke();
  ellipse(x, y, 20, 20);
}


// function limpiarCasa()  {
  // trapear();
  // encerar();
  // alimentarRingo();
  // barrer();
// }

```
