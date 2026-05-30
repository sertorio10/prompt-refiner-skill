# 🔧 prompt-refiner — Claude Cowork Skill

> **Turns vague prompts into precise, structured ones — automatically.**  
> **Convierte prompts vagos en instrucciones precisas y estructuradas — automáticamente.**

---

## English

### What it does

`prompt-refiner` is a skill for [Claude Cowork](https://claude.ai) that takes any prompt you write and returns an improved version — without executing it. The output is a refined, ready-to-copy prompt.

It only activates when you explicitly ask for it, so it never gets in the way of your normal workflow.

### Before / After

**Before:**
> "explain machine learning"

**After:**
```
Explain what machine learning is clearly and without unnecessary technical jargon.
Include: (1) a one-sentence definition, (2) how it works conceptually using an everyday analogy,
(3) three real, concrete use cases.
Length: maximum 300 words. Language: English.
```

### How to install

1. Download this repo as a ZIP
2. Rename the ZIP file to `prompt-refiner.skill`
3. Drag it into Claude Cowork

### How to use

Trigger it with phrases like:
- `refine this prompt: [your prompt]`
- `improve this prompt`
- `/refine [your prompt]`

### What it improves

| Dimension | What it checks |
|---|---|
| **Objective clarity** | Is the goal explicit or implicit? |
| **Context** | Is background info missing? |
| **Precise instructions** | Are there vague terms like "explain" or "analyze"? |
| **Output format** | Length, language, structure specified? |
| **Ambiguities** | Can any phrase be interpreted multiple ways? |
| **Completeness** | Are key details missing? Marks them as `[FILL IN: ...]` |

---

## Español

### Qué hace

`prompt-refiner` es un skill para [Claude Cowork](https://claude.ai) que toma cualquier prompt que escribas y devuelve una versión mejorada — sin ejecutarlo. El output es el prompt refinado, listo para copiar y usar.

Solo se activa cuando lo pedís explícitamente, así no interfiere con tu flujo normal de trabajo.

### Antes / Después

**Antes:**
> "explicame machine learning"

**Después:**
```
Explicá qué es machine learning de forma clara y sin jerga técnica innecesaria.
Incluí: (1) una definición en una oración, (2) cómo funciona a nivel conceptual usando
una analogía cotidiana, (3) tres casos de uso reales y concretos.
Extensión: máximo 300 palabras. Idioma: español.
```

### Cómo instalar

1. Descargá este repo como ZIP
2. Renombrá el archivo ZIP a `prompt-refiner.skill`
3. Arrastralo a Claude Cowork

### Cómo usar

Activalo con frases como:
- `refiná este prompt: [tu prompt]`
- `mejorá este prompt`
- `/refine [tu prompt]`

### Qué mejora

| Dimensión | Qué revisa |
|---|---|
| **Claridad de objetivo** | ¿El objetivo está explícito o implícito? |
| **Contexto** | ¿Falta información de fondo? |
| **Instrucciones precisas** | ¿Hay términos vagos como "explicá" o "analizá"? |
| **Formato de output** | ¿Especificó longitud, idioma, estructura? |
| **Ambigüedades** | ¿Alguna frase se puede interpretar de más de una forma? |
| **Completitud** | ¿Faltan datos clave? Los marca como `[COMPLETAR: ...]` |

---

## License / Licencia

MIT — free to use, share, and modify.  
MIT — libre para usar, compartir y modificar.
