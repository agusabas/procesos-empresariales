> **Nota para el agente.** Este molde se copia a `empresa/procesos/<area>/<codigo>-<slug>.md` al empezar el relevamiento de un proceso. Si la ficha ya existe, no se copia de nuevo: se le suma lo que cuenta cada persona. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean, y cada ayuda en cursiva se reemplaza por el contenido. Una parte que todavía no tiene nada conserva su ayuda hasta que haya algo para anotar. Las ayudas que encabezan "Cómo se hace hoy", "Problemas e ideas" y "Cambios propuestos (sin aprobar)" explican la parte y quedan en la copia. Lo que no se sabe se escribe `PENDIENTE: preguntar a <quién>`. Esta nota se borra de la copia. Las reglas de control están en `metodo/control-documental.md`.

# `<nombre del proceso, como figura en el mapa de procesos>`

| Código | Versión | Estado | Vigente desde | Próxima revisión |
|---|---|---|---|---|
| `<código>` | 0 | en curso | — | — |

| Elaboró | Revisó | Aprobó |
|---|---|---|
| `<nombre>` | — | — |

## Cómo se hace hoy

_Esta parte cuenta lo que pasa hoy, no lo que debería pasar._

### Objetivo

_Para qué se hace este trabajo, en una o dos frases. Qué pasaría si nadie lo hiciera._

### Alcance

_Dónde empieza y dónde termina. Qué casos incluye y cuáles quedan afuera. Con qué otros nombres se conoce este trabajo en la empresa, si los tiene._

### Dueño

_Quién responde por que esto salga bien, con nombre de pila y rol. Quién lo cubre cuando no está._

### Participantes

_Quiénes más intervienen, con nombre de pila y rol, y en qué parte. Aquí y en "Dueño" van los nombres; en la tabla de pasos va el rol._

### Qué lo pone en marcha

_Qué tiene que pasar para que este trabajo empiece._

### Qué hace falta para empezar

_Lo que hay que tener antes de empezar: datos, documentos, autorizaciones. Quién lo entrega._

### Pasos

_Una fila por paso, en el orden en que se hacen. Un paso termina cuando cambia quién lo hace, cuando se decide algo o cuando queda algo hecho. Si un paso lo hacen dos sectores, va en dos filas. En "Quién" va el rol o el sector, como lo dice la empresa: "quien atiende el mostrador", "Administración". Nunca un nombre de pila: los nombres van en "Participantes", en el mapa y en las hojas. En "Con qué" va el sistema, la planilla o el papel que se usa hoy. Si en el paso se copian datos de otro lugar, "Con qué" dice de dónde: `<sistema o planilla>`, copiado de `<origen>`. "Cuánto tarda" es el tiempo de trabajo del paso, en minutos, horas o días. Un paso que se hace solo en algunos casos dice cuándo y, si se sabe, en cuántos de cada diez._

| Paso | Quién | Qué hace | Con qué (sistema/planilla) | Cuánto tarda |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

De punta a punta: `<en un caso normal>`; `<en los que más tardan>`. Dónde se espera más: `<paso>`, esperando `<qué o a quién>`.

Pasos que hoy sabe hacer una sola persona: `<pasos y rol>`.

### Diagrama

_El diagrama sale de la tabla de pasos y se genera de nuevo cada vez que la tabla cambia, como indica "Diagramas" en `metodo/control-documental.md`. El que sigue es solo un esqueleto: se reemplaza entero._

```mermaid
flowchart TD
    inicio(["Qué lo pone en marcha"])
    fin(["Qué queda hecho al terminar"])

    subgraph sector_a ["Sector o rol A"]
        p1["1. Qué hace"]
        p2["2. Qué hace"]
    end

    subgraph sector_b ["Sector o rol B"]
        p3["3. Qué hace"]
    end

    inicio --> p1
    p1 --> p2
    p2 --> p3
    p3 --> fin
```

### Qué queda hecho al terminar

_Qué queda hecho cuando el trabajo termina y a quién le llega._

Sigue en: `<proceso, como figura en el mapa, o 'termina acá'>`. Espera hasta que lo toman: `<tiempo>`.

Plazo prometido a quien lo pide: `<plazo, o 'sin plazo prometido'>`.

### Reglas que se siguen

_Los criterios que se aplican para decidir. Una regla por renglón. Si se sabe, cada regla termina con dónde está escrita o quién la sabe de memoria, y quién la decidió._

### Excepciones

_Los casos que se salen de lo habitual, qué se hace en cada uno, quién lo autoriza y cada cuánto pasa. Si se sabe, en qué paso pasa: el número y qué hace, como en la tabla._

### Qué registro queda

_Dónde queda anotado que esto se hizo, quién lo guarda y por cuánto tiempo._

### Frecuencia y volumen

_Cada cuánto se hace y cuántos casos son, por día, por semana o por mes. En qué época hay más._

### Cómo nos damos cuenta de que anda bien

_Cómo se nota hoy que esto sale bien o mal. Si hoy no se mide, decirlo. Según quien lo hace, cuántos de cada diez casos hay que corregir o rehacer._

### Qué puede salir mal

_Lo que puede fallar, qué consecuencia tiene y qué se hace hoy para evitarlo o para resolverlo. Si se sabe, en qué paso pasa: el número y qué hace, como en la tabla. Si el trabajo lo necesita, los cuidados para las personas y los equipos._

## Documentos

_Los archivos que se usan en este trabajo y que aportaron las personas. Una línea por archivo, con el enlace y una frase que diga qué es. El detalle de cada archivo está en el `catalogo.md` de su carpeta, en `empresa/adjuntos/`. Una planilla, un cuaderno o una carpeta que se usa y no se aportó va también aquí, con dónde está guardado. Nunca usuarios ni claves. Si todavía no hay ninguno, esta parte queda vacía._

_Forma de cada línea:_ `- [<archivo>](../../adjuntos/<area>/<proceso>/<archivo>): <qué es>.`

_Para lo que se usa y no se aportó:_ `- <qué es>: guardado en <dónde>.`

## Problemas e ideas

_Esta parte va separada a propósito. Nada de lo que hay aquí describe cómo se hace hoy. Es material de trabajo: se pone al día sin aprobación y sin cambiar la versión, también con la ficha `vigente`, como indica "Cambios en un documento vigente" en `metodo/control-documental.md`._

### Problemas

_Dónde se traba, qué se repite, qué genera errores o esperas. Hechos, no juicios sobre personas. Si se sabe, cada cuánto pasa y qué consecuencia tiene._

### Ideas de mejora

_Lo que propone quien hace el trabajo. Anotar quién lo propuso y la fecha. Si alguien cuenta qué se decidió sobre la idea, anotarlo con quién lo decidió y la fecha._

## Cambios propuestos (sin aprobar)

_Se usa solo cuando el documento está `vigente`: lo que cambió no se escribe arriba, se anota aquí hasta que se apruebe. En "Qué cambió" van la parte afectada y el texto que va a quedar, tal como quedaría en el cuerpo. Mientras no haya cambios, la tabla queda sin filas._

| Fecha | Quién lo cuenta | Qué cambió | Confirmó el dueño |
|---|---|---|---|

## Historial

| Versión | Fecha | Qué cambió | Quién lo contó | Quién aprobó |
|---|---|---|---|---|
