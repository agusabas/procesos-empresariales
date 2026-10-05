# La carpeta de la empresa

En la plantilla esta carpeta está vacía: solo contiene este archivo. En el clon de una empresa, el agente la completa a medida que avanza el relevamiento. Todo lo que se sabe de la empresa vive en esta carpeta y en ningún otro lugar.

Este archivo es también el esquema: indica qué va en cada lugar y cómo se nombra. Forma parte del método, así que en un clon no se edita.

## Estructura

```
empresa/
├── README.md
├── contexto.md
├── mapa-de-procesos.md
├── lista-maestra.md
├── glosario.md
├── notas-para-el-metodo.md
├── personas/
│   └── <nombre>.md
├── procesos/
│   └── <area>/
│       └── <codigo>-<slug>.md
├── instructivos/
│   └── <area>/
│       └── <codigo>-<slug>.md
├── sesiones/
│   └── AAAA-MM-DD-<quien>-<tema>.md
├── insumos/
│   ├── catalogo.md
│   └── <material tal como se recibió>
├── adjuntos/
│   └── <area>/
│       └── <proceso>/
│           ├── catalogo.md
│           └── <archivos aportados>
└── cambios/
    └── <slug>/
        └── ficha-del-cambio.md
```

## Qué contiene cada lugar

| Lugar | Qué contiene |
|---|---|
| `contexto.md` | La empresa, cómo se organiza el programa de relevamiento (roles, forma de trato, datos que no se guardan), las áreas con sus tres letras, los sistemas en uso y la lista de arranque. |
| `mapa-de-procesos.md` | El inventario de los procesos de la empresa. Es la lista oficial de sus nombres. |
| `lista-maestra.md` | La lista de todos los documentos. Un código se asigna solo desde aquí. |
| `glosario.md` | Una sola definición por cada término propio de la empresa. |
| `notas-para-el-metodo.md` | Lo que faltó o no alcanzó en el método. Se escribe sin datos de la empresa. |
| `personas/<nombre>.md` | Una hoja por persona: rol, área, procesos en los que participa y preguntas preparadas para ella. |
| `procesos/<area>/<codigo>-<slug>.md` | Una ficha por proceso: cómo se hace hoy. |
| `instructivos/<area>/<codigo>-<slug>.md` | El paso a paso detallado de una tarea. |
| `sesiones/AAAA-MM-DD-<quien>-<tema>.md` | El registro de cada conversación. |
| `insumos/` | El material original tal como se recibió, con su `catalogo.md`. |
| `adjuntos/<area>/<proceso>/` | Los archivos aportados durante las sesiones, con su `catalogo.md`. |
| `cambios/<slug>/ficha-del-cambio.md` | Un cambio en curso que altera cómo se trabaja. |

Qué tipo de archivo es cada lugar, y cómo se controla, está en `metodo/control-documental.md`.

## Cómo se nombra

Los nombres van en minúsculas, con guiones en lugar de espacios, sin acentos ni eñes. La única excepción es `<codigo>`, que se escribe tal como figura en la lista maestra.

| Parte | Qué va |
|---|---|
| `<nombre>`, `<quien>` | El nombre de pila de la persona. Si dos personas comparten el nombre, se agrega el área: `<nombre>-<area>`. |
| `<area>` | El nombre del área, como figura en `contexto.md`. Lo que es de toda la empresa usa `general`. |
| `<codigo>` | El código del documento, asignado desde `lista-maestra.md`. |
| `<slug>` | El nombre del proceso, del instructivo o del cambio. |
| `<proceso>` | El mismo nombre que el archivo de la ficha del proceso, sin `.md`. |
| `<tema>` | El proceso o el asunto de la conversación. En una entrevista, el nombre del archivo de la ficha, sin `.md`. |
| Archivos de `insumos/` y de `adjuntos/` | `AAAA-MM-DD-descripcion-corta.extension`, con el día en que llegó. El nombre original queda en el `catalogo.md`. |
| `AAAA-MM-DD` | La fecha: año, mes y día. |

## Reglas de esta carpeta

- Cada archivo y cada carpeta se crean cuando hacen falta, no antes.
- No se crean lugares que no estén en este esquema. Si hace falta uno, se anota en `notas-para-el-metodo.md`.
- `insumos/` guarda el material como llegó. No se modifica.
- Un registro de `sesiones/` no se edita una vez cerrado.
- En toda la carpeta valen las reglas de privacidad de `metodo/reglas.md`.
