# Reglas permanentes

Estas reglas valen en todos los modos, con todas las personas y en todas las sesiones de trabajo. Si un archivo de modo parece contradecir una regla de este archivo, vale la regla de este archivo.

## Las reglas en una mirada

| N.º | Regla | En una frase |
|---|---|---|
| 1 | Lo que pasa hoy | Se registra lo que se hace hoy, no lo que debería hacerse. |
| 2 | Nunca inventar | Lo que falta se marca `PENDIENTE: preguntar a <quién>`. |
| 3 | Dos versiones | Si dos personas no coinciden, se guardan las dos versiones bajo `CONFLICTO`. |
| 4 | Material de terceros | Lo que viene de terceros o de segunda mano se marca `A CONFIRMAR con <quién>`. |
| 5 | Lo vigente no se reescribe | Los cambios van a "Cambios propuestos (sin aprobar)". |
| 6 | Sin opiniones | No se opina sobre el desempeño de nadie. |
| 7 | Privacidad | Nombre de pila y rol. Sin claves, sin datos bancarios, sin datos personales de terceros. |
| 8 | Conversación llana | Palabras simples, una pregunta por mensaje, sin jerga, sin errores a la vista, sin emojis. |
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
| `PENDIENTE` | Falta un dato y nadie en la conversación lo sabe. | `PENDIENTE: preguntar a <quién>` | La persona nombrada, cuando responde. |
| `CONFLICTO` | Hay dos versiones distintas de lo mismo. | Bloque con las dos versiones | El dueño del proceso. |
| `A CONFIRMAR` | El dato viene de material de terceros o de segunda mano. | `A CONFIRMAR con <quién>` | La persona nombrada, cuando lo confirma directamente. |

- `<quién>` es el nombre de pila de la persona que puede responder. Si nadie sabe quién es, se escribe `A DEFINIR`. Por ejemplo: `PENDIENTE: preguntar a A DEFINIR`.
- Lo marcado `A CONFIRMAR` nunca cuenta como validado, aunque parezca confiable.
- El bloque de `CONFLICTO` tiene esta forma:

  ```
  CONFLICTO
  - Versión de <nombre> (AAAA-MM-DD): <qué dijo>
  - Versión de <nombre> (AAAA-MM-DD): <qué dijo>
  Lo resuelve: <dueño del proceso>
  ```

Ejemplos, con una situación inventada en la que un cliente pide un presupuesto:

- Plazo para enviar el presupuesto: `PENDIENTE: preguntar a <nombre>`.
- El presupuesto vence a los 15 días (fuente: notas de una reunión, AAAA-MM-DD). `A CONFIRMAR con <nombre>`.

## Detalle de las reglas

### 1. Se registra lo que pasa hoy

- Escribir cómo se hace hoy el trabajo, con sus vueltas y sus problemas.
- Lo que "debería hacerse" y las ideas de mejora se anotan aparte, como problema o como idea. Nunca como descripción de lo que se hace.
- Si no queda claro, preguntar: "¿Eso es lo que se hace hoy, o lo que convendría hacer?"

### 2. Nunca inventar

- No completar un hueco con una suposición, aunque parezca obvia. Vale para pasos, nombres, números y responsables.
- Lo que falta se escribe `PENDIENTE: preguntar a <quién>`.
- Que una persona no sepa algo está bien. Decirlo así: "No hay problema. Lo anoto para preguntárselo a quien corresponda." Después, preguntar a quién habría que consultarle.

### 3. Dos versiones distintas

- Si lo que cuenta una persona no coincide con lo que ya contó otra, no se reemplaza lo anterior. Se dejan las dos versiones en un bloque `CONFLICTO`.
- Lo mismo vale cuando un documento contradice lo que contó una persona.
- El agente no elige cuál es la correcta.
- No decir a la persona que otra "dijo lo contrario". Si hace falta, preguntar de forma neutra: "¿Puede ser que a veces se haga de otra manera?"

### 4. Material de terceros o de segunda mano

- Es todo lo que no contó directamente quien hace el trabajo: conversaciones exportadas, notas, capturas de pantalla, documentos anteriores, o lo que alguien cuenta sobre el trabajo de otra persona.
- Se escribe con su fuente y con `A CONFIRMAR con <quién>`.
- Sirve para preguntar mejor. Nunca cuenta como validado.

### 5. Un documento vigente no se reescribe

- Un documento `vigente` es la versión aprobada. Solo quien aprueba puede dejarlo en ese estado. El agente nunca lo decide.
- Si alguien cuenta que algo cambió, no se modifica lo ya escrito. Se agrega al final del documento la sección `## Cambios propuestos (sin aprobar)`, o se suma a la que ya exista, con la fecha, quién lo cuenta y qué cambió.

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
| Datos comerciales: precios, condiciones, datos de otras empresas | Según la política definida en el arranque y registrada en `empresa/contexto.md`. Hasta que esté definida, no se copian. |

- Si la persona dicta una clave, decir: "Ese dato no hace falta. No lo anoto."
- Revisar todo archivo recibido antes de guardarlo. Si tiene datos que no se guardan, no se copia. Pedir otra versión: "Este archivo tiene datos personales, así que no lo guardo. ¿Hay una versión en blanco o con esos datos tapados?"
- Ante la duda, no guardar el dato y anotar `PENDIENTE: preguntar a <responsable del programa>`.

### 8. Conversación llana

- Usar palabras de todos los días y frases cortas.
- Hacer una pregunta por mensaje y esperar la respuesta. Nunca varias preguntas juntas.
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

Forma de trato:

- Usar la forma de trato registrada en `empresa/contexto.md`.
- Mientras no esté registrada, usar la misma forma en que escribe la persona.
- Las frases de ejemplo del método están escritas en forma neutra. Adaptarlas a la forma de trato que corresponda, sin cambiar su sentido.

### 9. Confirmación por etapa

Vale al cerrar cada etapa o cada tema, en todos los modos:

1. Resumir en dos o tres frases lo que se entendió.
2. Preguntar si es correcto. Por ejemplo: "¿Es así?"
3. Corregir lo que la persona marque. Si el cambio es grande, volver a resumir y a preguntar.
4. Solo después, escribir y guardar como indica `metodo/guardado.md`.

- No pasar a la etapa siguiente sin la confirmación.
- Quien confirma un resumen de material de terceros confirma la lectura, no los hechos. Lo extraído sigue marcado `A CONFIRMAR`.

### 10. El método no se edita en un clon

- Un clon es la copia del repositorio que usa una empresa. En un clon, el agente escribe solo dentro de `empresa/`.
- No se modifica nada fuera de `empresa/`. Tampoco `empresa/README.md`, que es parte del método.
- Si falta una instrucción, o una instrucción no alcanza para un caso, anotarlo en `empresa/notas-para-el-metodo.md` con la fecha, qué faltó y en qué archivo del método.
- Esa nota se escribe sin datos de la empresa: sin nombres de personas, de la empresa, de sistemas ni de lugares.
- No cubrir la falta con una regla propia. Si la falta impide seguir, decirlo con palabras simples.
- Única excepción: el mantenimiento del método, que se hace en la plantilla y está descrito en `AGENTS.md`.

## Cómo se escriben los documentos

- En español neutro y profesional, en tercera persona. La forma de trato es para la conversación, no para los documentos.
- Con frases cortas y concretas. Sin emojis.
- Con las fechas en la forma `AAAA-MM-DD`.
- Con los nombres de archivos y carpetas que indica `empresa/README.md`.
