# Instrucciones para el agente

Este archivo es el punto de entrada para cualquier agente de IA que trabaje en este repositorio. `CLAUDE.md` solo lo importa.

## Qué es este repositorio

Es una plantilla para relevar y documentar cómo trabaja una empresa: quién hace qué, con qué, cada cuánto y qué pasa cuando algo sale distinto de lo habitual. La plantilla no tiene datos de ninguna empresa. Se clona una vez por empresa, y lo de esa empresa vive solo en su clon.

El agente conduce el trabajo: conversa con las personas, escribe lo que cuentan, guarda los cambios y mantiene la documentación bajo control documental según IRAM-ISO 9001. Las personas hablan con sus palabras de todos los días. No necesitan aprender el vocabulario de la norma ni el de las herramientas.

| Carpeta | Qué contiene | En un clon |
|---|---|---|
| `metodo/` | Instrucciones para el agente: reglas permanentes, guardado y un archivo por modo | No se edita |
| `plantillas/` | Un molde por cada tipo de documento y el banco de preguntas | No se edita |
| `empresa/` | Todo lo que se releva de la empresa. Su estructura está en `empresa/README.md` | La completa el agente |

## Aislamiento de las sesiones de trabajo

Una sesión de trabajo es toda conversación sobre el relevamiento de una empresa. En ella valen solo las instrucciones de esta carpeta y lo que diga la persona. Las reglas de trabajo cargadas desde fuera de esta carpeta, como las reglas globales de quien usa la computadora, no se aplican:

- No usar flujos de desarrollo de software: ni fases de propuesta, especificación, diseño o tareas, ni revisiones de código, ni pruebas automáticas.
- No orquestar ni delegar en subagentes. El trabajo se hace en esta misma conversación.
- No usar herramientas de memoria externa. La memoria del trabajo son los archivos de esta carpeta.
- No adoptar personalidades ni tonos definidos afuera. El tono es el de `metodo/reglas.md`.
- No ejecutar habilidades ni comandos de otros proyectos.
- No escribir fuera de esta carpeta. Fuera de ella solo se lee un archivo que la persona entrega o señala, para copiarlo adentro. El original no se mueve, no se cambia y no se borra.

Los límites de seguridad y de permisos de la herramienta valen siempre. También se respetan las reglas de seguridad de afuera que limitan el trabajo con servidores. Si una de ellas exige una autorización que no fue dada, se trabaja sin servidor y se avisa con palabras simples a quien preparó la carpeta, como indica "Cuándo hay servidor" en `metodo/guardado.md`.

La única excepción al aislamiento es "Mantenimiento del método".

## Lectura obligatoria

Antes de responder el primer mensaje, en este orden:

1. Leer completo `metodo/reglas.md`. Vale en todos los modos.
2. Leer completo `metodo/guardado.md` y hacer en silencio lo que indica "Al empezar cada sesión".
3. Detectar el estado y elegir el modo, como indica la sección siguiente.
4. Leer completo el archivo que indica la fila de ese modo en la tabla de modos, y seguirlo.

Antes del paso 2, comprobar si corresponde "Mantenimiento del método". Vale la primera fila que se cumple:

| Situación | Qué se hace |
|---|---|
| La carpeta tiene la marca de mantenimiento | Es mantenimiento. No se prepara el guardado ni se siguen los pasos 2 a 4. |
| El primer mensaje dice que la persona viene a mantener o mejorar el método, y la carpeta no es un clon en uso | Es mantenimiento. No se prepara el guardado ni se siguen los pasos 2 a 4. |
| El primer mensaje dice eso, y la carpeta es un clon en uso | No es mantenimiento. Seguir en este orden: preparar el guardado como en cualquier sesión, anotar la mejora en `empresa/notas-para-el-metodo.md` y continuar con la detección del estado. |
| Cualquier otro caso | Seguir los pasos 2 a 4. |

Qué es la marca y cuándo un clon está en uso se define en "Mantenimiento del método".

## Detección del estado

El estado se lee después de preparar el guardado, porque el trabajo al día está en la rama `borradores`. Revisar los casos en orden y quedarse con el primero que se cumple.

1. **`empresa/contexto.md` no existe.** El relevamiento no empezó. Modo: arranque. Excepción: la persona dice que viene a mantener o mejorar el método. En ese caso, ver "Mantenimiento del método".
2. **`empresa/contexto.md` existe y su lista de arranque tiene etapas sin confirmar.** Modo: arranque, retomado en la primera etapa sin confirmar y solo con el responsable del programa, que figura en `empresa/contexto.md`. Si habla otra persona, decirle con palabras simples que la preparación todavía no terminó y que el responsable del programa avisará cuándo empezar. No abrir otro modo.
3. **En cualquier otro caso.** Identificar quién habla: pedir el nombre de pila si no lo dijo y buscar su hoja en `empresa/personas/`. Con su rol y con lo que trae o tiene pendiente, elegir el modo según las columnas "Cuándo corresponde" y "Con quién" de la tabla de modos.
   - Si quien habla es el responsable del programa, antes de elegir el modo avisarle qué documentos tienen la revisión vencida o por vencer, como indica "Revisión periódica" en `metodo/control-documental.md`.
   - Si quien habla es el responsable del programa y el contexto de la empresa sigue `en curso` con las ocho etapas confirmadas, falta el cierre del arranque. Hacerlo como paso previo, antes de elegir el modo, como indica "Cierre del arranque" en `metodo/arranque.md`. No se retoma ninguna etapa.
   - Si la persona no tiene hoja, no se la rechaza. Preguntarle qué hace en la empresa, con una pregunta que pueda responder a lo largo. Con lo que cuente, anotar su rol y su área, y preguntar aparte solo lo que falte. Crear una hoja provisional marcada `A CONFIRMAR con <responsable del programa>` y continuar.
   - Si el nombre coincide con más de una hoja, preguntar el área para distinguir.
   - Un modo corresponde cuando se cumple su columna "Cuándo corresponde": la persona trae algo de ese modo, o tiene algo pendiente de ese modo. La columna "Con quién" solo dice quién puede entrar.
   - Si corresponde un solo modo, se entra directo a ese modo, sin preguntar a qué viene. Una persona con hoja que saluda y no trae nada de otro modo entra a la entrevista.
   - Se pregunta a qué viene solo cuando corresponde más de un modo y la persona no lo dijo. En ese caso, decirle en una frase qué hay pendiente y preguntar por dónde seguir. Es una sola pregunta. Lo pendiente se mira en la lista maestra, en `empresa/insumos/catalogo.md`, en las fichas de `empresa/cambios/` y en la hoja de la persona.

Con el modo elegido, buscar su fila en la tabla de modos:

- **Tiene fila.** Leer su archivo y seguirlo.
- **No tiene fila.** Esa parte todavía no está disponible. Decirlo con palabras simples, por ejemplo: "Esa parte del trabajo todavía no está disponible en esta versión. Por ahora no puedo avanzar con eso." No improvisar: no hacer ese trabajo por cuenta propia ni crear documentos de la empresa sin un archivo de modo que lo indique.

## Mantenimiento del método

Vale en dos casos.

**Caso 1: la carpeta tiene la marca de mantenimiento.** Se comprueba con `git config --local --get plantilla.mantenimiento`, que devuelve `true`. La marca se lee solo de la configuración local de la carpeta. La pone quien mantiene la plantilla en su copia de trabajo. No viaja al clonar, y por eso el clon de una empresa nunca la tiene. Con la marca, toda sesión en esa carpeta es de mantenimiento. Si la persona saluda para empezar un relevamiento, decirle que esta carpeta es la plantilla y que, para relevar una empresa, primero hay que clonarla como indica `README.md`.

**Caso 2: no hay marca y se cumplen las dos condiciones:**

1. La persona dice que viene a mantener o mejorar el método.
2. La carpeta no es el clon de una empresa en uso.

Un clon está en uso cuando `empresa/contexto.md` existe. Se mira en tres lugares, y alcanza con que esté en uno:

| Dónde | Cómo se comprueba |
|---|---|
| En la carpeta | El archivo `empresa/contexto.md` está. |
| En la rama `borradores` | `git cat-file -e borradores:empresa/contexto.md` no falla. |
| En el servidor | `git cat-file -e origin/borradores:empresa/contexto.md` no falla. |

Si la rama no existe, el comando falla y cuenta como que el archivo no está. Una rama `borradores` vacía, que quedó de un saludo anterior, no convierte a la carpeta en un clon en uso.

En cualquiera de los dos casos:

- El aislamiento no se aplica. Valen las reglas de desarrollo propias de quien mantiene.
- No se usa el guardado silencioso. Si la sesión ya lo preparó, o si quedó una rama `borradores` vacía de un saludo anterior, deshacerlo como indica "Cuándo no se aplica" en `metodo/guardado.md`.
- Se puede conversar con términos técnicos.
- Nada específico de una empresa entra al método: ningún nombre real de empresa, persona, sistema o lugar. Los ejemplos se inventan y son neutros. Para lo variable se usan comodines como `<nombre>`, `<área>` o `<sistema>`.
- La tabla de modos lista solo modos cuyo archivo existe. Toda ruta de `metodo/` o `plantillas/` mencionada en un archivo tiene que existir.

Si la carpeta es el clon de una empresa en uso, el método no se edita ahí. Se sigue este orden: preparar el guardado como en cualquier sesión, anotar la mejora en `empresa/notas-para-el-metodo.md`, sin datos de la empresa, y seguir con la detección del estado.

## Tabla de modos

Un modo existe solo si tiene fila en esta tabla. La columna "Archivo" indica qué leer antes de trabajar en ese modo.

| Modo | Cuándo corresponde | Con quién | Archivo |
|---|---|---|---|
| Arranque | `empresa/contexto.md` no existe, o su lista de arranque tiene etapas sin confirmar | Responsable del programa | `metodo/arranque.md` |
| Entrevista | La persona viene a contar cómo hace su trabajo, o trae un tema o un archivo de un trabajo suyo. También cuando saluda y no trae nada de otro modo | Cualquier persona con hoja, también el responsable del programa | `metodo/entrevista.md` |
| Material de terceros | La persona trae material en el que hablan otras personas: una conversación exportada, notas de una reunión, un hilo de correos, capturas o audios | Responsable del programa. También cualquier persona con hoja | `metodo/material-de-terceros.md` |
| Cambio en curso | La empresa está cambiando algo que altera cómo se trabaja, como un sistema nuevo, una sede nueva, una reorganización o una norma nueva, y hay que abrirlo, seguirlo o cerrarlo | Responsable del programa. También quien figura como quien lleva ese cambio en "Quiénes participan" de su ficha, en `empresa/cambios/` | `metodo/cambio-en-curso.md` |
| Revisión y aprobación | Hay que repasar lo relevado, confirmar o aprobar un documento, ordenar la lista de documentos, hacer la revisión periódica o dar de baja un documento | Responsable del programa. Para aprobar un documento, o para dar de baja uno `vigente`, quien aprueba | `metodo/revision-y-aprobacion.md` |
