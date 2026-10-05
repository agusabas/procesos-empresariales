# Relación con la norma IRAM-ISO 9001:2015

Esta tabla dice en qué lugar de este repositorio vive cada cláusula de la norma, cuáles se cubren solo en parte y cuáles no se cubren.

**Esta estructura no certifica nada por sí sola.** Ordenar la documentación con esta plantilla no equivale a cumplir la norma. La certificación la decide un organismo de certificación, después de una auditoría.

## Cómo leer la tabla

| Cobertura | Qué significa |
|---|---|
| Sí | La plantilla tiene un lugar y reglas para esto. |
| En parte | La plantilla registra una parte. La fila dice qué falta. |
| No | La plantilla no lo cubre. |
| Previsto | Está pensado para una parte posterior de la plantilla. |

- Aquí figuran solo los números y los títulos de las cláusulas. El texto de la norma no se reproduce: hay que leerlo en la norma publicada.
- Los números y los títulos se comprobaron el 2026-10-05 contra el índice de la norma IRAM-ISO 9001:2015, tercera edición, que es una adopción idéntica de ISO 9001:2015.
- Las rutas que empiezan con `empresa/` son lugares del clon de una empresa. Su estructura está en `empresa/README.md`.

## Cláusulas 4 a 10

| Cláusula | Título | Cobertura | Dónde vive o qué falta |
|---|---|---|---|
| 4.1 | Comprensión de la organización y de su contexto | En parte | `empresa/contexto.md` describe la empresa: qué hace, su tamaño, dónde funciona, por qué encara el relevamiento y qué espera de él. Se completa en `metodo/arranque.md`, con el molde `plantillas/contexto-de-la-empresa.md`. No hace un análisis del contexto ni su seguimiento. |
| 4.2 | Comprensión de las necesidades y expectativas de las partes interesadas | No | La plantilla no identifica partes interesadas ni lo que esperan. `empresa/contexto.md` anota solo qué espera la empresa del relevamiento. |
| 4.3 | Determinación del alcance del sistema de gestión de la calidad | En parte | `empresa/mapa-de-procesos.md` muestra qué procesos abarca la documentación. No hay una declaración de alcance del sistema. |
| 4.4 | Sistema de gestión de la calidad y sus procesos | En parte | El mapa (`plantillas/mapa-de-procesos.md`) y las fichas (`plantillas/ficha-de-proceso.md`) dejan escrito qué procesos hay, quién responde por cada uno, sus pasos, lo que necesitan, lo que producen y lo que puede salir mal. El mapa se arma en `metodo/arranque.md` y cada ficha se completa en `metodo/entrevista.md`. Operar y mejorar esos procesos es tarea de la empresa. |
| 5.1 | Liderazgo y compromiso | No | La plantilla no lo cubre. Solo registra quién aprueba los documentos, en `empresa/contexto.md`. |
| 5.2 | Política | No | La plantilla no incluye una política de la calidad. |
| 5.3 | Roles, responsabilidades y autoridades en la organización | En parte | Los roles del relevamiento están en `metodo/reglas.md`. Se asignan en `metodo/arranque.md` y quedan en `empresa/contexto.md` y en cada hoja de `empresa/personas/` (molde `plantillas/persona.md`). Cada ficha dice quién es el dueño, quién participa y quién hace cada paso. No asigna las responsabilidades del sistema de gestión. |
| 6.1 | Acciones para abordar riesgos y oportunidades | En parte | Cada ficha anota "Qué puede salir mal" y "Problemas e ideas". La plantilla no planifica acciones ni evalúa su resultado. |
| 6.2 | Objetivos de la calidad y planificación para lograrlos | No | La plantilla no define objetivos. |
| 6.3 | Planificación de los cambios | Previsto | El lugar ya está definido en `empresa/README.md`: la carpeta `empresa/cambios/`. Las instrucciones para llevar un cambio llegan en una parte posterior. |
| 7.1 | Recursos | En parte | Solo los conocimientos de la organización: las fichas, los instructivos y el glosario dejan escrito lo que hoy sabe cada persona. Lo que ya estaba en conversaciones y notas se recoge en `metodo/material-de-terceros.md`. El resto de los recursos no se cubre. |
| 7.2 | Competencia | No | La plantilla no lo cubre. Los instructivos pueden servir de apoyo para capacitar. |
| 7.3 | Toma de conciencia | No | La plantilla no lo cubre. |
| 7.4 | Comunicación | No | La plantilla no lo cubre. |
| 7.5 | Información documentada | En parte | Es el centro de `metodo/control-documental.md`. El detalle y lo que falta están en las tres filas siguientes. |
| 7.5.1 | Generalidades | Sí | Los tres tipos de archivo, en `metodo/control-documental.md`. La lista de todo lo que se guarda, en `empresa/lista-maestra.md` (molde `plantillas/lista-maestra.md`). |
| 7.5.2 | Creación y actualización | Sí | Código y bloque de control, en `metodo/control-documental.md`. Un molde por tipo de documento, en `plantillas/`. Revisión y aprobación, en `metodo/revision-y-aprobacion.md`. |
| 7.5.3 | Control de la información documentada | En parte | Estados, versiones, historial, cambios propuestos, revisión periódica, documentos obsoletos y tabla de registros, en `metodo/control-documental.md`. Registro de cada conversación y catálogo de los archivos recibidos, con los moldes `plantillas/registro-de-sesion.md` y `plantillas/catalogo-de-archivos.md`. Guardado con historial de cambios, en `metodo/guardado.md`. Cuidado de los datos, en la regla 7 de `metodo/reglas.md`. Quién puede entrar a la carpeta depende de dónde la guarde la empresa. |
| 8 | Operación | En parte | Las fichas de `empresa/procesos/` y los instructivos de `empresa/instructivos/` describen cómo se opera hoy (moldes `plantillas/ficha-de-proceso.md` y `plantillas/instructivo.md`). Se escriben en `metodo/entrevista.md`. La plantilla no agrega controles ni dice cómo hay que operar. |
| 9.1 | Seguimiento, medición, análisis y evaluación | En parte | Cada ficha anota "Cómo nos damos cuenta de que anda bien". La plantilla no mide ni analiza. Un diagnóstico de lo relevado está previsto para una parte posterior. |
| 9.2 | Auditoría interna | No | La plantilla no lo cubre. |
| 9.3 | Revisión por la dirección | No | La plantilla no lo cubre. La revisión periódica de los documentos es otra cosa. El apoyo a la dirección está previsto para una parte posterior. |
| 10.1 | Generalidades | En parte | Cada ficha junta problemas e ideas de mejora. La plantilla no decide qué mejoras se hacen ni las sigue. |
| 10.2 | No conformidad y acción correctiva | No | La plantilla no lo cubre. Los problemas anotados en las fichas son hechos, no un registro de no conformidades. |
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
