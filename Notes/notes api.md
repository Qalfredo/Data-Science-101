# Data Science 101 - API's

Las APIs (Appliaction programming interfaces) son una gran parte de lo que se cononce como web. Para 2013 habian al rededor de 10000 APIs publicadas por companias para uso abierto. si se compara este numero con la cantidad de APIs disponibles de manera publica en 2010, tenemos el cuadruple. 

Las APIs se han vuelto una parte importante de nuevas areas de negocios, es por esta razon que tener un entendimiento solido de como funcionan es clave para culaquier carrera en la industria del software. 

## Marco de Referencia

Cuando se habla de APIs, gran parte se centra en conceptos abstractos. En aras de fijar los conceptos empecemos considerando algo que es de fisico: *el servidor*. Un servidor no es mas que una gran computadora. Posee las mismas partes y elementos de un desktop o laptop usados para trabajo, solo que en este caso son elementos mas potentes que hacen que los calculos sean mas rapidos. Tipicamente los servidores no tienen un monitor, teclado o raton, lo que los hace a simple vista poco accesibles. La realidad es que el personal IT se conecta de manera remota a este servidor para trabajar en el. 

Los servidores son usados para muchas cosas. Algunos solo almacenan datos, otros envian correos. El tipo de servidores con el cual el personal interactua mas es el de Web servers. Estos son servidores que entregan una pagina web cuando visitamos un sito web. Para entender mejor como funciona, una simple analogia:

---
*De la misma manera que un programa como Solitrio espera a que hagas click en alguna carta para hacer algo, un servidor web corre un programa que espera que una persona solicite alguna pagina web.*
---

No hay nada magico o de otro mundo en ello, un desarrollador escribe un programa, lo copia a un servidor y el servidor corre el programa de manera continua.

## Que es una API y porque debería importarnos

Los sitios web son disenados para usar las virtudes de las personas. Los humanos son increiblemente buenos para tomar informacion de manera visual, combinarla con experiencias para convertir esta informacion en conocimiento y luego accionar a partir de su significado. Es por esto que puedes apreciar una figura en un sitio web y saber que esa pequena caja con la frase *nombre* arriba significa que debes tipear la palabra que usualmente usas para identoicarte demanera informal.

Sin embargo, que sucede cuando tienes una tarea que consumiria mucho tiempo, tal como copiar la informacion de contacto de cientos de clientes de un sitio a otro? Lo ideal seria poder delegar esta tarea a una computadora, de manera que pueda ser llevada a cabo de manera rapida y precisa. Desafortunadamente, las caracteristicas que hacen que un sitio web sea accesible o intuitivo para los humanos, los hacen dificil de usar por computadoras.

La solucion es una API. Una API es la herramienta que hace los datos de un sitio web asimilables para una computadora. Mediante ella una computador puede ver y editar datos, justo como una persona puede hacerlo al cargar paginas y llenar formularios.


![73c10a4db7511d53234d673e9b37aaf9.png?format=jpg](https://images.zapier.com/storage/photos/73c10a4db7511d53234d673e9b37aaf9.png?format=jpg)

## Como se usa un API

Cuando dos sitemas (sitios web, pcs, telefonos inteligentes) se enlazan mediante una API, decimos que estan integrados. En una ontegracion, se tienen dos lados, cada uno con un nombre especial. Ya hemos mencionado uno de esos lados: el servidor. Este lado es el que provee la API. Esto ayuda a recordar que una API es simplemente otro programa corriendo en el servidor. Puede ser parte del mismo programa que maneja el trafico web, o puede ser otro completamente distinto. En cualquier caso, esta esperando por otros a que soliciten los datos. 

El otro lado es el cliente. Este es un programa separado que conoce que datos estan disponibles a traves de la API y puede manipularlos, tipicamente a pedido de un usuario. Un buen ejemplo es una aplicacion movil que se sincroniza con un sitio web. Cuando presionas el boton para recargar en la aplicacion, este habla al servidor via una API y actualiza la informacion ams reciente.

## Protocolos

### Conociendo las reglas

Las personas creamos la etiqueta social para guiar nuestras interacciones. Un ejemplo es como hablamos el uno con el otro por telefono. Imaginemos que hablamos con un amigo, mientras la otra persona esta hablando sabemos que debemos estar en silecio, incluso permitimos pausas breves. Si nos hacen una pregunta y permanecen en silencio sabemos que esperan una repsuesta de nosotros. 

Las computadoras tienen algo similar, a este algo lo llamamos protocolo. Un protocolo es un conjunto de reglas aceptado, que gobierna la manera en la que las computadoraas se comunican. Si lo comparamos con nuestros estandares, los protocolos son extremadamente rigidos. Piensen en 2 oraciones, "mi color favorito es el azul" y "el azul es mi color favorito". Las personas son capaces de analizar ambas y llegar a la conclusion de que significan lo mismo a pesar de que las palabras esten en diferente orden. Desafortunadamente las computadoras no son tan inteligentes.

Para que dos computadoras puedan comunicarse de manra efectiva, el servidor debe saber con exactitud como el cliente estructura sus mensajes. 

### El Protocolo de la Web

Existe un protocolo para casi todo, cada uno hecho con propositos diferentes y resolver diferentes tareas. Algunos ejemplos que seguro han escuchado son: bluetooth para conectar dispositiovs, POP o IMAP para obtener correos.

En la Web, el protocolo principal es el HTTP (Hyper-Text Transfer Protocol). Cuando se tipea una direccion como `http://example.com` en el navegador web, la parte "http" le esta diciendo al navegador que use las reglas de HTTP para comunicarse con el servidor. 

Con la ubicuidad del protocolo HTTP en la web, muchas companias eligen adoptarlo como el protocolo con el cual funcionan sus APIs. Una de las ventajas de usar un protocolo familiar, es que mejora la curva de aprendizaje para desarrolladores. Otro de los beneficios es que HTTP tiene varias caracteristicas utiles en cuanto a construir buenas APIs. 

### HTTP Requests

La comunicacion en HTTP se centra al rededor de un concepto llamado el ciclo Request-Response o pedido-respuesta. El cliente envia un pedido al servidor para hacer algo. El servidor, asu vez, envia una respuesta al cliente diciendo si el servidor pudo o no pudo hacer lo que el cliente pedia.

![9ec65c79de8ae54080c1b417540469a6.png?format=jpg](https://images.zapier.com/storage/photos/9ec65c79de8ae54080c1b417540469a6.png?format=jpg)
Para elaborar un pedido valido, el cleinte debe incluir 4 elementos:

* URL
* Method
* Lista de Headers
* Body 

#### URL 

Las URLs son familiares por el uso diario que le damos en la web, pero alguna se vez se han tomado el tiempo de considerar su estructura? En HTTP, una URL es una direccion unica para algo. Lo que pueda ser ese algo depende enteramente de lo que este corriendo en el servidor. Pueden ser paginas web, imagenes o incluso videos. 

API extiende esta idea un poco mas alla para incluir nombres como clientes, productos y tweets. De este modo, las URLs se vuelven una forma sencilla para el cliente de decirle al servidor con que cosa necesita interactuar. Dentro de una API esta cosas reciben el nombre de recursos.

#### Methods

El metodo del pedido le dice al servidor que tipo de accion el cliente quiere que el servidor lleve a cabo. Existen cuatro metodos comunmente usados en APIs:

* GET: pide al servidor recuperar un recurso.
* POST: pide al servidor crear un nuevo recurso.
* PUT: pide al servidor editar o actualizar un recurso existente.
* DELETE: pide al servidor borrar un recurso.

![935a8b3ca25e078bed0bc11488a2ef8c.png](https://cdn.zapier.com/storage/photos/935a8b3ca25e078bed0bc11488a2ef8c.png)

Consideremos un ejemplo para ilustrar estos conceptos. Digamos que hay una pizzeria con una API que puede ser usada para ordenar pizza. Se ordena una pizza haciendo un pedido POST al servidor del restaurant con los detalles de la orden, pidiendo crear la pizza. Tan pronto como envias el pedido, te das cuenta de que elegiste un ingrediente equivocado, entonces haces un pedido PUT para cambiarlo. Mientras que esperas la pizza, hacesvarios pedidos GET para chequear el status. Despues de una hora esperando, decides cancelar la pizza mediante un pedido DELETE.

#### Headers

el encabezado provee meta-informacion acerca de un request. Son simplemente una lista de items, como la fecha en la que el cliente realizo el pedido y el tamano de del body del request.

Por ejemplo, cuando visitamos un sitio web que es formateado especialmente para dispositivos moviles. Esto es posible gracias a un HTTP header llamando "User-Agent". El cliente usa este encabezado para decirle al servidor que tipo de dispositivo se esta usando, y los sitios web lo suficientemente inteligentes pueden detectarlo y enviar el meor formato para el dispositivo.

#### Body

El cuerpo de un pedido contiene los datos que el cliente quiere enviar al servidor. 

![4717d012f26dc6a4928e0d025102af7f.png?format=jpg](https://images.zapier.com/storage/photos/4717d012f26dc6a4928e0d025102af7f.png?format=jpg)

### HTTP Responses

Luego de que el servidor recibe un pedido del cliente, este intenta procesar el pedido y enviar una respuesta al cliente. Estas resouestas HTTP tienen una estructura similar a los pedidos. La principal diferncia es que en lugar de un URL se incluye un status code.

#### Status Codes

Son numeros de 3 digitos, con un significado especifico. Cuando se usa una API incorrectamente, este pequeno numero puede comunicar mucha informacion. Por ejemplo, la siguiente respuesta que es muy comun al visitar una pagina:

![8b38efb0fa87bbf81018ff532f929a8a.png?format=jpg](https://images.zapier.com/storage/photos/8b38efb0fa87bbf81018ff532f929a8a.png?format=jpg)

El codigo detras de esta respuesta es 404, que significa "Not Found". Siempre que el cliente haga un pedido por un recurso que no existe, el servidor respondera con un codigo 404. 

Luego de que se entrega la respuesta al cliente, el ciclo request-response se ha completado. Ahora depende del cliente iniciar futuras interacciones. El servidor no enviara mas datos hasta que el cliente haga un nuevo pedido.

![df8b6d09ab35aac47c1fb7b020a42d61.png?format=jpg](https://images.zapier.com/storage/photos/df8b6d09ab35aac47c1fb7b020a42d61.png?format=jpg)

## Formatos de Datos

### Representando los Datos

Cuando se comparten datos, las posibilidades de como mostrar la iformacion solo se limitan por la imaginacion humana. 

Un formato bien disenado viene dado por que hace que la informacion sea sencilla de entender por el usuario.

El mismo principio aplica cuano se comparten datos entre computadoras. Una computadora tiene que colocar los datos en un formato que la otra computadora entienda. Generalmente, esto significa algun tipo de formato de texto. Los formatos mas comunes encontrados en APIs actualmente son JSON y XML.

### JSON 

Muchas APIs nuevashan adoptado JSON como un formato debido a que esta basado en el popular lenguaje Javascript, que es ubicuo en la web y usable tanto en el front-end como en el backend de una aplicacion web o servicio web. JSON es un formato simple, se compone de dos elementos atomicos: keys y values. Las claves representan atributos de los datos o el objeto que esta siendo descrito.

```
{
    "crust" : "original",
    "toppings" : ["cheese", "pepperoni"],
    "status" : "cooking"
}
```

![5422e3c48cc047fb5c8f29b66367fffb.png?format=jpg](https://images.zapier.com/storage/photos/5422e3c48cc047fb5c8f29b66367fffb.png?format=jpg)


```
{
    "crust" : "original",
    "toppings" : ["cheese", "pepperoni"],
    "status" : "cooking",
    "customer" : {
        "name" : "Brian",
        "phone" : "55-555-55555"
    }
}
```

### XML

XML existe desde 1996. Con el apsar del tiempo se ha vuleto muy maduro y un formato poderoso y util para representar datos. Tal y como JSON, XML provee unos cuantos bloques que los desarrolladores de APIs usan para estructurar los datos. El bloque principal recibe el nombre de nodo. 

```
<order>
    <crust>original</crust>
    <toppings>
        <topping>cheese</topping>
        <topping>pepperoni</topping>
        ...
    </toppings>
    <status>cooking</status>
</order>
     
```

XML simepre inicia con un nodo raiz, que en nuestro ejemplo es "order". Dentro de cada nodo hay mas nodos hijos. El nombre de cada nodo nos dice el nombre del atributo, y los datos dentro el valor actual. 

![](https://images.zapier.com/storage/photos/5cfca2d3c6904339b4d1e06181b0c850.png?format=jpg)
### Como se usan los formatos de datos en las APIs


Luego de haber explorado someramente los formatos mas usados, necesitamos saber como usarlos en HTTP. Para hacerlo, usaremos uno de los conceptos fundamentales en HTTP de nuevo: Headers. Existe un header para decir que tipo de formato estan los datos: "content-type".

Cuando el cliente envia el content-type header en un pedido, le esta diciendo al servidor que los datos en el cuerpo del pedido son formateads en una forma particular. Analogamente cuando el servidor envia una respuesta, usa el mismo header para decirle al cliente que formato debe usarse para leer los datos. 

En ocasiones el cliente solo puede hablar un formato. Si el servidor devuelve cualquier otra cosa que no sea ese formato, el cliente fallara y arrojara un error. Afortunadamente, en ese caso hay otro header util. El cliente puede configurar el header "accept" para decrile al servidor que formato acepta.

![3a1025b070c2f50269f34379d8c220de.png?format=jpg](https://images.zapier.com/storage/photos/3a1025b070c2f50269f34379d8c220de.png?format=jpg)































