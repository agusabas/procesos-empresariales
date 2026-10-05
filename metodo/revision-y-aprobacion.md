# Modo: revisión y aprobación

En este modo se repasa lo relevado, se valida, se aprueba, se ordena la lista maestra, se hace la revisión periódica y se dan de baja documentos. Es el único modo que puede dejar un documento como `validado`, `vigente` u `obsoleto`, y el único que escribe en `main`.

Antes de empezar, leer completo `metodo/control-documental.md`. Este archivo usa su vocabulario.

## En una mirada

| Etapa | Qué se hace | Con quién |
|---|---|---|
| 1. Qué hay pendiente | Avisar las revisiones que vencen y contar lo que espera | Responsable del programa o quien aprueba |
| 2. Qué cambió | Repasar lo nuevo desde la última revisión | Responsable del programa |
| 3. Validar | Pasar a `validado` lo que confirmó el dueño del proceso | Responsable del programa |
| 4. Aprobar | Pasar a `vigente`, con las cuatro cosas juntas | Quien aprueba |
| 5. Conciliar | Poner la lista maestra al día con los documentos | Responsable del programa |
| 6. Revisión periódica | Volver a mirar los documentos que vencen | Responsable del programa y quien aprueba |
| 7. Dar de baja | Pasar a `obsoleto` lo que ya no se usa | Quien aprueba o el responsable del programa |
| 8. Cierre | Resumen final, paso a `main` y subida | Quien esté en la conversación |

- Las etapas se hacen en este orden. Una etapa sin nada pendiente se saltea sin comentarla.
- Si la persona pide empezar por otra etapa, se empieza por esa.
- Cada etapa se cierra igual: resumen de lo entendido, pregunta de confirmación y guardado. Es la regla 9 de `metodo/reglas.md`.

## Reglas de este modo

1. Este modo se abre solo con el responsable del programa o con quien aprueba. Quiénes son figura en `empresa/contexto.md`.
2. Todo se escribe en `borradores`. `main` se toca solo en la etapa 8, como indica "Pasar a `main` lo revisado". Es la única excepción a la regla de no guardar en `main`.
3. Un documento pasa a `vigente` solo con la palabra explícita de quien aprueba, dicha por esa persona en esta conversación.
4. Una aprobación que cuenta otra persona es de segunda mano. No se aprueba: se anota en el registro de la sesión `A CONFIRMAR con <quien aprueba>` y se espera a que esa persona lo diga.
5. Si la misma persona es responsable del programa y quien aprueba, su palabra alcanza. La pregunta de aprobación se hace igual.
6. Confirmar un resumen no es aprobar. La aprobación se pregunta aparte, en un mensaje propio y documento por documento.
7. Al aprobar se hacen las cuatro cosas juntas, o no se aprueba.
8. No se cambia lo que contó otra persona. El responsable del programa corrige cómo quedó anotado. Si no está de acuerdo con el contenido, su versión se registra en un bloque `CONFLICTO`.
9. Los registros cerrados de `sesiones/`, `insumos/` y `adjuntos/` no se editan.
10. La conversación es llana también en este modo. No se dice "vigente", "validado", "lista maestra" ni "rama": se usan las palabras de la regla 8 de `metodo/reglas.md`.

## Registro de la sesión

Al empezar, crear el registro en `empresa/sesiones/AAAA-MM-DD-<quien>-revision.md`. Anotar en él, etapa por etapa:

- Qué se repasó, qué quedó aceptado y qué no.
- Qué se validó.
- Qué se aprobó, con las palabras textuales de quien aprobó.
- Qué se dio de baja y por qué.
- Qué quedó pendiente y para quién.
- La línea de subida que indica `metodo/guardado.md`.

Una vez cerrado, el registro no se edita.

## Etapa 1. Qué hay pendiente

Reunir en silencio:

| Qué buscar | Dónde |
|---|---|
| Documentos con la revisión vencida o por vencer | Columna "Próxima revisión" de `empresa/lista-maestra.md` |
| Lo que cambió y todavía no se repasó | `git diff --stat main borradores -- empresa/` |
| Documentos en `borrador` y documentos `validado` | Columna "Estado" de la lista maestra |
| Documentos `vigente` con cambios propuestos | Sección "Cambios propuestos (sin aprobar)" con filas |
| Marcadores abiertos | `PENDIENTE`, `CONFLICTO` y `A CONFIRMAR` en los archivos de `empresa/` |
| Códigos duplicados | Columna "Observaciones" de la lista maestra |

Después:

1. Decir primero el aviso de revisiones, como indica "Revisión periódica" en `metodo/control-documental.md`.
2. Contar en dos o tres frases llanas lo que espera: cuántos documentos tienen cosas nuevas, cuántos están listos para confirmar y cuántos esperan aprobación.
3. Preguntar por dónde empezar. Es la pregunta de confirmación de esta etapa.

Si no hay nada pendiente, decirlo y pasar a la etapa 8.

## Etapa 2. Qué cambió

1. Agrupar por proceso los archivos que cambiaron.
2. Tomar un documento por vez. Leer lo que cambió con `git diff main borradores -- <ruta>` y contarlo en dos o tres frases llanas: qué se agregó, quién lo contó y qué quedó abierto.
3. Preguntar: "¿Está bien anotado?"
4. Seguir según la respuesta:

| Respuesta | Qué se hace |
|---|---|
| Está bien | El documento queda aceptado. Pasa a `main` en la etapa 8. |
| Hay un error de anotación | Corregirlo en `borradores` y volver a preguntar. |
| No coincide con lo que contó otra persona | No cambiar lo anotado. Registrar su versión en un bloque `CONFLICTO`. |
| Prefiere mirarlo otro día | No queda aceptado. Sigue solo en `borradores`. |

5. Anotar en el registro de la sesión qué quedó aceptado y qué no.
6. Cerrar la etapa: resumir qué quedó aceptado y qué no, preguntar si es correcto y guardar.

Los registros de sesión que respaldan un documento aceptado pasan junto con él.

## Etapa 3. Validar

Para cada documento en `borrador`, comprobar las tres condiciones:

| Condición | Cómo se comprueba |
|---|---|
| El dueño del proceso confirmó directamente que es así | Hay un registro en `empresa/sesiones/` donde lo confirma. |
| Ningún `PENDIENTE` ni `CONFLICTO` abierto cambia el sentido | Buscar los marcadores en el documento. |
| Nada que cambie el sentido sigue `A CONFIRMAR` | Buscar el marcador en el documento. |

Si se cumplen las tres:

1. Contar al responsable del programa qué documento queda confirmado y qué marcadores menores siguen abiertos.
2. Preguntar si está de acuerdo.
3. Escribir el estado `validado` en el bloque de control, en la lista maestra y en el mapa de procesos. Escribir en "Revisó" el nombre de pila del dueño del proceso. Sumar una fila al historial.

Si falta alguna:

1. Decir con palabras simples qué falta y a quién hay que preguntarle.
2. Dejar preparada la pregunta en la hoja de esa persona, en `empresa/personas/<nombre>.md`.
3. El documento sigue en `borrador`.

Los documentos de toda la empresa no tienen dueño de proceso. Los confirma el responsable del programa, en esta conversación.

Cerrar la etapa: resumir qué quedó confirmado y qué sigue esperando, preguntar si es correcto y guardar.

## Etapa 4. Aprobar

Esta etapa necesita a quien aprueba en la conversación. Si no está:

1. Decirlo con la frase de "Falta quien aprueba".
2. Ofrecer un resumen listo para enviar, con los documentos que esperan su palabra.
3. Pasar a la etapa siguiente.

Con quien aprueba, se trabaja cada documento `validado` y cada documento `vigente` con cambios propuestos que el dueño del proceso confirmó. Un documento por vez:

1. Resumir en llano qué documento es, qué describe, qué cambia respecto de la versión anterior y qué marcadores menores siguen abiertos.
2. Preguntar si el resumen es correcto.
3. Preguntar la aprobación, sola en un mensaje: "¿Queda aprobado como versión oficial?"
4. Tomar como aprobación solo una respuesta clara, como "sí, queda aprobado". Una duda, un silencio o un "después lo veo" no aprueban.
5. Hacer las cuatro cosas juntas, con el detalle de "Aprobar: cuatro cosas juntas" en `metodo/control-documental.md`:

   | N.º | Qué se hace |
   |---|---|
   | 1 | La versión suma 1. |
   | 2 | Se agrega la fila de esta aprobación al historial. |
   | 3 | La próxima revisión pasa a ser la fecha de hoy más el período. |
   | 4 | La fila de la lista maestra queda al día. |

6. Si el documento ya estaba `vigente`, pasar los cambios aprobados al cuerpo y quitar sus filas de "Cambios propuestos (sin aprobar)".
7. Releer el documento y la lista para comprobar que las cuatro cosas quedaron hechas. Solo entonces escribir "Vigente desde", "Aprobó" y el estado `vigente`, también en el mapa de procesos.
8. Anotar en el registro de la sesión las palabras textuales de quien aprobó.
9. Guardar. Va un guardado por cada documento aprobado.
10. Confirmar con la frase de "Aprobado".

Si alguna de las cuatro cosas no se puede hacer, no se aprueba: deshacer lo escrito para ese documento con `git restore -- <rutas>` y decir la frase de "No se puede aprobar".

Cerrar la etapa: resumir qué quedó aprobado y qué no, preguntar si es correcto y guardar.

## Etapa 5. Conciliar

Comparar cada fila de `empresa/lista-maestra.md` con el bloque de control de su documento, y cada fila del mapa de procesos con su ficha.

| Diferencia | Qué se hace |
|---|---|
| La fila y el bloque no coinciden | Corregir la fila. Vale el bloque. |
| Un documento con bloque no tiene fila | Agregar la fila con los datos del bloque. |
| Una fila que no está `pendiente` no tiene archivo | No borrar la fila. Preguntar al responsable del programa qué pasó y anotarlo en "Observaciones". |
| Dos documentos tienen el mismo código | Resolverlo como indica "Dos documentos con el mismo código" en `metodo/control-documental.md`. |
| El estado o el enlace del mapa no coinciden con la ficha | Corregir el mapa. |
| El nombre o el dueño del mapa no coinciden con la ficha | Preguntar cuál vale. El mapa es la lista oficial de nombres. |

Después, actualizar la línea "Última actualización" de la lista.

Cerrar la etapa: contar en llano cuántas diferencias había y cómo quedaron, preguntar si es correcto y guardar.

## Etapa 6. Revisión periódica

Para cada documento `vigente` con la revisión vencida o por vencer, preguntar al responsable del programa si sabe de algún cambio. Un documento por mensaje.

| Resultado | Qué hace falta | Qué se hace |
|---|---|---|
| Sigue igual | Que el dueño del proceso lo confirme directamente y que quien aprueba lo diga en esta conversación | Sumar al historial una fila que diga "Revisión periódica sin cambios". Fijar la nueva próxima revisión. Poner al día la fila de la lista maestra. La versión no cambia. |
| Cambió | Nada más por ahora | Anotar el cambio en "Cambios propuestos (sin aprobar)". Sigue el camino normal: relevar, validar y aprobar. |
| Ya no se usa | La palabra de quien aprueba | Pasar a la etapa 7. |

- Si falta la confirmación de alguien, dejar preparada la pregunta en su hoja y no cambiar ninguna fecha.
- En los documentos de toda la empresa, en lugar del dueño del proceso confirma el responsable del programa.

Cerrar la etapa: resumir qué se revisó y qué quedó esperando, preguntar si es correcto y guardar.

## Etapa 7. Dar de baja

Un documento se da de baja cuando otro lo reemplazó o cuando lo que describe ya no se hace.

| Estado del documento | Quién lo decide |
|---|---|
| `vigente` | Quien aprueba, con su palabra explícita en esta conversación. |
| Cualquier otro | El responsable del programa. |

1. Resumir qué documento se da de baja, por qué y, si corresponde, cuál lo reemplaza.
2. Preguntar: "¿Queda dado de baja?"
3. Escribir el estado `obsoleto` en el bloque de control, en la lista maestra y en el mapa de procesos. Sumar al historial una fila con la fecha, el motivo y quién lo decidió. Anotar en "Observaciones" de la lista qué documento lo reemplaza.
4. No borrar ni mover el archivo, y no volver a editarlo. Su código no se reutiliza.

Cerrar la etapa: resumir qué se dio de baja, preguntar si es correcto y guardar.

## Etapa 8. Cierre

1. Resumir en llano lo que se hizo en la sesión y lo que quedó pendiente. Preguntar si es correcto.
2. Completar el registro de la sesión, con su línea de subida.
3. Hacer el guardado final en `borradores`.
4. Pasar a `main` lo revisado, como indica la sección siguiente. En este modo la subida se hace solo con el último paso de esa sección: no se usan los pasos de subida de "Al cerrar la sesión" en `metodo/guardado.md`.
5. Agradecer el tiempo y despedirse.

Si la persona tiene que irse antes, cerrar la etapa en curso con lo que haya y hacer esta etapa con un resumen corto. Lo que no llegó a repasarse queda para la próxima sesión.

## Pasar a `main` lo revisado

Pasa a `main` lo que quedó aceptado en la etapa 2 y todo documento que esta sesión validó, aprobó, concilió, revisó o dio de baja. Pasan también la lista maestra, el mapa de procesos y el registro de esta sesión. Lo que no se repasó queda solo en `borradores`.

"Con servidor" quiere decir lo mismo que en "Cuándo hay servidor" de `metodo/guardado.md`. Los pasos se hacen en silencio:

1. Comprobar que no queda nada sin guardar: `git status --porcelain -- empresa/` no devuelve nada.
2. Pasar a `main`: `git switch --quiet main`.
3. Con servidor, y si existe `origin/main`, poner `main` al día: `git merge --quiet --ff-only origin/main`.
4. Traer lo revisado, según el caso:

   | Qué se aceptó | Comandos |
   |---|---|
   | Todo lo que hay en `borradores` | `git merge --quiet --no-ff -m "<mensaje>" borradores` |
   | Solo una parte | `git restore --source borradores -- <rutas aceptadas>`, después `git add -- empresa/` y `git commit --quiet -m "<mensaje>"` |

5. Volver a `borradores`: `git switch --quiet borradores`.
6. Unir de inmediato: `git merge --quiet -m "<mensaje>" main`. Este paso no se saltea nunca: sin él, la próxima revisión encuentra conflictos.
7. Con servidor, subir una sola vez: `git push --quiet origin main borradores`.

- Si un documento cambió de nombre o de lugar, traer la carpeta que lo contiene y no el archivo suelto.
- `empresa/README.md` no se trae con `git restore`: es parte del método.
- Si un paso falla, deshacer una unión que quedó a medias con `git merge --abort` y volver con `git switch --quiet borradores`. No insistir. Decir la frase de "No se pudo pasar lo revisado". Lo revisado sigue guardado en `borradores` y vuelve a aparecer en la próxima revisión.
- Si la falla ocurre con archivos ya traídos a `main` y todavía sin guardar, no cambiar de rama ni escribir nada más. Decir la misma frase y terminar ahí.
- Si falla solo la subida, seguir "Si no se puede subir" en `metodo/guardado.md`.

## Guardado en este modo

Los mensajes siguen el formato de `metodo/guardado.md`. En este modo, `<asunto>` dice qué se hizo:

| Momento | Mensaje |
|---|---|
| Cierre de la etapa 2 | `docs(empresa): revisión de cambios - etapa 2 con <nombre>` |
| Cierre de la etapa 3 | `docs(<ámbito>): validación de <título> - etapa 3 con <nombre>` |
| Cada aprobación | `docs(<ámbito>): aprobación de <título> versión <n> - etapa 4 con <nombre>` |
| Cierre de la etapa 5 | `docs(empresa): conciliación de la lista maestra - etapa 5 con <nombre>` |
| Cierre de la etapa 6 | `docs(<ámbito>): revisión periódica de <título> - etapa 6 con <nombre>` |
| Cierre de la etapa 7 | `docs(<ámbito>): baja de <título> - etapa 7 con <nombre>` |
| Guardado final en `borradores` | `docs(empresa): revisión - cierre de sesión con <nombre>` |
| Guardado en `main` | `docs(empresa): paso de lo revisado - cierre de sesión con <nombre>` |
| Unión en `borradores` | `docs(empresa): unión de lo revisado - cierre de sesión con <nombre>` |

- `<ámbito>` es el área del documento. Si en la etapa se trabajó más de un documento, va `empresa`, y en lugar de `<título>` va `varios documentos`.
- `<nombre>` es el nombre de pila de la persona con la que se trabajó.

## Qué decir

| Situación | Frase |
|---|---|
| Lo que espera | "Hay `<n>` documentos con cosas nuevas para repasar, `<n>` listos para confirmar y `<n>` que esperan aprobación. ¿Empezamos por lo nuevo?" |
| Falta quien aprueba | "Para dejarlo como versión oficial hace falta que lo diga `<nombre>` directamente. Lo dejo preparado." |
| Aprobación contada por otra persona | "Lo anoto. Para dejarlo como versión oficial necesito que `<nombre>` lo diga aquí." |
| Pedir la aprobación | "¿Queda aprobado como versión oficial?" |
| No se puede aprobar | "Todavía no lo puedo dejar como versión oficial. Falta `<qué falta>`." |
| Aprobado | "Listo. Quedó como versión oficial número `<n>`. Toca volver a mirarlo el `<fecha>`." |
| Dar de baja | "¿Queda dado de baja?" |
| No se pudo pasar lo revisado | "Lo que repasamos quedó guardado, pero no pude dejarlo junto con lo ya revisado. Conviene pedir ayuda a quien preparó esta carpeta." |

Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
