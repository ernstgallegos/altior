# ALTIOR | Asistente Estratégico para Profesionales de Ciencia, Tecnología e Innovación

ALTIOR es un asistente impulsado por técnicas avanzadas de prompt engineering, diseñado para acompañar a profesionales críticos en la sistematización, automatización y comunicación de ideas.

Este repositorio contiene el diseño, lógica funcional y casos de uso de ALTIOR, un microagente con capacidades narrativas, analíticas y estructurales, orientado a profesionales que operan en el cruce entre conocimiento, territorio y política pública.

---

## ¿Qué hace ALTIOR?

- Redacta [fichas de proyectos](./prompts/altior-proyectos.md) y propuestas estratégicas.
- Resume y estructura [informes ejecutivos](./prompts/altior-informes.md).
- Sugiere y mejora [posteos para LinkedIn](./prompts/altior-linkedin.md) con identidad crítica.
- [Clasifica ideas](./prompts/altior-clasificador-tematico.md), destaca conceptos clave, y propone estructuras narrativas.
- [Evalúa impacto](./prompts/altior-evaluador-impacto.md) potencial de iniciativas tecnológicas o sociales.
- Se integra a flujos con Notion, Zapier, Airtable o APIs ([ver ejemplo](./flujo-api/ejemplo-integracion-zapier.md)).

---

## Público destinatario

Profesionales de 30 a 55 años con formación en ciencia, tecnología, innovación, gestión pública o pensamiento crítico. Especialmente orientado a contextos como:

- Universidades
- Agencias estatales
- Organizaciones del conocimiento
- Consultoría independiente
- Escritura de proyectos de base tecnológica o social

---

## Estructura del repositorio

```
altior/
├── README.md
├── prompts/
│   ├── altior-agente-base.md
│   ├── altior-proyectos.md
│   ├── altior-informes.md
│   ├── altior-linkedin.md
│   ├── altior-clasificador-tematico.md
│   └── altior-evaluador-impacto.md
├── casos/
│   ├── caso-ficha-pyme-social.md
│   ├── informe-productividad.md
│   └── linkedin-sobre-el-tiempo.md
├── templates/
│   ├── ficha-proyecto.md
│   ├── informe-base.md
│   └── encabezado-posteo.md
├── flujo-api/
│   ├── ejemplo-integracion-zapier.md
│   └── payload-api-openai.md
└── docs/
    ├── altior-gpt.md
    └── roadmap.md
```

---

## Cómo usar ALTIOR

Podés interactuar con ALTIOR:

- Desde este repositorio (copiando y adaptando [prompts funcionales](./prompts/altior-agente-base.md))
- A través de herramientas como Notion + Zapier + OpenAI ([ver integración](./flujo-api/ejemplo-integracion-zapier.md))
- Integrando la lógica a tus flujos de redacción o análisis con la [API de OpenAI](./flujo-api/payload-api-openai.md)
- Como base para un [GPT personalizado público](./docs/altior-gpt.md)

---

## Autor

Creado por **Ernesto Gallegos**, como proyecto final del Curso Intensivo de Prompt Engineering Aplicado.

Más sobre el autor:
- [github.com/ernstgallegos](https://github.com/ernstgallegos)
- [linktr.ee/ernstgallegos](https://linktr.ee/ernstgallegos)
- [Newsletter: Quiero Creer](https://quierocreer.substack.com)

---

## Licencia

Este proyecto está liberado bajo licencia MIT. Podés utilizarlo, adaptarlo y expandirlo libremente, dando el crédito correspondiente.
