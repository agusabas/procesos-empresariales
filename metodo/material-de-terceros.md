# Modo: material de terceros

En este modo alguien trae material en el que hablan otras personas, y el agente lo convierte en trabajo de relevamiento. Lo guarda sin datos personales, lo lee, anota lo que dice sobre cada proceso y prepara las preguntas para confirmarlo. El material típico es una conversación exportada con sus adjuntos, las notas de una reunión, un hilo de correos, capturas de pantalla o un mensaje de voz transcripto.

Nada de lo que sale del material cuenta como validado. Sirve para saber qué preguntar y a quién.

Antes de empezar, leer completo `metodo/control-documental.md`. Este modo guarda archivos, crea fichas y asigna códigos.

## En una mirada

| Etapa | Qué se hace | Qué queda escrito |
|---|---|---|
| 1. Recibir y catalogar | Pedir el material. Saber qué es, quiénes participan, qué fechas cubre y cómo llegó. Guardarlo sin los datos que no se guardan. | `empresa/insumos/` y su `catalogo.md`, hojas de personas y registro de la sesión |
| 2. Leer y clasificar | Leer en orden y clasificar cada fragmento útil. | Notas de lectura en el registro. Hasta dónde se leyó, en el catálogo |
| 3. Resumen de lectura | Contar lo leído, proceso por proceso, y preguntar "¿Leí bien?" | Correcciones en el registro |
| 4. Escribir | Pasar cada afirmación a su ficha, con su fuente y `A CONFIRMAR`. | Fichas, mapa de procesos, glosario y lista maestra |
| 5. Preguntas | Preparar las preguntas para cada persona nombrada. | "Preguntas preparadas" de cada hoja |
| Cierre | Decir qué se escribió, dónde, y qué falta confirmar. | Registro de la sesión |

Cada etapa se cierra igual: resumen de lo entendido, pregunta de confirmación y guardado. Es la regla 9 de `metodo/reglas.md`.

## Reglas de este modo

1. El material lo trae, por lo general, el responsable del programa. Lo puede traer cualquier persona con hoja, y las reglas son las mismas.
2. Todo lo que se escribe a partir del material lleva su fuente y `A CONFIRMAR con <quién>`.
3. Hay dos excepciones, las de la regla 4 de `metodo/reglas.md`: lo que dijo en el material la misma persona que lo trae, y lo que el material dice sobre el trabajo de esa persona. Se le pregunta en el momento. Si lo confirma, vale como su palabra directa y no lleva marcador.
4. Quien trae el material confirma la lectura, no los hechos.
5. Nada se copia a `empresa/` antes de quitarle los datos personales de terceros y los datos comerciales que la empresa deja afuera.
6. El original no se mueve, no se cambia y no se borra.
7. Lo que dice un audio nunca se adivina ni se completa por el contexto.
8. Las críticas a personas no se anotan. Se anota el hecho que afecta al trabajo.
9. Este modo nunca lleva una ficha a `borrador`: nadie que hace el trabajo lo contó directamente. El glosario no es una ficha: su estado sigue lo que indica "Estados" en `metodo/control-documental.md`.
10. Lo que trata de un cambio que está en marcha no se desarrolla aquí. Se anota en "Temas para otra sesión" del registro, en una línea que empieza con `Cambio:`, y se retoma en `metodo/cambio-en-curso.md`.
11. Los códigos se asignan desde la lista maestra, con los pasos de "Cómo se asigna un código" en `metodo/control-documental.md`. A la persona no se le dicen: cada documento se nombra por su título.
12. Cada marcador se escribe una sola vez, en el documento donde vive el dato. Lo que falta sobre un archivo va en su fila del catálogo. En el registro de la sesión no se escriben marcadores.

## Etapa 1. Recibir y catalogar

### Material que ya estaba anotado

Antes de recibir lo nuevo, leer `empresa/insumos/catalogo.md` y los catálogos de `empresa/adjuntos/`. Las filas con `se lee en otra sesión`, con `sin transcribir`, con `no entregado` o con `leído hasta` son material que espera.

1. Contar a la persona qué material espera y preguntar si lo tiene a mano.
2. Cuando lo entrega, seguir los pasos de esta etapa.
3. Completar la columna "Archivo" de su fila y cambiar la frase de "Observaciones" por la que corresponde. Si la fila decía `no entregado`, completar también "Quién lo aportó" y "Fecha", y quitar su marcador.

### Pedir el material

Lo primero es tener el material a la vista. Si la persona todavía no lo entregó:

1. Pedirlo con las tres maneras de "Archivos recibidos", en `metodo/control-documental.md`, y en ese orden: arrastrarlo o adjuntarlo, decir dónde está, o pegarlo en la conversación.
2. Con el material a la vista, hacer la pregunta de apertura de "Qué se pregunta".
3. Preparar la copia como indica "La copia sin datos personales" y dejarla en `empresa/insumos/` al recibirla. No espera la confirmación de la etapa. El guardado va con el cierre de la etapa.

### Qué se pregunta

Pregunta de apertura: "¿Qué es este material? Sirve todo lo que se pueda contar: de dónde salió, de cuándo es y quiénes hablan."

Con la respuesta y con lo que el material muestra por sí mismo, como las fechas y los nombres, decir lo que se entendió y preguntar qué hay que corregir. Después se pregunta solo lo que falta, con una pregunta por mensaje:

| Qué tiene que quedar | Pregunta, solo si no salió |
|---|---|
| Qué es | "¿Qué es este material?" |
| Fechas | "¿De qué fechas es?" |
| Quiénes participan | "¿Qué hace en la empresa cada una de las personas que hablan ahí?" |
| Cómo llegó | "¿Cómo se obtuvo: lo exportó alguien que participa, lo reenviaron, lo anotó alguien?" |
| Si lo saben | "¿Las personas que hablan ahí saben que se usa para este trabajo?" |

- Si no lo saben, decir una sola vez la frase de "Conviene avisar", anotar la respuesta en "Cómo llegó" y seguir.
- Si quien trae el material no sabe si lo saben, decir la misma frase y anotarlo en "Observaciones" de su fila del catálogo: `PENDIENTE: preguntar a <responsable del programa>`, con la aclaración "si quienes hablan saben que se usa". No se pregunta a quién consultar.
- El material no se rechaza: si se usa o no lo decide el responsable del programa.

### La copia sin datos personales

El material no se copia tal cual. Se guarda una copia que el agente prepara:

| Material | Qué se guarda |
|---|---|
| Texto: una conversación, notas o correos | Un archivo `.md` con el texto completo y los reemplazos de la tabla siguiente. |
| Una imagen sin datos personales de terceros | La imagen. |
| Una imagen con datos personales de terceros | La imagen no se guarda. Se guarda una descripción en un archivo `.md`, sin esos datos. |
| Un audio | No se guarda. Su transcripción, cuando llega, se trata como texto. |
| Otro adjunto, como una planilla o un formulario | Lo que indica "Archivos recibidos", en `metodo/control-documental.md`. |

| Qué aparece en el texto | Qué va en la copia |
|---|---|
| Un apellido | `[apellido omitido]` |
| Un teléfono, un correo, un domicilio, un documento de identidad u otro dato personal | `[dato omitido]` |
| Una clave, un usuario de acceso o un dato bancario | `[dato omitido]` |
| El nombre de un cliente o de otra persona de afuera que solo se menciona | Su rol: "un cliente", "un proveedor" |
| Un mensaje personal, que no tiene que ver con el trabajo | `[mensaje personal omitido]` |
| Un dato comercial que la fila "Datos comerciales" de `empresa/contexto.md` deja afuera, o sobre el que todavía no define nada | `[dato omitido]` |

- Las personas de la empresa quedan con su nombre de pila.
- Se filtra el texto completo, no solo las partes que se van a usar.
- En el catálogo, una copia lleva `guardado sin los datos personales de terceros` solo si de verdad se le quitó algo. Si se le quitaron datos comerciales, lleva `guardado sin los datos comerciales que la empresa deja afuera`. Una copia a la que no hubo que quitarle nada no lleva ninguna de las dos frases.
- La imagen que no se guardó lleva `no se guardó: contiene datos personales de terceros`, y su descripción lleva `transcripto por el agente, sin el original`.

### Cómo se guarda y se cataloga

- Todo va a `empresa/insumos/`, con el nombre `AAAA-MM-DD-descripcion-corta.extension`. La fecha es el día en que llegó.
- Una entrega de varios archivos, como una conversación con sus adjuntos, va en una carpeta propia: `empresa/insumos/AAAA-MM-DD-descripcion-corta/`. Si de la entrega se guarda un solo archivo, va suelto.
- Hay un solo catálogo, `empresa/insumos/catalogo.md`. Lleva una fila por archivo. En "Archivo" va la ruta a partir de `insumos/`.
- En "Fecha del material" van las fechas que cubre. Por ejemplo: "del AAAA-MM-DD al AAAA-MM-DD". Si no se saben, va `sin fecha`.
- En "Proceso y paso" va `sin definir` hasta terminar la etapa 2. Después va el nombre del proceso, si el material trata de uno solo, o `—`, si trata de varios.
- Los adjuntos quedan con su entrega. Si una ficha usa uno, lo enlaza desde "Documentos" con `../../insumos/` y su ruta.
- Los adjuntos que no tienen que ver con el trabajo no se guardan ni se anotan.

| Caso | Qué se hace |
|---|---|
| Un audio sin transcripción | Anotarlo en el catálogo con `sin transcribir` y con `PENDIENTE: falta la transcripción de <archivo>`. Pedir la transcripción a quien lo trajo, con la frase de "Pedir una transcripción". |
| Una conversación con respuestas en audio | Se lee igual. En la copia, en el lugar de cada audio va `[audio sin transcribir]`, con su nombre original. Cada audio lleva su fila en el catálogo, como en el caso anterior. En la ficha y en las notas de lectura se nombra el audio, sin el marcador. Lo que depende de él no se deduce por el contexto. |
| Llega la transcripción de un audio | Guardarla como texto, filtrada, con el tipo `transcripción`. En la fila del audio, cambiar `sin transcribir` por `transcripción en` y el nombre del archivo, y quitar el marcador. Leerla con este mismo modo y escribir en las fichas lo que dice, con su fuente y `A CONFIRMAR`. |
| Un adjunto que el material nombra y que nadie entregó | Pedirlo una vez a quien trajo el material. Si no llega, anotarlo en el catálogo con `no entregado`, seguido del archivo que lo nombra, y con `PENDIENTE: preguntar a <quién>`. En "Archivo", en "Quién lo aportó" y en "Fecha" va `—`. En el registro va una línea "No entregado". Lo que depende de él no se deduce. |
| Una imagen | Leerla y describirla: qué es y qué muestra del trabajo. Los datos personales de terceros que tenga no se transcriben. |
| Una imagen que no se puede ver | Anotarla con `no revisado por el agente` y pedir a quien la trajo que cuente qué muestra. Lo que cuente es de segunda mano. Si no lo sabe, en su fila va también `PENDIENTE: preguntar a <quién>`. |
| Material que sigue creciendo, como una conversación exportada otra vez | Cada entrega se cataloga aparte, con las fechas que cubre. De la entrega nueva se guarda y se lee solo lo posterior a la fecha de `leído hasta` de la anterior. |
| Material muy largo | Se lee por partes, en orden de fecha. Al terminar cada parte se pone al día `leído hasta AAAA-MM-DD` en su fila. |

### Las personas que aparecen

Comparar cada persona del material con las hojas de `empresa/personas/`:

| Quién es | Qué se hace |
|---|---|
| Tiene hoja | Se la nombra como figura en su hoja. |
| Es de la empresa, no tiene hoja, y el material lo trajo el responsable del programa | Preguntarle quién es y qué hace. Crear su hoja copiando `plantillas/persona.md`. En "Origen de la hoja" van el responsable del programa, el archivo y la fecha. |
| Es de la empresa, no tiene hoja, y el material lo trajo otra persona | Crear una hoja provisional con lo que se sabe y con `A CONFIRMAR con <responsable del programa>`. |
| Es de afuera de la empresa, como alguien de un proveedor | No lleva hoja. Su nombre de pila y su rol se anotan en el registro de la sesión. |
| No se sabe quién es | No lleva hoja. La pregunta por quién es se suma a "Preguntas preparadas" de la hoja del responsable del programa. |

En toda hoja nueva, "Confirmada por la persona" queda en `no`. Lo que la hoja dice de la persona, como su rol, lleva `A CONFIRMAR con <esa persona>` en "De dónde sale cada dato". Lo que el material muestra de su trabajo en un proceso lleva el marcador en la ficha de ese proceso, no en la hoja.

### Qué se anota en el registro

Quiénes participan y cómo llegó el material van en el registro de la sesión, no en el catálogo. En "Documentos", debajo de cada archivo:

```
- Incorporado: <archivo>, <qué es>. Quedó en <carpeta>.
  - Quiénes participan: <nombre de pila y rol de cada persona>
  - Fechas que cubre: del <AAAA-MM-DD> al <AAAA-MM-DD>
  - Cómo llegó: <quién lo obtuvo, de qué manera, y si quienes participan lo saben>
```

Cerrar la etapa: decir qué se guardó, qué no se pudo guardar y qué quedó esperando. Lo que la persona ya corrigió o aceptó al abrir la etapa no se le vuelve a preguntar. Guardar.

## Etapa 2. Leer y clasificar

Leer el material completo, en orden de fecha. Cada fragmento útil va a una de estas clases:

| Clase | Qué es | A dónde va en la etapa 4 |
|---|---|---|
| Cómo se hace hoy | Alguien cuenta o muestra cómo se hace un trabajo. | A la parte que corresponde de "Cómo se hace hoy", en la ficha del proceso. |
| Regla o excepción | Un criterio para decidir, o un caso que se sale de lo habitual. | A "Reglas que se siguen" o a "Excepciones". |
| Decisión sobre un cambio en marcha | Algo que se decidió o se definió sobre un cambio, como un sistema nuevo o una reorganización. | A "Temas para otra sesión" del registro, en una línea que empieza con `Cambio:` y lleva su fuente. No se escribe en ninguna ficha. |
| Pregunta abierta con un tercero | Algo que se le preguntó a alguien de afuera y sigue sin respuesta. | A la ficha, como `PENDIENTE: preguntar a <quién>`, con el nombre de la persona de la empresa que trata con ese tercero. Si es sobre un cambio en marcha, a "Temas para otra sesión", también con `Cambio:`. |
| Término para el glosario | Una palabra propia de la empresa. | Al glosario, con su fuente y `A CONFIRMAR con <quién>`. |
| Ruido | Saludos, bromas, temas personales o la coordinación de un día puntual. | No se escribe. En el registro se anota solo que lo hubo. |

- Un problema que se repite, como un error o una espera, es parte de cómo se hace hoy. Va a "Problemas", como hecho y sin juicio sobre personas.
- De cada fragmento útil se anota en el registro la fecha, quién lo dijo, qué dice en una frase, su clase y su proceso.
- Lo que no se entiende se anota como poco claro, para la etapa 3. No se interpreta.
- Al terminar, poner al día `leído hasta AAAA-MM-DD` en el catálogo.

Cerrar la etapa: contar cuánto se leyó, de qué fechas y sobre cuántos procesos. Preguntar si se repasa ahora. Guardar.

## Etapa 3. Resumen de lectura

Se repasa un proceso por mensaje:

1. Contar en dos o tres frases lo que dice el material sobre ese proceso, y quién lo dice.
2. Decir qué quedó poco claro: frases ambiguas, audios sin transcripción, imágenes que no se pudieron leer.
3. Preguntar: "¿Leí bien?"
4. Corregir la lectura en el registro, si la persona la corrige.

- Lo leído sobre un cambio en marcha, y lo que no se pudo ubicar en ningún proceso, se repasan en un mensaje aparte, con la misma pregunta.
- La persona confirma la lectura, no los hechos. Lo leído sigue `A CONFIRMAR`.
- Hay dos excepciones: lo que ella misma dijo en el material, y lo que el material dice sobre su propio trabajo, lo haya dicho quien lo haya dicho. Se le pregunta con la frase de "Lo que dijo quien lo trae" o con la de "Lo que se dice de quien lo trae". Si lo confirma, vale como su palabra directa y se escribe sin marcador. Si lo corrige, se escribe lo que cuenta ahora.
- Lo que la persona agrega de su parte sobre el trabajo de otras es de segunda mano: también lleva `A CONFIRMAR con <esa persona>`.
- Lo poco claro se escribe en la etapa 4 como `PENDIENTE: preguntar a <quién>`, con el nombre de quien lo dijo, en la ficha donde iría el dato.

Cerrar la etapa: resumir qué se va a escribir y en qué fichas. Preguntar "¿Es así?" y guardar.

## Etapa 4. Escribir

Cada afirmación se escribe con esta forma:

```
<afirmación> (fuente: <quién lo dijo>, <archivo>, <AAAA-MM-DD>). A CONFIRMAR con <quién>.
```

- `<quién>` es la persona que hace ese trabajo. Si no se sabe, el dueño del proceso. Si tampoco se sabe, el responsable del programa.
- En la tabla de pasos, la fuente y el marcador van en la celda "Qué hace".
- Lo que viene del material no reemplaza lo que una persona contó directamente. Se agrega.
- Lo que quien trajo el material confirmó en la etapa 3, por cualquiera de las dos excepciones, se escribe sin marcador, con ella como fuente y con la fecha de hoy.

Qué se hace según el estado de la ficha. Vale la primera fila que se cumple:

| La ficha | Qué se hace |
|---|---|
| No existe | Crearla como indica "La primera vez" en `metodo/entrevista.md`. Queda `en curso`. |
| Está `en curso` o en `borrador` | Se suma a lo escrito. El estado no cambia. |
| Está `validado` | Se suma. Si lo nuevo cambia el sentido, vuelve a `borrador` en el bloque de control, en la lista maestra y en el mapa. |
| Está `vigente` | No se toca lo escrito. Va una fila en "Cambios propuestos (sin aprobar)", con la fuente. En "Confirmó el dueño" va `no`. |
| Está `obsoleto` | No se toca. Lo que el material dice sobre ese proceso se suma como pregunta a "Preguntas preparadas" de la hoja del responsable del programa. |

Además:

- Si lo que dice el material no coincide con lo ya escrito, se dejan las dos versiones en un bloque `CONFLICTO`, con la forma que indica `metodo/reglas.md`. El agente no elige cuál es la correcta. Si el proceso todavía no tiene dueño, en "Lo resuelve" va el responsable del programa.
- Un proceso que no está en el mapa recibe su fila como indica "Un proceso que aparece en la conversación" en `metodo/entrevista.md`. En "Participantes" van las personas que el material muestra.
- Si el proceso no tiene código, preguntar su área a quien trajo el material. Con el área, se le asigna el código, se crea la ficha y se escribe como cualquier otro. Si en el mapa había un `PENDIENTE` por el área, se trata como indica el paso 2 de "Un proceso sin código" en `metodo/entrevista.md`. Si quien lo trajo es el responsable del programa, también se le preguntan en el momento el dueño y la prioridad.
- Si quien trajo el material no sabe el área, el proceso queda sin código y sin ficha. Lo leído sobre él va a "Pendientes del mapa", con su fuente y `A CONFIRMAR con <quién>`. La pregunta por el área se suma a la hoja del responsable del programa.
- Las personas que el material muestra trabajando en un proceso sin código reciben igual su fila en "Procesos en los que participa", con `—` en "Código", y su pregunta en la etapa 5.
- Si el material trae un dato de la empresa que cambia `empresa/contexto.md`, como para qué se usa una herramienta, se escribe ahí, como indica "Datos del contexto que aparecen después del arranque" en `metodo/control-documental.md`.
- Si cambió la tabla de pasos, el diagrama se genera de nuevo, con las reglas de "Diagramas" en `metodo/control-documental.md`.
- Cada término nuevo va al glosario con la segunda forma de su molde: con la fuente y `A CONFIRMAR con <quién>`. Si `empresa/glosario.md` todavía no existe, se crea copiando `plantillas/glosario.md`, en estado `en curso`, y se pone al día la fila `GL-GEN-001` de la lista maestra. Si ya está `validado` o `vigente`, el término se suma como indica "Estados" en `metodo/control-documental.md`.
- En la hoja de cada persona que el material muestra trabajando, se agrega el proceso en "Procesos en los que participa", con lo que hace en "Su parte". Va sin marcador: el marcador se escribe una sola vez, en la ficha. Si esa persona no figuraba en "Participantes" del mapa, se suma su nombre.
- La fila del historial de cada documento que cambió se suma al cerrar la sesión, como indica "Cierre".

Cerrar la etapa: decir qué se escribió y en qué ficha, y guardar. Se pregunta "¿Es así?" solo si se escribió algo distinto de lo acordado al cerrar la etapa 3.

## Etapa 5. Preguntas para las personas

1. Tomar cada `A CONFIRMAR con` y cada `PENDIENTE: preguntar a` que se escribió en la etapa 4, y los que quedaron en las filas del catálogo en la etapa 1.
2. Convertir cada uno en una pregunta en palabras simples.
3. Escribirla en "Preguntas preparadas" de la hoja de la persona nombrada, agrupada por proceso, con el lugar de donde sale. La pregunta nombra lo que falta: el marcador queda donde estaba.
4. Lo marcado `PENDIENTE: preguntar a A DEFINIR` va a la hoja del responsable del programa, como pregunta sobre a quién hay que consultar.
5. Ofrecer la lista para enviar, como indica la etapa 8 de `metodo/arranque.md`.

- Las preguntas se responden después, en la entrevista de cada persona.
- Si quien trajo el material aparece en él y quedó algo suyo sin confirmar, ofrecerle una entrevista para otra conversación. La respuesta se anota en "Próximo paso" de "Cómo terminó".
- Lo que hay que preguntarle a alguien de afuera de la empresa se anota para la persona de la empresa que trata con ese tercero.

Cerrar la etapa: contar cuántas preguntas quedaron y para quién. Preguntar "¿Es así?" y guardar.

## Cierre

Los pasos 1 a 3 se dicen cuando se terminó la etapa 5. Los demás se hacen siempre que una sesión termina, también si se cortó antes.

1. Decir qué se escribió y dónde: cuántas fichas se tocaron, cuáles se crearon y qué términos se sumaron.
2. Decir qué falta confirmar y con quién.
3. Decir qué material quedó esperando: audios sin transcripción, partes sin leer.
4. Sumar una fila al historial de cada documento controlado que la sesión cambió. Va una sola fila por documento, también si la sesión lo creó. En "Quién lo contó" van el archivo y quién lo trajo.
5. Si en esta sesión se creó el glosario, pasarlo a `borrador`, en su bloque de control y en la lista maestra.
6. Completar "Cómo terminó" en el registro, con su línea de subida. En "Último resumen que confirmó la persona" va el de la última etapa cerrada.
7. Hacer el guardado final y la subida, como indica "Al cerrar la sesión" en `metodo/guardado.md`.
8. Agradecer el tiempo.

## El tiempo

- Leer lleva tiempo y se hace en silencio. Antes de empezar la etapa 2, avisar con la frase de "Aviso de lectura".
- Se corta al terminar una etapa. Si pasaron unos 25 minutos, ofrecer cortar con la frase de "Ofrecer cortar".
- Si la persona elige seguir, no se vuelve a ofrecer hasta que pasen otros 25 minutos. Después de la etapa 5 no se ofrece: solo falta el cierre.
- Antes de escribir en la etapa 4, avisar que lleva un rato, como indica la regla 9 de `metodo/reglas.md`.
- Si la sesión se corta, la siguiente crea un registro nuevo, pone el anterior en "Sesión anterior" y sigue desde la primera etapa sin marcar.
- Lo que ya se leyó no se lee de nuevo: lo dice `leído hasta` en el catálogo.

## El registro de la sesión

- Va uno por sesión. Se crea copiando `plantillas/registro-de-sesion.md` a `empresa/sesiones/AAAA-MM-DD-<quien>-material.md`. `<quien>` es la persona que trajo el material.
- En "Modo" va `material de terceros`.
- En "Etapas o temas" van las cinco etapas.
- En el bloque de la etapa 2 van las notas de lectura. Las citas del material se copian ya filtradas.
- Al cerrar la sesión, el registro no se edita más, salvo su línea de subida.

## Guardado en este modo

Los mensajes siguen el formato de `metodo/guardado.md`:

| Momento | Mensaje |
|---|---|
| Cierre de cada etapa | `docs(empresa): material de terceros - etapa <número> con <nombre>` |
| Cierre de la sesión | `docs(empresa): material de terceros - cierre de sesión con <nombre>` |

`<nombre>` es el nombre de pila de quien trajo el material.

## Qué decir

Las frases son modelos. Se dicen cada vez con otras palabras, como indica la regla 8 de `metodo/reglas.md`.

| Situación | Frase |
|---|---|
| Conviene avisar | "Conviene que esas personas sepan que su conversación se usa para este trabajo. Lo dejo anotado y sigo." |
| Copia sin datos personales | "En el material hay datos que no guardo, como los datos personales de otras personas. Guardo una copia sin esos datos. El original queda donde está." |
| Lo que dijo quien lo trae | "En el material figura esto, dicho por quien lo trae: `<qué dijo>`. ¿Sigue siendo así?" |
| Lo que se dice de quien lo trae | "En el material figura esto sobre su trabajo: `<qué dice>`. ¿Es así?" |
| Pedir una transcripción | "Hay mensajes de voz, y no puedo saber qué dicen. ¿Se puede conseguir su transcripción? Mientras tanto dejo anotado que falta." |
| Aviso de lectura | "Ahora leo todo el material. Puede llevar unos minutos. Después repasamos lo que encontré." |
| Resumen de lectura | "Sobre `<proceso>`, el material dice esto: `<resumen>`. ¿Leí bien?" |
| La persona agrega algo de otra | "Lo anoto, y queda para confirmarlo con `<nombre>`." |
| Ofrecer cortar | "Ya llevamos un buen rato. Lo hecho quedó guardado. ¿Seguimos, o cortamos aquí y continuamos otro día?" |
| Cierre | "Listo. Quedó anotado lo que dice el material, y preparadas las preguntas para confirmarlo con cada persona." |

En la conversación se usan palabras simples, como indica la regla 8 de `metodo/reglas.md`:

| En lugar de | Decir |
|---|---|
| "material de terceros" | "lo que escribieron o dijeron otras personas" |
| "catalogar" | "anotar qué es cada archivo" |
| "fragmento", "clasificar" | "parte", "ordenar" |
| "A CONFIRMAR" | "falta confirmarlo con quien lo hace" |

Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
