# Guardado silencioso

El trabajo se guarda con git sin que la persona lo note. Este archivo es solo para el agente: a la persona nunca se le nombran ramas, guardados técnicos ni servidores, y nunca se le muestra un error.

## En una mirada

| Momento | Qué hacer | Sección |
|---|---|---|
| Al empezar la sesión | Quedar en la rama `borradores`, al día | "Al empezar cada sesión" |
| Al cerrar cada tema o etapa | Un guardado local con el mensaje de formato fijo | "Al cerrar cada tema o etapa" |
| Al cerrar la sesión | Guardado final y un solo intento de subida | "Al cerrar la sesión" |
| Si algo falla | Resolverlo en silencio o decirlo con palabras simples | "Qué decir a la persona" |

## Reglas fijas

1. Todas las sesiones escriben en una sola rama: `borradores`.
2. `main` tiene solo lo que el responsable del programa ya revisó. Una sesión nunca guarda en `main`, con una sola excepción: el modo de revisión y aprobación, que pasa a `main` lo revisado con los pasos de `metodo/revision-y-aprobacion.md`.
3. Antes de escribir cualquier archivo, comprobar la rama con `git branch --show-current`. Si no es `borradores`, cambiar antes de escribir.
4. El estado del trabajo se lee siempre en `borradores`. Ahí está lo que contaron todas las personas.
5. Se guarda solo lo que está dentro de `empresa/`. Los cambios fuera de esa carpeta no se guardan ni se deshacen. Si aparecen, anotarlo en `empresa/notas-para-el-metodo.md`.
6. No usar `git commit --amend`, `git push --force` ni `git reset`.
7. Ejecutar los comandos sin comentarlos, con `--quiet` cuando la opción existe.

## Cuándo hay servidor

Hay servidor solo si se cumplen las dos condiciones:

1. Existe el remoto `origin`: `git remote` lo muestra.
2. Después de `git fetch --quiet origin`, existe la rama `origin/borradores`: `git rev-parse --verify --quiet origin/borradores` devuelve un resultado.

En cualquier otro caso se trabaja sin servidor. Todo queda en esta computadora, y los pasos de poner al día y de subir se saltan en silencio.

El agente nunca crea `borradores` en el servidor y nunca sube nada a un remoto que no sea `origin`. Motivo: un clon nuevo tiene como `origin` a la plantilla, y subir ahí publicaría datos de la empresa. La rama `borradores` del servidor la crea una persona, una sola vez, al preparar el lugar donde la empresa guarda su copia.

## Al empezar cada sesión

Hacerlo apenas empieza la conversación, antes de leer nada de `empresa/`. En silencio.

1. Recordar en qué rama está la carpeta: `git branch --show-current`.
2. Si existe el remoto `origin`, traer lo último: `git fetch --quiet origin`. Si falla, seguir igual.
3. Quedar en `borradores`, según la situación:

   | Situación | Comando |
   |---|---|
   | `borradores` existe en esta computadora | `git switch --quiet borradores` |
   | No existe en esta computadora y existe `origin/borradores` | `git switch --quiet -c borradores --track origin/borradores` |
   | No existe en ningún lado: es la primera sesión de esta copia | `git switch --quiet -c borradores` |

   En la primera sesión, la rama se crea desde donde está la carpeta. En un clon nuevo, eso es `main`.
4. Si `borradores` ya existía y quedaron cambios sin guardar dentro de `empresa/` (`git status --porcelain -- empresa/` los muestra), no borrarlos. Guardarlos con los pasos 2 y 3 de "Al cerrar cada tema o etapa" y el mensaje `docs: cambios sin guardar de una sesión anterior`.
5. Si hay servidor, poner `borradores` al día: `git rebase --quiet --autostash --rebase-merges origin/borradores`. Si aparece un conflicto, deshacerlo de inmediato con `git rebase --abort` y seguir con lo que hay en esta computadora.
6. Si no se logra quedar en `borradores`, no escribir nada. Decir a la persona la frase de "No se puede guardar hoy" y terminar ahí. Vale también cuando la carpeta no tiene git.

## Al cerrar cada tema o etapa

Se guarda después de que la persona confirmó el resumen y de que los archivos quedaron escritos.

1. Comprobar que la rama es `borradores`.
2. Preparar solo la carpeta de la empresa: `git add -- empresa/`.
3. Guardar: `git commit --quiet -m "<mensaje>"`, con el mensaje que indica "Formato de los mensajes".

- Un solo guardado por tema o etapa, al cerrarlo. No uno por pregunta ni por corrección.
- Si no hay nada nuevo para guardar, seguir sin avisar.
- Este guardado es local. No se sube nada hasta el cierre de la sesión.

### Si un guardado falla

| Causa | Qué hacer |
|---|---|
| La computadora no tiene configurado quién guarda: `git config user.name` no devuelve nada | Configurarlo solo para esta carpeta, con los valores neutros de abajo, y repetir el guardado. |
| Otra causa que no se logra resolver | No detener la conversación. Lo escrito queda en los archivos y se guarda al empezar la próxima sesión. |

```
git config user.name "Relevamiento de procesos"
git config user.email "relevamiento@empresa.invalid"
```

No usar datos personales en esa configuración. Si ya hay una identidad configurada, no cambiarla.

## Formato de los mensajes

Todos los guardados usan el mismo formato:

```
docs(<ámbito>): <asunto> - <cierre> con <nombre>
```

| Parte | Qué va |
|---|---|
| `<ámbito>` | El área del trabajo, escrita como en las rutas de `empresa/`. Si el trabajo no es de un área, `empresa`. |
| `<asunto>` | El nombre del proceso, o de lo que se trabajó, en minúsculas. |
| `<cierre>` | Lo que se cerró: `tema <letra>`, `etapa <número>` o `cierre de sesión`. |
| `<nombre>` | El nombre de pila de la persona con la que se trabajó. |

| Momento | Mensaje |
|---|---|
| Cierre de un tema | `docs(<ámbito>): <asunto> - tema <letra> con <nombre>` |
| Cierre de una etapa | `docs(<ámbito>): <asunto> - etapa <número> con <nombre>` |
| Archivos recibidos | `docs(<ámbito>): <asunto> - archivos aportados por <nombre>` |
| Cierre de la sesión | `docs(<ámbito>): <asunto> - cierre de sesión con <nombre>` |
| Subida que no se pudo hacer | `docs(<ámbito>): <asunto> - subida pendiente` |
| Cambios de una sesión anterior | `docs: cambios sin guardar de una sesión anterior` |

Ejemplo: `docs(ventas): presupuesto a un cliente - tema B con <nombre>`.

- El mensaje va en español neutro, en una sola línea y sin punto final.
- Sin firmas ni líneas de autoría de ningún asistente o herramienta.
- Solo nombre de pila. Nunca apellidos ni datos de terceros.

## Al cerrar la sesión

1. Si la sesión lleva registro en `empresa/sesiones/`, completar su línea de subida antes del guardado final:
   - Con servidor: `Subida: hecha`.
   - Sin servidor: `Subida: sin servidor; queda en esta computadora`.
2. Hacer el guardado final, con el mensaje de cierre de la sesión.
3. Sin servidor, terminar ahí. El trabajo queda en esta computadora.
4. Con servidor, intentar subir una sola vez, en este orden:

   ```
   git fetch --quiet origin
   git rebase --quiet --autostash --rebase-merges origin/borradores
   git push --quiet origin borradores
   ```

5. Si el `rebase` da conflicto, deshacerlo de inmediato con `git rebase --abort`, para que nada quede a medias. Lo guardado sigue en esta computadora. Seguir con "Si no se puede subir".
6. Si la subida falla por cualquier motivo, como falta de conexión o de acceso, seguir con "Si no se puede subir".

### Si no se puede subir

- No insistir. Lo guardado en esta computadora no se pierde, y sube en la próxima sesión que logre subir.
- Si la sesión lleva registro, cambiar su línea de subida por `SUBIDA PENDIENTE: quedó solo en esta computadora`. Guardar ese cambio con un guardado nuevo, con el mensaje de subida pendiente.
- Decir con calma la frase de "No se pudo subir".

## Qué decir a la persona

| Situación | Frase |
|---|---|
| Se guardó | "Listo, quedó guardado." |
| No se pudo subir | "Quedó guardado en esta computadora." |
| No se puede guardar hoy | "Hoy tengo un problema para guardar lo que conversemos y prefiero no seguir así. Conviene avisar a `<nombre del responsable del programa>`. Disculpas por la molestia." |

- Si quien habla es el responsable del programa, en la última frase reemplazar el pedido de avisar por: "Conviene pedir ayuda a quien preparó esta carpeta."
- Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
- Nunca decir "commit", "rama", "repositorio", "push" ni "servidor". Nunca mostrar la salida de un comando ni un mensaje de error.

## Cuándo no se aplica

En el mantenimiento del método, descrito en `AGENTS.md`, este archivo no se usa: quien mantiene decide cómo guarda. Si la sesión ya había preparado el guardado antes de saberlo:

1. Volver a la rama en la que estaba la carpeta: `git switch --quiet <rama anterior>`.
2. Si `borradores` se creó en esta sesión, borrarla: `git branch -d borradores`. Si no se puede borrar, avisar a quien mantiene.
