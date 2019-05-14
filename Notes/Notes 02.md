# Data Science 101 - Class 02

Muchas organizaciones piensan que por el simple hecho de generar una gran cantidad de reportes o poseer muchos dashboards, son *Data Driven*. A pesar de que estas actividades son parte de lo que una organización *Data Driven* hace, ellas están típicamente enfocadas en el pasado. Es decir, estas actividades son en muchas ocasiones declaraciones de hechos sin una gran cantidad de contexto, sin una explicación del porqué algo ha o no ha sucedido, mucho menos aportan recomendaciones de que acciones tomar en un futuro. Por lo tanto tienen ventajas limitadas.
En contraste, cosideremos análisis con una perspectiva mas hacia hechos futuros, tales como modelos predictivos que optimizan el costo de avisos publicitarios, el reabastecimiento en cadenas de producción y suministro, o que minimizen la rotación de clientes. Estas tareas contemplan el hecho de dar respuestas a lo que en ingles llaman w-questions (why: porqué, who: quién, where: donde, etc.) a la vez que hacen recomendaciones y pronósticos, elaborando una narrativa en torno los resultados o respuestas. 
No obstante, estos resultados requieren que se haya recolectado los datos correctos, que los datos son confiables, el análisis es bueno, que los resultados estén siendousados en la toma de decisiones, y que ellos conducen a actciones concretas y por lo tanto el potencial puede realizarse.
La Analítica no es *Data Driven* si sus resultados y conclusiones no son considerados realmente o no se actua sobre la base de ellos. Para ser *Data Driven* una organización debe poseer los procesos correctos y la cultura correcta para dirigir las decisiones cr161ticas de negocio con estos analisis y así tener un impacto directo en el negocio.
La cultura es entonces, la clave. Este es un problema que involucra calidad y accesibilidad de los datos, reclutamiento y entrenamiento de personal de analítica, comunicación, diseño de métricas, tests A/B, procesos de toma de decisión, y más.

Data Driven no es un estado binario si no uno continuo: siempre se puede ser mas *Data Driven*, recolectar mejores datos de alta calidad y mas relevantes, tener una organización mas preparada para la Analítica, y hacer mas pruebas.

#### Calidad de los Datos

Los Datos son la base de una organización *Data Driven*. Si no se poseen datos vigentes, relevantes y confiables, los encargados de tomar las decisiones no tienen mas alternativa que decidir basándose solo e su intuición. La Calidad asociado a estos datos es clave.
Los Analistas necesitan los datos correctos, recolectados de la manera correcta, en el lugar y tiempo adecuado. Si alguno de estos aspectos no está presente, los analistas están limitados en cuanto a las preguntas que pueden responder y el tipo y la calidad de ideas que pueden derivarse de los datos.

##### Facetas de la calidad de los datos

La calidad de los datos no es algo que pueda ser descrito cun un simple número. Calidad no es un 5 o un 32. La razón es que el término engloba una serie de facetas o dimensiones. En consecuencia, existen grados de calidad, con algunas cuestiones mas importantes que ptras. El rigor de estas cuestiones dependerá del contexto del análisis que se llevarán a cabo sobre los datos. Asi, si se tiene unna tabla que contiene las direcciones de los clientes donde el código de estado está presente pero el código ZIP está ausente en muchos registros, entonces los ZIP ausentes presentaran un obstáculo si se quiere realizar un análisis que sea por códigos ZIP.
De manera mas concreta, la calidad de los datos tiene muchas facetas. Los datos deben ser: 
* Accesibles: Un analista necesita poder acceder a los datos. Esto no solo contempla permisos, si no también las herramientas apropiadas que hacen los datos usables y analizables. Por ejemplo, mientras que un archivo SQL puede contener los datos que el analista necesita, este no es un formato usable. Tiene que ser expuesto en una base de datos o una herramienta del tipo BI para que los analistas sean capaces de analizar los datos.
* Precisos : los valores representan el verdadero estado de una entidad. Por ejemplo, un termómetro descalibrado, una fecha  de nacimiento mal tipeada o una dirección no actualizada son representaciones de datos que no son precisos.
* Coherentes Los datos pueden ser combinados con otrs datos relevantes de una manera precisa. Por ejemplo, una orden de venta debería poder ser asociada a un cliente,a uno o mas productos en la misma orden, o a una dirección. Este conjunto de información porvee una imagen coherente de una orden de venta. La coherencia es dirigida por el cojutno de IDs o llaves que unen los datos en diferentes partes de la base de datos.
* Completos :  No existen datos faltantes. Esto puede significar una porción de datos dentro de un reistro, tal como el primer nombre faltante en un registro de clientes, o registros completos faltantes, tal como un registro de clientes que no se guardó en la base de datos.
* Consistentes: Los datos son un acuerdo. Por ejemplo, una dirección de correo de un cliente en particular en una fuente coincide con la dirección de otro cliente en otra fuente. Cuando exsiten este tipo de conflictos, un a fuente debe ser considerada como maestra, o ambos no se usan hasta que se entienda la razón del desacuerdo y sea corregido.
* Definidos: Campos de datos bien nombrados junto con un diccionario de datos de calidad.
* Relevantes : Los datos tienen relación con los análisis que sean llevados acabo.
* Confiable : Los datos están completos, es decir se poseen todos los datos que podrían esperarse, y es precisa, es decir, los datos proveen la infromación correcta.
* Vigente: Existe una pequeña porción de tiempo considerable entre la recolección de los datos y la disponibilidad para los analistas. En la práctica esto significa que los datos llegan a tiempo para ser realizados los análisis corresopondientes antes de que expiren.

##### Errores en los Datos
Los datos pueden estar mal, es decir, contener errores en muchas formas distintas. 

Siempre pueden estar peor. De acuerdo con un Eckerson, W., “Data Warehousing Special Report: Data Quality and the Bottom Line.” Conjuntos de datos defectuosos o con errores le costaron mas de 600mil millones de dolares a empresas estadounidenses (3.5% of GDP).

* Generación de los datos: Los problemas presentes aqui pueden deberse a errores en el hardware (sensores), software(bugs), operadores (humanos). 
* Data Entry: Cuando los datos son generados manualmente, tal como cuando una efermera mide la estatura de un paciente, tiene que ser registrada en alguna computadora.
* Datos Faltantes : Un valor faltante dentro de un registro por ejemplo.
* Duplicado : Los datos duplicados son otro problema común. Duplicados quiere decir el mismo y exacto registro que se repite. Esto puede suceder debido a distintas razones; por ejempplo si suponemos que tenemos 10 archivos de datos, y accidentalmente cargamos el sexto archivo mas de una vez.

##### Procedencia de los datos

Cuando se encuentran problemas de calidad de datos, es crucial rastearlos hasta su origen. En ese sentido, todo el subconjunto de datos puede ser removido del análisis. Los metadatos pueden ayudar en llevar un control adecuado de la precodencia de los datos. Por ejemplo, supongamos que se recolectan archivos de datos diariamente desde una variedad de proveedores y son cargados en nuestra base de datos para la elaboración de reportes y análisis. Tipicamente estos archivos en formas de tablas poseen 2 columnas adicionales: fecha de carga y nombre de archivo. De esa manera si se encuentran problemas de calidad en los datos, se hace sencillo a partir de que archivo vinieron los datos, inspeccionar de manera detallada la línea exacta en el archivo con errores.

##### La calidad de los datos es una responsabilidad compratida

Las maneras en que los datos pueden ser imprecisos o de baja calidad son muchos. Además de los mecionados anteriormente, existen problemas de lineending, encoding, donde valores unicode son comprimidos en ASCII, datos corruptos, entre otros.

imgen tabla aquui

#### Recolección de los datos

##### Recolectar Todo
Imaginemos que se trata de desplegar un nuevo sistema de checkout en un sitio web. Se quiere saber exactamente como se desarrolla este proceso en contraste a las métricas, pero tambien será instructivo entender como está siendo usado. Por ejemplo, en algunos sitios, "añadir al carrito" es un solo click libre de complicaciones, así un patrón de conducta de un cliente puede ser añadir una cantidad de items al carito como area de espera y luego filtrar esa lista de productos hasta la selección final antes de hacer checkout. sin embargo hay sitios en los que "añadir al carrito" puede involucrar varios clicks, y remover items puede ser mas tedioso, de manera que los clientes necesitan tomar su decisión final antes de añadir items al carrito. Puede verse porque instrumentar el proceso tanto como sea posible puede conducir a la obtención de información valiosa acerca de esta característica.
Debe recolectarse y medirse tanto como sea posible. Nunca se sabrá que pueda necesitarse, en ocasiones sólo habrá una oportunidad de recolectar cietos datos. Mientras mas datos se recolectne, mayor será la posibilidad de modelar el comportamiento de los usuarios.

##### Priorizar Fuentes de Datos

Como decide una organización limitada por sus recursos, que conjuntos de datos son los siguientes a consumir?.
La motivación primordial del equipo de datos debería ser hacer coincidir las necesidades del negocio y las necesidades de los analistas, además de proveer un impacto en la organización.

tabla aqui 3-1

##### Conectando Puntos

Si bien es cierto que se ha establecido que existe valor en consumir datos a lo largo de una organización para una analítica mas profunda, existe mayor valor cuando se comienzan a conectar datos "adyacentes". 

##### Recolectar los Datos

Ahora que hemos considerado la pregunta, que datos recolectar, debemos considerar la peugnta como deben estos datos ser recolectdos.
Para muchas fuentes de datos, simplemente se toma un enfoque sistemático y se extraen todos los datos disponibles en esa fuente. Existen muchas maneras de consumir funetes de datos. Puede usarse una API, o recolectar datos desde un sitio FTP, o se puede incluso escarbar y extraer lo que se necesite. Si se trata de una descarga de una vez, entonces tod está dicho. Sin embargo, si los datos son actualizados o agregados frecuentemente, y esto es un flujo continuo, debe decidirse la manera en que los datos serán consumidos.

##### Adquirir o comprar Datos

Mientras que tipicamente existe riqueza de información en los sistemas de datos internos de una organización por si solos, y que además estos conjuntos de datos pueden ser suplementados con datos disponibles de manera pública, a veces solo se necesit apagar por datos adicionales proveniente de terceros.
Existen muchas razones por las cuales se podría adquirir conjuntos de datos externos.

Para decidir acerca de la adquisición de estos conjutnos de datos, debemos tener en cuenta:
* Precio : Los analistas y sus jefes aman lo gratis, pero en ocasiones es mejor pagar por datos de alta calidad. Se tiene que considerar si es un precio justo y considerar el valor que aportará a la organización. 
* Calidad : Cuan limpios y confiables son los datos?
* Exclusividad : son estos datos exclusivos del propietario y proveerán una ventaja frente a los competidores?
* Muestra : Puede obtenerse una muestra de los datos que permita juzgarel contenido y la calidad de losmismos?
* Actualizaciones : Con que frecuencia cambian los datos? 
* Confiabilidad
* Seguridad
* Términos de uso
* Formato
* Documentación
* Volumen
* Granularidad
* 













#### Data Analytics

#### Diseño de Métricas

#### Tests A/B

#### Toma de Decisiones
 