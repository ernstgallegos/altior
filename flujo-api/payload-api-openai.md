# Ejemplo de payload para usar módulos de ALTIOR con la API de OpenAI

Este documento muestra cómo estructurar una solicitud (`payload`) para utilizar un módulo de ALTIOR directamente a través de la API de OpenAI. Es útil para desarrolladores, integradores o usuarios avanzados que quieran automatizar procesos con mayor control.

---

## Requisitos
- Clave de API de OpenAI (https://platform.openai.com/account/api-keys)
- Entorno con capacidad para enviar solicitudes HTTP (`curl`, Postman, Python, etc.)

---

## Endpoint
```
POST https://api.openai.com/v1/chat/completions
```

---

## Payload básico (ejemplo con módulo `altior-informes`)

```json
{
  "model": "gpt-4",
  "temperature": 0.4,
  "messages": [
    {
      "role": "system",
      "content": "Actuás como ALTIOR, un asistente estratégico con experiencia en redacción de informes ejecutivos para ciencia, tecnología e innovación."
    },
    {
      "role": "user",
      "content": "Redactá un resumen ejecutivo a partir del siguiente informe:\n\n[PEGA AQUÍ EL TEXTO DEL INFORME]\n\nFormato: - 5 bullets clave - conclusión de dos líneas."
    }
  ]
}
```

---

## Headers necesarios
```http
Authorization: Bearer TU_API_KEY
Content-Type: application/json
```

---

## Sugerencias de uso
- Limitar el contenido del informe a menos de 3.000 palabras (por límite de tokens)
- Encapsular el módulo de ALTIOR que se use dentro del mensaje `system` y el `user`
- Agregar validación o fallback en caso de respuestas incompletas

---

## Variantes posibles
- Cambiar el `content` según el módulo: `altior-proyectos`, `altior-linkedin`, etc.
- Modificar el `temperature` según el nivel de creatividad o formalidad deseado

---

Este ejemplo puede combinarse con herramientas como Zapier, Make, Retool o apps personalizadas.
