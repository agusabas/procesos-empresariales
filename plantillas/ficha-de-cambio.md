> **Nota para el agente.** Este molde se copia a `empresa/cambios/<slug>/ficha-del-cambio.md` al cerrar la etapa 1 de la apertura de un cambio, como indica `metodo/cambio-en-curso.md`. Va una carpeta por cambio. Es un documento de trabajo: no lleva bloque de control. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean. Cada ayuda en cursiva se reemplaza por el contenido cuando se trabaja su etapa, y las filas de muestra se reemplazan por las reales. Lo que no se sabe se escribe `PENDIENTE: preguntar a <quién>`. Esta nota se borra de la copia.

# Cambio: `<nombre corto del cambio>`

- **Estado:** abierto
- **Abierto el:** `<AAAA-MM-DD>`
- **En uso desde:** —
- **Cerrado el:** —
- **Última actualización:** `<AAAA-MM-DD>`

Esta ficha sigue algo que la empresa está cambiando y que altera cómo se trabaja. Lo que dice sobre cómo va a quedar cada proceso es un plan. Cómo se hace hoy está en la ficha de cada proceso.

## Qué cambia y por qué

_Qué es lo que cambia, por qué se hace y qué se espera que mejore._

## Quiénes participan

De cada persona se anota el nombre de pila y el rol. Las personas de afuera de la empresa se anotan aquí y no llevan hoja.

| Quién | Qué hace en el cambio | De dónde es |
|---|---|---|
| `<nombre>` | Lleva el cambio dentro de la empresa | La empresa |
| `<nombre>` | `<qué hace>` | `<la empresa, un proveedor u otro>` |

## Etapa y fechas

_En qué punto está el cambio hoy._

| Hito | Fecha | Cómo está |
|---|---|---|
| `<hito>` | `<AAAA-MM-DD>` | `<hecho, en marcha o por hacer>` |

## Procesos afectados

"Cómo se hace hoy" es un enlace a la ficha del proceso, por su código: no se describe aquí. Si el proceso todavía no tiene ficha, dice "sin ficha: relevar primero".

| Proceso | Cómo se hace hoy | Cómo va a quedar | Qué falta definir |
|---|---|---|---|
| `<nombre del proceso>` | `<enlace a la ficha, por su código>` | `<cómo se piensa hacer>` | `<qué falta definir>` |

## Decisiones tomadas

| Fecha | Qué se decidió | Quién lo decidió | Por qué | Fuente |
|---|---|---|---|---|
| `<AAAA-MM-DD>` | `<decisión>` | `<nombre>` | `<motivo>` | `<quién lo contó o de qué material sale>` |

## Pendientes con terceros

Lo que se le preguntó a alguien de afuera de la empresa. La respuesta va con su fecha.

| Pregunta | A quién | Desde cuándo | Respuesta |
|---|---|---|---|
| `<pregunta>` | `<nombre y rol>` | `<AAAA-MM-DD>` | — |

## Datos y configuración a preparar

Lo que tiene que estar listo antes de usar la forma nueva. Nunca se anotan claves ni usuarios de acceso.

| Qué hay que preparar | Quién lo prepara | Para cuándo | Cómo está |
|---|---|---|---|
| `<qué>` | `<nombre>` | `<AAAA-MM-DD>` | `<por hacer, en preparación o listo>` |

## Qué puede salir mal

| Qué puede fallar | Qué pasaría | Qué se prevé hacer |
|---|---|---|
| `<qué>` | `<consecuencia>` | `<qué se prevé>` |

## Diferencias entre la forma de hoy y la nueva

### Lo que hoy se hace solo porque la forma actual lo exige

_Pasos, controles o anotaciones que dejan de hacer falta._

### Lo que la forma nueva no tiene previsto

_Cosas que hoy se hacen y que la forma nueva no contempla._

## Fichas a actualizar

Se completa cuando la forma nueva empieza a usarse. Va una fila por proceso afectado. El cambio se cierra cuando todas las filas dicen "actualizada" o "se deja como está".

| Proceso | Cómo quedó | Fecha |
|---|---|---|
| `<nombre del proceso>` | `<falta contarlo, falta aprobarlo, actualizada, o se deja como está y por qué>` | `<AAAA-MM-DD>` |

## Registros de sesión ya leídos

Los registros de sesión de los que ya se tomó lo anotado sobre este cambio. No se vuelven a leer.

| Registro | Qué se tomó | Fecha de lectura |
|---|---|---|
| `<archivo del registro>` | `<qué se tomó, o nada>` | `<AAAA-MM-DD>` |

## Historial

| Fecha | Qué pasó | Quién lo contó |
|---|---|---|
| `<AAAA-MM-DD>` | Se abrió el cambio | `<nombre>` |
