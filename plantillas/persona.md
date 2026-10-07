> **Nota para el agente.** Este molde se copia a `empresa/personas/<nombre>.md`, una hoja por persona. Es un documento de trabajo: no lleva bloque de control y se actualiza cada vez que se sabe algo nuevo. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean, y cada ayuda en cursiva se reemplaza por el contenido. Una parte que todavía no tiene nada conserva su ayuda y su línea de muestra hasta que haya algo para anotar. De la persona se anota solo el nombre de pila y el rol. Lo que no se sabe se escribe `PENDIENTE: preguntar a <quién>`. El marcador `A CONFIRMAR` va una sola vez. Si el dato está también en la ficha de un proceso, va en la ficha y no en esta hoja. Si no, va en "De dónde sale cada dato", y no junto a cada dato. La línea "Confirmada por la persona" pasa a `sí`, con la fecha, cuando la persona confirma sus datos en la primera entrevista en que la línea siga en `no`, como indica "Etapa 1. Apertura" en `metodo/entrevista.md`. La línea "Cómo participa" pasa a "recibe las preguntas por escrito" cuando se sabe que la persona no va a poder conversar. Esta nota se borra de la copia.

# `<nombre de pila>`

- **Última actualización:** `<AAAA-MM-DD>`
- **Origen de la hoja:** `<quién dio los datos y en qué fecha>`
- **Confirmada por la persona:** no
- **Cómo participa:** conversa

## Rol en la empresa

_Qué hace en la empresa, en una o dos frases._

## Rol en el relevamiento

_Uno o más de estos: responsable del programa, quien aprueba, dueño de proceso, participante. Si es dueño de proceso, de cuáles._

## Áreas

_Las áreas en las que trabaja, con el nombre que figura en el contexto de la empresa._

## Sistemas y herramientas que usa

_Con el nombre que figura en el contexto de la empresa. Si no usa ninguna, va `—`. Si no se sabe, va `PENDIENTE: preguntar a <quién>`. Nunca se anotan usuarios ni claves._

## Procesos en los que participa

_Una fila por proceso, con el nombre exacto del mapa de procesos. Si el proceso todavía no tiene código, en "Código" va `—`. Si todavía no se sabe qué hace la persona en el proceso, en "Su parte" va `—`: se completa en su entrevista. El estado y la prioridad de cada proceso no se copian aquí: se leen en el mapa._

| Código | Proceso | Su parte |
|---|---|---|
| `<código>` | `<nombre del proceso>` | `<qué hace esta persona en el proceso>` |

## Preguntas preparadas

_Lo que hay que preguntarle, agrupado por proceso. Son lo primero que se le pregunta en su próxima conversación. Cada pregunta se marca cuando la respondió, en una conversación o por escrito; en ese caso, con la fecha y el archivo de la respuesta. Una pregunta nombra lo que falta saber y de dónde sale; el marcador queda en el documento donde vive el dato. Si la pregunta sale de un marcador que cambia el sentido, la línea termina con "frena la validación": esas se hacen primero._

- [ ] `<pregunta>` (`<proceso o asunto>`; sale de `<de dónde sale la pregunta>`)

## Documentos prometidos

_Lo que dijo que iba a acercar y todavía no llegó. Se le recuerda una sola vez, en su próxima conversación. Cada uno se marca cuando llega._

- [ ] `<qué documento es>`, prometido el `<AAAA-MM-DD>`

## De dónde sale cada dato

_Una línea por dato o por grupo de datos, con su fuente y su fecha. Lo que no contó la propia persona lleva `A CONFIRMAR`. Cuando la persona lo confirma, se quita el marcador y la fuente pasa a ser ella._

- `<dato>`: `<quién lo contó o de qué material sale>`, `<AAAA-MM-DD>`. `A CONFIRMAR con <quién>`.
