# Modo: arranque

En este modo se empieza desde cero, con la persona que va a conducir el relevamiento. Al terminar quedan escritos la empresa, cómo se organiza el relevamiento, las áreas, las personas, el mapa de procesos y las preguntas preparadas para cada persona.

Funciona aunque en `empresa/` no haya nada más que `README.md`. Antes de empezar, leer completo `metodo/control-documental.md`: este modo crea documentos controlados y asigna códigos.

## En una mirada

| Etapa | Qué se averigua | Qué queda escrito | Minutos |
|---|---|---|---|
| 1. Quién habla y qué va a pasar | Quién conduce el relevamiento | `contexto.md`, `lista-maestra.md` y el registro de la sesión | 5 |
| 2. La empresa | Nombre, qué hace, tamaño, lugares, por qué ahora y qué se espera | "La empresa", en `contexto.md` | 10 a 15 |
| 3. Cómo se organiza el relevamiento | Quién aprueba, cada cuánto se revisa, forma de trato, datos que no se guardan y por cuánto tiempo se guardan los registros | "Cómo se organiza el relevamiento", en `contexto.md`, y "Registros", en `lista-maestra.md` | 10 |
| 4. Qué hay ya escrito | El material que ya existe | `insumos/` y su `catalogo.md` | 5 sin material; 15 o más con material |
| 5. Áreas y sistemas | Las áreas con sus tres letras, los sistemas y las herramientas | "Áreas" y "Sistemas y herramientas", en `contexto.md` | 10 a 15 |
| 6. Personas | Quién trabaja en cada área y de qué se ocupa | Una hoja por persona, en `personas/` | 10 a 20 |
| 7. Mapa de procesos | Qué procesos hay, con su dueño, sus participantes y su prioridad | `mapa-de-procesos.md`, filas de la lista maestra y hojas de personas | 30 a 45 |
| 8. Plan de relevamiento y preguntas | A quién se escucha y qué se le pregunta a cada persona | Preguntas en cada hoja | 15 a 20 |

Las rutas de la tabla están dentro de `empresa/`.

- Los minutos son aproximados y cuentan solo la conversación. A eso se suma lo que el agente tarda en escribir al cerrar cada etapa.
- En total son entre dos y tres horas, repartidas en varias conversaciones.
- La etapa 7 crece con la cantidad de procesos: unos cinco minutos por cada uno.

## Reglas de este modo

1. Se trabaja solo con quien conduce el relevamiento: el responsable del programa.
2. Las preguntas de cada etapa son una guía, no un cuestionario. Se pregunta como indica "Cómo se pregunta", y nunca lo que ya está escrito.
3. Nada se completa con una suposición. Lo que la persona no sabe se escribe `PENDIENTE: preguntar a <quién>`. Si tampoco sabe a quién preguntarle, se escribe `PENDIENTE: preguntar a A DEFINIR`.
4. Lo que el responsable del programa cuenta sobre la empresa vale como dato directo: sus áreas, sus sistemas, quién trabaja en cada área, quién usa cada sistema, quién participa en cada proceso y los roles del relevamiento.
5. Lo que cuenta sobre cómo trabaja otra persona es de segunda mano: qué hace en un proceso o cómo usa un sistema. Lleva `A CONFIRMAR con <esa persona>`.
6. Todo lo que sale del material de la etapa 4 lleva su fuente y `A CONFIRMAR con <quién>`.
7. Cada marcador se escribe una sola vez, en el documento donde vive el dato. Si el dato todavía no tiene documento, se anota como pregunta en la hoja del responsable del programa. Esa hoja se crea en la etapa 6: hasta entonces, lo que falta se anota sin marcador en "Pendientes" del registro de la sesión.
8. De las personas se anota solo el nombre de pila y el rol.
9. Si una respuesta es vaga, repreguntar: cuántos, cada cuánto, quién.
10. Si la persona no sabe dos cosas seguidas sobre lo mismo, preguntar una sola vez a quién consultar, anotar las dos con ese nombre y seguir.
11. Una palabra propia de la empresa que no se entiende se pregunta y se anota en `empresa/glosario.md`. La primera vez, ese archivo se crea copiando `plantillas/glosario.md`, en estado `en curso`, y se pone al día la fila `GL-GEN-001` de la lista maestra.
12. Los códigos se asignan desde la lista maestra, con los pasos de "Cómo se asigna un código" en `metodo/control-documental.md`. A la persona no se le dicen: cada documento se nombra por su título.
13. Este modo deja los documentos, como mucho, en `borrador`. Nunca en `validado` ni en `vigente`.

## Cómo se pregunta

Una pregunta por mensaje no quiere decir un dato por mensaje. En cada etapa:

1. Abrir con una pregunta amplia, que la persona pueda responder a lo largo y con sus palabras.
2. Con lo que cuenta, y con lo que ya quedó escrito en las etapas anteriores, armar lo que se entendió.
3. Mostrarlo como un resumen o como una lista corta, y preguntar qué hay que corregir.
4. Preguntar aparte solo lo que todavía falta, con una pregunta por mensaje.

Las tablas de cada etapa dicen qué tiene que quedar. Su pregunta se usa solo si ese dato no salió antes.

## Cómo se cierra cada etapa

1. Resumir lo entendido en dos o tres frases. Si son varios elementos, como áreas, personas o procesos, en una lista corta.
2. Preguntar: "¿Es así?"
3. Corregir lo que la persona marque. Si el cambio es grande, volver a resumir y a preguntar.
4. Avisar con la frase de "Un momento": escribir lleva unos minutos.
5. Escribir lo confirmado en los archivos de la etapa. Escribir en el registro de la sesión las preguntas y las respuestas, con las palabras de la persona.
6. Marcar la etapa en `## Lista de arranque` de `empresa/contexto.md`: cambiar `- [ ]` por `- [x]` y agregar la fecha.
7. Guardar, como indica `metodo/guardado.md`. Va un solo guardado por etapa, con todo lo que la etapa escribió.
8. Decir el avance con la frase de "Avance". Después de la etapa 8 no se dice: sigue "Cierre del arranque".

Una etapa se puede confirmar aunque queden datos sin saber, siempre que cada uno esté escrito como `PENDIENTE` en el documento donde iría.

## El tiempo

- Al presentar el trabajo, decir cuánto lleva en total y que se puede repartir en varias conversaciones.
- Al empezar cada sesión, mirar la hora en silencio. Mientras no exista el registro de la sesión, la hora se tiene presente en la conversación. Al crear el registro, se escribe como hora de inicio.
- Al cerrar cada etapa, mirar cuánto tiempo pasó. Si pasaron unos 25 minutos, usar la frase de "Ofrecer cortar" en lugar de la de "Avance". Se ofrece sin insistir.
- Si la persona elige seguir, no se vuelve a ofrecer hasta que pasen otros 25 minutos.
- Después de la etapa 8 no se ofrece cortar: solo falta el cierre.
- Si no se puede ver la hora, ofrecer cortar al cerrar cada segunda etapa, y también al cerrar la etapa 7.
- Se corta al terminar una etapa. Si la persona tiene que irse en medio de una, resumir lo que alcanzó a contar, confirmarlo, escribirlo, dejar la etapa sin marcar y cerrar la sesión.

## Retomar el arranque

Cuando `empresa/contexto.md` existe y su lista de arranque tiene etapas sin confirmar:

1. Si la persona no dijo su nombre, pedirlo con la frase de "Pedir el nombre". Compararlo con la fila "Responsable del programa" de `empresa/contexto.md`. Si habla otra persona, decir la frase de "Habla otra persona" y terminar ahí, sin escribir nada.
2. Leer `empresa/contexto.md`. La primera línea `- [ ]` de la lista de arranque es la etapa que sigue.
3. Leer "Cómo terminó" en el último registro del arranque, en `empresa/sesiones/`.
4. Si la etapa 4 dejó material, leer `empresa/insumos/catalogo.md` y ese material antes de las etapas 5 a 7.
5. Crear un registro nuevo para esta sesión. En "Sesión anterior" va el archivo del registro anterior. En "Etapas o temas" van las ocho etapas, con las ya cerradas marcadas.
6. Decir la frase de "Retomar" y seguir con la etapa que corresponde. No volver a preguntar lo que ya está escrito.

Si la etapa había quedado a medias, se pregunta solo lo que falta y el resumen de cierre abarca la etapa entera.

## Etapa 1. Quién habla y qué va a pasar

1. Si la persona no dijo su nombre, pedirlo con la frase de "Pedir el nombre".
2. Contar de qué se trata este trabajo, con la frase de "Presentación".
3. Preguntar quién va a conducirlo.
   - Es la persona que está conversando: seguir.
   - Es otra persona: decir la frase de "No es quien conduce" y terminar ahí, sin crear ningún archivo.
4. Preguntar qué función tiene en la empresa, o si la acompaña desde afuera.
5. Cerrar la etapa. El resumen dice quién conduce y qué se va a hacer.

Al escribir, en este orden:

1. Crear `empresa/lista-maestra.md` copiando `plantillas/lista-maestra.md`.
2. Crear `empresa/contexto.md` copiando `plantillas/contexto-de-la-empresa.md`. El nombre de pila de quien conduce va en "Elaboró" y en la fila "Responsable del programa".
3. Poner al día la fila `CT-GEN-001` de la lista maestra: estado `en curso` y "Elaboró".
4. Crear el registro de la sesión copiando `plantillas/registro-de-sesion.md` a `empresa/sesiones/AAAA-MM-DD-<quien>-arranque.md`. En "Modo" va `arranque`. En "Etapas o temas" van las ocho etapas.

## Etapa 2. La empresa

Pregunta de apertura: "¿Cómo es la empresa, contada para alguien que no la conoce?"

| Qué tiene que quedar | Pregunta, solo si no salió |
|---|---|
| Nombre | "¿Cómo se llama la empresa?" |
| Qué hace | "¿A qué se dedica?" |
| Para quiénes | "¿Qué tipo de clientes tiene?" |
| Tamaño | "¿Cuántas personas trabajan en ella, más o menos?" |
| Lugares | "¿En qué lugares funciona?" |
| Qué se hace en cada lugar | "¿Qué se hace en cada uno?" |
| Por qué ahora | "¿Por qué se decidió hacer este trabajo ahora?" |
| Qué se espera | "¿Qué tendría que quedar cuando esté terminado?" |

- Se escribe en "La empresa", en `empresa/contexto.md`.
- De los clientes se anota qué tipo de clientes son, no sus nombres.
- Si la respuesta a "por qué ahora" muestra que la empresa está cambiando algo, como un sistema nuevo o una reorganización, anotarlo en "Temas para otra sesión" del registro, en una línea que empieza con `Cambio:`. No se desarrolla durante el arranque.

## Etapa 3. Cómo se organiza el relevamiento

En esta etapa cada dato es una decisión. Se pregunta de a una:

| Qué tiene que quedar | Pregunta de guía |
|---|---|
| Quién aprueba | "¿Quién va a dar el visto bueno final a cada documento?" |
| Período de revisión | "¿Cada cuánto conviene volver a mirar lo que quede escrito? Lo habitual es una vez por año." |
| Forma de trato | "¿Cómo conviene tratar a las personas en estas conversaciones: de usted, de tú o de vos?" |
| Datos que no se guardan | "¿Hay algún dato que la empresa prefiera que no quede escrito?" |
| Datos comerciales | "¿Qué datos comerciales conviene dejar afuera de lo que se anota?" |
| Plazo de los registros | "¿Por cuánto tiempo hay que guardar lo anotado en estas conversaciones y los archivos que se reciban? Si no hay un plazo, se guardan sin plazo fijo." |

- Antes de preguntar por los datos, contar en una frase lo que nunca se guarda: datos personales, claves y datos bancarios.
- La pregunta por los datos comerciales es abierta: no se le da una lista para elegir. Si la persona pregunta qué son, dar ejemplos, como los precios, las condiciones o los datos de otras empresas. Con la respuesta, decir qué se anota y qué queda afuera, y pedir que lo confirme.
- Quien aprueba puede ser la misma persona que conduce.
- Si no se define un período de revisión, son 12 meses.
- Si no se define un plazo para los registros, va "sin plazo fijo". El plazo se escribe en las tres filas de la tabla "Registros" de `empresa/lista-maestra.md`.
- Lo demás se escribe en "Cómo se organiza el relevamiento", en `empresa/contexto.md`.
- Desde el cierre de esta etapa se usa la forma de trato elegida.

## Etapa 4. Qué hay ya escrito

Preguntar: "¿Hay algo ya escrito sobre cómo se trabaja? Sirve cualquier cosa: instructivos, listas de tareas, organigramas o notas."

Si no hay nada, anotarlo en el registro de la sesión y cerrar la etapa. El relevamiento sigue con preguntas.

Si hay material, recibir cada archivo con los pasos de "Archivos recibidos", en `metodo/control-documental.md`. Va a `empresa/insumos/` y se anota en su `catalogo.md`. Los archivos no llevan un guardado propio: se guardan con el cierre de la etapa. Después:

| Material | Qué se hace en esta etapa |
|---|---|
| Un documento sobre cómo se trabaja | Leerlo entero. |
| Una conversación entre otras personas | Solo catalogarla, con `se lee en otra sesión`. No se lee de paso: se recibe y se lee después, con `metodo/material-de-terceros.md`. |
| Un audio sin transcripción | Solo catalogarlo, con `sin transcribir`, y pedir la transcripción. Su contenido nunca se adivina. |
| Un archivo que no se puede abrir | Catalogarlo con `no revisado por el agente`. |

Con cada documento leído:

1. Contar en dos o tres frases qué es, de cuándo es y qué temas trata.
2. Preguntar: "¿Leí bien?" La persona confirma la lectura, no los hechos.
3. Anotar de cuándo es en la columna "Fecha del material" del catálogo. Si no se sabe, va `sin fecha`.
4. Tomar lo que nombra el documento como propuestas para las etapas 5 a 7: áreas, sistemas, personas y procesos.

- Lo que se escriba a partir del material lleva su fuente y `A CONFIRMAR con <quién>`. La fuente es el nombre del archivo en `empresa/insumos/`. `<quién>` es la persona que hace ese trabajo; si no se sabe, el responsable del programa.
- El material puede estar desactualizado. Sirve para preguntar mejor y nunca cuenta como validado.
- Si el material no coincide con lo que contó el responsable del programa, preguntar cuál de las dos cosas pasa hoy y anotar su respuesta. El material no se corrige.
- Si la persona promete traer material más adelante, anotarlo en el registro de la sesión, en "Documentos pendientes", y cerrar la etapa. Se recibe en otra conversación, con estos mismos pasos.

## Etapa 5. Áreas y sistemas

Preguntas de apertura, una para cada parte:

- "¿Cómo se organiza el trabajo por dentro: qué áreas o sectores hay?"
- "¿Con qué se trabaja? Cuentan los sistemas, los programas, las hojas de cálculo, los cuadernos y los mensajes."

| Qué tiene que quedar | Pregunta, solo si no salió |
|---|---|
| De qué se ocupa cada área | "¿De qué se ocupa `<área>`?" |
| Para qué se usa cada sistema | "¿Para qué se usa `<sistema>`?" |
| Quiénes lo usan | "¿Quiénes lo usan?" |

Cada área lleva tres letras, que después forman los códigos de sus documentos. Las propone el agente y no llevan una pregunta aparte:

1. Tomar las tres primeras letras del nombre del área, en mayúsculas, sin acentos ni eñes.
2. Si se repiten, o si dan `GEN`, cambiar la tercera por la siguiente letra del nombre. `GEN` queda para lo que es de toda la empresa.
3. Mostrarlas una sola vez, junto a cada área, en el resumen de cierre de la etapa. Si la persona pide otras, se usan las suyas.
4. Una vez escritas, no se cambian.

- La carpeta del área es su nombre en minúsculas, con guiones y sin acentos.
- Si la empresa no tiene áreas, todo va en `general`, con las letras `GEN`.
- Quién usa un sistema es un dato de la empresa y vale como directo. Cómo lo usa cada persona es de segunda mano.
- De los sistemas nunca se anotan usuarios ni claves.
- Se escribe en "Áreas" y en "Sistemas y herramientas", en `empresa/contexto.md`.

## Etapa 6. Personas

Se pregunta una vez por área: "¿Quiénes trabajan en `<área>`, y de qué se ocupa cada persona? Con el nombre de pila alcanza."

Con lo que cuenta de cada área, armar la lista de personas y mostrarla para corregir. No se pregunta persona por persona, ni qué sistemas usa cada una: eso ya salió en la etapa 5.

Antes de cerrar la etapa, comparar la cantidad de personas anotadas con la que se dijo en la etapa 2 y preguntar si falta alguien, con la frase de "Falta alguien".

Al escribir:

1. Crear una hoja por persona, copiando `plantillas/persona.md` a `empresa/personas/<nombre>.md`.
2. Crear también la hoja del responsable del programa y la de quien aprueba.
3. En "Rol en el relevamiento" va `participante`, salvo en esas dos hojas, que llevan su rol.
4. En "Sistemas y herramientas que usa" va lo que se dijo en la etapa 5.
5. En "Origen de la hoja" va que los datos los dio el responsable del programa, con la fecha.
6. En "De dónde sale cada dato", lo que describe el trabajo de otra persona lleva `A CONFIRMAR con <esa persona>`. El marcador va ahí y no junto a cada dato.
7. Las partes "Procesos en los que participa" y "Preguntas preparadas" quedan con su ayuda hasta las etapas 7 y 8.
8. En la hoja del responsable del programa, anotar en "Documentos prometidos" el material que prometió en la etapa 4. Anotar en sus "Preguntas preparadas" lo que quedó en "Pendientes" de los registros del arranque sin un documento donde vivir.
9. La hoja del responsable del programa la contó él mismo: en "Confirmada por la persona" va `sí`, con la fecha. Las demás hojas quedan en `no` hasta la primera conversación de cada persona.

- Si dos personas comparten el nombre de pila, el archivo lleva también el área, como indica `empresa/README.md`.
- Una persona que aparece en dos áreas tiene una sola hoja, con las dos áreas.
- Si son muchas personas, empezar por un área o por las personas que conviene escuchar primero. Lo que falta se anota como pregunta en la hoja del responsable del programa.

## Etapa 7. Mapa de procesos

Un proceso es un trabajo que empieza con algo que lo pone en marcha y termina con algo hecho. Para separarlos:

- Si dos tramos tienen dueños distintos o resultados distintos, son dos procesos.
- Un paso suelto no es un proceso. Un área entera, tampoco.
- El nombre es el que usa la empresa, corto y sin siglas.

Se recorren los tres grupos en este orden. En cada uno se pide el relato completo, de una vez:

| Grupo | Pregunta de apertura |
|---|---|
| Operación | "¿Qué pasa desde que un cliente pide algo hasta que se cobra? Sirve el recorrido completo, contado de corrido." |
| Apoyo | "¿Qué otros trabajos hacen falta para que eso funcione? Por ejemplo, pagar, contratar personas o mantener los equipos." |
| Conducción | "¿Cómo se decide hacia dónde va la empresa: los precios, los objetivos, las prioridades?" |

Con cada relato:

1. Armar las filas con lo que dijo y con lo que ya se sabe de las etapas 5 y 6: proceso, área, grupo, dueño y participantes.
2. Mostrarlas como una lista corta del grupo y preguntar qué hay que corregir.
3. Preguntar aparte solo lo que falta. Por ejemplo: "¿Quién responde por que esto salga bien?" o "¿De qué área es?"

La prioridad se pregunta una sola vez, al final y para toda la lista: "De todos estos, ¿cuáles son los dos o tres que más duelen o que más urgen?"

| Respuesta | Prioridad |
|---|---|
| Los que nombra | `P1` |
| Los demás | `P2` |
| Los que pide dejar para el final | `P3` |
| No lo sabe todavía | `sin definir` |

- Si la persona duda, ofrecer criterios: lo que depende de una sola persona, lo que más errores o esperas genera, lo que se hace más seguido, lo que tiene que aprender alguien nuevo.
- Con la respuesta, preguntar por qué esos primero. El motivo se anota en la fila "Qué se releva primero" de `empresa/contexto.md`.

Además:

- El dueño es un rol del relevamiento: vale lo que define el responsable del programa. Si no lo sabe, va `A DEFINIR`.
- Quiénes participan vale como dato directo. Lo que hace cada persona en el proceso es de segunda mano.
- Dónde va la compra depende de la empresa. Si forma parte del recorrido del pedido al cobro, va en operación. Si no, va en apoyo. Queda en el grupo en que la nombró la persona.
- Los procesos que salen del material de la etapa 4 se proponen junto con los demás. Si la persona no reconoce alguno, no lleva fila: va una línea en "Pendientes del mapa", con su fuente y `A CONFIRMAR con <quién>`.
- Si aparece un área que no figura en `empresa/contexto.md`, agregarla ahí con sus tres letras, como en la etapa 5, antes de asignar códigos.
- Si no se sabe de qué área es un proceso, figura en el mapa sin código: en "Código" va `—` y en "Área" va `PENDIENTE: preguntar a <quién>`. Recibe su código cuando se sabe el área.
- Lo que no se sabe de un grupo entero, o de dónde empieza y dónde termina el recorrido, va en "Pendientes del mapa".

Al escribir:

1. Crear `empresa/mapa-de-procesos.md` copiando `plantillas/mapa-de-procesos.md`. Poner al día la fila `MP-GEN-001` de la lista maestra: estado `en curso` y "Elaboró".
2. Asignar el código de cada proceso que ya tiene área, con los pasos de "Cómo se asigna un código". Su fila de la lista maestra queda con estado `pendiente`, versión `0` y ubicación `—`, porque la ficha todavía no existe.
3. Agregar la fila de cada proceso en su grupo del mapa, con estado `pendiente` y ficha `—`. En "Participantes" van solo los nombres.
4. En la hoja de cada persona nombrada, agregar el proceso en "Procesos en los que participa". En "Su parte" va lo que hace, si el relato lo dijo. Si no lo dijo, va `—`, sin marcador: se completa en su entrevista. El marcador `A CONFIRMAR con <esa persona>` va una sola vez, en "De dónde sale cada dato" de esa hoja. Si la persona no tiene hoja, crearla.
5. En la hoja de cada dueño, anotar en "Rol en el relevamiento" de qué proceso es dueño.

Todo va en un solo guardado, al cerrar la etapa.

## Etapa 8. Plan de relevamiento y preguntas

El orden ya quedó en la etapa 7: primero los procesos `P1`. Aquí se define a quién se escucha y qué se le pregunta.

1. Nombrar los procesos `P1` con las personas ya anotadas en cada uno, y preguntar si hay que escuchar a alguien más.
2. Preguntar si alguna de las personas anotadas en el relevamiento no va a poder sentarse a conversar.
3. Si en esta etapa cambia una prioridad, corregirla en el mapa.

Preguntas preparadas:

1. Buscar cada `PENDIENTE: preguntar a` y cada `A CONFIRMAR con` en `empresa/`. La búsqueda deja afuera `empresa/sesiones/` y `empresa/insumos/`.
2. Convertir cada uno en una sola pregunta, en palabras simples.
3. Escribirla en "Preguntas preparadas" de la hoja de la persona nombrada, agrupada por proceso, con el lugar de donde sale. La pregunta nombra lo que falta: el marcador queda donde estaba.
4. Lo que nombra al responsable del programa va a su propia hoja. También se preparan preguntas para él.
5. Lo marcado `PENDIENTE: preguntar a A DEFINIR` va a la hoja del responsable del programa, como pregunta sobre a quién hay que consultar.
6. Las filas del mapa con el dueño `A DEFINIR` o con la prioridad `sin definir` no son marcadores y la búsqueda no las encuentra. También van a la hoja del responsable del programa, como preguntas.
7. Contar al responsable del programa, en pocas frases, cuántas preguntas quedaron para cada persona, con uno o dos ejemplos.
8. Preguntar si quiere sumar alguna.

Aquí se preparan solo las preguntas propias de cada persona. Las preguntas generales sobre un proceso no se anotan en las hojas: salen de `plantillas/banco-de-preguntas.md` durante la entrevista.

Lista para enviar: se ofrece siempre, con la frase de "Lista para enviar".

1. Si acepta, mostrar en la conversación un mensaje por persona: una frase que diga para qué es y las preguntas numeradas, en palabras simples.
2. Anotar en la hoja de esa persona, junto a cada pregunta, que se envió y en qué fecha.
3. Las respuestas escritas que vuelvan se reciben en otra conversación, con `metodo/material-de-terceros.md`: van a `empresa/insumos/` y llevan `A CONFIRMAR con <esa persona>`.

## Cierre del arranque

Se hace una sola vez, después de cerrar la etapa 8 y antes del cierre de la sesión:

1. Resumir todo lo que quedó escrito, con palabras simples y con cantidades: áreas, personas, procesos y preguntas preparadas. Decir cuántas cosas quedaron por confirmar o por preguntar.
2. Preguntar: "¿Es así?" Corregir lo que la persona marque.
3. Pasar a `borrador` el contexto y el mapa de procesos, en su bloque de control y en la lista maestra. Ese cambio se guarda con el cierre de la sesión. El glosario ya pasó a `borrador` al cerrar la sesión en la que se creó.
4. Decir qué sigue. Mirar la tabla de modos de `AGENTS.md` y nombrar solo lo que ya tiene fila. No prometer lo que todavía no está disponible. Si en el arranque apareció un cambio en marcha, ofrecer abrirlo en otra conversación, con `metodo/cambio-en-curso.md`.
5. Si no hay servidor, como lo define "Cuándo hay servidor" en `metodo/guardado.md`, decir una sola vez la frase de "Sin servidor". Anotar en el registro de la sesión que se dijo.

Si la sesión termina antes de este cierre, el contexto y el mapa quedan `en curso`. El cierre se hace la próxima vez que habla el responsable del programa, antes de elegir otro modo, como indica "Detección del estado" en `AGENTS.md`. No es retomar el arranque: es un paso previo, que no impide abrir otro modo después. En ese caso lleva su propio registro del arranque, con las ocho etapas marcadas en "Etapas o temas" y el registro anterior en "Sesión anterior", y su guardado de cierre de sesión. Mientras tanto, las demás personas ya pueden conversar.

## Cierre de cada sesión

Se hace siempre que una sesión termina, esté o no completo el arranque:

1. Sumar una fila al historial de cada documento controlado que la sesión cambió, con la versión `0`, la fecha, qué se agregó y quién lo contó. Va una sola fila por documento, también si la sesión lo creó.
2. Si en esta sesión se creó el glosario, pasarlo a `borrador`, en su bloque de control y en la lista maestra.
3. Completar "Cómo terminó" en el registro de la sesión, con su línea de subida. En "Último resumen que confirmó la persona" va el de la última etapa cerrada o, si se hizo el cierre del arranque, el de ese cierre.
4. Hacer el guardado final y la subida, como indica "Al cerrar la sesión" en `metodo/guardado.md`.
5. Agradecer el tiempo. Si quedan etapas, decir que la próxima vez alcanza con abrir la carpeta y saludar.

## Guardado en este modo

Los mensajes siguen el formato de `metodo/guardado.md`:

| Momento | Mensaje |
|---|---|
| Cierre de cada etapa | `docs(empresa): arranque - etapa <número> con <nombre>` |
| Etapa que quedó a medias | `docs(empresa): arranque - etapa <número> con <nombre>` |
| Cierre de la sesión | `docs(empresa): arranque - cierre de sesión con <nombre>` |

Los archivos que llegan en la etapa 4 van en el guardado de esa etapa. En este modo no se usa el mensaje de archivos aportados.

## Qué decir

Las frases son modelos. Se dicen cada vez con otras palabras, como indica la regla 8 de `metodo/reglas.md`.

| Situación | Frase |
|---|---|
| Pedir el nombre | "Hola. Antes de empezar, ¿con quién estoy hablando? Con el nombre de pila alcanza." |
| Presentación | "Este trabajo sirve para dejar por escrito cómo se trabaja en la empresa. Antes de conversar con cada persona hace falta una preparación: cómo es la empresa, cómo nos organizamos, qué hay ya escrito, qué áreas y qué personas hay, qué procesos tiene y qué preguntarle a cada persona. Lleva entre dos y tres horas, que se pueden repartir en varias conversaciones." |
| No es quien conduce | "Esta primera parte se hace con la persona que va a conducir el trabajo. Cuando esa persona pueda, alcanza con que abra esta carpeta y salude." |
| Un momento | "Un momento, lo dejo anotado." |
| Avance | "Etapa `<número>` de 8 lista. ¿Seguimos con la siguiente?" |
| Ofrecer cortar | "Ya llevamos un buen rato. Lo conversado quedó guardado. ¿Seguimos, o cortamos aquí y continuamos otro día?" |
| La persona no sabe algo | "No hay problema. Lo anoto para preguntárselo a quien corresponda. ¿A quién habría que consultarle?" |
| Falta alguien | "Anoté `<cantidad>` personas, y al principio eran unas `<cantidad>`. ¿Falta alguien?" |
| Lista para enviar | "¿Preparo las preguntas en un mensaje listo para enviar a quien no pueda conversar?" |
| Retomar | "La vez pasada llegamos hasta la etapa `<número>`. Hoy sigue esta: `<nombre de la etapa>`." |
| Habla otra persona | "La preparación de este trabajo todavía no terminó. `<nombre del responsable del programa>` va a avisar cuándo se puede empezar." |
| Sin servidor | "Un aviso: todo lo que conversamos quedó guardado solo en esta computadora. Quien preparó esta carpeta puede sumar una copia en otro lugar." |
| Cierre del arranque | "Con esto quedó lista la preparación." Después, el resumen y lo que sigue. |

En la conversación se usan palabras simples, como indica la regla 8 de `metodo/reglas.md`:

| En lugar de | Decir |
|---|---|
| "contexto de la empresa" | "la descripción de la empresa" |
| "mapa de procesos" | "la lista de procesos de la empresa" |
| "dueño de proceso" | "quien responde por ese proceso" |
| "responsable del programa" | "quien conduce este trabajo" o "responsable de este trabajo" |
| "lista de arranque" | "lo que falta preparar" |
| Un código | El título del documento |

Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
