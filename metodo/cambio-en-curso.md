# Modo: cambio en curso

En este modo se sigue algo que la empresa está cambiando y que altera cómo se trabaja: un sistema nuevo, una sede nueva, una reorganización o una norma nueva. Cada cambio tiene su ficha, donde quedan el plan, las decisiones, lo que falta responder y lo que puede salir mal.

La ficha de un proceso sigue contando cómo se hace hoy. Este modo no la toca.

Antes de empezar, leer completo `metodo/control-documental.md`.

## En una mirada

| Qué se hace | Cuándo | Cómo |
|---|---|---|
| Abrir un cambio | La primera vez que se habla de ese cambio | Ocho etapas, como indica "Abrir un cambio". |
| Seguir un cambio | Cada vez que hay novedades | Tres etapas, como indica "Seguir un cambio". Primero se dice lo que sigue sin respuesta. |
| Cerrar un cambio | Cuando la forma nueva ya se usa | Los pasos de "Cerrar un cambio". |

Cada etapa se cierra igual: resumen de lo entendido, pregunta de confirmación y guardado. Es la regla 9 de `metodo/reglas.md`.

## Reglas de este modo

1. Se trabaja con el responsable del programa.
2. Quien lleva el cambio dentro de la empresa puede ser otra persona. Se anota en la ficha del cambio. No es un rol del relevamiento.
3. Las personas de afuera de la empresa, como alguien de un proveedor, se anotan en la ficha del cambio con su nombre de pila y su rol. No llevan hoja.
4. La ficha de un proceso cuenta lo que pasa hoy. "Cómo va a quedar" es un plan y vive solo en la ficha del cambio.
5. Este modo no escribe en las fichas de proceso. Una ficha cambia cuando la forma nueva ya se usa, y por el camino normal: quien hace el trabajo lo cuenta en una entrevista, y la revisión y la aprobación suben la versión.
6. Una decisión que tomó otra persona, o que sale de material, lleva `A CONFIRMAR con <quién>` hasta que quien decidió la confirma.
7. Nada se completa con una suposición. Lo que no se sabe se escribe `PENDIENTE: preguntar a <quién>`.
8. Va una carpeta por cambio. Puede haber varios cambios abiertos a la vez.
9. Un cambio `cerrado` no se reabre. Si vuelve a moverse, se abre un cambio nuevo que lo nombra.
10. Los códigos se asignan desde la lista maestra, con los pasos de "Cómo se asigna un código" en `metodo/control-documental.md`.

## Al empezar cada sesión

1. Leer qué cambios hay en `empresa/cambios/` y en qué estado está cada uno.
2. Saber de qué cambio se trata:

   | Situación | Qué se hace |
   |---|---|
   | No hay ningún cambio, o la persona trae uno nuevo | Seguir "Abrir un cambio". |
   | Hay un solo cambio `abierto` | Seguir "Seguir un cambio". |
   | Hay más de uno | Preguntar de cuál se trata. |
   | El cambio está `en pausa` y la persona dice que se retomó | Pasarlo a `abierto`, anotarlo en su historial y seguir "Seguir un cambio". |

3. Crear el registro de la sesión, como indica "El registro de la sesión".

## Abrir un cambio

Son ocho etapas. Las preguntas son una guía: se hace una por mensaje y no se pregunta lo que ya está escrito.

| Etapa | Preguntas de guía | Dónde se escribe |
|---|---|---|
| 1. Qué cambia y por qué | "¿Qué es lo que está cambiando?", "¿Por qué se hace?" y "¿Qué se espera que mejore?" | "Qué cambia y por qué" |
| 2. Quién lo lleva y qué terceros participan | "¿Quién lleva este cambio dentro de la empresa?" y "¿Participa alguien de afuera, como un proveedor o un asesor?" | "Quiénes participan" |
| 3. En qué etapa está y qué fechas se conocen | "¿En qué punto está hoy?" y "¿Qué fechas se conocen?" | "Etapa y fechas" |
| 4. Qué procesos afecta | "¿Qué trabajos van a cambiar?", "¿Cómo va a quedar cada uno?" y "¿Qué falta definir?" | "Procesos afectados" y "Diferencias entre la forma de hoy y la nueva" |
| 5. Qué ya se decidió | "¿Qué se decidió hasta ahora?", "¿Quién lo decidió?" y "¿Por qué?" | "Decisiones tomadas" |
| 6. Qué está abierto con terceros | "¿Qué se le preguntó a alguien de afuera y sigue sin respuesta?" y "¿Desde cuándo?" | "Pendientes con terceros" |
| 7. Qué hay que preparar | "¿Qué tiene que estar listo antes de usar lo nuevo: datos, listas, permisos, formularios?" y "¿Quién lo prepara?" | "Datos y configuración a preparar" |
| 8. Qué puede salir mal | "¿Qué puede salir mal con este cambio?" y "¿Qué se piensa hacer si pasa?" | "Qué puede salir mal" |

Al cerrar la etapa 1, después de la confirmación:

1. Acordar con la persona un nombre corto para el cambio. De ese nombre sale `<slug>`: en minúsculas, con guiones y sin acentos.
2. Crear la ficha copiando `plantillas/ficha-de-cambio.md` a `empresa/cambios/<slug>/ficha-del-cambio.md`, con estado `abierto`.

En la etapa 2:

- Una persona de la empresa que no tiene hoja recibe una, como en la etapa 6 de `metodo/arranque.md`.
- Una persona de afuera se anota solo en la ficha del cambio.

En la etapa 4:

- Recorrer el mapa de procesos y anotar cada proceso afectado como indica "Procesos afectados".
- Para cada proceso que ya tiene ficha, leer sus pasos, sus reglas y sus excepciones, y preguntar dos cosas: "¿Qué de esto se hace solo porque la forma actual lo exige?" y "¿Hay algo que hoy se hace y que la forma nueva no tiene previsto?"

Al cerrar la etapa 8:

1. Buscar lo que ya se anotó sobre este cambio en otras sesiones, como indica "Lo anotado en otras sesiones".
2. Sumar cada `PENDIENTE: preguntar a` y cada `A CONFIRMAR con` de la ficha del cambio a "Preguntas preparadas" de la hoja de la persona nombrada.
3. Resumir toda la ficha y decir qué sigue.

- Se puede cortar al terminar cualquier etapa. Si pasaron unos 25 minutos, ofrecer cortar con la frase de "Ofrecer cortar".
- Si la apertura se corta, la sesión siguiente sigue desde la primera etapa sin marcar del registro anterior.

## Procesos afectados

La tabla tiene estas columnas: `| Proceso | Cómo se hace hoy | Cómo va a quedar | Qué falta definir |`.

| El proceso | En "Cómo se hace hoy" va | Además |
|---|---|---|
| Tiene ficha | Un enlace a la ficha, con su código: `[<codigo>](../../procesos/<area>/<codigo>-<slug>.md)` | Nada. Lo que dice la ficha no se copia ni se reescribe. |
| Está en el mapa y todavía no tiene ficha | "sin ficha: relevar primero" | En el mapa, su prioridad pasa a `P1`, para que se releve primero. |
| No está en el mapa | "sin ficha: relevar primero" | Agregarlo como indica "Un proceso que aparece en la conversación" en `metodo/entrevista.md`, con prioridad `P1`. |
| Va a dejar de hacerse | El enlace a su ficha, si la tiene | En "Cómo va a quedar" va "deja de hacerse". Su baja se decide en la revisión, cuando ya no se haga. |
| Es nuevo y todavía no se hace | "todavía no se hace" | No entra al mapa hasta que empiece a hacerse. |

- "Cómo va a quedar" es un plan. No pasa a ninguna ficha de proceso.
- "Qué falta definir" dice qué falta y quién lo tiene que definir. Si depende de alguien de afuera, va también a "Pendientes con terceros".

## Decisiones

Cada decisión lleva fecha, qué se decidió, quién lo decidió, por qué y la fuente.

| De dónde sale | Cómo se anota |
|---|---|
| La cuenta quien la tomó, en esta conversación | Sin marcador. La fuente es esa persona, con la fecha. |
| La cuenta otra persona | Con `A CONFIRMAR con <quién decidió>`. |
| Sale de material o de un registro de sesión | Con la fuente en la forma que indica `metodo/material-de-terceros.md` y con `A CONFIRMAR con <quién decidió>`. |
| La tomó alguien de afuera de la empresa | Con `A CONFIRMAR con` y el nombre de quien lleva el cambio en la empresa. |

Cuando quien decidió la confirma, se quita el marcador y se anota la fecha en la fuente.

## Pendientes con terceros

Cada pendiente lleva la pregunta, a quién se le hizo, desde cuándo y la respuesta.

- En "A quién" van el nombre de pila y el rol de la persona de afuera.
- Al empezar cada sesión de seguimiento se dice primero qué sigue sin respuesta y desde cuándo.
- Cuando llega una respuesta, se escribe con su fecha y con quién la contó.
- Se ofrece la lista para enviar: un mensaje con las preguntas numeradas, en palabras simples, para que lo envíe la persona de la empresa que trata con ese tercero.

## Lo anotado en otras sesiones

Las entrevistas y las sesiones de material dejan lo que aparece sobre un cambio en "Temas para otra sesión" de su registro, en líneas que empiezan con `Cambio:`. Los registros están cerrados, así que la ficha del cambio lleva la cuenta de cuáles ya se leyeron.

1. Tomar los registros de `empresa/sesiones/` que no figuran en "Registros de sesión ya leídos" de esta ficha.
2. En cada uno, leer las líneas de "Temas para otra sesión" que empiezan con `Cambio:`.
3. Contar a la persona lo que se encontró sobre este cambio y preguntar con la frase de "Lo anotado en otras conversaciones".
4. Llevar cada línea aceptada a su lugar en la ficha: una decisión, un pendiente con un tercero, un proceso afectado, algo para preparar o algo que puede salir mal. Va con su fuente y con `A CONFIRMAR con <quién lo dijo>`.
5. Anotar cada registro en "Registros de sesión ya leídos", con lo que se tomó. Se anota también cuando no se tomó nada.

- La fuente dice quién lo dijo, en qué registro o material y en qué fecha.
- Si la línea la dijo la misma persona que está en la conversación, y la confirma ahora, vale como su palabra directa y va sin marcador.
- Si una línea es de otro cambio que todavía no tiene ficha, decirlo con la frase de "Otro cambio".

## Seguir un cambio

| Etapa | Qué se hace |
|---|---|
| 1. Qué sigue abierto | Decir primero los pendientes con terceros que siguen sin respuesta, y desde cuándo. Después, lo que hay que preparar y todavía no está listo, y las decisiones que siguen `A CONFIRMAR`. Preguntar por cada uno si hay novedades. |
| 2. Novedades | Buscar lo anotado en otras sesiones. Preguntar por decisiones nuevas, fechas que cambiaron, procesos que se suman y cosas nuevas que pueden salir mal. |
| 3. Qué sigue | Anotar los próximos pasos. Ofrecer la lista para enviar con lo que sigue sin respuesta. |

- Cada novedad se escribe en su parte de la ficha y suma una fila al historial.
- Si la persona dice que el cambio se frenó, pasa a `en pausa`, con la fecha y el motivo en el historial.
- Si dice que la forma nueva ya se usa, seguir "Cerrar un cambio".

## Cerrar un cambio

Cerrar un cambio es comprobar que lo que cambió ya quedó contado y aprobado. Este modo no edita ninguna ficha de proceso.

1. Preguntar desde cuándo se usa la forma nueva y en qué procesos. Anotar la fecha en "En uso desde".
2. Completar "Fichas a actualizar", con una fila por proceso afectado.
3. Preguntar por cada proceso si en la práctica cambió.
   - Si no cambió, va "se deja como está", con el motivo, quién lo dijo y la fecha.
   - Si cambió, sumar a "Preguntas preparadas" del dueño y de los participantes la pregunta por cómo se hace ahora.
4. En cada sesión posterior, mirar la ficha de cada proceso que falta y poner al día su fila:

   | Qué muestra la ficha del proceso | Qué va en "Cómo quedó" |
   |---|---|
   | Nada posterior a "En uso desde" | "falta contarlo" |
   | Algo contado después, todavía sin aprobar | "falta aprobarlo" |
   | Una versión aprobada después | "actualizada", con el número de versión |

5. Cuando todas las filas dicen "actualizada" o "se deja como está", el cambio pasa a `cerrado`. Anotar la fecha en "Cerrado el" y sumar una fila al historial.

- Lo que se cuenta de nuevo sigue el camino normal: una ficha `vigente` recibe el cambio como propuesto y lo aprueba quien aprueba.
- Un proceso que dejó de hacerse se anota para la revisión, que decide su baja.

## Estados de un cambio

| Estado | Qué significa | Cuándo se pone |
|---|---|---|
| `abierto` | El cambio se está siguiendo. | Al abrirlo, o cuando se retoma. |
| `en pausa` | La empresa lo frenó. | Cuando el responsable del programa lo dice. |
| `cerrado` | La forma nueva está en uso y cada ficha afectada quedó actualizada o se dejó como está. | Al completar "Fichas a actualizar". |

## El registro de la sesión

- Va uno por sesión. Se crea copiando `plantillas/registro-de-sesion.md` a `empresa/sesiones/AAAA-MM-DD-<quien>-cambio-<slug>.md`.
- En "Modo" va `cambio en curso`.
- En "Etapas o temas" van las etapas de lo que se hace: las ocho de la apertura o las tres del seguimiento.
- Al cerrar la sesión, completar "Cómo terminó" y seguir "Al cerrar la sesión" en `metodo/guardado.md`.

## Guardado en este modo

Los mensajes siguen el formato de `metodo/guardado.md`:

| Momento | Mensaje |
|---|---|
| Cierre de cada etapa | `docs(empresa): cambio <nombre corto> - etapa <número> con <nombre>` |
| Cierre de la sesión | `docs(empresa): cambio <nombre corto> - cierre de sesión con <nombre>` |

## Qué decir

| Situación | Frase |
|---|---|
| Plan y no hecho | "Esto lo anoto como plan. Lo que está escrito de cada trabajo sigue contando cómo se hace hoy, hasta que lo nuevo se use." |
| Lo que sigue abierto | "Antes de seguir: hay `<cantidad>` preguntas sin respuesta. La más antigua espera desde el `<fecha>`." |
| Lo anotado en otras conversaciones | "En otras conversaciones quedó anotado esto sobre el cambio: `<resumen>`. ¿Lo sumo así?" |
| Otro cambio | "También apareció otro cambio: `<qué es>`. ¿Conviene abrirlo aparte?" |
| Lista para enviar | "¿Preparo las preguntas pendientes en un mensaje listo para enviar?" |
| Ofrecer cortar | "Ya llevamos un buen rato. Lo hecho quedó guardado. ¿Seguimos, o cortamos aquí y continuamos otro día?" |
| Falta para cerrar | "Para cerrar el cambio falta esto: `<qué falta>`." |
| Cambio cerrado | "Con esto el cambio queda cerrado: todo lo que cambió ya está escrito y aprobado." |

En la conversación se usan palabras simples, como indica la regla 8 de `metodo/reglas.md`:

| En lugar de | Decir |
|---|---|
| "cambio en curso" | "lo que está cambiando" |
| "ficha del cambio" | "lo anotado sobre este cambio" |
| "procesos afectados" | "los trabajos que cambian" |
| "pendientes con terceros" | "lo que falta que respondan de afuera" |

Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
