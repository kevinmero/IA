---
title: 'Espacio de Estados'
taxonomy:
    category:
        - docs
visible: true
---

<p># Prueba ## Subprueba Blablabla Sin lugar a dudas, una de las princdipales caraccter&iacute;sticas que reconocemos en la inteligencia es la capacidad para resolver problemas. Si consideramos una inteligencia como la humana, a la habilidad para analizar los elementos intr&iacute;nsecos de cada problema, que est&aacute; presente tambi&eacute;n ecccn muchas otras especies animales, se a&ntilde;ade la capacidad de abstraerlofdfs e identiﬁcar las acciones que se pueden rxxealizar sobre ellos para resolver el problema. En un nivel incluso superior de abstracci&oacute;n, reconocible solo en las llamadas especies superiores, podemos considerar tambi&eacute;n la capacidad de determinar cu&aacute;l puede ser, de entre los posibles m&eacute;todos que sve idean, el m&aacute;s adecuado, ya sea en t&eacute;rminos de tiempo, de recursos, de seguridad para el individuo, etc. De esta forma, aparece una triple capacidad de an&aacute;lisis, abstraccci&oacute;n y estrategia que sit&uacute;a el tema general de la resoluci&oacute;n de problemas en el n&uacute;cleo de la inteligencia artiﬁcial y, por ello, no resulta extra&ntilde;o que se consideren deseables para cualquier individuo, artificial o no, que queramos que se comporte inteligentemente. Podemos pensar en una variedad de problemas que van desde c&oacute;mo alcanzar una fuente de comida situada a cierta distancia y a la que no se puede ir directamente, hasta c&oacute;mo resolver un peque&ntilde;o juego como podr&iacute;a ser el famoso cubo de Rubik, o resolver el problema matem&aacute;tico de encontrar la soluci&oacute;n a una ecuaci&oacute;n num&eacute;rica. En todos ellos encontramos elementos comunes tras un proceso de abstracci&oacute;n que nos permiten de forma general deﬁnir la resoluci&oacute;n de problemas como: el proceso que, partiendo de una situaci&oacute;n inicial y utilizando un conjunto de procedimientos/reglas/acciones seleccionados a priori, es capaz de explicitar el conjunto de pasos que nos llevan a una situaci&oacute;n posterior que llamamos soluci&oacute;n. Lo que consideremos o no soluci&oacute;n depender&aacute; del contexto concreto del problema, y puede ser, por ejemplo, el conjunto de acciones que nos llevan a cumplir cierta propiedad, conseguir cierto objetivo, o verificar ciertas restricciones. Como estamos interesados en la generaci&oacute;n de mecanismos autom&aacute;ticos que se puedan llamar inteligentes, no nos contentamos con resolver problemas individuales y dar para cada problema una soluci&oacute;n independiente, sino que intentaremos buscar elementos comunes a una gran bolsa de problemas que faciliten dar una clasificaci&oacute;n de los mismos y reconocer m&eacute;todos y estrategias que puedan ser v&aacute;lidos de la forma m&aacute;s general posible. Para ello, y teniendo en cuenta lo la idea de modelar, es necesario que podamos expresar las caracter&iacute;sticas de los problemas usando un lenguaje formal com&uacute;n a todos ellos, para posteriormente proporcionar m&eacute;todos y estrategias generales (en forma de algoritmos o de heur&iacute;sticas, en nuestro caso) con los que poder obtener con ciertas garant&iacute;as soluciones de esos problemas. [[image file="2017-09/kr-entc.gif" ]] Una de las aproximaciones m&aacute;s generales y sencillas de formalizar un problema y sus posibles mecanismos de soluci&oacute;n es por medio de lo que se denomina espacio de estados. Antes de definir formalmente en qu&eacute; consiste este espacio, observemos que en todo momento estamos tratando con m&eacute;todos en los que la resoluci&oacute;n de los problemas se dan de forma din&aacute;mica, es decir, se supone que se produce una evoluci&oacute;n temporal, que pasa por etapas, que nos permite llegar de la situaci&oacute;n inicial en la que el problema se presenta hasta una situaci&oacute;n final en la que se ha encontrado la soluci&oacute;n del mismo. Es precisamente esta din&aacute;mica, en la que aplicamos las reglas u operaciones de las que disponemos, la que permite ir modificando cada situaci&oacute;n posible para llevarnos desde el inicio a la soluci&oacute;n. Simplemente, denominaremos estado a la representaci&oacute;n de los elementos que describen el problema en un momento dado, es decir, a la situaci&oacute;n en que se encuentra o se podr&iacute;a encontrar el problema en cada instante de tiempo. Estado: representaci&oacute;n de los elementos que describen el problema en un momento dado. La cuesti&oacute;n principal que debemos plantearnos para esta metodolog&iacute;a es acerca de qu&eacute; debemos incluir en el estado. Por desgracia, no existen directrices generales que permitan dar una respuesta satisfactoria a esta cuesti&oacute;n pero, siguiendo t&eacute;cnicas de resoluci&oacute;n de problemas cl&aacute;sicas, podemos asegurar que es importante guardar un equlibrio entre el ahorro de recursos de almacenamiento para la descripci&oacute;n del estado y la necesidad de tener suficiente informaci&oacute;n almacenada como para poder resolver el problema. Aunque a priori puede parecer una buena idea almacenar toda la informaci&oacute;n posible, pronto veremos que en problemas relativamente peque&ntilde;os la cantidad de estados puede ser tan grande que la capacidad de almacenamiento computacional se nos puede agotar sin darnos la opci&oacute;n de resolver el problema. Vemos, pues, que este enfoque entronca directamente con teor&iacute;as matem&aacute;ticas bien establecidas, como son la Teor&iacute;a de la Computabilidad (que estudia qu&eacute; es resoluble de forma autom&aacute;tica) y la Teor&iacute;a de la Complejidad (que estudia cu&aacute;ntos recursos necesitamos para resolver los problemas que s&iacute; son resolubles). Debe existir un equilibrio entre el ahorro de recursos de almacenamiento para la descripci&oacute;n del estado y la necesidad de tener suficiente informaci&oacute;n almacenada como para poder resolver el problema Este proceso de elegir adecuadamente la informaci&oacute;n que almacenamos en un estado es tan importante que se ha convertido en un eje central de la Inteligencia Artificial, recibiendo el nombre de Teor&iacute;a de la Representaci&oacute;n, y ha demostrado ser esencial para que algoritmos y heur&iacute;sticas concretas de resoluci&oacute;n sean o no eficientes a la hora de resolver problemas. Un buen algoritmo con una mala representaci&oacute;n puede ser tan ineficiente como un mal algoritmo y, muchas veces, una buena representaci&oacute;n es capaz de llevarnos a una soluci&oacute;n del problema incluso usando algoritmos malos. La elecci&oacute;n de los estados, como veremos m&aacute;s adelante en casos concretos, no solo determina qu&eacute; informaci&oacute;n se almacenar&aacute; de las diversas situaciones por las que pasa el problema, sino que en muchos casos es determinante tambi&eacute;n para decidir cu&aacute;les son las reglas u operaciones b&aacute;sicas que se permiten para realizar transformaciones entre estados. Otras veces tambi&eacute;n podemos encontrar restricciones debido a la incapacidad para realizar ciertas acciones para resolver un problema, lo que puede influir en c&oacute;mo se elegir&aacute;n los estados para hacerlos coherentes con las operaciones disponibles. En general, el proceso de transformar el problema original (al que muchas veces llamaremos simplemente "mundo real") en este espacio de estados que es manipulable por medios autom&aacute;ticos es lo que conocemos como modelar el problema (debe tenerse en cuenta que el modelado existe en otras muchas ramas de la ciencia, y nosotros aqu&iacute; solo consideramos el modelado computacional, que es un tipo particular de modelado matem&aacute;tico). Modelar computacional de un problema: proceso de transformar el problema original ("mundo real") en un espacio de estados que es manipulable por medios autom&aacute;ticos. Problema de b&uacute;squeda b&aacute;sico [[image file="2016-11/GraphStateSpace.png" align="right" width=300px ]]Si nos imaginamos este espacio de estados como un terreno por el cual nos podemos mover, donde partimos de un punto concreto del terreno (estado inicial) y podemos aplicar las reglas v&aacute;lidas para ir saltando de un estado a otro, podemos identificar la resoluci&oacute;n del problema (llegar hasta un estado final v&aacute;lido) con el problema de buscar un camino adecuado entre un estado inicial y un estado final. Es por ello que muy habitualmente se habla del Problema de B&uacute;squeda en el Espacio de Estados. Pasemos pues a dar una definici&oacute;n formal de esta idea: Un problema de b&uacute;queda b&aacute;sico es una 4-tupla \((X,S,G,d)\), donde \(X\) es un conjunto de estados (el que hemos estado llamando Espacio de Estados). \(S \subseteq X\), es un conjunto no vac&iacute;o de estados iniciales (no tiene porqu&eacute; existir un solo estado de partida). \(G \subseteq X\), es un conjunto no vac&iacute;o de estados finales (\(G\) se usa como inicial de Goals, objetivos en ingl&eacute;s, y al igual que no existe un &uacute;nico estado de partida, puede ocurrir que haya muchos estados finales v&aacute;lidos para el mismo problema). \(d: X \rightarrow \cal{P}(X)\) es una funci&oacute;n de transici&oacute;n. Para cada \(x\in X\), \(d(x)\) determina el conjunto de estados sucesores de \(x\) (\(\cal{P}(X)\) representa las partes de \(X\), es decir, el conjunto de los posibles subconjuntos de \(X\), ya que desde un estado concreto podemos llegar a varios posibles estados aplicando distintas operaciones o reglas permitidas). Observa que esta definici&oacute;n formal no explicita ni la forma en que hay que almacenar la informaci&oacute;n en los estados ni cu&aacute;les son las reglas v&aacute;lidas que permiten pasar de un estado a otro durante la resoluci&oacute;n, ya que todo ello depende del problema concreto que se est&eacute; resolviendo y nosotros estamos interesados en dar un marco general que permita aplicar los m&eacute;todos que desarrollemos al mayor conjunto posible de problemas. Una vez fijado este primer marco de representaci&oacute;n, podemos dar los pasos generales necesarios para "buscar" el camino que lleve desde el planteamiento inicial del problema hasta una soluci&oacute;n: Dar una representaci&oacute;n del problema, es decir, definir un espacio de estados que refleje las caracter&iacute;sticas del mundo real que sean necesarias para la resoluci&oacute;n del problema. Como ya se ha indicado, ha de tenerse en cuenta que esta elecci&oacute;n no es &uacute;nica, y que determinar&aacute; en gran medida la facilidad o dificultad de resolver el problema que tenemos entre manos. Asimismo, este paso determina tambi&eacute;n las acciones disponibles para moverse por este espacio. La capacidad para cambiar de representaci&oacute;n para obtener una m&aacute;s adecuada a la soluci&oacute;n del problema es lo que se denomina perspicacia. Especificar uno, o m&aacute;s, estados iniciales. Especificar uno, o m&aacute;s estados finales (objetivos o metas). A veces no se especifican propiamente los estados finales, sino alguna propiedad que han de cumplir para que se consideren v&aacute;lidos. Definir reglas a partir de las acciones disponibles. El conjunto de reglas definir&aacute; la funci&oacute;n de transici&oacute;n del sistema formal. Estas reglas determinan la estructura del espacio de estados, y esta estructura es responsable, en gran medida de la dificultad que nos encontremos posteriormente para realizar b&uacute;squedas en el espacio. El problema se resuelve usando las reglas en combinaci&oacute;n con una estrategia de control. De nuevo, obs&eacute;rvese que aqu&iacute; no prefijamos ninguna estrategia de control espec&iacute;fica. M&aacute;s adelante veremos algunas de las m&aacute;s habituales y estudiaremos sus bondades e inconvenientes para resolver problemas de forma general. Una buena estrategia de control debe establecer el orden de aplicaci&oacute;n de las reglas y resuelve los posibles conflictos que puedan aparecer. Dependiendo de la estrategia de control utilizada, o de las necesidades de la b&uacute;squeda, puede ser necesaria una funci&oacute;n de coste que indique cu&aacute;nto cuesta aplicar una regla determinada a un estado determinado, de esa forma podemos calcular cu&aacute;nto cuesta el proceso total de ir desde un estado inicial hasta un estado final aplicando dicha estrategia, y de esta forma comparar entre s&iacute; los distintos caminos que existen para resolver el problema. Ejemplo Como primer ejemplo, consideremos el puzle de piezas deslizantes, donde el objetivo es deslizar las piezas usando el hueco hasta conseguir el orden deseado. El caso general consiste en un puzzle de \(n\times m\) cuadr&iacute;culas, con \(n\times m-1\) piezas numeradas consecutivamente y 1 hueco. A veces podemos encontrar este puzle en una variante equivalente haciendo uso de im&aacute;genes que han de reconstruirse situando el orden adecuado en sus piezas. [[image file="2015-07/a1c910b4-1527-11e2-bb76-001e670c2818.jpg" ]] El espacio de estados, \(X\), describe todas las posibles combinaciones de las piezas y el hueco. Como queremos dar un m&eacute;todo general de resoluci&oacute;n, el conjunto de los estados iniciales es, en este caso, todo el espacio \(S=X\), y el conjunto de estados finales es &uacute;nicamente uno, el estado en el que todos est&aacute;n en orden y el hueco se sit&uacute;a al final, tal y como muestra la figura anterior. La funci&oacute;n de transici&oacute;n describe el cambio que resulta de mover, en un estado concreto, el hueco en cualquiera de las 4 direcciones (en los bordes y esquinas s&oacute;lo podr&aacute; moverse en 3 o 2 direcciones posibles, respectivamente). Obs&eacute;rvese que, en este caso, la soluci&oacute;n al puzzle no es el estado final, que sabemos ex&aacute;ctamente cu&aacute;l es, sino el camino que lleva desde un estado inicial (prefijado, o aleatorio) hasta ese estado final. Es decir, deseamos conocer la sucesi&oacute;n de movimientos que nos permiten resolver el puzle. [[image file="2015-07/23717796-1528-11e2-bb76-001e670c2818.jpg" ]] En el caso de un puzle de tama&ntilde;o \(3\times 3\) (en este caso el puzle se conoce como 8-puzle, que es el n&uacute;mero de piezas m&oacute;viles) el n&uacute;mero de posibles estados es de \(9!= 362880\), un tama&ntilde;o que permite, con la capacidad de los ordenadores actuales, hacer una b&uacute;squeda exahustiva para encontrar el camino desde cualquier estado al estado final ordenado. Esta b&uacute;squeda exahustiva se consigue comenzando por el estado inicial e ir visitando a partir de &eacute;l todos los dem&aacute;s estados por la aplicaci&oacute;n sucesiva de las reglas de transici&oacute;n, de esta forma, si existe una soluci&oacute;n (un camino que conecta el estado inicial y el final) este m&eacute;todo la encontrar&aacute;, aunque, posiblemente, de una forma completamente ineficiente. Si jugamos con el puzle de tama&ntilde;o \(4\times 4\) (que se conoce como 15-puzle) el n&uacute;mero de posibles estados es de \(16! \approx 2x10^{13}\), demasiado grande para una b&uacute;squeda exahustiva. En casos como &eacute;ste, donde el espacio de estados es excesivamente grande para hacer un recorrido exahustivo de sus elementos, hemos de encontrar estrategias de b&uacute;squeda m&aacute;s depuradas que nos permitan alcanzar las soluciones de forma m&aacute;s eficiente y usando menos recursos (en tiempo y en espacio almacenado). Consideremos otro puzle habitual, el puzle de los misioneros y can&iacute;bales: Tres misioneros se perdieron explorando una jungla. Separados de sus compa&ntilde;eros, sin alimento y sin radio, s&oacute;lo sab&iacute;an que para llegar a su destino deb&iacute;an ir siempre hacia adelante. Los tres misioneros se detuvieron frente a un r&iacute;o que les bloqueaba el paso, pregunt&aacute;ndose que pod&iacute;an hacer. De repente, aparecieron tres can&iacute;bales llevando un bote, pues tambi&eacute;n ellos quer&iacute;an cruzar el r&iacute;o. Ya anteriormente se hab&iacute;an encontrado grupos de misioneros y can&iacute;bales, y cada uno respetaba a los otros, pero sin confiar entre ellos. Los can&iacute;bales se com&iacute;an a los misioneros cuando les superaban en n&uacute;mero, y los misioneros bautizaban a los can&iacute;bales en situaciones similares. Todos quer&iacute;an cruzar el r&iacute;o, pero el bote no pod&iacute;a llevar m&aacute;s de dos personas a la vez y los misioneros no quer&iacute;an que los can&iacute;bales les aventajaran en n&uacute;mero. &iquest;C&oacute;mo puede resolverse el problema, sin que en ning&uacute;n momento hayan m&aacute;s can&iacute;bales que misioneros en cualquier orilla del r&iacute;o? El espacio de estados asociado al problema podr&iacute;a representarse de la siguiente forma (muy descriptiva, pero poco pr&aacute;ctica desde el punto de vista computacional): [[image file="2017-09/mc-search-space.png" ]] Ejercicio: Formaliza la siguiente versi&oacute;n del puzle "Todos los d&iacute;gitos del Rey" explicitando una representaci&oacute;n de sus estados y la funci&oacute;n de transici&oacute;n entre ellos: Dado el conjunto de d&iacute;gitos \(0123456789\), inserta los s&iacute;mbolos de los operadores aritm&eacute;ticos (\(\times + - /,\)) entre ellos para que la expresi&oacute;n resultante se eval&uacute;e como 100. Por ejemplo: \[0+1+2+3+4+5+6+7+(8\times 9) =100\] &iquest;Puedes encontrar otros? Criterios de evaluaci&oacute;n Antes de que pasemos a ver la variedad de algoritmos (estrategias) que han sido dise&ntilde;ados para resolver problemas de b&uacute;squeda en espacios de estados, puede merecer la pena mencionar, aunque sea de forma breve, c&oacute;mo podemos evaluar la eficiencia de estos algoritmos. Habitualmente, se suelen usar los siguientes criterios de evaluaci&oacute;n: Complejidad en tiempo: Se puede medir como el n&uacute;mero de veces que se aplica la funci&oacute;n de transici&oacute;n que necesita el algoritmo para encontrar la soluci&oacute;n. En un contexto m&aacute;s amplio suele medirse por medio del n&uacute;mero de pasos que da un algoritmo en su ejecuci&oacute;n. Complejidad en espacio: Se mide por la cantidad de espacio de almacenamiento necesario para encontrar la soluci&oacute;n. En el caso que estamos viendo lo podemos medir como el n&uacute;mero de estados que el algoritmo debe mantener en memoria para encontrar la soluci&oacute;n. Algunos algoritmos podr&aacute;n "olvidar" los estados por los que van pasando, mientras que otros necesitan mantener una memoria con esos estados para poder volver atr&aacute;s en la b&uacute;squeda o saber por cu&aacute;les ha pasado. Completitud: Si existe una soluci&oacute;n, &iquest;est&aacute; garantizado por el algoritmo que la encontraremos? Optimalidad: Si existen varias soluciones, &iquest;encuentra el algoritmo la &oacute;ptima? Esta optimalidad se mide respecto de alguna medida, por ejemplo, la que est&aacute; m&aacute;s cerca en n&uacute;mero de transformaciones para llegar desde el estado inicial, o la que ha usado menos memoria. Una representaci&oacute;n (casi) universal Normalmente, los algoritmos que vamos a ver se basan en la suposici&oacute;n de que el espacio de b&uacute;squeda tiene la estructura de un grafo dirigido: cada nodo del grafo representa uno de los estados del espacio, y dos nodos est&aacute;n conectados si existe una forma de ir de uno al otro por medio de la funci&oacute;n de transici&oacute;n. Normalmente, cuando resolvemos el problema a partir de un estado particular, podemos construir un &aacute;rbol que se construye partiendo del estado inicial y donde en cada nivel se a&ntilde;aden los estados que se pueden alcanzar desde los estados del nivel anterior (y que, en consecuencia, puede contener estados repetidos). En este caso, la profundidad (\(d\), de depth) del &aacute;rbol es la longitud m&aacute;xima de los caminos que se pueden construir desde cualquier nodo a la ra&iacute;z; y el factor de ramificaci&oacute;n (\(b\), de branch) del &aacute;rbol es el m&aacute;ximo n&uacute;mero de sucesores que puede tener un nodo del &aacute;rbol. En un &aacute;rbol, los sucesores inmediatos de un nodo (salvo las hojas, claro, que son los nodos terminales) se llaman hijos, el predecesor de un nodo (salvo la ra&iacute;z, que no tiene predecesor), que es &uacute;nico, se llama padre, y los nodos que tienen el padre com&uacute;n se llaman hermanos. [[image file="2015-07/96a74992-1529-11e2-bb76-001e670c2818.png" ]] Es importante destacar que nuestro espacio de estados NO es un &aacute;rbol, sino que el &aacute;rbol se consigue al considerar la estructura ordenada que surge entre los diversos estados de nuestro problema al aplicar las reglas que permiten pasar de unos estados a otros. Si cambiamos la representaci&oacute;n de los estados (y en consecuencia las reglas que se pueden aplicar) cambiar&aacute; el &aacute;rbol asociado, pero nuestro problema sigue siendo el mismo. Es por ello que la representaci&oacute;n es fundamental para obtener soluciones m&aacute;s o menos eficientes, ya que los posibles caminos entre los nodos que representan estados iniciales y los nodos que representan estados finales pueden cambiar completamente dependiendo del &aacute;rbol que obtengamos. Para saber m&aacute;s... Tema 3 de la asignatura de IA del Grado en Ingenier&iacute;a en Inform&aacute;tica - Tecnolog&iacute;as Inform&aacute;ticashttp://www.cs.us.es/cursos/iati/temas/tema-03.pdf Tema 3 Artificial Intellicenge and its teaching http://aries.ektf.hu/~gkusper/ArtificialIntelligence_LectureNotes.v.1.0.4.pdf Tema 3 Artificial Intellicenge. Foundations of Computational Agents http://artint.info/html/ArtInt_46.html</p>