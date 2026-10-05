> **Nota para el agente.** Este molde se copia a `empresa/lista-maestra.md` la primera vez que hace falta asignar un código. Es un documento de trabajo: no lleva bloque de control. En la copia, cada comodín (lo que va entre `<` y `>`) se reemplaza junto con las comillas invertidas que lo rodean. Un plazo que todavía no se definió se escribe `PENDIENTE: preguntar a <responsable del programa>`. Esta nota se borra de la copia. Cómo se asigna un código y cómo se concilia esta lista está en `metodo/control-documental.md`.

# Lista maestra

- **Última actualización:** `<AAAA-MM-DD>`

Esta lista reúne todos los documentos controlados de la empresa y los registros que se guardan. Los códigos se asignan solo desde aquí. Si esta lista y el bloque de control de un documento no coinciden, vale el bloque.

## Documentos controlados

Una fila por documento, ordenadas por código. Las filas no se borran: un documento que ya no se usa queda con estado `obsoleto`. La ubicación se escribe a partir de la carpeta `empresa/`.

| Código | Título | Tipo | Área | Estado | Versión | Vigente desde | Próxima revisión | Elaboró | Revisó | Aprobó | Ubicación | Observaciones |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CT-GEN-001 | Contexto de la empresa | CT | GEN | pendiente | 0 | — | — | — | — | — | `contexto.md` | |
| GL-GEN-001 | Glosario | GL | GEN | pendiente | 0 | — | — | — | — | — | `glosario.md` | |
| MP-GEN-001 | Mapa de procesos | MP | GEN | pendiente | 0 | — | — | — | — | — | `mapa-de-procesos.md` | |

## Registros

Qué se guarda como registro, dónde y por cuánto tiempo. Un registro no se edita una vez cerrado. Los registros propios de cada proceso figuran en su ficha, en "Qué registro queda".

| Registro | Qué se guarda | Dónde | Por cuánto tiempo |
|---|---|---|---|
| Sesiones | El registro de cada conversación | `sesiones/` | `<plazo>` |
| Insumos | El material original, tal como se recibió | `insumos/` | `<plazo>` |
| Adjuntos | Los archivos aportados durante las sesiones | `adjuntos/` | `<plazo>` |
