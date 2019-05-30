# Data Science 101 - class 03

### Analytics

Para comenzar valdría la pena tomarse un momento para considerar el origen del término *análisis*. Deriva del Griego, y significa desentrañar. Esto tiene sentido, pero es de muy alto nivel como para ayudarnos a comprender lo que implica realmente. A efectos de una perspectiva mas orientada a negocios, consideremos la definición de Mario Faria: *Transformar activos de datos en insights competitivos, que conduzca las decisiones y acciones de negocio por medio de personal, procesos y tecnología.*
De acuerdo con Wikipedia, *Insight* es un término que se usa para referirse al entendiemiento de una causa y su efecto en un contexto en esepecífico. Existen varios significados relacionados:
* Una porción de información.
* Acción o resultado del entendimiento de la naturalza interna de las cosas.
* Una Instrospección.
Por otra parte, definimos *Información* como el resultado de aplicar procesamiento a los datos, dándole así contexto y significado.
##### Datos VS Información VS Conocimiento
Los datos representan los hechos crudos, sin procesar, acerca del universo. Información son los datos capturados y procesados. Y por otra parte el conociemiento es un conjutno de modelos mentales y creencias acerca del universo construidos a partir de información a lo largo del tiempo.
Por ejemplo, *La gtemperatura actual es 44 grados F*. Eso es un hecho numérico. Existe y es cierto asi alguien lo observe o no. Sin embargo no es útil, porque es ambiguo, carece de contexto. 
*La temperatura en New York a las 10am el 2 de Noviembre de 2014 es 44 grados F.* Eso es un dato mas cotextualizado. Sin embargo, sigue siendo una declaración de hechos sin interpretación. 
*44 grados F es mucho mas frío de lo normal*. Esto es información. Hemos procesado el dato, y lo hemos combinado con otros datos para establecer un punto de comparación con respecto a lo que es normal.
*A 44 grados F hace frío, voy a necesotar mi abrigo.* Hemos combinado la información a lo largo del tiempo y construido un modelo mental de lo que eso significa, eso es conocimiento.

Dado ese nuevo nivel de entendimiento, examinemos el conjunto de herrmamientas a las que un analista necesita acceso. En este caso no nos referimos a herramientas de software, como excel o R, si no a herramientas estadísticas y el tipo de análisis que puede realizarse.

#### Tipos de Análisis

Según J. Leek, un profesor asistente de Bioestadística en la Universidad Jhons Hopkins y coeditor del blog [simply statistics](https://simplystatistics.org/), existen 6 tipos de análisis, desde el mas simple hasta el mas complejo son:

* Descriptivo
* Exploratorio
* Inferencial
* Predictivo
* Causal
* Mecánico

antes de ahondar en cada tipo, repsaremos un par de definiciones relevantes y que en ocasiones se prestan para confusión. 

* Variable: algo que es propenso a cambiar a través del espacio, tiempo, u otra unidad, por ejemplo *sea v = velocidad del carro*.
* Dimensión : Una variable en particular. Mientras "variable" es mas usado frecuentemente por científicos y programadores, dimensión es mas común en BI. Una dimensión es una variable para categorizar hechos y medidas y típicamente es categórica o temporal tambien puede ser ranking, rating, o enteros.
* Medida : Una medida de un valor crudo de un objeto, tal como longitud.
* Métrica : Función de una o mas medidas.
* Estadístico : Una medida sencilla de algún atributo de los datos, porejemplo media aritmética.
* KPI (Key Performance Indicator): Esto es una medida en un contexto de negocios, donde se asocia con un objetivo de rendimiento y algún valor base. Muestra el rendimiento relativo a algún objetivo de negocio o punto de partida.

##### Análisis Descriptivo

Este tipo de análisis es el mas simple que existe. Este describe y sumariza un comjunto de datos de manera cunatitativa. De alguna manera caracteriza la muestra de datos actual y no intenta describir nada acerca de la población a la cual pertenece dicha muestra. El análisis exploratorio nos permite confirmar o desmentir asunciones acerca de los datos.


##### Análisis Exploratorio

El análisis descriptivo es muy importante como primer paso. Sin embargo, los resumenes numéricos solo llegan hasta ahí. Puede suceder por ejemplo que dos conjuntos de datos generen la misma descripción numérica pero tengan diferentes distribuciones. imagen aqui
![imagen](C://users/quint/documents/data-science-101/notes/img3.png)

![imagen](C://users/quint/documents/data-science-101/notes/img4.png)

![imagen](C://users/quint/documents/data-science-101/notes/img5.png)


##### Análsis Inferencial

El analisis ddescriptivo y exploratorio viven bajo el espectro de la estadística descriptiva, es decir describen propiedades de las muestras de datos actuales. Ahora bien, existe otra rama principal, la estadistica inferencial. Tal y como lo indica el nombre la idea u objetivo es inferir alguna unformacion, esta informacion pueden ser parametros, distribuciones o incluso relaciones, acerca de la muestra de la que provienen.
Necesitamos la inferencia debido a que en ocasiones el conjunto de datos puede ser muy extenso y la recolección costosa en terminos de recursos.

##### Analisis Predictivo 

El análiss predictivo tienes sus bases en el analisis inferencial. El objetivo aqui es aprender relaciones entre variables a partir de un cojunto de datos de entrenamiento existente, y desarrollar un modelo estadistico que pueda predecir valores de los atributos de un nuevo registro de datos.

##### Analisis Causal

Probablemente todos hemos escuchado la maxima: *correlacion no implica causalidad*. sise recolectan datos, luego se hace un poco de analisis exploratorio para observar relaciones interesantes entre las variables, seguramente se encuentra algo. Incluso si existe una fuerte correlacion entre dos variables, esto no quiere decir que una cause la otra.

Fuente de la infografia  cuanto gana un conetifico de datos
#### El Equipo

Una organización *Data Driven* es probable que tenga una variedad de roles entre los analistas, tipicamente organizados en múltiples equipos. Diferentes perosnas describen describen distintos roles dentro del equipo de analistas de maneras diferentes, y en muchas ocasiones las habilidades se superponen entre ellas. Consideremos de aquí en adelante la siguiente descripción: Analistas de Datos, Ingenieros de Datos, analistas de negocio, Científicos de Datos, Estadistas, Quants, analistas Contable y Financiero y Especialistas en Visualización de Datos. 

* Analista de Datos: este es el término mas común, al menos comparado con roles mas especializados descritos mas adelante. En muchos casos, ellos son T-shaped: es decir tienen una experiencia superficial en un gran conjunto de habilidades pero con profundos conocimientos y experticia en un área en específico.

* Ingenieros de Datos: Principalmente responsable de obtener, limpiar y procesar los datos, además de entregarla de manera que pueda ser accesada por los analistas. Ellos son responsables de las cuestiones operacionales, y pueden en algunos casos ser los encargados de construir las herrmientas de BI que usan los analistas.
* Analista de Negocio: Son analistas que típicamente sirven como una interafaz entre la dirección y el departamento de IT. Su rol se basa en mejorar los procesos de negocio o ayudar a diseñar y desarrollar nuevas características de los sitemas tanto en el backend como frontend.
* Científico de Datos: Un término mas amplio que incluye un personal mas inclinado hacia la rama matemática o estadística con grados avanzados (muchas veces en ciencias y computación) y habilidades avanzadas de programación.
* Estadistas: Personal con habilidades enfocadas en modelación estadística. Ellos típicamente tienen al menos una maestría en estadística y estan escencialmente presentes en aseguradoras, clínicas, investigación y desarrollo y el gobierno.
* Quants : Analistas con habilidades matemáticas que típicamente trabajan en el sector financiero modelando el comportamiento de instrumentos financieros, manejo de riesgo, y movimientos del mercado de bolsa.
* Analaistas Contables y Financieros: Personal que se enfoca en declaraciones financieras internas, auditando, pronosticando y analizando el rendimiento del negocio.
* Especialistas en Visualización de Datos: Personas con un sentido estético del diseño que crea infografías, dashboards, entre otros. Ellos pueden trabajar con tecnologías como JavaScript, CofeeScript, CSS y HTML, y trabajar con librerias para la visualización de datos como D3. 


### Metric Design


Una Organizacion Data Driven necesita establecer una estrategia clara, esto es, una direccion en la que el negocio se mueve, y entonces determinar un conjunto de metricas de alto nivel (KPIs) para llevar un seguimiento de si el negocio se esta moviendo en la direccion correcta ademas de moitorear el progreso y exito. 

Existem diversas consideraciones a la hora de escoger o designar una metrica. En un mundo ideal, las metricas deberían exhibir un cierto numero de raasgos.

* Simple: diseñar una metrica para que sea los mas simple que pueda ser. 
* Estandarizada ; hacer coincidir definiciones estandares de metricas siempre y cuando sea posible. Por ejemplo, si existe un estandar, una metrica bien definida para website bounce rate, entonces usarla a menos de que exista una muy buena razon para la implementacion de una variante disenada por el equipo. La estandarizacion generara menos confusion, especialmente para personal que llega al equipo proveneinte de otras organizaciones. La mejor practica es tener una fuente documentada, centralizada y automatizada de las definiciones.
* Concreta : las metricas deben ser concretas, esto es, su valor numerico medio debe estar cerca del valor medio real. 
* Precisa : las metricas deben ser precisas, es decir, deberian retornar valores similares si se miden repetidas veces en las mismas condiciones.
* Robusta
* Directa

#### Key Performance Indicators (KPIs)

Los indicadores clave del negocio, tambien conocidos como indicadores clave de exito (KSIs), son el conjunto de medidas de alto nivel relacionadas con los objetivos estrategicos de una compañia. Ayudan a definir y llevar un seguimiento de la direccion que lleva el negocio y tambien ayuda a realizar sus objetivos. 

Se considera critico que los KPIs:

*Esten definidos de manera clara*

No se quiere ninguna confusion o ambiguedad con respecto a una metrica clave, la cual el negocio esta tratando de dirigir. Se necesita una definicion clara, un objetivo claro, y un intervalo de tiempo calro y especifico, normalmente de un año.

*Sean medibles*

Los KPIs deben ser cuantificables. La organizacion debe ser capaz de medir el progresp de manera numerica a traves del tiempo. Tal y como DJ Patil, US Chief Data Scientist, dice en su libro [Building Data Science Teams](https://www.oreilly.com/data/free/building-data-science-teams.csp), *"He encontrado que las organizaciones Data Driven mas fuertes todas viven por el lema: si no puedes medirlo, entonces no puedes arreglarlo."*

*Fijar Objetivos*

*Incrementar ganancias* is una definición pobre de lo que es una KPI debido a que no tiene un objetivo numerico. Por ejemplo, si la organizacion incrementa los ingresos solo por 5$, el equipo puede determinar que se cumplió la meta y dejar de intentar. Por otra parte , si el objetivo es muy dificil, o imposible de cumplir, el mismo no sera tomado en serio, o la gente puede rendirse, las KPI deben ser alcanzables pero con trabajo continuo.

*Ser visibles* 
Las KPIs necesitan ser visibles al menos para las personas responsables de dirigirlas, pero idelamente se necesita mas que eso. El equipo necesita tener feedback y tener un claro sentido de si sus esfuerzos valen la pena o si necesitan cambiar  cambiar el rumbo y probar algo diferente a lo que han hecho.

*Reflejar lo que la organizacion esta tratando de alcanzar*

Es muy facil caer en la trampa de seguir lo que puede ser facilmente medible, tl como el tiempo de respuesta para antender llamadas en un call center, cuando el verdadero objetivo pudiera ser incrementar la satisfaccion del cliente. 

---

Ademas, tal como los objetivos, deben ser *SMART*:
1. Specific
2. Measurable
3. Achivable
4. Result-oriented
5. Time-Bound

Indicadores CLave Ejemplos:

imagen aqui

Sin embargo, cada negocio necesita seleccionar y valorar su propio conjunto de KPIs para su sector, su propio modelo de neocio, su actual posición y sus objetivos particulares. Con esto se quiere resaltar que no existe una receta para un conjunto de KPIs que una compania debe usar. Se requiere de un estudio meticuloso desde los directivos y accionistas acerca de hacia donde dirigir el negocio, donde debe enfocarse la atencion y esfuerzo de todo el equipo a lo largo de el ano siguiente.

##### Cuantas KPIs usar?

Los indicadores clave tendran que cubrir la mayor cantidad de areas del negocio, y cualquier parte de enfoque estrategico para el periodo crrespondiente, tipicamente un ano. Una organizacion puede tener un punado (4-5) perspectivas dentro de grupos de accionistas. Esto puede, no necesariamente, estar alineado con los directivos. Asi, una perspectiva puede ser supervisada por el CFO, objetivos estrategicos en tecnologia administrados por el equipo del CTO/CIO, objetivos de mercadeo por el CMO, entre otros. [Bob Champagne]() sugiere que en cada una de estas debe haber de dos a cinco objetivos estrategicos, y estos a su vez deben estar asociados con una hasta tres KPIs. sin embargo el numero total de KPIS deberia ser al menos 10. 5x(2-5)x(1-3)

##### Definiciones y Metas

Si los KPIs deben ser SMART, estos deben ser especificos y medibles. Esto quiere decir que uno debe evitar definiciones ambiguas y genericas tales como "mejorar" o "realzar", o nombres o adjetivos como "el mejor" o "de calidad". [Stacy Barr](http://www.staceybarr.com/measure-up/setting-your-goals-without-jargon-hbr/) llama a estas palabras "weasel words" que puede traducirse como palabras equivocas. En cambio ella recomienda tomar un objetivo vago, tal como " transformar el rendimiento de nuestros clientes", tener una conversacion acerca de estas weasel words, y  entenderlas, reemplazarlas con un lenguaje mas sensorial, " cuando nuestrso clientes trabajan con nosotros, ellos pueden alcanzar sus metas de negocio mucho mas pronto."

---
Stacey Barr Stacey is a specialist in strategic performance measurement and evidence-based leadership.

Her purpose is to help leaders get tangibly clear about the results they intend to achieve in their organisation, to know how to recognise if and how well they are achieving those results.

---

### A/B Testing

En 1998, Greg Linden, uno de los empleados de Amazon tuvo una idea. Porque no crear recomendaciones en el checkout? los supermercados ponen dulces en las cajas para estimular compras por impulso. Eso funciona. Porque no dar un vistazo al carrito de compras de amazon y hacer recomendaciones personalizadas y relevantes que el cliente pieda apreciar? El ideo un prototipo, lo puso a funcionar, y lo mostro. El resto de la historia en sus propias palabras:

* Mientras que la reaccion fue positiva, hubo cierta inquietud. En aprticular, un vice presidente de marketing estaba totalmente en contra. Su objecion principal era que ello podria distraer a las personas de hacer el checkout-es cierto que es mucho mas comun ver que una persona abandona el carrito en un sitio de ecomerce- y el alio a otros a su causa. En este punto se me habia prohibido trabajar mas en esto. Me dijeron que Amazon no estaba listo para lanzar esta caracteristica. Debio haberse detenido en ese momento. En lugar de eso, me encargue de preparar la adicion para una prueba online. Yo creia en este sistema de recomendaciones y por ende queria medir que impacto podia tener en las ventas. Llegue a escuchar que el vicepresidente estaba furioso cuando descubrio que estaba preparando una prueba. Pero incluso para los ejecutivos, era dificil bloquear una prueba. Medir es bueno. El test fue llevado a cabo. Los resultados fueron claros no solo ganaron, sino que ganaron por un margen tan amplio que el simple hecho de no tenerlo en produccion le costaba a amazon una buena parte de sus ventas. Luego fue lanzado con urgencia el sistema de recomendaciones en el checkout. *

Obviamente Greg tuvo suerte. No tanto porque haya funcionado (aunque es por supuiesto significante), si no poruqe incluso  en aquel entonces amazon disponia de la infraestructura  y la cultura Data Driven para que el pudiera realizar dicha prueba.

En muchas situaciones , especialmente en aquellas que son nuevas, nuestra intuicion es pobre. A menudo nos sorprendemos con los resultados. Si no se cree solo vemaos un par de ejemplos de experimentos en linea. La primera es una accion de llamada en un anuncio. En terminos de CTR( Click through rate) cual gano y por cuanto?

---

* Get $10 off the first purchase. Book online now!
* Get an additional $10 off. Book online now.

---

La respuesta es que la segunda version gana, con un CTR del doble que la orimera. Ok ahora que tal la imagen, puedes ver la diferencia al menos? Cual gana y por cuanto?

imagen aqui


![imagen](C://users/quint/documents/data-science-101/notes/img1.png)


Finalmente, en el ultimo ejemplo, vemos dos casi identicas versiones de una pagina, excepto que en la derecha todas las formularios son opcionales. Esa version condujo a un CTR 31% mayor.


![imagen](C://users/quint/documents/data-science-101/notes/img2.png)

En todos los ejemplos hubiera sido dificil predecir cual ganaria, mas dificil aun por cuanto, y tmbien predecir el iimpacto en otras metricas. Esta es la razon por la cual un byen diseno del experimento es necesario. Cambia la conversacion de " Yo creo que" a " Los datos muestra que". Asi finalmente vemos que este tipo de experimentos forman una parte invaluable de toda organizacion data driven.


Los  experimientos antes expuestos forman instancias de un tipo especial llamado TEsts A/B.

Como se menciono anteriormente nuestra intuicion puede ser bastante mala. Incluso expertos en el dominio de ttrabajo se equivocan mas a menudo de lo que les gustaria admitir. En el libro *A/B Testing: The most powerful way to turn clicks into customers* Dan Siroker, CEO y confundador de la plataforma para tests A/B Optimizely, habla de su tiempo durante la campana de Obama del 2008. Ellos propusieron optimizar la pagina de registro de sus partidarios, el sitio disenado para reunir los emails de las personas. La pagina original contenia una imagen estatica que decia "Sign up". El equipo penso que videos de los discursos mas importantes sobrepasarina a la imagen estatica. Despues de testear varias imagenes y videos diferentes, econtraron que cada video quedo muy por debajo de cada imagen de manera dramatica. La mejor combinacion de imagen y boto de "sign up" mejoro los registros por un 40.6%. Eso se tradujo en mas de 2.8 millones de emails adicionales, 280k voluntarios, y recolecta de $57 millones de dolares en donaciones para la campana. Muchas veces el ojo humano ser aincapaz de detectar o acertar en que funcionaria. 





















