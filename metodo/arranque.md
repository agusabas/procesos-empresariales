# Modo: arranque

En este modo se empieza desde cero, con la persona que va a conducir el relevamiento. Al terminar quedan escritos la empresa, cómo se organiza el relevamiento, las áreas, las personas, el mapa de procesos y las preguntas preparadas para cada persona.

Funciona aunque en `empresa/` no haya nada más que `README.md`. Antes de empezar, leer completo `metodo/control-documental.md`: este modo crea documentos controlados y asigna códigos.

## En una mirada

| Etapa | Qué se averigua | Qué queda escrito | Minutos |
|---|---|---|---|
| 1. Quién habla y qué va a pasar | Quién conduce el relevamiento | `contexto.md`, `lista-maestra.md` y el registro de la sesión | 5 |
| 2. La empresa | Qué hace, tamaño, lugares, por qué ahora y qué se espera | "La empresa", en `contexto.md` | 10 |
| 3. Cómo se organiza el relevamiento | Quién aprueba, cada cuánto se revisa, forma de trato y datos que no se guardan | "Cómo se organiza el relevamiento", en `contexto.md` | 10 |
| 4. Qué hay ya escrito | El material que ya existe | `insumos/` y su `catalogo.md` | 10 o más |
| 5. Áreas y sistemas | Las áreas con sus tres letras, los sistemas y las herramientas | "Áreas" y "Sistemas y herramientas", en `contexto.md` | 10 |
| 6. Personas | Quién trabaja en cada área | Una hoja por persona, en `personas/` | 15 |
| 7. Mapa de procesos | Qué procesos hay, con su dueño, sus participantes y su prioridad | `mapa-de-procesos.md`, filas de la lista maestra y hojas de personas | 30 |
| 8. Plan de relevamiento y preguntas | Por dónde se empieza y qué se le pregunta a cada persona | Prioridades en el mapa y preguntas en cada hoja | 20 |

Las rutas de la tabla están dentro de `empresa/`. Los minutos son aproximados: en total, alrededor de dos horas, repartidas en varias conversaciones.

## Reglas de este modo

1. Se trabaja solo con quien conduce el relevamiento: el responsable del programa.
2. Las preguntas de cada etapa son una guía, no un cuestionario. Se hace una por mensaje, se adaptan a lo que la persona ya contó y no se pregunta lo que ya está escrito.
3. Nada se completa con una suposición. Lo que la persona no sabe se escribe `PENDIENTE: preguntar a <quién>`. Si tampoco sabe a quién preguntarle, se escribe `PENDIENTE: preguntar a A DEFINIR`.
4. Lo que el responsable del programa cuenta sobre la empresa, sus áreas, sus sistemas y los roles del relevamiento vale como dato directo.
5. Lo que cuenta sobre cómo trabaja otra persona es de segunda mano. Se escribe con `A CONFIRMAR con <esa persona>`.
6. Todo lo que sale del material de la etapa 4 lleva su fuente y `A CONFIRMAR con <quién>`.
7. De las personas se anota solo el nombre de pila y el rol.
8. Si una respuesta es vaga, repreguntar: cuántos, cada cuánto, quién.
9. Una palabra propia de la empresa que no se entiende se pregunta y se anota en `empresa/glosario.md`. La primera vez, ese archivo se crea copiando `plantillas/glosario.md` y se pone al día la fila `GL-GEN-001` de la lista maestra.
10. Los códigos se asignan desde la lista maestra, con los pasos de "Cómo se asigna un código" en `metodo/control-documental.md`.
11. Este modo deja los documentos, como mucho, en `borrador`. Nunca en `validado` ni en `vigente`.

## Cómo se cierra cada etapa

1. Resumir lo entendido en dos o tres frases. Si son varios elementos, como áreas, personas o procesos, en una lista corta.
2. Preguntar: "¿Es así?"
3. Corregir lo que la persona marque. Si el cambio es grande, volver a resumir y a preguntar.
4. Escribir lo confirmado en los archivos de la etapa. Escribir en el registro de la sesión las preguntas y las respuestas, con las palabras de la persona.
5. Marcar la etapa en `## Lista de arranque` de `empresa/contexto.md`: cambiar `- [ ]` por `- [x]` y agregar la fecha.
6. Guardar, como indica `metodo/guardado.md`.
7. Decir el avance con la frase de "Avance" y preguntar si se sigue.

Una etapa se puede confirmar aunque queden datos sin saber, siempre que cada uno esté escrito como `PENDIENTE` en el lugar donde iría. Si todavía no existe ese lugar, se anota en "Pendientes" del registro de la sesión.

## El tiempo

- Al presentar el trabajo, decir cuánto lleva en total y que se puede repartir en varias conversaciones.
- Al empezar cada sesión, anotar la hora en silencio.
- Al cerrar cada etapa, mirar cuánto tiempo pasó. Si pasaron unos 25 minutos o más, usar la frase de "Ofrecer cortar" en lugar de la pregunta de "Avance". Se ofrece sin insistir.
- Si no se puede ver la hora, ofrecer cortar al cerrar cada segunda etapa.
- Se corta al terminar una etapa. Si la persona tiene que irse en medio de una, resumir lo que alcanzó a contar, confirmarlo, escribirlo, dejar la etapa sin marcar y cerrar la sesión.

## Retomar el arranque

Cuando `empresa/contexto.md` existe y su lista de arranque tiene etapas sin confirmar:

1. Si la persona no dijo su nombre, pedirlo con la frase de "Pedir el nombre". Compararlo con la fila "Responsable del programa" de `empresa/contexto.md`. Si habla otra persona, decir la frase de "Habla otra persona" y terminar ahí, sin escribir nada.
2. Leer `empresa/contexto.md`. La primera línea `- [ ]` de la lista de arranque es la etapa que sigue.
3. Leer "Cómo terminó" en el último registro del arranque, en `empresa/sesiones/`.
4. Si la etapa 4 dejó material, leer `empresa/insumos/catalogo.md` y ese material antes de las etapas 5 a 7.
5. Crear un registro nuevo para esta sesión. En "Sesión anterior" va el archivo del registro anterior.
6. Decir la frase de "Retomar" y seguir con la etapa que corresponde. No volver a preguntar lo que ya está escrito.

Si la etapa había quedado a medias, se pregunta solo lo que falta y el resumen de cierre abarca la etapa entera.

## Etapa 1. Quién habla y qué va a pasar

1. Si la persona no dijo su nombre, pedirlo con la frase de "Pedir el nombre".
2. Preguntar quién va a conducir este trabajo.
   - Es la persona que está conversando: seguir.
   - Es otra persona: decir la frase de "No es quien conduce" y terminar ahí, sin crear ningún archivo.
3. Preguntar qué función tiene en la empresa, o si la acompaña desde afuera.
4. Contar qué va a pasar con la frase de "Presentación".
5. Cerrar la etapa. El resumen dice quién conduce y qué se va a hacer.

Al escribir, en este orden:

1. Crear `empresa/lista-maestra.md` copiando `plantillas/lista-maestra.md`.
2. Crear `empresa/contexto.md` copiando `plantillas/contexto-de-la-empresa.md`. El nombre de pila de quien conduce va en "Elaboró" y en la fila "Responsable del programa".
3. Poner al día la fila `CT-GEN-001` de la lista maestra: estado `en curso` y "Elaboró".
4. Crear el registro de la sesión copiando `plantillas/registro-de-sesion.md` a `empresa/sesiones/AAAA-MM-DD-<quien>-arranque.md`. En "Etapas o temas" van las ocho etapas.

## Etapa 2. La empresa

| Qué se busca | Pregunta de guía |
|---|---|
| Qué hace | "¿A qué se dedica la empresa?" |
| Para quiénes | "¿Qué tipo de clientes tiene?" |
| Tamaño | "¿Cuántas personas trabajan en ella, más o menos?" |
| Lugares | "¿En cuántos lugares funciona, y qué se hace en cada uno?" |
| Por qué ahora | "¿Por qué se decidió hacer este trabajo ahora?" |
| Qué se espera | "¿Qué tendría que quedar cuando esté terminado?" |

- Se escribe en "La empresa", en `empresa/contexto.md`.
- De los clientes se anota qué tipo de clientes son, no sus nombres.

## Etapa 3. Cómo se organiza el relevamiento

| Qué se busca | Pregunta de guía |
|---|---|
| Quién aprueba | "¿Quién va a dar el visto bueno final a cada documento?" |
| Período de revisión | "¿Cada cuánto conviene volver a mirar lo que quede escrito? Lo habitual es una vez por año." |
| Forma de trato | "¿Cómo conviene tratar a las personas en estas conversaciones: de usted, de tú o de vos?" |
| Datos que no se guardan | "¿Hay algún dato que la empresa prefiera que no quede escrito?" |
| Datos comerciales | "Los precios, las condiciones comerciales y los datos de otras empresas, ¿se pueden anotar o se dejan afuera?" |

- Antes de preguntar por los datos, contar en una frase lo que nunca se guarda: datos personales, claves y datos bancarios.
- Quien aprueba puede ser la misma persona que conduce.
- Si no se define un período de revisión, son 12 meses.
- Se escribe en "Cómo se organiza el relevamiento", en `empresa/contexto.md`.
- Desde el cierre de esta etapa se usa la forma de trato elegida.

## Etapa 4. Qué hay ya escrito

Preguntar: "¿Hay algo ya escrito sobre cómo se trabaja? Sirve cualquier cosa: instructivos, listas de tareas, organigramas o notas."

Si no hay nada, anotarlo en el registro de la sesión y cerrar la etapa. El relevamiento sigue con preguntas.

Si hay material, recibir cada archivo con los pasos de "Archivos recibidos", en `metodo/control-documental.md`. Va a `empresa/insumos/` y se anota en su `catalogo.md`. Después:

| Material | Qué se hace en esta etapa |
|---|---|
| Un documento sobre cómo se trabaja | Leerlo entero. |
| Una conversación entre otras personas | Solo catalogarla, con `se lee en otra sesión`. No se lee de paso. |
| Un audio sin transcripción | Solo catalogarlo, con `sin transcribir`, y pedir la transcripción. Su contenido nunca se adivina. |
| Un archivo que no se puede abrir | Catalogarlo con `no revisado por el agente`. |

Con cada documento leído:

1. Contar en dos o tres frases qué es, de cuándo es y qué temas trata.
2. Preguntar: "¿Leí bien?" La persona confirma la lectura, no los hechos.
3. Tomar lo que nombra el documento como propuestas para las etapas 5 a 7: áreas, sistemas, personas y procesos.

- Lo que se escriba a partir del material lleva su fuente y `A CONFIRMAR con <quién>`. La fuente es el nombre del archivo en `empresa/insumos/`. `<quién>` es la persona que hace ese trabajo; si no se sabe, el responsable del programa.
- El material puede estar desactualizado. Sirve para preguntar mejor y nunca cuenta como validado.
- Si el material no coincide con lo que contó el responsable del programa, preguntar cuál de las dos cosas pasa hoy y anotar su respuesta. El material no se corrige.
- Si la persona promete traer material más adelante, anotarlo en el registro de la sesión, en "Documentos pendientes", y cerrar la etapa. Se recibe en otra conversación, con estos mismos pasos.

## Etapa 5. Áreas y sistemas

| Qué se busca | Pregunta de guía |
|---|---|
| Áreas | "¿En qué áreas o sectores se organiza el trabajo?" |
| Qué hace cada una | "¿De qué se ocupa `<área>`?" |
| Sistemas y herramientas | "¿Qué sistemas, programas o herramientas se usan para trabajar? También cuentan las hojas de cálculo, los cuadernos y los mensajes." |
| Uso | "¿Para qué se usa `<sistema>` y quiénes lo usan?" |

Cada área lleva tres letras, que después forman los códigos de sus documentos:

1. Proponer tres letras mayúsculas tomadas del nombre del área, sin acentos ni eñes.
2. Comprobar que no se repiten y que no son `GEN`, que queda para lo que es de toda la empresa.
3. Confirmarlas con la persona. Después no se cambian.

- La carpeta del área es su nombre en minúsculas, con guiones y sin acentos.
- Si la empresa no tiene áreas, todo va en `general`, con las letras `GEN`.
- De los sistemas nunca se anotan usuarios ni claves.
- Se escribe en "Áreas" y en "Sistemas y herramientas", en `empresa/contexto.md`.

## Etapa 6. Personas

Recorrer las áreas de a una:

| Qué se busca | Pregunta de guía |
|---|---|
| Quiénes | "¿Quiénes trabajan en `<área>`? Con el nombre de pila alcanza." |
| Qué hace cada persona | "¿De qué se ocupa `<nombre>`?" |
| Otras áreas | "¿Trabaja también en otra área?" |
| Sistemas | "¿Qué sistemas o herramientas usa?" |

Al escribir:

1. Crear una hoja por persona, copiando `plantillas/persona.md` a `empresa/personas/<nombre>.md`.
2. Crear también la hoja del responsable del programa y la de quien aprueba.
3. En "Rol en el relevamiento" va `participante`, salvo en esas dos hojas, que llevan su rol.
4. En "Origen de la hoja" va que los datos los dio el responsable del programa, con la fecha.
5. En "De dónde sale cada dato", lo que describe el trabajo de otra persona lleva `A CONFIRMAR con <esa persona>`.
6. En la hoja del responsable del programa, anotar en "Documentos prometidos" el material que prometió en la etapa 4.

- Si dos personas comparten el nombre de pila, el archivo lleva también el área, como indica `empresa/README.md`.
- Si son muchas personas, empezar por un área o por las personas que conviene escuchar primero. Lo que falta se anota como `PENDIENTE: preguntar a <quién>` en "Pendientes" del registro de la sesión.

## Etapa 7. Mapa de procesos

Un proceso es un trabajo que empieza con algo que lo pone en marcha y termina con algo hecho. Para separarlos:

- Si dos tramos tienen dueños distintos o resultados distintos, son dos procesos.
- Un paso suelto no es un proceso. Un área entera, tampoco.
- El nombre es el que usa la empresa, corto y sin siglas.

Se recorren los tres grupos en este orden:

| Grupo | Preguntas de guía |
|---|---|
| Operación | "Cuando un cliente pide algo, ¿qué es lo primero que pasa?" Después, "¿Y qué pasa después?", hasta llegar al cobro. Al final, "¿Cuándo se da por terminado?" |
| Apoyo | "¿Qué otros trabajos hacen falta para que eso funcione? Por ejemplo, comprar, pagar, contratar personas o mantener los equipos." |
| Conducción | "¿Cómo se decide hacia dónde va la empresa?" y "¿Quién fija los precios, los objetivos o las prioridades, y cada cuánto?" |

De cada proceso se pregunta:

| Qué se busca | Pregunta de guía |
|---|---|
| Dueño | "¿Quién responde por que esto salga bien?" |
| Participantes | "¿Quiénes más intervienen?" |
| Prioridad | "¿Conviene dejarlo escrito primero, después o al final?" |

- El dueño es un rol del relevamiento: vale lo que define el responsable del programa. Si no lo sabe, va `A DEFINIR`.
- Los participantes y lo que hace cada uno son de segunda mano: llevan `A CONFIRMAR con <esa persona>`.
- La prioridad se anota como `P1`, `P2` o `P3`.
- Los procesos que salen del material de la etapa 4 se proponen de a uno. Si la persona no los reconoce, quedan con `A CONFIRMAR con <quién>`.
- Si aparece un área que no figura en `empresa/contexto.md`, agregarla ahí con sus tres letras, como en la etapa 5, antes de asignar códigos.

Al escribir:

1. Crear `empresa/mapa-de-procesos.md` copiando `plantillas/mapa-de-procesos.md`. Poner al día la fila `MP-GEN-001` de la lista maestra: estado `en curso` y "Elaboró".
2. Asignar el código de cada proceso con los pasos de "Cómo se asigna un código". Su fila de la lista maestra queda con estado `pendiente`, versión `0` y ubicación `—`, porque la ficha todavía no existe.
3. Agregar la fila de cada proceso en su grupo del mapa, con estado `pendiente` y ficha `—`.
4. En la hoja de cada persona nombrada, agregar el proceso en "Procesos en los que participa". "Su parte" lleva `A CONFIRMAR con <esa persona>`. Si la persona no tiene hoja, crearla.
5. En la hoja de cada dueño, anotar en "Rol en el relevamiento" de qué proceso es dueño.

## Etapa 8. Plan de relevamiento y preguntas

El plan dice por qué procesos se empieza, por qué, y a quién se escucha en cada uno.

1. Nombrar los procesos `P1` y preguntar por cuál conviene empezar y por qué. Si la persona duda, ofrecer criterios: lo que depende de una sola persona, lo que más errores o esperas genera, lo que se hace más seguido, lo que tiene que aprender alguien nuevo.
2. Anotar el criterio en la fila "Qué se releva primero" de `empresa/contexto.md`. Si cambia una prioridad, corregirla en el mapa.
3. De cada proceso `P1`, preguntar si hay que escuchar a alguien más que al dueño y a los participantes ya anotados.
4. Preguntar si alguna de esas personas no va a poder sentarse a conversar.

Preguntas preparadas, por cada persona:

1. Buscar en `empresa/` cada `PENDIENTE: preguntar a` y cada `A CONFIRMAR con` que la nombra.
2. Convertir cada uno en una pregunta en palabras simples.
3. Preguntar al responsable del programa si quiere sumar alguna pregunta para esa persona.
4. Escribirlas en "Preguntas preparadas" de su hoja, agrupadas por proceso, cada una con el lugar de donde sale.

Lista para enviar: ofrecerla para las personas que no van a sentarse a conversar.

1. Preguntar: "¿Preparo las preguntas en un mensaje listo para enviar?"
2. Si acepta, mostrar en la conversación un mensaje por persona: una frase que diga para qué es y las preguntas numeradas, en palabras simples.
3. Anotar en la hoja de esa persona, junto a cada pregunta, que se envió y en qué fecha.
4. Las respuestas escritas que vuelvan se reciben en otra conversación, como material: van a `empresa/insumos/` y llevan `A CONFIRMAR con <esa persona>`.

## Cierre de cada sesión

Se hace siempre que una sesión termina, esté o no completo el arranque:

1. Sumar una fila al historial de cada documento controlado que la sesión cambió, con la versión `0`, la fecha, qué se agregó y quién lo contó.
2. Completar "Cómo terminó" en el registro de la sesión, con su línea de subida.
3. Hacer el guardado final y la subida, como indica "Al cerrar la sesión" en `metodo/guardado.md`.
4. Agradecer el tiempo. Si quedan etapas, decir que la próxima vez alcanza con abrir la carpeta y saludar.

## Cierre del arranque

Se hace una sola vez, al cerrar la etapa 8 y antes del cierre de la sesión:

1. Pasar a `borrador` el contexto y el mapa de procesos, y también el glosario si existe. El estado se cambia en el bloque de control y en la lista maestra.
2. Resumir todo lo que quedó escrito, con palabras simples y con cantidades: áreas, personas, procesos y preguntas preparadas. Decir cuántas cosas quedaron por confirmar o por preguntar.
3. Decir qué sigue. Mirar la tabla de modos de `AGENTS.md` y nombrar solo lo que ya tiene fila. No prometer lo que todavía no está disponible.
4. Si no hay servidor, como lo define "Cuándo hay servidor" en `metodo/guardado.md`, decir una sola vez la frase de "Sin servidor". Anotar en el registro de la sesión que se dijo.

## Guardado en este modo

Los mensajes siguen el formato de `metodo/guardado.md`:

| Momento | Mensaje |
|---|---|
| Cierre de cada etapa | `docs(empresa): arranque - etapa <número> con <nombre>` |
| Etapa que quedó a medias | `docs(empresa): arranque - etapa <número> con <nombre>` |
| Cierre de la sesión | `docs(empresa): arranque - cierre de sesión con <nombre>` |

## Qué decir

| Situación | Frase |
|---|---|
| Pedir el nombre | "Hola. Antes de empezar, ¿con quién estoy hablando? Con el nombre de pila alcanza." |
| Presentación | "Este trabajo sirve para dejar por escrito cómo se trabaja en la empresa. Para prepararlo hay ocho etapas cortas. Esta presentación es la primera. Después vienen la empresa, cómo nos organizamos, lo que ya hay escrito, las áreas, las personas, la lista de trabajos y las preguntas para cada persona. En total llevan alrededor de dos horas y se pueden repartir en varias conversaciones. Se puede cortar al terminar cualquier etapa." |
| No es quien conduce | "Esta primera parte se hace con la persona que va a conducir el trabajo. Cuando esa persona pueda, alcanza con que abra esta carpeta y salude." |
| Avance | "Etapa `<número>` de 8 lista. ¿Seguimos con la siguiente o cortamos aquí?" |
| Ofrecer cortar | "Ya llevamos un buen rato. Lo conversado quedó guardado. ¿Seguimos, o cortamos aquí y continuamos otro día?" |
| La persona no sabe algo | "No hay problema. Lo anoto para preguntárselo a quien corresponda. ¿A quién habría que consultarle?" |
| Retomar | "La vez pasada quedaron listas las etapas 1 a `<número>`. Hoy sigue esta: `<nombre de la etapa>`." |
| Habla otra persona | "La preparación de este trabajo todavía no terminó. `<nombre del responsable del programa>` va a avisar cuándo se puede empezar." |
| Sin servidor | "Un aviso: todo lo que conversamos quedó guardado solo en esta computadora. Quien preparó esta carpeta puede sumar una copia en otro lugar." |
| Cierre del arranque | "Con esto quedó lista la preparación." Después, el resumen y lo que sigue. |

En la conversación se usan palabras simples, como indica la regla 8 de `metodo/reglas.md`:

| En lugar de | Decir |
|---|---|
| "contexto de la empresa" | "la descripción de la empresa" |
| "mapa de procesos", "proceso" | "la lista de los trabajos de la empresa", "trabajo" o "tarea" |
| "dueño de proceso" | "quien responde por ese trabajo" |
| "responsable del programa" | "quien conduce este trabajo" |
| "lista de arranque" | "lo que falta preparar" |

Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
