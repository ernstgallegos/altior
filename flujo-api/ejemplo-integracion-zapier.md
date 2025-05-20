# Ejemplo de integración de ALTIOR con Zapier + Notion + OpenAI

Este documento describe un flujo básico para automatizar el uso de un módulo de ALTIOR (por ejemplo, `altior-informes.md`) utilizando herramientas nocode.

---

## Objetivo del flujo

Generar automáticamente un resumen ejecutivo cuando se carga un nuevo informe o texto largo en una base de datos de Notion.

---

## Herramientas necesarias

- [Zapier](https://zapier.com)
- [Notion](https://notion.so) (con tabla/base de datos estructurada)
- [OpenAI API key](https://platform.openai.com/account/api-keys)
- Prompt funcional (como el de `altior-informes.md`)

---

## Paso a paso

### 🔹 Paso 1 – Estructurar base de datos en Notion

Creá una tabla con los siguientes campos:
- Título del informe
- Contenido del informe (texto largo)
- Resumen generado (campo vacío que se llenará automáticamente)

### 🔹 Paso 2 – Crear el Zap

1. **Trigger:** “New Database Item in Notion”
   - Seleccioná la base de datos creada.

2. **Action:** “Formatter by Zapier” (opcional)
   - Usalo si necesitás limpiar texto, cortar longitud o concatenar campos.

3. **Action:** “OpenAI”
   - Modelo: `gpt-4`
   - Prompt: Pegá el texto completo del prompt de `altior-informes.md`, reemplazando la parte del input con un campo dinámico de Zapier (`{{Contenido del informe}}`).
   - Temperatura: 0.4 (para respuestas más sobrias y estables)

4. **Action final:** “Update Database Item in Notion”
   - Escribí el resultado de OpenAI en el campo “Resumen generado”.

### 🔹 Paso 3 – Testear y activar

Verificá que el resumen aparezca en Notion luego de ingresar un nuevo registro.

---

## Recomendaciones

- Limitar la longitud del texto si usás modelos con tokens restringidos.
- Asegurarte de usar prompts bien estructurados y con formato de salida claro.
- Guardar logs o duplicados de los outputs para control de calidad.

---

Este flujo puede replicarse con otros módulos de ALTIOR, como los de LinkedIn, proyectos o clasificador temático.
