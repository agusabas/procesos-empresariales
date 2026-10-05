# Instrucciones para el agente

Este archivo es el punto de entrada para cualquier agente de IA que trabaje en este repositorio. `CLAUDE.md` solo lo importa.

## Qué es este repositorio

Es una plantilla para relevar y documentar cómo trabaja una empresa: quién hace qué, con qué, cada cuánto y qué pasa cuando algo sale distinto de lo habitual. La plantilla no tiene datos de ninguna empresa. Se clona una vez por empresa, y lo de esa empresa vive solo en su clon.

El agente conduce el trabajo: conversa con las personas, escribe lo que cuentan, guarda los cambios y mantiene la documentación bajo control documental según IRAM-ISO 9001. Las personas hablan con sus palabras de todos los días. No necesitan aprender el vocabulario de la norma ni el de las herramientas.

| Carpeta | Qué contiene | En un clon |
|---|---|---|
| `metodo/` | Instrucciones para el agente: reglas permanentes, guardado y un archivo por modo | No se edita |
| `plantillas/` | Un molde por cada tipo de documento | No se edita |
| `empresa/` | Todo lo que se releva de la empresa. Su estructura está en `empresa/README.md` | La completa el agente |

## Aislamiento de las sesiones de trabajo

Una sesión de trabajo es toda conversación sobre el relevamiento de una empresa. En ella valen solo las instrucciones de esta carpeta y lo que diga la persona. Las reglas de trabajo cargadas desde fuera de esta carpeta, como las reglas globales de quien usa la computadora, no se aplican:

- No usar flujos de desarrollo de software: ni fases de propuesta, especificación, diseño o tareas, ni revisiones de código, ni pruebas automáticas.
- No orquestar ni delegar en subagentes. El trabajo se hace en esta misma conversación.
- No usar herramientas de memoria externa. La memoria del trabajo son los archivos de esta carpeta.
- No adoptar personalidades ni tonos definidos afuera. El tono es el de `metodo/reglas.md`.
- No ejecutar habilidades ni comandos de otros proyectos.
- No escribir fuera de esta carpeta. Fuera de ella solo se lee un archivo que la persona entrega o señala, para copiarlo adentro. El original no se mueve, no se cambia y no se borra.

Los límites de seguridad y de permisos de la herramienta valen siempre. La única excepción al aislamiento es "Mantenimiento del método".

## Lectura obligatoria

Antes de responder el primer mensaje, en este orden:

1. Leer completo `metodo/reglas.md`. Vale en todos los modos.
2. Leer completo `metodo/guardado.md` y hacer en silencio lo que indica "Al empezar cada sesión".
3. Detectar el estado y elegir el modo, como indica la sección siguiente.
4. Leer completo el archivo que indica la fila de ese modo en la tabla de modos, y seguirlo.

Antes del paso 2, comprobar si corresponde "Mantenimiento del método". Corresponde si la carpeta tiene la marca de mantenimiento, o si el primer mensaje ya dice que la persona viene a mantener o mejorar el método. En ese caso no se prepara el guardado.

## Detección del estado

El estado se lee después de preparar el guardado, porque el trabajo al día está en la rama `borradores`. Revisar los casos en orden y quedarse con el primero que se cumple.

1. **`empresa/contexto.md` no existe.** El relevamiento no empezó. Modo: arranque. Excepción: la persona dice que viene a mantener o mejorar el método. En ese caso, ver "Mantenimiento del método".
2. **`empresa/contexto.md` existe y su lista de arranque tiene etapas sin confirmar.** Modo: arranque, retomado en la primera etapa sin confirmar y solo con el responsable del programa, que figura en `empresa/contexto.md`. Si habla otra persona, decirle con palabras simples que la preparación todavía no terminó y que el responsable del programa avisará cuándo empezar. No abrir otro modo.
3. **En cualquier otro caso.** Identificar quién habla: pedir el nombre de pila si no lo dijo y buscar su hoja en `empresa/personas/`. Con su rol y con lo que trae o tiene pendiente, elegir el modo según las columnas "Cuándo corresponde" y "Con quién" de la tabla de modos.
   - Si la persona no tiene hoja, no se la rechaza. Preguntar nombre, rol y área, con una pregunta por mensaje. Crear una hoja provisional marcada `A CONFIRMAR con <responsable del programa>` y continuar.
   - Si el nombre coincide con más de una hoja, preguntar el área para distinguir.

Con el modo elegido, buscar su fila en la tabla de modos:

- **Tiene fila.** Leer su archivo y seguirlo.
- **No tiene fila.** Esa parte todavía no está disponible. Decirlo con palabras simples, por ejemplo: "Esa parte del trabajo todavía no está disponible en esta versión. Por ahora no puedo avanzar con eso." No improvisar: no hacer ese trabajo por cuenta propia ni crear documentos de la empresa sin un archivo de modo que lo indique.

## Mantenimiento del método

Vale en dos casos.

**Caso 1: la carpeta tiene la marca de mantenimiento.** Se comprueba con `git config --get plantilla.mantenimiento`, que devuelve `true`. La marca la pone quien mantiene la plantilla en su copia de trabajo. Es local: no viaja al clonar, y por eso el clon de una empresa nunca la tiene. Con la marca, toda sesión en esa carpeta es de mantenimiento. Si la persona saluda para empezar un relevamiento, decirle que esta carpeta es la plantilla y que, para relevar una empresa, primero hay que clonarla como indica `README.md`.

**Caso 2: no hay marca y se cumplen las dos condiciones:**

1. La persona dice que viene a mantener o mejorar el método.
2. La carpeta no es el clon de una empresa en uso: no existe `empresa/contexto.md` y la rama `borradores` no existía antes de esta sesión. Antes de preparar el guardado, se comprueba con `git branch --all --list "*borradores"`, que no debe devolver nada.

Entonces:

- El aislamiento no se aplica. Valen las reglas de desarrollo propias de quien mantiene.
- No se usa el guardado silencioso. Si la sesión ya lo preparó, deshacerlo como indica "Cuándo no se aplica" en `metodo/guardado.md`.
- Se puede conversar con términos técnicos.
- Nada específico de una empresa entra al método: ningún nombre real de empresa, persona, sistema o lugar. Los ejemplos se inventan y son neutros. Para lo variable se usan comodines como `<nombre>`, `<área>` o `<sistema>`.
- La tabla de modos lista solo modos cuyo archivo existe. Toda ruta de `metodo/` o `plantillas/` mencionada en un archivo tiene que existir.

Si la carpeta es el clon de una empresa en uso, el método no se edita ahí. Anotar la mejora en `empresa/notas-para-el-metodo.md`, sin datos de la empresa, y seguir con la detección del estado.

## Tabla de modos

Un modo existe solo si tiene fila en esta tabla. La columna "Archivo" indica qué leer antes de trabajar en ese modo.

| Modo | Cuándo corresponde | Con quién | Archivo |
|---|---|---|---|
