## Parte 1: Ingenieria de software
Una definicion formal de la ingenieria de software se puede encontrar en el [glosario de la ieee](https://ieeexplore.ieee.org/document/159342) donde se establece que:

>Software engineering is defined as the application of a systematic, disciplined, quantifiable approach to the development, operation, and maintenance of software.

Esta definicion establece que es la aplicacion de un proceso (o aproximacion) sistematico, disciplinado y cuantificable del desarrollo, operacion y mantenimiento del software. Lo importante en la frase anterior es `sistematico`, `disciplinado` y `cuantificable`, entonces explorando los tres terminos tenemos:
* `sistematico`: Que sigue o se ajusta a un sistema (conjunto ordenado de normas y procedimientos).
* `disciplinado`: Conjunto de reglas de comportamiento para mantener el orden y la subordinación entre los miembros de un cuerpo o una colectividad en una profesión o en una determinada colectividad.
* `cuantificable`: De la cantidad o relacionado con ella.

Entonces, volviendo a la definicion de ingenieria de software podemos entenderla como que es seguir las normas y procedimientos que nos dan un sentido y direccion en la construccion del software, teniendo en cuenta que todo debe ser medido o cuantificado en algun punto.

Si bien ya tenemos la definicion de lo que es la ingenieria del software, la misma definicion nos puede mostrar que todo en la construccion del software es guiado por un proceso y que el desarrollador es una parte del mismo. El ingeniero de software no solo tiene que escribir codigo que sea de buena calidad y mantenible, sino tambien tiene que pensar cosas como por ejemplo cuales son las reglas de negocio que se aplican, como se va a testear el codigo de modo que sea mantenible y automatizable, como se va a desplegar el codigo en un servidor, con que otros componentes de la arquitectura interactua y como responde el codigo escrito bajo estres?

En la ingenieria de software existen roles que soportan el proceso de definicion, construccion y prueba del mismo. El SDLC (software development life cycle) es como se describe el proceso complejo y con multiples fases y etapas con el que se desarrolla el software.

## SDLC
Como mencionamos en el apartado anterior, SDLC (softare development life cycle) se refiere al proceso complejo multifases que se utiliza para la construccion del sfotware, y como tambien establecimos antes, el ingeniero de software es un rol de este proceso que no solo escribe buen codigo. Dentro de SDLC existen otros roles:

- `SWE`: Software Engineer.
- `TAE`: Test Software Engineer.
- `SRE`: Site Reliability Engineer.
- `RE`: Release Engineer.
- `System Architect`: Architect.
  
### Software Engineer (SWE)
Este es un rol muy importante ya que es quien diseña y escribe las nuevas piezas de codigo que generan el software, aunque tambien es responsable de operar y mantener el software existente y el legado (legacy).

Los SWE se pueden categorizar segun su cantidad de experiencia en:

- `Junior`: Son aquellos que recien comienzan su carrera profesional y no poseen experiencia desarrollando software de produccion. Estos SWE son aquellos que aprenden mas de lo que aportan en una organizacion pero tambien son quienes van a desarrollar y operar software en un futuro no muy lejano.
- `Semi-Senior`: Tambien conocido como `mid-level`, es un SWE que cuenta con 2 o 3 años de experiencia desarrollando en empresas y con experiencia en desarrollos que son desplegados a produccion. Estos desarrolladores o ingenieros no solo escriben codigo sino que tambien pueden hacer criticas al codigo de otras personas y ayudar a los `juniors` con sus tareas tecnicas como asi tambien actuar como mentor de carrera. Los semi-senior conocen generalmente varias tareas del `SDLC`.
- `Senior`: Estos SWE conocen en profundidad muchas partes del `SDLC` y tienen habilidades de coordinacion de equipos, manejo de clientes, despliegues a produccion y sobre todo adquieren un nivel de entendimiento profundo sobre una industria o negocio lo que los hace una fuente de conocimiento para personal tecnico y no tecnico.

Tambien se puede clasificar a los SWE segun su expertise en ciertas capas del software. Otra forma seria entonces:

- `Frontend engineers`: Estos son aquellos que trabajan exclusivamente en las partes o componentes de la aplicacion (o software) que tiene interaccion con los usuarios, por ejemplo un mobile developer solo escribe codigo para aplicaciones que ejecutan en un celular (comunmente llamadas apps) o tambien un WebUI developer que puede escribir codigo para renderizar paginas web via un servidor.
- `Backend engineers`: Son aquellos que trabajan en las partes de la applicacion o software que ejecuta en los servidores y se encargan del almacenamiento, busqueda y devolucion de datos, logica de negocios y escalabilidad de la solucion.
- `full stack engineers`: Son aquellos que pueden trabajar en los dos anteriores sin problemas.

### Test Software Engineer (TAE)
Tambien conocido como Software Development Engineer in Test (`SDET`), el Test Automation Engineer es aquel developer que escribe codigo para probar y estresar el software que escribe el `SWE`. La mision de los `TAE` es velar porque el equipo de desarrollo (`SWE`) escriba cofigo de alta calidad y sin fallas.

Los `TAE` por definicion tienen como objetivo principal automatizar el testing, esto ayuda a repetir las pruebas y mantener la calidad constantemente. Para la automatizacion de las pruebas se utilizan Continuous Integration (`CI`) pipelines, que son basicamente una serie de pasos automaticos que usan los equipos de desarrollos para integrar sus cambios usando una serie de pasos automaticos. Cuando nos referimos a integrar cambios son aquellos cambios en el software que son testeables para luego integrar en produccion con algun release de la aplicacion.

Los testeos (tests) que los `TAE` escriben pueden ser test de aceptacion o test de performance, donde los primeros son para probar que una pieza de codigo haga correctamente lo que tiene que hacer y los segundos son para estresar y evaluar el comportamiento bajo estres, por ejemplo simular 2 millones de usuarios tratando de comprar algo.

### Site Reliability Engineer (SRE)
El Site Reliability Engineer conocido como `SRE` es aquel cuya mision es mantener los sistemas productivos en produccion sin contratiempos. El `SRE` es un software engineer que no solo desarrolla software sino tambien que opera sistemas productivos y en caso de fallas hace correcciones y/o crea incidencias (tickets/casos) con los equipos de soporte.

Es dogma de los `SRE` automatizar la mayor cantidad de tareas posibles evitando asi la intervencion humana y potencialmente fallas, para esto se utiliza Continuous Delivery (`CD`) pipelines que son herramientas de software que establecen pasos secuenciales y repetitivos que permiten desplegar software en servidores entre otras cosas.

### Release Engineer (RE)
Un release engineer es aquel que trabaja con todos los equipos necesarios para poder definir que comprende una version determinada del software a desplegar (release), esto comprende tareas de documentacion, escribir manuales y pasos para poder desplegar correctamente la solucion y tambien pasos para recuperar el sistema en caso de problemas.

### Architect
El arquitecto es un rol que usualmente se encuentra en grandes empresas mientras que en empresas mas pequeñas este rol lo ocupa un `swe` senior. Este rol es el encargado de ver el `big picture`, es decir, observa la el sistema desde un punto mas macro, toma decisiones de tecnologia, ve como se integran los diferentes componentes y es la guia tecnologica del resto de la organizacion. Generalmente un arquitecto tiene mas de 10 años de experiencia en una industria y tiene conocimiento de casi todos los roles del SDLC, algunos mas en profundidad que otros pero conoce muy bien el ciclo de desarrollo.