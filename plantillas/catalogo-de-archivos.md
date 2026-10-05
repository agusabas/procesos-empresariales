> **Nota para el agente.** Este molde se copia con el nombre `catalogo.md` a la carpeta que se cataloga: `empresa/insumos/` o `empresa/adjuntos/<area>/<proceso>/`. Se crea cuando llega el primer archivo de esa carpeta. Es un documento de trabajo: no lleva bloque de control y se actualiza cada vez que llega un archivo. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean. La fila de muestra se reemplaza por el primer archivo. Esta nota se borra de la copia. Cómo se recibe y se guarda un archivo está en "Archivos recibidos", en `metodo/control-documental.md`.

# Catálogo de `<insumos, o el nombre del proceso como figura en el mapa>`

- **Última actualización:** `<AAAA-MM-DD>`

Este catálogo dice qué es cada archivo de esta carpeta, de dónde vino y a qué corresponde, para poder entenderlo sin abrirlo.

| Archivo | Qué es | Tipo | Proceso y paso | Quién lo aportó | Fecha | Fecha del material | Nombre original | Observaciones |
|---|---|---|---|---|---|---|---|---|
| `<archivo>` | `<qué es, en una frase>` | `<tipo>` | `<proceso y paso>` | `<nombre>` | `<AAAA-MM-DD>` | `<fecha del material>` | `<nombre original>` | `<observaciones>` |

## Cómo leerlo

- **Archivo:** el nombre con el que quedó guardado, con su carpeta si está dentro de una. `—` si el archivo no se copió a esta carpeta.
- **Qué es:** una frase que dice qué es el archivo.
- **Tipo:** una sola de estas palabras: `instructivo`, `formulario`, `planilla`, `captura de pantalla`, `ejemplo`, `comprobante`, `conversación`, `nota`, `audio`, `transcripción`, `otro`.
- **Proceso y paso:** el proceso, con el nombre del mapa, y el paso de su ficha al que corresponde el archivo. `—` si no corresponde a un solo proceso. La marca `PENDIENTE` si todavía no se sabe.
- **Quién lo aportó:** el nombre de pila de quien lo acercó.
- **Fecha:** el día en que llegó.
- **Fecha del material:** de cuándo es el material. Si es una conversación, notas o correos, las fechas que cubre, de la primera a la última. `sin fecha` si no se sabe.
- **Nombre original:** cómo se llamaba el archivo antes de guardarlo.

En "Observaciones" se usan estas frases, tal cual, cuando corresponden:

| Frase | Cuándo se usa |
|---|---|
| `sin transcribir` | Es un audio y todavía no hay transcripción. Hay que pedirla. Su contenido no se adivina. |
| `transcripción en`, seguido del nombre del archivo | Es un audio cuya transcripción ya llegó. Reemplaza a `sin transcribir`. |
| `se lee en otra sesión` | Es una conversación entre otras personas. Por ahora solo se cataloga. |
| `leído hasta`, seguido de una fecha | Es material que se lee por partes o que sigue creciendo. Dice hasta qué fecha del material ya se leyó. |
| `no revisado por el agente` | El formato no se pudo abrir. |
| `transcripto por el agente, sin el original` | La persona lo dictó o lo pegó en la conversación. |
| `guardado sin los datos personales de terceros` | Se guardó una versión en blanco o con esos datos tapados. |
| `guardado sin los datos comerciales que la empresa deja afuera` | Se guardó una versión sin los datos comerciales que la empresa pidió no guardar, o que todavía no definió. |
| `no se guardó: contiene datos personales de terceros` | El archivo no está en esta carpeta. Esta fila es su único rastro. |
| `no se guardó: contiene datos comerciales que la empresa deja afuera` | El archivo no está en esta carpeta. Esta fila es su único rastro. |
| `no se copió: pesa más de 10 MB` | El archivo sigue donde lo tiene la persona. |
