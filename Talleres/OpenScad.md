---
title: Diseño de piezas con OpenScad
description: 
published: true
date: 2020-06-20T18:19:48.836Z
tags: 
editor: undefined
dateCreated: 2020-06-18T16:37:12.795Z
---

## Introducción

**¡Bienvenid@s!**

En este curso tomamos el contenido de los cursos de **[Obijuanacademy]()** como punto de partida para desarrollar una experiencia aprendizaje colaboraivo de Openscad.

* Openscad
* Flujos de trabajo
* Herramientas para dar potencia al Openscad.

<br>

### ¿Qué es OpenScad?

OpenSCAD es un programa para crear modelos 3D por computadora (CAD). Es gratuito y está disponible para Linux/Unix, Windows y Mac OS.

Los modelos se diseñan escribiendo una serie de instrucciones en texto plano que es compilada y visualizada por el programa en un entorno tridimensional.

Así tenemos un control total sobre el proceso de modelado porque podemos cambiar fácilmente cualquier instrucción y realizar diseños definidos por parámetros configurables.

Dado a su naturaleza textual los archivos fáciles de compartir.

<br>

## Sesión 1. Primeros pasos con OpenScad

<br>

### 1. Cubo "Hola mundo"

<br>

#### Video Tutorial

**[![Video Tutorial]()](http://www.youtube.com/watch?v=xvhbrUSQRTc)**

<br>

#### **Programa**

```
//-- Cubo Hola Mundo
 cube([10,10,10]);
```

<br>

#### Pasos a realizar:

* Abrimos OpenScad.

* Escribimos el código del programa.

* Pulsamos <kbd>F5</kbd> para visualizar el cubo en pantalla. Hemos creado un cubo de 10mm de arista.

* Con la '''rueda''' del ratón hacemos zoom.

* Manteniendo pulsado el <kbd>botón izquierdo</kbd> del ratón y moviendolo rotamos la vista del cubo.

* Manteniendo pulsado el <kbd>botón derecho</kbd> del ratón y moviendolo hacemos la traslación del punto de vista.

* Por último grabamos el programa OpenScad creado.

* Pulsamos <kbd>F6</kbd> para hacer una visualización con más definición.

* Exportamos la pieza al '''formato STL''' (view/export as STL).

* ¡¡El cubo está listo para ser impreso en una impresora 3D de código abierto!!

<br>

### 2. Traslaciones y rotaciones

**[![Video Tutorial]()](http://www.youtube.com/watch?v=QMsTnDUkJ1E)**

<br>

#### Programa

``` 
//-- Ejemplo de translación y rotación <br>
 //-- Traslación y rotación de un cubo
 rotate([0,0,30])
   translate([50,0,0])
     cube([20,20,20],center=true);
 //-- rotación de un cubo
 rotate([0,0,45])
   cube([20,20,10],center=true);
```

Las traslaciones y rotaciones se realizan con los operadores `translate()` y `rotate()` respectivamente.

<br>

### 3. Cilindros: la navaja suiza 

**[![Video Tutorial]()](http://www.youtube.com/watch?v=OdUgqYm5lXQ)**

<br>

#### Programa

```
 //-- Moneda
 translate([-50,0,0])
   cylinder(r=40/2, h=5, $fn=100);
 //-- Hexágono
 cylinder(r=40/2, h=5, $fn=6);
 //-- Triángulo equilátero
 translate([50,0,0])
   cylinder(r=40/2, h=5, $fn=3);
```



Se muestra la versatilidad de los **cilindros**. Cambiando el parámetro `$fn`, se puede hacer cualquier polígono regular.

<br>

### 4. Haciendo taladros

**[![Video Tutorial]()](http://www.youtube.com/watch?v=WJFqa7LUpmA)**

<br>

#### Programa
```
 //-- Rueda simple
 difference() {
   //-- Base de la rueda
   cylinder(r=50/2, h=5,$fn=100);
   //-- Taladro de 8mm
   cylinder(r=8/2, h=20,$fn=20,center=true);
 }
```

Utilización de la operación booleana `difference()` con los cilindros para perforar piezas.

<br>

### 5. Pegando piezas

**[![Video Tutorial]()](http://www.youtube.com/watch?v=UlM_N_HPhVk)**

<br>

#### Programa

```
 //-- Rueda con portaejes y taladro para el eje
 difference() {
   //-- Rueda
   union() {
     //-- Base de la rueda
     cylinder(r=50/2, h=5, $fn=100);
     //-- Portaejes
     cylinder(r=20/2, h=20, $fn=80);
   }
   //-- Taladro
   cylinder(r=8/2, h=80, $fn=30,center=true);
 }
```

<br>

Utilizamos la operación booleana `union()` para pegar objetos

<br>

## Sesion 2. Vislumbrando la potencia de OpenScad

<br>

### 6. Parametricemos

**[![Video Tutorial]()](http://www.youtube.com/watch?v=86PLSLyK3Bc)**

<br>

#### Programa

```
  //-- Parámetros de la rueda
  grosor = 5;
  diametro=50;
  diam_eje = 8;
  //-- Construcción de la rueda a partir de
  //-- los parámetros
  difference() {
    //-- Base de la rueda
    cylinder(r=diametro/2, h=grosor,$fn=100);
    //-- Taladro del eje
    cylinder(r=diam_eje/2, h=3*grosor,$fn=20,center=true);
  }
```

Rueda paramétrica: La rueda se define por unos parámetros, y luego se construye la rueda usando esos parámetros.

<br>

### 7. Modularízame!

**[![Video Tutorial]()](http://www.youtube.com/watch?v=irMSrEzh0JM)**

<br>

#### Programa

```
 module rueda_simple(grosor, diametro, diam_eje)
 {
   //-- Construcción de la rueda a partir de
   //-- los parámetros
   difference() {
     //-- Base de la rueda
     cylinder(r=diametro/2, h=grosor,$fn=100);
     //-- Taladro del eje
     cylinder(r=diam_eje/2, h=3*grosor,$fn=20,center=true);
   }
 } <br>
 rueda_simple(diametro=50, grosor=5, diam_eje=8);<br>
 translate([50,0,0])
   rueda_simple(diametro=40, grosor=20, diam_eje=10);
|}
```

<br>

Convertimos la rueda en un módulo para poder reutilizarla fácilmente.

<br>

### 8. Parámetros por defecto

**[![Video Tutorial]()](http://www.youtube.com/watch?v=Tf5NCHbjfqI)**

<br>

#### Programa

```
 module rueda_simple(grosor=5, diametro=40, diam_eje=8)
 {
   //-- Construcción de la rueda a partir de
   //-- los parámetros
   difference() {
     //-- Base de la rueda
     cylinder(r=diametro/2, h=grosor,$fn=100);
     //-- Taladro del eje
     cylinder(r=diam_eje/2, h=3*grosor,$fn=20,center=true);
   }
 }
 //-- Ejemplos de utilizacion del modulo Rueda simple
 //-- Rueda por defecto
 rueda_simple();
 translate([50,0,0])
   rueda_simple(grosor=20);
 translate([-50,0,0])
   rueda_simple(diametro=20, grosor=10);
```

<br>

Dando **parámetros por defecto** al módulo de la rueda simple para facilitar su utilización.

<br>

### 9. Usando módulos

**[![Video Tutorial]()](http://www.youtube.com/watch?v=wZt9ROx2_Co)**

<br>

#### Programa

```
 //-- Ejemplo sencillo de como utilizar los modulos
 use <rueda_simple.scad>
 //-- Chasis del cohe
 translate([30,0,0])

cube([100,60,10],center=true);
 //-- Rueda delantera izquierda
 translate([0,-30,0])
  rotate([90,0,0])
    rueda_simple();
 //-- Rueda trasera izquierda
 translate([60,-30,0])
   rotate([90,0,0])
     rueda_simple(grosor=20, diametro=50);
 //-- Lado derecho del coche. Es simetrico con respecto
 //-- al izquierdo
 mirror([0,1,0]) {
   //-- Rueda delantera derecha
   translate([0,-30,0])
     rotate([90,0,0])
       rueda_simple();
   //-- Rueda trasera derecha
   translate([60,-30,0])
     rotate([90,0,0])
       rueda_simple(grosor=20, diametro=50);
 }
```

<br>

Utilización del módulo de la rueda simple para construir un coche sencillo

<br>

### 10. Repitiendo tareas

**[![Video Tutorial]()](http://www.youtube.com/watch?v=J5nCIrlQj_g)**

<br>

#### Programa

```
 drill=4;
 h1=10;
 d=10;
 n = 20;
 for (i=[0:n-1]) {
   translate([i*d,0,0])
    cylinder(r=drill/2, h=h1, $fn=20,center=true);
 }
```

<br>

Se crean **multiples cilindros** utilizando un **bucle for**

<br>

## Sesion 3. Ejemplo 1: Piezas de mecano básicas.

En este bloque utilizaremos lo que hemos aprendido para **cerrar el ciclo de diseño**. Diseñaremos una **pieza de mecano simple** y la **imprimiremos** en la impresora 3D opensource. Durante el diseño se introducen también algunos conceptos nuevos.

<br>

### 11. Pieza de mecano parametrizable I

**[![Video Tutorial]()](http://www.youtube.com/watch?v=YHg5QApmFO4)**

<br>

#### Programa

```
 drill=3;
 d=10;
 n = 4; 
 lx = n*d;
 anchura = 10;
 grosor = 3;
 difference() {
   //-- Cuerpo de la pieza
   cube([lx,anchura,grosor],center=true);
   //-- Taladros
   translate([-lx/2+d/2,0,0])
     for (i=[0:n-1]) {
       translate([i*d,0,0])
         cylinder(r=drill/2, h=grosor+5, $fn=20,center=true);
   }
 }
```

<br>

En este ejemplo construimos la pieza de mecano básica.

<br>

### 12 Pieza de Mecano parametrizable II

**[![Video Tutorial]()](http://www.youtube.com/watch?v=2u9gaYx6j7w)**

<br>

#### Programa

```
 module pieza_mecano(n=4, drill=4, d=10, anchura=10, grosor=3)
 {
   //-- Calcular al longitud de la pieza
   lx = n*d;
   //-- Construir la pieza
   difference() {
     //-- Cuerpo de la pieza
     cube([lx,anchura,grosor],center=true);
     //-- Taladros
     translate([-lx/2+d/2,0,0])
       for (i=[0:n-1]) {
         translate([i*d,0,0])
           cylinder(r=drill/2, h=grosor+5, $fn=20,center=true);
      }
   }
 }
 //-- Ejemplos de utilizacion
 pieza_mecano();
 translate([0,20,0])
   pieza_mecano(n=2);
```

<br>

La pieza de mecano se modulariza y se asignan parámetros por defecto.

<br>

### Depurando piezas

**[![Video Tutorial]()](http://www.youtube.com/watch?v=X34wjwg3HeU)**

<br>

#### Programa

``` 
difference() {
  //-- Pieza sin taladros
  union() {
    //-- Cuerpo
    color("blue")
    cube([167.8, 30, 5],center=true);
    //-- Torre derecha
    color("green")
    translate([167.8/2-20/2,0,13/2+5/2])
       cube([20,30,13],center=true);
    //-- Torre izquierda
    color("green")
    translate([-167.8/2+20/2,0,13/2+5/2])
      cube([20,30,13],center=true);
  }
  //-- Taladros
  #translate([-167.8/2+10,0,0])
    cylinder(r=9/2, h=50, center=true);
  #translate([+167.8/2-10,0,0])
    cylinder(r=9/2, h=50, center=true);
 }
```

<br>

Describimos algunos modificadores y operadores para hacer depuración:

- '''Operador color()''': Cambiar el color de una pieza o partes de una pieza.

- '''Modificador *''' : Comentar la rama. Se ignora al hacer el renderizado, pero se muestra el resto de objetos.

- '''Modificador !''' : Lo contrario a *: Sólo se muestra el objeto al que se aplica y el resto NO se renderiza.

- '''Modificador #''' : Mostrar en transparente las partes usadas en las diferencias. Genial para ver cómo están hechos los taladros.

<br>

## Imprimiendo las piezas de mecano.

**[![Video Tutorial]()](http://www.youtube.com/watch?v=w8Cy3gviRsg)**

<br>

#### Programa

```
use <pieza_mecano.scad>  
pieza_mecano();
 translate([0,15,0])
   pieza_mecano(n=3);
 translate([0,30,0])
   pieza_mecano(n=2);
```

<br>

Se generan 3 piezas de mecano de 4, 3 y 2 taladros. Las imprimimos usando una impresora 3D opensource.

<br>

||||
|-|-|-|
|![Imprimiendo las  ]()|![Piezas impresas]()|![Probando las piezas]()|

<br>

## Recursos

<br>

### Descargas

**[Paquete con los primeros 14 ejemplos de este tutorial](http://www.ibueotics.com/downloads/2012-05-22-openscad-tutorial/tutorial_openscad-01-14.zip)**

<br>

### Repositorio

Los ficheros fuentes están en este [repositorio SVN](http://svn.iearobotics.com/tutorial_openscad):

<br>

## Referencias

**[Obijanacademy]()**
**[Wikipedia]()**