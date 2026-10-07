# Plantilla para documentar cómo trabaja una empresa

*A template for documenting how a company actually works. An AI agent interviews people and writes process maps, SOP-style process sheets with flowcharts, and work instructions, under ISO 9001-style document control. Everything is Markdown and git. The method and the conversations are in Spanish.*

Esta plantilla sirve para relevar, es decir, averiguar y dejar por escrito, cómo trabaja una empresa: quién hace qué, con qué, cada cuánto y qué pasa cuando algo sale distinto de lo habitual. El trabajo lo conduce un agente de IA que conversa con las personas. Nadie tiene que llenar formularios ni aprender palabras técnicas.

Este trabajo se conoce también como relevamiento o levantamiento de procesos, mapeo de procesos o documentación de procesos. Lo que queda escrito es lo que muchas empresas llaman manual de procedimientos. Tiene un mapa de procesos, una ficha por cada proceso con su diagrama de flujo, e instructivos de trabajo. Cada ficha cumple la función de un procedimiento operativo estándar (SOP). Todo son archivos de texto en formato Markdown, en una carpeta con `git`.

## Para quién es

- Para una empresa de cualquier tamaño que quiere dejar escrito cómo trabaja, tenga o no procesos documentados.
- Para la persona que conduce ese trabajo, sea de la empresa o un consultor externo.
- Para quien quiere ordenar esa documentación según la norma IRAM-ISO 9001, sin pedir a las personas que aprendan su vocabulario. Incluye el control documental y la lista maestra que pide un sistema de gestión de la calidad.
- Para una pyme donde cómo se trabaja vive en la cabeza de pocas personas. Sirve para dejarlo escrito antes de que alguien se vaya, o para que alguien nuevo aprenda el trabajo.

La plantilla ayuda a ordenar la documentación. No certifica nada por sí sola. Qué cubre de la norma, qué cubre solo en parte y qué no cubre está en `metodo/norma.md`.

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
3. Permitir al agente, sin que pregunte cada vez, los comandos de `git` que usan `metodo/guardado.md` y `metodo/revision-y-aprobacion.md`, y la escritura dentro de `empresa/`. Para todo lo demás, que siga preguntando. Cada herramienta lo configura de una forma distinta. Sin este paso, el agente pide permiso en cada guardado.
4. Saludar. Con un "Hola" alcanza: el agente lee sus instrucciones y dice cómo seguir.

Cada empresa trabaja en su propio clon. La plantilla no guarda datos de ninguna empresa, y el clon de una empresa no debe subirse a la plantilla ni a un lugar público.

Quien prepara la carpeta le dice a la persona que conduce el trabajo cómo ubicarlo. Si algo del guardado falla, el agente va a pedir su ayuda.

## Cómo tener una copia en un servidor

Este paso no es obligatorio, pero conviene hacerlo: sin él, todo el trabajo queda guardado solo en la computadora donde se conversa con el agente.

Para tener además una copia en un servidor privado de la empresa, quien preparó el clon lo conecta una sola vez:

```
git remote add origin <dirección-del-repositorio-privado-de-la-empresa>
git push origin main:main main:borradores
```

Desde ese momento, el agente sube el trabajo al cerrar cada conversación. El repositorio de la empresa tiene que ser privado.

## Qué puede hacer hoy

La plantilla se construye por partes. Hoy tiene:

- El punto de entrada del agente, que revisa en qué estado está la carpeta y decide cómo seguir.
- Las reglas permanentes: registrar lo que pasa hoy, no inventar, cuidar los datos de las personas y conversar con palabras simples. La conversación sigue el lenguaje claro de la norma ISO 24495-1:2023.
- El guardado: el agente guarda el trabajo sin que la persona tenga que hacer nada.
- La estructura de la carpeta `empresa/`.
- El arranque: quien conduce el relevamiento conversa con el agente, y quedan escritos la empresa, sus áreas, sus personas y la lista de sus procesos, con las preguntas preparadas para cada persona. Lleva entre dos y tres horas, que se pueden repartir en varias conversaciones.
- Las entrevistas: cada persona cuenta cómo hace su trabajo, en conversaciones de unos 20 minutos, y el agente lo deja escrito en la ficha de cada proceso, con su diagrama.
- El material de otras personas: conversaciones exportadas, notas de reuniones, correos, capturas o audios transcriptos. El agente guarda una copia sin datos personales, anota lo que dicen sobre cada trabajo y prepara las preguntas para confirmarlo con quien corresponde.
- Los cambios en marcha: cuando la empresa cambia algo que altera cómo se trabaja, como un sistema nuevo o una reorganización, el agente lleva una ficha con el plan, las decisiones, lo que falta responder y lo que puede salir mal, hasta que lo nuevo se usa y queda escrito.
- El control de los documentos: cada documento lleva un código, una versión, un estado, quién lo aprobó y cuándo toca volver a mirarlo.
- Los moldes de cada documento: el contexto de la empresa, la hoja de cada persona, el mapa de procesos, la ficha de proceso, el instructivo, la lista de documentos, el glosario, la ficha de cambio, el catálogo de archivos y el registro de cada conversación. También hay un banco de preguntas para las entrevistas.
- La revisión y la aprobación: repasar lo relevado, confirmarlo, aprobarlo como versión oficial y volver a mirarlo cada cierto tiempo.
- La relación con la norma: qué parte cubre la plantilla y cuál no.

Con esto queda completa la primera parte de la plantilla. Para partes posteriores quedan el diagnóstico de lo relevado, las consultas del día a día y el apoyo a la dirección. Si alguien pide una parte que todavía no está, el agente lo dice con palabras simples.

## Qué hay en cada carpeta

| Carpeta o archivo | Qué es |
|---|---|
| `AGENTS.md` | Las instrucciones de entrada para el agente. |
| `CLAUDE.md` | Solo importa `AGENTS.md`, para los agentes que buscan ese nombre de archivo. |
| `metodo/` | Las instrucciones que sigue el agente: las reglas permanentes, el guardado, el control de los documentos, la relación con la norma y un archivo por cada modo de trabajo. |
| `plantillas/` | Un molde por cada tipo de documento que el agente crea en `empresa/`, y el banco de preguntas para las entrevistas. |
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
git config --local plantilla.mantenimiento true
```

La marca es local: no viaja al clonar. Con ella, el agente trata toda sesión en esa carpeta como mantenimiento del método y no empieza un relevamiento ahí.

Dos cuidados:

- La plantilla publicada nunca tiene una rama `borradores`. Esa rama existe solo en los clones.
- Nada de una empresa entra a la plantilla: ningún nombre real de empresa, persona, sistema o lugar, tampoco en los mensajes de guardado.

## Licencia

Licencia: pendiente de definir.
