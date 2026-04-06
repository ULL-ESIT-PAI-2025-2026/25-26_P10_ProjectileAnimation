# Práctica 10. Animaciones gráficas en TypeScript. Trayectoria de un proyectil.
### Factor de ponderación: 9
### Estimación de horas de trabajo para realizar la práctica: 4,5

### Objetivos
Los objetivos de esta tarea son poner en práctica:
* Desarrollo de animaciones gráficas en TS/JS
* Conceptos básicos de Programación Gráfica en TypeScript usando la API Canvas.
* Metodologías y conceptos de diseño y Programación Orientada a Objetos en TypeScript.
* Principios y Buenas prácticas de programación Orientada a Objetos.
* Alguno de los patrones de diseño que se han estudiado en la asignatura.

### Rúbrica de evaluacion del ejercicio
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva)
que se tendrán en cuenta a la hora de evaluar esta práctica:
* Se valorará la realización de las diferentes tareas que se proponen
* El comportamiento del programa debe ajustarse a lo descrito en este documento
* Capacidad de la programadora de introducir cambios en el programa desarrollado
* La documentación de la aplicación incluirá un fichero README.md con la información correspondiente al
  proyecto desarrollado
* La estructura de directorios del proyecto será conforme a los requisitos establecidos en la asignatura
* Se acredita conocimiento y puesta en práctica de principios y buenas prácticas de programación orientada a objetos
* Saber corregir bugs en sus programas utilizando el depurador de Visual Studio Code
* Deben usarse estructuras de datos adecuadas para representar los diferentes elementos que intervienen en el problema
* Ser capaz de desarrollar programas simples en TypeScript en el entorno Linux de la VM de la asignatura usando
  `ts-node`
* Ser capaz de generar documentación para sus programas TS utilizando
  [TypeDoc](https://typedoc.org/)
  y de visualizar dicha documentación en un servidor web
* El alumnado debe ser capaz de resolver problemas tanto en JS como en TS en la plataforma Exercism subiendo sus soluciones a la misma
* Ser capaz de desarrollar tests unitarios para sus programas utilizando
  [Jest](https://jestjs.io/)
* Acreditar su capacidad para configurar y utilizar 
  [ESLint](https://eslint.org/)
y que es capaz de trabajar con la misma en Visual Studio Code
* Acreditar que conoce las etiquetas de 
  [JSDoc](https://jsdoc.app/)
* Se comprobará que el código que el alumnado escribe se adhiere a las reglas de las Guías de Estilo de Google
  para Javascript y/o TypeScript
* Todas las prácticas realizadas hasta la fecha, incluída la que se presenta para su evaluación, se encuentran alojadas en repositorios privados de GitHub.
* Acreditar que es capaz de editar ficheros de forma remota en su VM usando Visual Studio Code

### Animaciones en TypeScript/JavaScript
XXX

### Indicaciones de caracter general
El programa que desarrolle ha de ser orientados a objetos.
Ponga en práctica los principios de abstracción y encapsulamiento característicos 
de la OOP así como las buenas prácticas, principios y patrones que han sido expuestos en las clases de la asignatura.

La estructura de directorios de su proyecto de práctica debe ser conforme con la estructura establecida para
las prácticas de PAI.

Configure adecuadamente ficheros `package.json` y `tsconfig.json` en el directorio raíz de su ejercicio 
que permitan la instalación de las dependencias de su proyecto.

Incluya en el fichero `README.md` la información relevante de su proyecto de práctica y haga que ese fichero
sea la primera página de la documentación (TypeDoc) de la práctica.

En el desarrollo de esta práctica, utilice el depurador integrado en el navegador para confirmar que el flujo
de ejecución de su programa es el correcto.

No intente desarrollar su aplicación en un único paso.

Previo al desarrollo, realice un diseño de su aplicación identificando las diferentes clases que
intervienen en el programa. 
Utilice lápiz y papel para hacer un esquema de las relaciones entre las diferentes clases que intervienen en
su aplicación.

Después de esa planificación inicial, trabaje mediante sucesivos refinamientos de una primera aproximación.
También puede resultarle conveniente realizar pequeñas aplicaciones auxiliares que le sirvan para comprobar y
aprender el funcionamiento de algún aspecto concreto de la aplicación.

Cuando finalice su aplicación, utilice 
[Mermaid.js](https://mermaid.js.org/), 
[Lucidchart](https://www.lucidchart.com/pages) o cualquier otra herramienta que conozca para trasladar sus
diseños en papel a un diagrama en formato digital que pueda mostrar a través de una web.

### Tiro parabólico
El objetivo de esta práctica es el desarrollo de una aplicación que permita la visualización en una página web
de la representación gráfica de una función.

Intente que su aplicación imite en la medida de lo posible el aspecto de
[esta otra](https://www.geogebra.org/m/BTC45Jzp)
que se tomará como referencia.

De esa página imite los ejes coordenados así como la numeración de los mismos y el área de dibujo de la
función.
En esa página de referencia pruebe a dibujar diferentes funciones usando el campo "Entrada" de la parte
inferior.
Pruebe a introducir funciones como *sin(x)*, *exp(x)* o *sqrt(x)* y visualice el resultado.

En la aplicación que ha de desarrollar comience, a diferencia de la aplicación de referencia, haciendo que la
función que se vaya a representar figure codificada (*cableada*, *hardcoded*) en su código fuente de modo que
para cambiar la función que se representa habría que modificar la función principal del programa.
Con posterioridad, intente una aproximación más elaborada, como la de la página de referencia, en la que la
función pueda ser introducida por el usuario. 
Para explorar esta segunda aproximación tal vez le resulte útil estudiar el analizador de expresiones
(*Expression parser*) de librería
[mathjs](https://mathjs.org/) 

### Interfaz gráfica de la aplicación 
La interfaz gráfica de la aplicación se desarrollará a través de diferentes páginas HTML.
Haga que en el elemento `title` del código HTML de todas las páginas web de su poroyecto figure su nombre y apellidos.

La visualización de la ejecución del programa se realizará a través de una página web alojada
en la máquina IaaS-ULL de la asignatura (puede utilizar si lo desea la extensión *Live View* de VSC).
En esa página se embeberá un lienzo (canvas) para dibujar la gráfica de una función.
La mostrará un canvas que ocupe la mayor parte del viewport de su navegador.

No es necesario que invierta esfuerzo en la programación de los aspectos de esa página que no tienen relación
con TypeScript. 
Los estilos de CSS son aspectos que se estudiarán con mayor nivel de detalle en el futuro. 
No se requiere que dedique esfuerzo a esos aspectos en esta práctica.
Tampoco se propone en esta práctica que utilice elementos interactivos (botones, campos de texto, selectores,
etc.) salvo quizás un campo de texto para leer la función que el usuario propone representar.

Configure asimismo en el directorio `/public` de su práctica, la página `index.html`, 
que servirá de "página índice" para los ejercicios de la sesión de evaluación de la práctica.
Enlace también en esa página índice tanto la página que contiene la documentación de su proyecto, generada con
Typedoc como otra que mostrará el diagrama UML de las clases que intervienen en su programa.

Las siguientes deben tomarse como especificaciones adicionales de la aplicación a desarrollar:

## Diseño orientado a objetos
Se deja total libertad al alumnado para diseñar la aplicación de la forma que estime más conveniente.
Se valorará la puesta en práctica en el diseño que se realice de los contenidos relacionados con principios y
buenas prácticas de OOP estudiados en la asignatura así como el uso de alguno de los patrones de diseño que ha
estudiado.

## Referencias
* [TypeScript Tutorial](https://www.typescripttutorial.net/)
* [TypeDoc](https://typedoc.org/)
* [TypeScript track in Exercism](https://exercism.org/tracks/typescript)
* [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html)
* [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
* [Jutge web site](https://jutge.org/)
* [Jest](https://jestjs.io/)
* [ESLint](https://eslint.org/)
* [JSDoc](https://jsdoc.app/)
