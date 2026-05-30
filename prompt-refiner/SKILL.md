---
name: prompt-refiner
description: Refina y mejora un prompt escrito por el usuario, de forma explícita y solo cuando se solicita. Activar cuando el usuario use frases como "refiná este prompt", "mejorá este prompt", "refine this prompt", "/refine", "quiero mejorar este prompt", "optimizá este prompt", o cuando pegue un prompt y pida que lo mejore. NO activar para cualquier consulta genérica — solo cuando hay una intención clara de mejorar un prompt específico.
---

# Prompt Refiner

## Objetivo

Tomar un prompt escrito por el usuario y devolver una versión mejorada, sin ejecutarlo. El output es el prompt refinado, listo para ser copiado y usado.

## Cuándo activar

Solo cuando el usuario lo pide explícitamente. Señales claras:
- "refiná este prompt"
- "mejorá este prompt"
- "/refine [prompt]"
- "quiero mejorar este prompt"
- "optimizá este prompt"
- pega un prompt y pide explícitamente que lo mejore

## Proceso de refinamiento

Analizá el prompt original aplicando todas estas dimensiones:

### 1. Claridad de objetivo
- ¿Qué quiere lograr el usuario con este prompt?
- ¿El objetivo está explícito o implícito?
- Si está implícito, hacerlo explícito en el prompt refinado.

### 2. Contexto
- ¿Falta información de fondo que el modelo necesitaría para responder bien?
- Agregar rol, dominio, situación o restricciones relevantes cuando aplique.

### 3. Instrucciones precisas
- ¿Las instrucciones son ambiguas o genéricas?
- Reemplazar términos vagos ("analiza", "explica") con instrucciones concretas y accionables.

### 4. Formato de output esperado
- ¿El usuario especificó cómo quiere la respuesta? (lista, tabla, párrafo, longitud, idioma)
- Si no lo especificó, inferirlo del contexto y agregarlo.

### 5. Detección de ambigüedades
- Identificar palabras o frases que pueden interpretarse de más de una forma.
- Resolverlas explícitamente en el prompt refinado.

### 6. Completitud
- ¿Falta algún dato clave que el modelo necesitaría para responder? (fechas, nombres, cantidades, fuentes)
- Si falta algo que el usuario podría proveer, señalarlo como un `[COMPLETAR: ...]` dentro del prompt refinado.

## Formato de output

Devolver **solo** el prompt refinado, dentro de un bloque de código para facilitar la copia. 

Después del bloque, agregar una sección breve titulada **Cambios aplicados** con bullets concisos explicando qué se modificó y por qué. Máximo 6 bullets.

Si el prompt original ya es muy bueno y los cambios son menores, indicarlo.

## Ejemplo

**Input del usuario:**
> refiná este prompt: "explicame machine learning"

**Output:**

```
Explicá qué es machine learning de forma clara y sin jerga técnica innecesaria. 
Incluí: (1) una definición en una oración, (2) cómo funciona a nivel conceptual usando 
una analogía cotidiana, (3) tres casos de uso reales y concretos. 
Extensión: máximo 300 palabras. Idioma: español.
```

**Cambios aplicados:**
- Agregado formato de output explícito (3 secciones numeradas)
- Especificada extensión máxima para evitar respuestas excesivas
- Pedida analogía cotidiana para mejorar comprensión
- Especificado idioma
- Reemplazado "explicame" (vago) por instrucción estructurada
