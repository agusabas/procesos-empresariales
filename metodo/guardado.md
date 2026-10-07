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
5. Se guarda solo lo que está dentro de `empresa/`. Los cambios fuera de esa carpeta no se guardan ni se deshacen. Si aparecen, y `empresa/contexto.md` ya existe, anotarlo en `empresa/notas-para-el-metodo.md`.
6. No usar `git commit --amend`, `git push --force` ni `git reset`.
7. Ejecutar los comandos sin comentarlos, con `--quiet` cuando la opción existe.
8. Algunas herramientas muestran cada comando a la persona, o piden una descripción de lo que hace. Esa descripción va en palabras simples, sin términos técnicos y en el idioma de la persona. Por ejemplo: "Guardar el trabajo".

## Cuándo hay servidor

Hay servidor solo si se cumplen las dos condiciones:

1. Existe el remoto `origin`: `git remote` lo muestra. Los remotos con otro nombre no se miran.
2. Después de `git fetch --quiet origin`, existe la rama `borradores` del servidor: `git rev-parse --verify --quiet refs/remotes/origin/borradores` devuelve un resultado.

En cualquier otro caso se trabaja sin servidor. Todo queda en esta computadora, y los pasos de poner al día y de subir se saltan en silencio.

Tampoco hay servidor cuando una regla de seguridad de la computadora exige, para trabajar con servidores, una autorización que no fue dada. En ese caso no se trae ni se sube nada. Al cerrar la sesión se dice una sola vez la frase de "No se usa el servidor", y se anota en el registro de la sesión que se dijo. No se repite si un registro de sesión anterior ya anota que se dijo.

El agente nunca crea `borradores` en el servidor y nunca sube nada a un remoto que no sea `origin`. Motivo: si al clonar se salteó el paso que le cambia el nombre a `origin`, que indica `README.md`, `origin` sigue siendo la plantilla, y subir ahí publicaría datos de la empresa. La rama `borradores` del servidor la crea una persona, una sola vez, al preparar el lugar donde la empresa guarda su copia.

## Al empezar cada sesión

Hacerlo apenas empieza la conversación, antes de leer nada de `empresa/`. En silencio.

1. Recordar en qué rama está la carpeta: `git branch --show-current`.
2. Si existe el remoto `origin`, y ninguna regla de seguridad lo impide, traer lo último: `git fetch --quiet origin`. Si falla, seguir igual.
3. Quedar en `borradores`, según la situación. La rama existe en esta computadora si `git rev-parse --verify --quiet refs/heads/borradores` devuelve un resultado. Existe en el servidor si lo devuelve `git rev-parse --verify --quiet refs/remotes/origin/borradores`. Los remotos que no se llaman `origin` no se miran.

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

- Un solo guardado por tema o etapa, al cerrarlo. No uno por pregunta ni por corrección. Tampoco uno por cada archivo recibido ni por cada código asignado: todo lo que el tema o la etapa escribió va en ese guardado.
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
| Archivos que llegan fuera de un tema o de una etapa | `docs(<ámbito>): <asunto> - archivos aportados por <nombre>` |
| Cierre de la sesión | `docs(<ámbito>): <asunto> - cierre de sesión con <nombre>` |
| Subida que no se pudo hacer | `docs(<ámbito>): <asunto> - subida pendiente` |
| Cambios de una sesión anterior | `docs: cambios sin guardar de una sesión anterior` |

Ejemplo: `docs(ventas): presupuesto a un cliente - tema B con <nombre>`.

- Un archivo que llega dentro de un tema o de una etapa se guarda con el cierre de ese tema o de esa etapa. El mensaje de archivos aportados se usa solo cuando el archivo llega fuera de uno. El archivo de cada modo dice si lo usa.
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
| No se usa el servidor | "Un aviso: el trabajo queda guardado solo en esta computadora. Conviene avisar a quien preparó esta carpeta." |

- En la frase de "No se puede guardar hoy", si quien habla es el responsable del programa, o si todavía no se sabe quién es, reemplazar el pedido de avisar por: "Conviene pedir ayuda a quien preparó esta carpeta."
- Las frases están en forma neutra. Adaptarlas a la forma de trato, como indica la regla 8 de `metodo/reglas.md`.
- Nunca decir "commit", "rama", "repositorio", "push" ni "servidor". Nunca mostrar la salida de un comando ni un mensaje de error.

## Cuándo no se aplica

En el mantenimiento del método, descrito en `AGENTS.md`, este archivo no se usa: quien mantiene decide cómo guarda. Si la sesión ya había preparado el guardado antes de saberlo, o si quedó una rama `borradores` de un saludo anterior:

1. Volver a la rama en la que estaba la carpeta: `git switch --quiet <rama anterior>`. Si no se sabe cuál era, preguntarlo a quien mantiene.
2. Si `borradores` existe y no tiene `empresa/contexto.md`, borrarla: `git branch -d borradores`. Se comprueba con `git cat-file -e borradores:empresa/contexto.md`, que en ese caso falla.
3. Si git se niega a borrarla, porque tiene algo guardado que no está en otra rama, no insistir y avisar a quien mantiene.

Si `borradores` tiene `empresa/contexto.md`, la carpeta es el clon de una empresa en uso. Ahí no hay mantenimiento y la rama no se toca.
