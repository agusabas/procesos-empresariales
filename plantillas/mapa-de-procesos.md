> **Nota para el agente.** Este molde se copia a `empresa/mapa-de-procesos.md` cuando se arma el mapa por primera vez. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean. La fila de muestra de cada grupo se reemplaza por los procesos reales, y se quita si el grupo todavía no tiene ninguno. Lo que no se sabe de un proceso se escribe en su fila, como `PENDIENTE: preguntar a <quién>`. Lo que no se sabe de un grupo entero va en "Pendientes del mapa": su ayuda en cursiva se reemplaza por esos pendientes, o por "Ninguno". Esta nota se borra de la copia. Las reglas de control están en `metodo/control-documental.md`.

# Mapa de procesos

| Código | Versión | Estado | Vigente desde | Próxima revisión |
|---|---|---|---|---|
| MP-GEN-001 | 0 | en curso | — | — |

| Elaboró | Revisó | Aprobó |
|---|---|---|
| `<nombre>` | — | — |

Este mapa reúne todos los procesos de la empresa que se identificaron hasta ahora. Dice quién responde por cada uno, quiénes participan, en qué estado está su documentación y en qué orden se relevan. No describe cómo se hace cada proceso: eso está en cada ficha.

## Cómo leerlo

- **Código:** el código de la ficha del proceso. `—` quiere decir que todavía no lo tiene, porque falta saber su área.
- **Proceso:** es el nombre oficial. Todos los demás documentos lo usan exactamente así.
- **Área:** el área a la que pertenece el proceso. "General" quiere decir que es de toda la empresa. Si lleva `A CONFIRMAR`, es provisoria.
- **Dueño:** quien responde por el proceso. `A DEFINIR` quiere decir que todavía no se sabe.
- **Participantes:** quiénes intervienen además del dueño, por su nombre de pila. `—` quiere decir que no interviene nadie más. Lo que hace cada persona está en la ficha del proceso.
- **Estado:** el estado de la ficha de ese proceso.
- **Ficha:** el enlace a la ficha. `—` quiere decir que todavía no se creó.

| Estado | Qué significa |
|---|---|
| `pendiente` | Está identificado. Todavía no se relevó. |
| `en curso` | El relevamiento empezó. |
| `borrador` | Ya se conversó todo. Falta confirmar o resolver algo. |
| `validado` | Lo confirmó el dueño del proceso. |
| `vigente` | Está aprobado. Es la versión oficial. |
| `obsoleto` | Ya no se usa. Se conserva. |

| Prioridad | Qué significa |
|---|---|
| `P1` | Se releva primero. |
| `P2` | Se releva después de los `P1`. |
| `P3` | Se releva al final. |
| `sin definir` | Todavía no se decidió. |

## Conducción

Cómo se decide y se dirige.

| Código | Proceso | Área | Tipo | Dueño | Participantes | Estado | Prioridad | Ficha |
|---|---|---|---|---|---|---|---|---|
| `<código>` | `<nombre del proceso>` | `<área>` | conducción | `<nombre>` | `<nombres>` | pendiente | `<prioridad>` | — |

## Operación

La cadena que va desde el pedido de un cliente hasta el cobro.

| Código | Proceso | Área | Tipo | Dueño | Participantes | Estado | Prioridad | Ficha |
|---|---|---|---|---|---|---|---|---|
| `<código>` | `<nombre del proceso>` | `<área>` | operación | `<nombre>` | `<nombres>` | pendiente | `<prioridad>` | — |

## Apoyo

Lo que sostiene a la operación.

| Código | Proceso | Área | Tipo | Dueño | Participantes | Estado | Prioridad | Ficha |
|---|---|---|---|---|---|---|---|---|
| `<código>` | `<nombre del proceso>` | `<área>` | apoyo | `<nombre>` | `<nombres>` | pendiente | `<prioridad>` | — |

## Pendientes del mapa

_Lo que todavía no se sabe y no entra en la fila de un proceso: lo que falta de un grupo entero, dónde empieza y dónde termina la cadena, un proceso que nombra el material y que nadie reconoció todavía, o lo que el material dice sobre un proceso que todavía no tiene código. Una línea por pendiente, con `PENDIENTE: preguntar a <quién>` o con `A CONFIRMAR con <quién>`. Si no hay ninguno, se escribe "Ninguno"._

## Historial

| Versión | Fecha | Qué cambió | Quién lo contó | Quién aprobó |
|---|---|---|---|---|
