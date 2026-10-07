# Relación con la norma IRAM-ISO 9001:2015

Esta tabla dice en qué lugar de este repositorio vive cada cláusula de la norma, cuáles se cubren solo en parte y cuáles no se cubren.

**Esta estructura no certifica nada por sí sola.** Ordenar la documentación con esta plantilla no equivale a cumplir la norma. La certificación la decide un organismo de certificación, después de una auditoría.

Lo escrito describe el trabajo como lo cuentan y confirman quienes lo hacen. Los documentos y las pantallas que aparecen se enlazan como evidencia. No reemplaza una observación directa ni una auditoría.

ISO publicó ISO 9001:2026 el 2026-09-16. Esta tabla sigue la edición 2015, que es la que IRAM adoptó. Al 2026-10-07 no se comprobó si IRAM publicó la adopción de la edición nueva. Contra qué edición se audita durante la transición lo define el organismo de certificación.

## Cómo leer la tabla

| Cobertura | Qué significa |
|---|---|
| Sí | La plantilla tiene un lugar y reglas para esto. |
| En parte | La plantilla registra una parte. La fila dice qué falta. |
| No | La plantilla no lo cubre. |

- Aquí figuran solo los números y los títulos de las cláusulas. El texto de la norma no se reproduce: hay que leerlo en la norma publicada.
- Los números y los títulos se comprobaron el 2026-10-05 contra el índice de la norma IRAM-ISO 9001:2015, tercera edición, que es una adopción idéntica de ISO 9001:2015.
- Las rutas que empiezan con `empresa/` son lugares del clon de una empresa. Su estructura está en `empresa/README.md`.

## Cláusulas 4 a 10

| Cláusula | Título | Cobertura | Dónde vive o qué falta |
|---|---|---|---|
| 4.1 | Comprensión de la organización y de su contexto | En parte | `empresa/contexto.md` describe la empresa: qué hace, su tamaño, dónde funciona, por qué encara el relevamiento y qué espera de él. Se completa en `metodo/arranque.md`, con el molde `plantillas/contexto-de-la-empresa.md`. No hace un análisis del contexto ni su seguimiento. No determina si el cambio climático es un tema pertinente, como pide la enmienda ISO 9001:2015/Amd 1:2024; no se comprobó si IRAM la adoptó. |
| 4.2 | Comprensión de las necesidades y expectativas de las partes interesadas | En parte | `empresa/contexto.md` registra qué tipo de clientes tiene la empresa. Cada ficha de proceso anota a quién le llega su resultado, y cada ficha de cambio qué terceros participan (molde `plantillas/ficha-de-cambio.md`). No identifica de forma sistemática las partes interesadas ni sus requisitos. No determina si el cambio climático importa para ellas, como pide la enmienda 1:2024. |
| 4.3 | Determinación del alcance del sistema de gestión de la calidad | En parte | `empresa/mapa-de-procesos.md` muestra qué procesos abarca la documentación. No hay una declaración de alcance del sistema. |
| 4.4 | Sistema de gestión de la calidad y sus procesos | En parte | El mapa (`plantillas/mapa-de-procesos.md`) y las fichas (`plantillas/ficha-de-proceso.md`) dejan escrito qué procesos hay, quién responde por cada uno, sus pasos, lo que necesitan, lo que producen y lo que puede salir mal. El mapa se arma en `metodo/arranque.md` y cada ficha se completa en `metodo/entrevista.md`. La ficha anota a quién le llega el resultado y, cuando se sabe, qué proceso del mapa lo sigue. No registra la secuencia ni la interacción entre procesos de forma sistemática: el mapa no dibuja qué proceso recibe lo que otro produce. No fija criterios ni indicadores por proceso. Operar y mejorar esos procesos es tarea de la empresa. |
| 5.1 | Liderazgo y compromiso | No | La plantilla no lo cubre. Solo registra quién aprueba los documentos, en `empresa/contexto.md`. |
| 5.2 | Política | No | La plantilla no incluye una política de la calidad. |
| 5.3 | Roles, responsabilidades y autoridades en la organización | En parte | Los roles del relevamiento están en `metodo/reglas.md`. Se asignan en `metodo/arranque.md` y quedan en `empresa/contexto.md` y en cada hoja de `empresa/personas/` (molde `plantillas/persona.md`). Cada ficha dice quién es el dueño, quién participa y quién hace cada paso. No asigna las responsabilidades del sistema de gestión. |
| 6.1 | Acciones para abordar riesgos y oportunidades | En parte | Cada ficha anota "Qué puede salir mal" y "Problemas e ideas", y cada ficha de cambio anota qué puede salir mal con ese cambio. La plantilla no planifica acciones ni evalúa su resultado. |
| 6.2 | Objetivos de la calidad y planificación para lograrlos | No | La plantilla no define objetivos. |
| 6.3 | Planificación de los cambios | En parte | Un cambio que altera cómo se trabaja se sigue en `metodo/cambio-en-curso.md`, con una ficha por cambio en `empresa/cambios/` (molde `plantillas/ficha-de-cambio.md`): qué cambia y por qué, quién lo lleva, qué procesos afecta, qué se decidió, qué falta responder y qué puede salir mal. Decidir el cambio y llevarlo adelante es tarea de la empresa. La plantilla no planifica los cambios del sistema de gestión. |
| 7.1 | Recursos | En parte | Registra las personas de cada área (7.1.2), en `empresa/contexto.md` y en las hojas de `empresa/personas/`; los lugares y los sistemas en uso (7.1.3), en `empresa/contexto.md` y en la columna "Con qué" de cada ficha; y lo que sabe cada persona (7.1.6), en las fichas, los instructivos y el glosario. Lo que ya estaba en conversaciones y notas se recoge en `metodo/material-de-terceros.md`. No cubre el ambiente para la operación (7.1.4) ni los recursos de seguimiento y medición (7.1.5). |
| 7.2 | Competencia | No | La plantilla no lo cubre. Los instructivos pueden servir de apoyo para capacitar. |
| 7.3 | Toma de conciencia | No | La plantilla no lo cubre. |
| 7.4 | Comunicación | En parte | Cada ficha registra qué pone en marcha el trabajo y por qué medio llega el aviso, a quién le llega el resultado y quién avisa cuando algo sale mal (molde `plantillas/ficha-de-proceso.md`, preguntas en `plantillas/banco-de-preguntas.md`). No determina qué se comunica sobre el sistema de gestión, cuándo, a quién ni quién lo comunica. |
| 7.5 | Información documentada | En parte | Es el centro de `metodo/control-documental.md`. El detalle y lo que falta están en las tres filas siguientes. |
| 7.5.1 | Generalidades | En parte | Cubre lo que la empresa decide documentar sobre cómo trabaja (7.5.1 b): contexto, mapa, fichas, instructivos y glosario. Los tres tipos de archivo están en `metodo/control-documental.md`. La lista de los documentos controlados y de los registros que se guardan está en `empresa/lista-maestra.md` (molde `plantillas/lista-maestra.md`). No cubre la información documentada que la norma exige (7.5.1 a): alcance, política, objetivos, evidencia de competencia, auditorías, revisión por la dirección ni no conformidades. Los formularios y los documentos de afuera que la empresa usa se catalogan, pero todavía no se controlan. |
| 7.5.2 | Creación y actualización | En parte | Código y bloque de control, en `metodo/control-documental.md`. Un molde por tipo de documento, en `plantillas/`. Validación del dueño, lectura del texto antes de aprobar y aprobación, en `metodo/revision-y-aprobacion.md`. Lo que falta: la evidencia de la aprobación es el registro de la sesión con las palabras de quien aprobó, sin firma, y la identidad es un nombre de pila que nadie comprueba. Que el documento sirva a quien lo usa se comprueba solo si alguien acepta la prueba de uso, que es un ofrecimiento. |
| 7.5.3 | Control de la información documentada | En parte | Estados, versiones, historial, cambios propuestos, revisión periódica, documentos obsoletos y tabla de registros, en `metodo/control-documental.md`. Registro de cada conversación y catálogo de los archivos recibidos, con los moldes `plantillas/registro-de-sesion.md` y `plantillas/catalogo-de-archivos.md`. Guardado con historial de cambios, en `metodo/guardado.md`. Cuidado de los datos, en la regla 7 de `metodo/reglas.md`. Quién puede entrar a la carpeta depende de dónde la guarde la empresa. Lo que falta: cómo llega la versión aprobada a quien la usa; al aprobar, el agente anota a quién hay que avisar y dónde encontrará la versión oficial, y avisar es tarea de quien aprueba. Tampoco cubre el retiro de las copias impresas que quedaron viejas, la copia de resguardo cuando no hay servidor, los formularios ni los documentos de afuera en uso, que se catalogan sin controlar su versión, ni la disposición final de los registros: lo escrito se conserva siempre y la lista maestra anota solo un plazo mínimo. |
| 8 | Operación | En parte | Las fichas de `empresa/procesos/` y los instructivos de `empresa/instructivos/` describen cómo se opera hoy (moldes `plantillas/ficha-de-proceso.md` y `plantillas/instructivo.md`). Se escriben en `metodo/entrevista.md`. Los cambios en la forma de operar se siguen en `metodo/cambio-en-curso.md`. La plantilla no agrega controles ni dice cómo hay que operar. |
| 9.1 | Seguimiento, medición, análisis y evaluación | En parte | Cada ficha registra, en "Cómo nos damos cuenta de que anda bien", si hoy se mide algo, quién mira ese dato y cada cuánto. La plantilla no mide ni analiza, y no releva la satisfacción del cliente (9.1.2). Un diagnóstico de lo relevado está previsto para una parte posterior. |
| 9.2 | Auditoría interna | No | La plantilla no lo cubre. |
| 9.3 | Revisión por la dirección | No | La plantilla no lo cubre. La revisión periódica de los documentos es otra cosa. El apoyo a la dirección está previsto para una parte posterior. |
| 10.1 | Generalidades | En parte | Cada ficha junta problemas e ideas de mejora. La plantilla no decide qué mejoras se hacen ni las sigue. |
| 10.2 | No conformidad y acción correctiva | En parte | Cada ficha registra cómo se reacciona hoy cuando algo sale mal y quién autoriza las excepciones, en "Excepciones" y en "Qué puede salir mal". No registra cada no conformidad, ni sus causas, ni las acciones correctivas ni su eficacia. |
| 10.3 | Mejora continua | No | La plantilla no lo cubre. |

## Qué decir si alguien pregunta

| Pregunta | Respuesta |
|---|---|
| Si con esto la empresa cumple la norma | "Con esto solo, no. Esto deja ordenado y por escrito cómo se trabaja, que es una parte de lo que pide la norma." |
| Si con esto la empresa certifica | "No. La certificación la decide un organismo de certificación, después de una auditoría." |

En la conversación no se usan los números ni los títulos de las cláusulas, salvo que la persona los use primero. Es la regla 8 de `metodo/reglas.md`.

## Mantenimiento de esta tabla

- Cuando la plantilla suma un modo o un molde, revisar las filas que cambian.
- No nombrar archivos que todavía no existen.
- Esta tabla corresponde a la edición 2015. Si la empresa trabaja con otra edición, comprobar los números y los títulos contra esa edición publicada.
- Comprobar también las enmiendas publicadas de la edición que sigue la tabla, y anotar en las filas que tocan si la plantilla las cubre.
- Cuando IRAM adopte la edición 2026, decidir si la tabla se rehace contra esa edición. Hace falta tener su texto.
