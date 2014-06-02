# Atoms
## Atomic & Reactive Development
2013-2014, Javier Jimenez Villar - @soyjavi

Es por todos sabido que la programación web esta cambiando a pasos agigantados, en los últimos 5 años hemos pasado de hablar de *simples* páginas web a *avanzadas* aplicaciones web. Esta situación ha dado lugar a que el desarrollo de WebApps se modifique por completo y cada compañia ha ofrecido su paradigma, a veces basandose en patrones ya conocidos como el MVC o MVVM y otras veces estableciendo su forma (vease los productos de tapquo Monocle, Lungo, Tuktuk... ).

Lo que tambien se ha demostrado es que por la propia naturaleza de las www, el desarrollo web normalmente es una tarea tediosa puesto que hay que combinar tres tecnologías: HTML, CSS y JavaScript; y a veces dependiendo del perfil del desarrollador esto se convierte en una verdadera tortura. Atoms te da la posibilidad de crear un sistema estanco donde el desarrollador puede olvidarse del contenido (HTML) y la forma (CSS) para centrarse en lo que da realmente valor a una Web Application el negocio (JavaScript).


### Los inicios del proyecto *Atoms*
Es un proyecto creado por uno de los fundadores de Tapquo](http://tapquo.com), Javi Jimenez (aka [@soyjavi](http://twitter.com/soyjavi)) el cual encontró un problema en dos de los frameworks que había desarrollado anteriormente, [Lungo](http://lungo.tapquo.com) y [Monocle](http://monocle.tapquo.com). A pesar de que ambos estan acogidos por un gran grupo de desarrolladores por todo el mundo, y de ofrecer todas las técnicas necesarias parar crear Apps, los dos frameworks tenían la misma finalidad pero con diferente funcionalidad.

Con esto, conociendo a [@soyjavi](http://twitter.com/soyjavi) como una persona que se aleja de las duplicidades comenzó a estudiar otras posibilidades de creación para lo que iba a ser Lungo v3. Dentro de la especificación [W3C](http://www.w3.org/) se está trabajando en varias *spec* que en un futuro nos ayudarán a crear mejores WebApps, como pueden ser los [WebComponents](https://dvcs.w3.org/hg/webcomponents/raw-file/tip/explainer/index.html) HTMLTemplates, ShadowDOM ... pero por desgracia, eso será en el futuro y Javi necesitaba implementarlo en el presente. 

Despues de mucho estudiar Javi llegó a la conclusión de que podía crear un sistema en el que se desarrollasen Apps las cuales en un futuro y de manera automática se adaptasen a la *spec* WebComponents. Para ello decidio en crear lo que el ha llamado el *pseudo-DOM*, el cual se encarga de representar los elementos HTML y decidir los estilos CSS oportunos, todo esto de una manera automática y optimizada para todos los dispositivos. Pongamos el siguiente un ejemplo, el proceso natural de desarrollo sería creamos una maqueta con el lenguaje HTML, el diseñador establece los estilos CSS y tras esto el desarrollador frontend se encarga de dar lógica al proceso... pero... ¿qué pasa si hay que cambiar maquetación, o el diseñador decide establecer un nuevo estilo?... el proceso vuelve a comenzar en un HTML->CSS->JS. Atoms con el pseudo-DOM permite que el desarrollador se encargue de establecer los comportamientos y elementos de la aplicación y el pseudo-DOM se encarga de saber como y cuando representarlos; ahorrando la carga (no crea elementos HTML hasta que sea realmente necesario) y dando la posibilidad de cambiar negocio muy facilmente.


### ¿Programación atómica y reactiva?
El paradigma "Atomic Development" establecido por [Javi Jiménez](https://twitter.com/soyjavi) se basa en la gran idea de [Brad Frost](http://bradfrostweb.com) llamada [Atomic Design](http://bradfrostweb.com/blog/post/atomic-web-design/), la cual establece un primer acercamiento a la reutilización de tus propios *Components*. Realmente es una idea muy bien definida con el único pero de que Brad unicamente la estableció para el contexto del Diseño. Javi, como developer, pensó que sería una muy buena idea utilizar ese paradigma pero pensandolo para el mundo del desarrollo de Apps, de ahí "Atomic Development". Ambos paradigmas pueden ser definidos con la siguiente cita:

***We’re not designing pages, we’re designing systems of components.*** - Stephen Hay

La realidad es que una Web Application no solo se compone del diseño, necesita de una lógica de negocio para que realmente sea de utilidad. Para ello el paradigma establecido por Javi se basa en: *Atoms*, *Molécules* y *Organisms*, para que te hagas una idea vamos a utilizar un diseño que realizó Brad para "Atomic Design":

![image](http://cdn.tapquo.com/images/atoms/atomic-design-process.png)

La tradución que 

* **Atom**: Es el elemento básico de tu Web Application como pueden ser `input`, `button`, `ul`, `img` ...
* **Molecule**: La agrupación de varios elementos `Atom`, la cual genera un comportamiento definido. Uj ejemplo puede ser `Search` el cual une los Atoms `label`, `input` y `button`.
* **Organisms**: La agrupación de elementos `Atom` y `Molecule`, comunicandose cada elemento. Por ejemplo un *Organism* `Header` contiene las *Molecules* `Navigation` y `Search`.
* **Extensions**: Para crear funcionalidades totalmente definidas y que podamos reutilizar.
* **Pages**: Brad habla de *Pages* y Javi lo renombra a *Systems* ... aunque el concepto es el mismo. Es el resultado de la química entre todos los elementos de tu Web Application.


### Indice
- [1. Introducción](https://github.com/soyjavi/atoms-documentation/blob/master/ES/01.md)
- [2. Atom: El elemento básico](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [3. Molecule: Agrupando átomos](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [4. Organism: El contenedor](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [5. Entity: Dando valor a tus átomos](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [6. Eventos](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [7. Extensions: Extendiendo](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [8. Atoms.APP: Extension para tus Apps](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)
- [9. Atoms.IDE: El diseñador de Apps](https://github.com/soyjavi/atoms-documentation/blob/master/ES/02.md)


### Licencia
Atoms esta licenciado por medio de MIT licensed. Echa un vistazo al fichero [LICENSE.md](https://github.com/tapquo/atoms/blob/master/LICENSE) para obtener más información.