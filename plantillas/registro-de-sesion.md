> **Nota para el agente.** Este molde se copia a `empresa/sesiones/AAAA-MM-DD-<quien>-<tema>.md` cuando se empieza a escribir una sesión. Si ya hay una sesión de ese día con la misma persona y el mismo tema, se agrega `-2` al final del nombre. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean, y cada ayuda en cursiva se reemplaza por el contenido. Las respuestas se copian con las palabras de la persona, sin mejorarlas ni resumirlas. Valen las reglas de privacidad de `metodo/reglas.md`. Es un registro: una vez cerrada la sesión, no se edita. La única parte que puede cambiar después es la línea de subida, si la subida falla, como indica `metodo/guardado.md`. Esta nota se borra de la copia.

# Sesión `<AAAA-MM-DD>`: `<nombre>`, `<tema>`

- **Persona:** `<nombre de pila y rol>`
- **Modo:** `<arranque, entrevista, material de terceros, cambio en curso o revisión y aprobación>`
- **Proceso o asunto:** `<nombre del proceso, como figura en el mapa, o asunto de la sesión>`
- **Ficha:** `<ruta de la ficha del proceso, o —>`
- **Hora de inicio y de fin:** `<HH:MM>` a `<HH:MM>`
- **Sesión anterior:** `<archivo de la sesión anterior sobre lo mismo, o ninguna>`

## Etapas o temas

_Una línea por cada etapa o tema previsto. Las etapas llevan número y los temas llevan letra. Cada línea se marca cuando la persona confirmó su resumen. La sesión siguiente continúa desde la primera línea sin marcar._

- [ ] `<número o letra>`. `<nombre de la etapa o del tema>`

## `<Etapa y número, o Tema y letra>`. `<nombre>`

_Se repite un bloque como este por cada etapa o tema que se trabajó._

**Pregunta:** `<la pregunta que se hizo>`

> `<la respuesta, con las palabras de la persona>`

**Repregunta:** `<la repregunta, si hizo falta>`

> `<la respuesta>`

- Resumen confirmado: `<sí, no o a medias>`
- Qué se escribió con esto: `<documentos y partes que se completaron o cambiaron>`

## Pendientes

_Lo que quedó sin saber, una línea por dato, con la forma `PENDIENTE: preguntar a <quién>`. Si no quedó nada, se escribe "Ninguno"._

## Documentos

_Los archivos que llegaron en la sesión, uno por línea, con la forma que corresponda. Del archivo que no se incorpora no se copia nada: esta línea es su único rastro. En una sesión de material de terceros, debajo de cada archivo incorporado van tres líneas más: quiénes participan, qué fechas cubre y cómo llegó._

- Incorporado: `<archivo>`, `<qué es>`. Quedó en `<carpeta>`.
- NO INCORPORADO: `<archivo>`, contiene datos personales de terceros.
- Para `<nombre del responsable del programa>`: `<archivo>`, `<qué hay que mirar>`.

## Documentos pendientes

_Lo que la persona dijo que iba a acercar y todavía no llegó. Se anota también en su hoja, en "Documentos prometidos"._

## Temas para otra sesión

_Lo que apareció y no era de esta sesión, una línea por tema. Lo que trata de un cambio que la empresa está haciendo empieza con `Cambio:` y dice quién lo contó._

## Cómo terminó

- Resumen final confirmado por la persona: `<sí, no o a medias>`
- Hasta dónde se llegó: `<última etapa o tema cerrado>`
- Estado en que quedó cada documento: `<documento y estado>`
- Próximo paso: `<qué sigue y con quién>`
- Subida: `<hecha, o sin servidor; queda en esta computadora>`
