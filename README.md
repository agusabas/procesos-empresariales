# Plantilla para documentar cómo trabaja una empresa

Esta plantilla sirve para relevar, es decir, averiguar y dejar por escrito, cómo trabaja una empresa: quién hace qué, con qué, cada cuánto y qué pasa cuando algo sale distinto de lo habitual. El trabajo lo conduce un agente de IA que conversa con las personas. Nadie tiene que llenar formularios ni aprender palabras técnicas.

## Para quién es

- Para una empresa de cualquier tamaño que quiere dejar escrito cómo trabaja, tenga o no procesos documentados.
- Para la persona que conduce ese trabajo, sea de la empresa o un consultor externo.
- Para quien quiere ordenar esa documentación según la norma IRAM-ISO 9001, sin pedir a las personas que aprendan su vocabulario.

La plantilla ayuda a ordenar la documentación. No certifica nada por sí sola.

## Cómo empezar

Hace falta tener instalado `git` y contar con un agente de IA que lea el archivo `AGENTS.md` y que pueda leer y escribir archivos en una carpeta.

1. Clonar la plantilla en una carpeta nueva. Se hace una vez por empresa:

   ```
   git clone <dirección-de-la-plantilla> <carpeta-de-la-empresa>
   cd <carpeta-de-la-empresa>
   git remote rename origin plantilla
   ```

   La última línea deja anotado dónde está la plantilla con el nombre `plantilla`. Así el clon puede recibir mejoras del método, y el trabajo de la empresa nunca se sube a la plantilla.

2. Abrir esa carpeta con el agente de IA.
3. Saludar. Con un "Hola" alcanza: el agente lee sus instrucciones y dice cómo seguir.

Cada empresa trabaja en su propio clon. La plantilla no guarda datos de ninguna empresa, y el clon de una empresa no debe subirse a la plantilla ni a un lugar público.

## Cómo tener una copia en un servidor

Este paso es opcional. Sin él, todo el trabajo queda guardado solo en la computadora donde se conversa con el agente.

Para tener además una copia en un servidor privado de la empresa, quien preparó el clon lo conecta una sola vez:

```
git remote add origin <dirección-del-repositorio-privado-de-la-empresa>
git push origin main:main main:borradores
```

Desde ese momento, el agente sube el trabajo al cerrar cada conversación. El repositorio de la empresa tiene que ser privado.

## Qué puede hacer hoy

La plantilla se construye por partes. Hoy tiene la base:

- El punto de entrada del agente, que revisa en qué estado está la carpeta y decide cómo seguir.
- Las reglas permanentes: registrar lo que pasa hoy, no inventar, cuidar los datos de las personas y conversar con palabras simples.
- El guardado: el agente guarda el trabajo sin que la persona tenga que hacer nada.
- La estructura de la carpeta `empresa/`.

Todavía no incluye las instrucciones para conducir las conversaciones ni los moldes de los documentos. Por eso el relevamiento aún no puede empezar: si alguien saluda al agente, este responde con palabras simples que esa parte todavía no está disponible.

## Qué hay en cada carpeta

| Carpeta o archivo | Qué es |
|---|---|
| `AGENTS.md` | Las instrucciones de entrada para el agente. |
| `CLAUDE.md` | Solo importa `AGENTS.md`, para los agentes que buscan ese nombre de archivo. |
| `metodo/` | Las instrucciones que sigue el agente. Hoy contiene `metodo/reglas.md` y `metodo/guardado.md`. |
| `plantillas/` | Un molde por cada tipo de documento. Todavía no hay ninguno, y por eso la carpeta aún no aparece. |
| `empresa/` | Todo lo que se releva de la empresa. En la plantilla está vacía. Su estructura se explica en `empresa/README.md`. |

En un clon, el agente escribe solo dentro de `empresa/`. Todo lo demás es el método y no se edita.

## Cómo traer mejoras del método a un clon

Cuando la plantilla mejora, cada clon puede recibir esas mejoras. Lo hace quien preparó el clon, en un momento en que no haya una conversación en curso.

1. Comprobar que el clon sabe dónde está la plantilla: `git remote` tiene que mostrar `plantilla`. Si no aparece, agregarla. Se hace una sola vez:

   ```
   git remote add plantilla <dirección-de-la-plantilla>
   ```

2. Traer las mejoras:

   ```
   git switch main
   git pull --no-rebase --no-edit plantilla main
   ```

3. Pasarlas a `borradores`, la rama donde el agente guarda el trabajo de todos los días. Si esa rama todavía no existe, este paso no hace falta:

   ```
   git switch borradores
   git merge --no-edit main
   ```

No hay conflictos, porque en un clon solo se escribe dentro de `empresa/` y las mejoras de la plantilla no tocan lo que la empresa escribió ahí.

## Para quien mantiene la plantilla

Quien mantiene la plantilla marca su copia de trabajo una sola vez:

```
git config plantilla.mantenimiento true
```

La marca es local: no viaja al clonar. Con ella, el agente trata toda sesión en esa carpeta como mantenimiento del método y no empieza un relevamiento ahí.

Dos cuidados:

- La plantilla publicada nunca tiene una rama `borradores`. Esa rama existe solo en los clones.
- Nada de una empresa entra a la plantilla: ningún nombre real de empresa, persona, sistema o lugar, tampoco en los mensajes de guardado.

## Licencia

Licencia: pendiente de definir.
