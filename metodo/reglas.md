# Reglas permanentes

Estas reglas valen en todos los modos, con todas las personas y en todas las sesiones de trabajo. Si un archivo de modo parece contradecir una regla de este archivo, vale la regla de este archivo.

## Las reglas en una mirada

| N.º | Regla | En una frase |
|---|---|---|
| 1 | Lo que pasa hoy | Se registra lo que se hace hoy, no lo que debería hacerse. |
| 2 | Nunca inventar | Lo que falta se marca `PENDIENTE: preguntar a <quién>`. |
| 3 | Dos versiones | Si dos personas no coinciden sobre lo mismo, se guardan las dos versiones bajo `CONFLICTO`. |
| 4 | Material de terceros | Lo que viene de terceros o de segunda mano se marca `A CONFIRMAR con <quién>`. |
| 5 | Lo vigente no se reescribe | Los cambios van a "Cambios propuestos (sin aprobar)". |
| 6 | Sin opiniones | No se opina sobre el desempeño de nadie. |
| 7 | Privacidad | Nombre de pila y rol. Sin claves, sin datos bancarios, sin datos personales de terceros. |
| 8 | Conversación llana | Lenguaje claro: palabras simples, una idea por frase, una pregunta por mensaje, sin jerga, sin errores a la vista, sin emojis. |
| 9 | Confirmación por etapa | Al cerrar cada etapa: resumen de lo entendido y pregunta de confirmación. |
| 10 | El método no se edita en un clon | Lo que falta en el método se anota en `empresa/notas-para-el-metodo.md`. |

## Roles

El método nombra roles, nunca personas.

| Rol | Qué hace |
|---|---|
| Responsable del programa | Conduce el relevamiento, trae material y revisa lo escrito. Puede ser de la empresa o un consultor externo. |
| Quien aprueba | Es el único rol que puede dejar un documento como `vigente`. |
| Dueño de proceso | Valida que lo escrito coincide con lo que pasa. |
| Participante | Interviene en un proceso y es entrevistado. |

- Los roles se asignan en el arranque y quedan registrados en `empresa/contexto.md`.
- Una misma persona puede tener más de un rol.
- El agente no tiene ningún rol: no valida, no aprueba y no figura como persona en ningún documento.
- En los archivos del método no aparece ningún nombre propio. Donde el método dice `<responsable del programa>`, en el clon va el nombre de pila de esa persona.
- En la conversación se nombra a cada persona por su nombre de pila, no por el nombre de su rol.

## Marcadores

Tres marcadores señalan lo que todavía no es firme. Se escriben siempre igual y en mayúsculas, para poder buscarlos. Un marcador queda abierto hasta que lo cierra quien corresponde: nunca se borra por cuenta propia.

| Marcador | Qué significa | Forma exacta | Quién lo cierra |
|---|---|---|---|
| `PENDIENTE` | Falta un dato y nadie en la conversación lo sabe. | `PENDIENTE: <qué falta>`. Tiene dos formas habituales: `PENDIENTE: preguntar a <quién>` y `PENDIENTE: falta la transcripción de <archivo>` | La persona nombrada, cuando responde. En la segunda forma, la transcripción, cuando llega. |
| `CONFLICTO` | Hay dos versiones distintas de lo mismo. | Bloque con las dos versiones | El dueño del proceso, cuando dice qué pasa hoy. Si el proceso no tiene dueño, el responsable del programa. |
| `A CONFIRMAR` | El dato viene de material de terceros o de segunda mano. | `A CONFIRMAR con <quién>` | La persona nombrada, cuando lo confirma directamente, en una conversación o por escrito. |

- `<quién>` es el nombre de pila de la persona que puede responder. Si nadie sabe quién es, se escribe `A DEFINIR`. Por ejemplo: `PENDIENTE: preguntar a A DEFINIR`.
- Lo marcado `A CONFIRMAR` nunca cuenta como validado, aunque parezca confiable.
- Un marcador se cierra solo cuando la persona que nombra responde sobre ese punto. Confirmar un resumen, aceptar un documento en una revisión o aprobarlo no cierra sus marcadores.
- La respuesta escrita de la persona nombrada también cierra los marcadores que la nombran, cuando responde a sus propias preguntas preparadas. Se escribe con su fuente: la persona, el archivo y la fecha. Lo que esa respuesta diga sobre el trabajo de otras personas sigue `A CONFIRMAR`. Cómo se recibe una respuesta escrita está en `metodo/material-de-terceros.md`.
- Un `CONFLICTO` se cierra cuando quien lo resuelve dice qué pasa hoy. Si pasan las dos cosas, se escriben como regla o como excepción, con lo que hace que pase una u otra. El bloque se reemplaza por ese texto. La fila del historial dice quién lo resolvió y cuándo. Si el documento está `vigente`, el texto va a "Cambios propuestos (sin aprobar)", como indica "Cambios en un documento vigente" en `metodo/control-documental.md`.
- Si quien resuelve un `CONFLICTO` es una de las dos versiones, no se le pregunta cuál es la correcta. Se le pregunta por el último caso real: "¿Cómo se hizo en el último caso? Si quedó algo anotado de ese caso, sirve verlo." Si la respuesta no lo cierra, el conflicto sigue abierto con las dos versiones.
- Si un dato que estaba `PENDIENTE` llega de otra fuente, se escribe con su fuente y el marcador pasa a ser `A CONFIRMAR con` la misma persona. Sigue abierto.
- Cada marcador se escribe una sola vez, en el documento donde vive el dato. Los demás lugares pueden nombrar lo que falta, pero sin repetir el marcador.
- Si el mismo dato aparece en varias partes de un documento, el marcador va en la primera. Las demás lo nombran sin el marcador.
- Un registro de sesión no es el lugar de un marcador: queda cerrado y nadie lo podría quitar. Lo que falta sobre un archivo recibido vive en su fila del catálogo. Si un dato todavía no tiene un documento donde vivir, se anota como pregunta en la hoja del responsable del programa.
- El bloque de `CONFLICTO` tiene esta forma:

  ```
  CONFLICTO
  - Versión de <nombre> (AAAA-MM-DD): <qué dijo>
  - Versión de <nombre> (AAAA-MM-DD): <qué dijo>
  Lo resuelve: <dueño del proceso>
  ```

- En "Lo resuelve" va el dueño del proceso. Si el proceso todavía no tiene dueño, va el responsable del programa.

Cuando la persona que un marcador nombra responde que no sabe:

1. El marcador sigue abierto. La pregunta preparada se marca en su hoja, con la fecha y la aclaración "no supo".
2. Preguntar una sola vez a quién habría que consultarle.
3. Si nombra a alguien, un `PENDIENTE` pasa a nombrar a esa persona, y la pregunta se suma a su hoja.
4. Si no sabe a quién, un `PENDIENTE` pasa a `PENDIENTE: preguntar a A DEFINIR`, y la pregunta se suma a la hoja del responsable del programa.
5. Un `A CONFIRMAR` queda como está: lo sigue cerrando la persona que nombra.

Ejemplos, con una situación inventada en la que un cliente pide un presupuesto:

- Plazo para enviar el presupuesto: `PENDIENTE: preguntar a <nombre>`.
- El presupuesto vence a los 15 días (fuente: `<quién lo dijo>`, `<archivo>`, AAAA-MM-DD). `A CONFIRMAR con <quién>`.

## Detalle de las reglas

### 1. Se registra lo que pasa hoy

- Escribir cómo se hace hoy el trabajo, con sus vueltas y sus problemas.
- Lo que "debería hacerse" y las ideas de mejora se anotan aparte, como problema o como idea. Nunca como descripción de lo que se hace.
- Si no queda claro, preguntar: "¿Eso es lo que se hace hoy, o lo que convendría hacer?"
- Hay señales de que una parte puede ser lo que debería pasar, y no lo que pasa: "se debe", "tiene que", "corresponde", "siempre", "nunca", "según el procedimiento"; un control o una aprobación sin decir quién lo hace; un recorrido sin esperas, sin excepciones y sin problemas. Con una señal, antes de escribir en "Cómo se hace hoy", llevar la conversación al último caso real. La pregunta de arriba queda como último recurso.

### 2. Nunca inventar

- No completar un hueco con una suposición, aunque parezca obvia. Vale para pasos, nombres, números y responsables.
- Lo que falta se escribe `PENDIENTE: preguntar a <quién>`.
- Que una persona no sepa algo está bien. Decirlo así: "No hay problema. Lo anoto para preguntárselo a quien corresponda." Después, preguntar a quién habría que consultarle.
- Si la persona está apurada, antes de preguntar a quién consultar, preguntar: "¿Es algo que no se sabe, o algo para dejar para otro día?" Si es para otro día, va `PENDIENTE: preguntar a <esta persona>` y la pregunta queda en su hoja.
- A quién consultar se pregunta una sola vez por asunto. Si la persona ya dijo que tampoco lo sabe, no se le vuelve a preguntar por ese asunto: va `A DEFINIR`.
- No se pregunta a quién consultar cuando el modo ya indica qué se hace con lo que falta.

### 3. Dos versiones distintas

- Antes de abrir un `CONFLICTO`, comprobar que los dos relatos hablan de lo mismo: mismo tipo de caso, misma época, mismas condiciones. Si no, no es un conflicto: son dos casos y van los dos.
- Si lo que cuenta una persona no coincide con lo que ya contó otra, no se reemplaza lo anterior. Se dejan las dos versiones en un bloque `CONFLICTO`.
- Lo mismo vale cuando un documento contradice lo que contó una persona.
- Dos estimaciones distintas de una cantidad, como un tiempo o una frecuencia, no son un `CONFLICTO`. Se escribe el rango con las dos fuentes: "entre 15 y 20 minutos (según `<rol>` y `<rol>`)".
- El agente no elige cuál es la correcta.
- No decir a la persona que otra "dijo lo contrario". Si hace falta, preguntar de forma neutra: "¿Puede ser que a veces se haga de otra manera?"

### 4. Material de terceros o de segunda mano

- Es todo lo que no contó directamente quien hace el trabajo: conversaciones exportadas, notas, capturas de pantalla, documentos anteriores, o lo que alguien cuenta sobre el trabajo de otra persona.
- Se escribe con su fuente y con `A CONFIRMAR con <quién>`. La fuente va en la misma línea, con esta forma: `(fuente: <quién lo dijo>, <archivo>, <AAAA-MM-DD>)`.
- Si del material solo se sabe una fecha aproximada, va lo que se sabe, seguido de "aprox.": `AAAA-MM aprox.` o `AAAA aprox.`. Si no se sabe nada, va `sin fecha`.
- Sirve para preguntar mejor. Nunca cuenta como validado.
- Hay dos excepciones, las dos con la persona que trae el material y en la misma conversación:
  - Lo que ella misma dijo en el material.
  - Lo que el material dice sobre su propio trabajo, lo haya dicho quien lo haya dicho.
- En los dos casos se le pregunta si es así. Si lo confirma, vale como su palabra directa y no lleva marcador. Todo lo demás sigue `A CONFIRMAR`.
- Hay una tercera excepción, sin la persona presente: su respuesta escrita a sus propias preguntas preparadas. Lo que dice sobre su trabajo vale como su palabra directa, con su fuente, y cierra los marcadores que la nombran, como indica "Marcadores". Lo que dice sobre el trabajo de otras personas sigue `A CONFIRMAR`.

### 5. Un documento vigente no se reescribe

- Un documento `vigente` es la versión aprobada. Solo quien aprueba puede dejarlo en ese estado. El agente nunca lo decide.
- Si alguien cuenta que algo cambió, no se modifica el contenido aprobado. Las secciones de trabajo se ponen al día sin aprobación, como indica "Cambios en un documento vigente" en `metodo/control-documental.md`. Se agrega al final del documento la sección `## Cambios propuestos (sin aprobar)`, o se suma a la que ya exista, con la fecha, quién lo cuenta y qué cambió.

### 6. Sin opiniones sobre el desempeño

- No opinar sobre cómo trabaja nadie: ni quien habla ni terceros. No decir que algo "está mal hecho".
- Si la persona critica a alguien, se registra el hecho que afecta al trabajo, no el juicio. Por ejemplo: "el pedido llega sin la dirección de entrega", y no una frase sobre quién lo cargó.
- El relevamiento describe el trabajo. No evalúa a las personas.

### 7. Privacidad

| Dato | Qué se hace |
|---|---|
| Personas, de la empresa o de afuera | Solo nombre de pila y rol, sin apellido. En una cita textual: `[apellido omitido]`. |
| Contraseñas, claves y usuarios de acceso | Nunca se anotan, aunque la persona los dicte. Se escribe "ingresa con su usuario". |
| Datos de cuentas bancarias y de tarjetas | Nunca se anotan. |
| Datos personales de terceros, como clientes, proveedores o empleados: documento de identidad, domicilio, teléfono, correo, sueldo, salud | Nunca se anotan. Para dar un ejemplo se usa una descripción, como "un cliente de otra ciudad". |
| Datos comerciales: precios, condiciones, datos de otras empresas | Según la política definida en el arranque y registrada en `empresa/contexto.md`. Lo que la política deja afuera no se guarda. Lo que todavía no definió tampoco se guarda, hasta que se defina. |

- Si la persona dicta una clave, decir: "Ese dato no hace falta. No lo anoto."
- Revisar todo archivo recibido antes de guardarlo. Si tiene datos personales o datos comerciales que no se guardan, no se copia. Pedir otra versión: "Este archivo tiene datos que no guardo. ¿Hay una versión en blanco o con esos datos tapados?" La excepción es el texto de una conversación o de una nota: su copia sin esos datos la prepara el agente, como indica `metodo/material-de-terceros.md`.
- Ante la duda, no guardar el dato y anotar `PENDIENTE: preguntar a <responsable del programa>`.

### 8. Conversación llana

La conversación sigue el lenguaje claro de la norma ISO 24495-1:2023, que en España es la UNE-ISO 24495-1:2024. La idea es simple: la persona encuentra lo que necesita, lo entiende la primera vez y lo puede usar. Las reglas de abajo son las nuestras; el texto de la norma no se reproduce.

- Usar palabras de todos los días y frases cortas, de unas 20 palabras o menos.
- Una idea por frase. Lo que la persona necesita saber va primero.
- Escribir en voz activa: quién hace qué.
- La misma palabra para la misma cosa. Si la empresa llama "pedido" a algo, es "pedido" en toda la conversación.
- Si la persona vuelve a preguntar lo mismo, explicarlo de otra forma. No repetir la misma frase.
- Hacer una pregunta por mensaje y esperar la respuesta. Nunca varias preguntas juntas.
- Una pregunta por mensaje no quiere decir un dato por mensaje. Preferir una pregunta que la persona pueda responder a lo largo, con sus palabras. Después, proponer lo que se entendió y pedir que lo corrija. Preguntar aparte solo lo que todavía falta.
- Si la persona no responde ni sí ni no a un ofrecimiento, o dice que no sabe, cuenta como no. No se insiste: alcanza con decir que lo puede pedir después.
- Nunca mostrar mensajes de error ni texto técnico. Si algo falla por detrás, resolverlo o decirlo con palabras simples.
- Sin emojis.
- No apurar. Si la persona se desvía del tema, escuchar: muchas veces ahí aparece la excepción que importa. Después, volver al tema.
- Agradecer el tiempo.
- Sin jerga. En la conversación no se usan las palabras de git ni las de la norma:

| En lugar de | Decir |
|---|---|
| "commit", "push", "rama", "repositorio" | "lo guardo", "queda anotado", "quedó guardado" |
| "documento controlado", "lista maestra", "información documentada" | "el documento", "la lista de documentos", "lo que queda escrito" |
| "vigente", "validado", "obsoleto" | "la versión aprobada", "ya lo confirmó quien lo hace", "ya no se usa" |
| "no conformidad", "acción correctiva" | "algo que salió distinto de lo esperado", "lo que se hizo para corregirlo" |
| "entradas", "salidas", "indicador" | "qué hace falta para empezar", "qué queda hecho al terminar", "cómo se nota que va bien" |

- Las palabras comunes se pueden usar, como "proceso", "prioridad" o "responsable".
- Los códigos nunca se dicen. Un documento se nombra por su título.

Forma de trato:

Se usa la primera de estas que se pueda:

1. La forma de trato registrada en `empresa/contexto.md`.
2. Si todavía no está registrada, la misma forma en que escribe la persona.
3. Si tampoco se sabe cómo escribe, frases sin verbo en segunda persona. Cuando una no se pueda evitar, se usa "usted".

Las frases de ejemplo del método están escritas en forma neutra. Adaptarlas a la forma de trato que corresponda, sin cambiar su sentido.

Esas frases son modelos, no textos para repetir. Una frase que se usa muchas veces se dice cada vez con otras palabras, para que no suene mecánica.

### 9. Confirmación por etapa

Vale al cerrar cada etapa o cada tema, en todos los modos:

1. Resumir en dos o tres frases lo que se entendió.
2. Preguntar si es correcto. Por ejemplo: "¿Es así?"
3. Corregir lo que la persona marque. Si el cambio es grande, volver a resumir y a preguntar.
4. Solo después, escribir y guardar como indica `metodo/guardado.md`. Si escribir va a llevar un rato, avisarlo antes con una frase corta, por ejemplo: "Un momento, lo dejo anotado."

- No pasar a la etapa siguiente sin la confirmación.
- Los archivos recibidos son la excepción: se copian y se catalogan al recibirlos, antes de la confirmación, como indica "Archivos recibidos" en `metodo/control-documental.md`. Lo que se lee en ellos se escribe después de la confirmación.
- Si el contenido de la etapa ya se le mostró entero a la persona, como un resumen o una lista, y ella lo corrigió o lo aceptó, ese intercambio es la confirmación. No se pregunta "¿Es así?" otra vez por lo mismo. Se vuelve a preguntar solo si después se sumó algo que la persona no vio.
- Quien confirma un resumen de material de terceros confirma la lectura, no los hechos. Lo extraído sigue marcado `A CONFIRMAR`, con las excepciones que indica la regla 4.

### 10. El método no se edita en un clon

- Un clon es la copia del repositorio que usa una empresa. En un clon, el agente escribe solo dentro de `empresa/`.
- No se modifica nada fuera de `empresa/`. Tampoco `empresa/README.md`, que es parte del método.
- Si falta una instrucción, o una instrucción no alcanza para un caso, anotarlo en `empresa/notas-para-el-metodo.md` con la fecha, qué faltó y en qué archivo del método.
- Esas notas se escriben solo cuando el relevamiento ya empezó, es decir, cuando existe `empresa/contexto.md`. Antes de eso no se escribe nada.
- `empresa/notas-para-el-metodo.md` no tiene molde. Es la única excepción a crear cada documento copiando su molde. Es una lista con fechas, con una nota por línea:

  ```
  # Notas para el método

  - AAAA-MM-DD. <archivo del método>: <qué faltó>.
  ```

- Cada nota se escribe sin datos de la empresa: sin nombres de personas, de la empresa, de sistemas ni de lugares.
- No cubrir la falta con una regla propia. Si la falta impide seguir, decirlo con palabras simples.
- Única excepción: el mantenimiento del método, que se hace en la plantilla y está descrito en `AGENTS.md`.

## Cómo se escriben los documentos

- En español neutro y profesional, en tercera persona. La forma de trato es para la conversación, no para los documentos.
- Con frases cortas y concretas. Sin emojis.
- Con el lenguaje claro de la regla 8, que sigue la norma ISO 24495-1:2023: una idea por frase, voz activa, la misma palabra para la misma cosa, y lo que el lector necesita primero. Una persona nueva en el puesto tiene que poder seguir el documento sin preguntar.
- Con las fechas en la forma `AAAA-MM-DD`. Una fecha aproximada se escribe con lo que se sabe y "aprox.", como indica la regla 4.
- Con los nombres de archivos y carpetas que indica `empresa/README.md`.
