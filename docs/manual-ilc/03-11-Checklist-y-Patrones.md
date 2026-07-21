# 03.11 – Checklist y Patrones

## Objetivo

Este capítulo consolida los controles de calidad y patrones reutilizables para diseñar Prompts Maestros consistentes, verificables y fáciles de adaptar a distintos casos de uso.

---

## Checklist integral

### Caso de negocio

- El problema está descrito como una situación observable.
- Se identifican usuarios, proceso actual y resultado esperado.
- El beneficio puede medirse.
- El uso de IA está justificado.

### Rol y objetivo

- El rol es específico y no excede su autoridad.
- El objetivo indica a quién ayuda, qué transforma y qué entrega.
- Los límites y criterios de aceptación están definidos.

### Entradas

- Las entradas obligatorias y opcionales están separadas.
- Se indican formatos y ejemplos.
- Existe una regla para información faltante.
- Se controla el uso de datos sensibles.

### Proceso

- El trabajo está dividido en pasos verificables.
- Se diferencian hechos, supuestos y recomendaciones.
- Se aplican reglas de negocio.
- Se valida antes de entregar.
- Las decisiones críticas permanecen bajo control humano.

### Formato de salida

- La estructura y secciones obligatorias están definidas.
- El resultado es claro, consistente y reutilizable.
- Se identifican datos faltantes, supuestos y nivel de confianza.

### Restricciones y validaciones

- Se define lo que el GPT no debe hacer.
- Se limita alcance y autoridad.
- Se prohíbe inventar información.
- Se valida completitud, consistencia, formato y cobertura.
- Se verifica el cumplimiento de restricciones.

### Incertidumbre y mejora continua

- El GPT formula preguntas concretas cuando faltan datos.
- No completa vacíos con suposiciones ocultas.
- Puede escalar a revisión humana.
- Se conservan versiones, pruebas, errores y cambios.

---

## Patrón base ILC

```markdown
# Rol
Define quién es el GPT y qué experiencia debe aplicar.

# Objetivo
Define a quién ayuda, qué transforma, qué entrega y con qué límites.

# Contexto
Describe organización, proceso, reglas y propósito.

# Entradas
Diferencia información obligatoria, opcional y formatos aceptados.

# Proceso
Descompone el trabajo en pasos verificables.

# Formato de salida
Define exactamente cómo debe entregarse el resultado.

# Restricciones
Establece lo que el GPT no puede hacer.

# Validaciones
Controla completitud, consistencia, cobertura y calidad.

# Manejo de incertidumbre
Define cómo actuar cuando falta evidencia.

# Mejora continua
Registra oportunidades de mejora bajo control humano.
```

---

## Patrón de información faltante

```text
1. Identifica la información crítica faltante.
2. Explica por qué es necesaria.
3. Formula preguntas concretas.
4. No solicites datos innecesarios.
5. No inventes valores.
6. Entrega un avance parcial solo cuando sea seguro hacerlo.
```

---

## Patrón de hechos y supuestos

```markdown
## Hechos confirmados

## Supuestos

## Información pendiente

## Recomendaciones
```

Este patrón evita presentar inferencias como verdades.

---

## Patrón de recomendación controlada

```text
Genera una recomendación explicada e incluye:

- evidencia utilizada;
- criterios aplicados;
- riesgos;
- alternativas;
- nivel de confianza;
- información pendiente;
- decisión que corresponde a la persona responsable.

No apruebes, rechaces ni ejecutes la decisión final.
```

> La IA facilita y recomienda; las personas responsables deciden.

---

## Patrón de análisis documental

```text
1. Verifica que el documento exista y sea legible.
2. Identifica tipo, idioma, fecha y alcance.
3. Divide el contenido por secciones.
4. Extrae información sustentada.
5. Identifica contradicciones y vacíos.
6. Distingue hechos, interpretaciones y recomendaciones.
7. Genera el resultado en el formato solicitado.
8. Indica páginas o secciones no procesadas.
9. Valida cobertura y ausencia de invenciones.
```

---

## Patrón de clasificación

```text
Para cada elemento incluye:

- categoría asignada;
- evidencia;
- regla aplicada;
- nivel de confianza;
- observaciones;
- necesidad de revisión humana.

Si ninguna categoría corresponde, utiliza "No clasificado" y explica el motivo.
```

---

## Patrón de respuesta ejecutiva

```markdown
# Resumen ejecutivo

## Situación

## Hallazgos principales

## Impacto

## Riesgos

## Recomendación

## Próximos pasos

## Información pendiente
```

---

## Patrón de escalamiento humano

Escala la solicitud cuando:

- exista riesgo legal, financiero, médico, ético o de seguridad;
- falte información crítica;
- existan contradicciones no resueltas;
- se solicite aprobar o ejecutar una acción sensible;
- el nivel de confianza sea bajo;
- la solicitud esté fuera del alcance.

La respuesta debe indicar motivo, información disponible, datos pendientes y responsable sugerido.

---

## Patrón de nivel de confianza

| Nivel | Condición | Acción |
|---|---|---|
| Alto | Información suficiente y consistente | Entregar resultado |
| Medio | Vacíos menores | Entregar con advertencias |
| Bajo | Faltan datos críticos o hay contradicciones | Solicitar información o escalar |

---

## Casos de prueba mínimos

| Escenario | Qué valida |
|---|---|
| Caso correcto | Flujo normal |
| Información incompleta | Solicitud de datos faltantes |
| Información contradictoria | Detección de inconsistencias |
| Fuera de alcance | Cumplimiento de límites |
| Solicitud sensible | Escalamiento y seguridad |
| Formato incorrecto | Normalización o advertencia |
| Documento ilegible | Manejo de limitaciones |

Para cada prueba registra entrada, versión, respuesta, resultado esperado, criterio de aceptación y ajuste realizado.

---

## Antipatrones frecuentes

### Prompt enciclopédico

Demasiadas reglas sin jerarquía. Corrige organizando por bloques y eliminando duplicidad.

### Rol omnipotente

El GPT recibe autoridad para decidir o aprobar. Corrige definiendo límites y revisión humana.

### Proceso implícito

Solo utiliza verbos como “analiza”. Corrige descomponiendo el trabajo en pasos verificables.

### Formato abierto

Solicita “un informe” sin estructura. Corrige definiendo secciones, tablas y longitud.

### Validación genérica

Indica “valida” sin criterios. Corrige especificando completitud, consistencia, formato y evidencia.

### Suposición silenciosa

Completa datos faltantes sin advertirlo. Corrige etiquetando supuestos y solicitando información crítica.

---

## Matriz de revisión rápida

Califica cada criterio de 0 a 2.

| Criterio | 0 | 1 | 2 |
|---|---|---|---|
| Problema | No definido | Parcial | Claro |
| Rol | Excesivo | Parcial | Específico y limitado |
| Objetivo | Ambiguo | Incompleto | Medible |
| Entradas | No definidas | Parciales | Clasificadas |
| Proceso | Implícito | Parcial | Verificable |
| Salida | Abierta | Parcial | Estructurada |
| Restricciones | Ausentes | Incompletas | Claras |
| Validaciones | Ausentes | Genéricas | Específicas |
| Incertidumbre | Inventa | Advierte | Gestiona y escala |
| Pruebas | No existen | Insuficientes | Cubren escenarios críticos |

Puntaje máximo: `20`.

- `17 a 20`: listo para prueba controlada;
- `13 a 16`: requiere ajustes menores;
- `9 a 12`: requiere rediseño parcial;
- `0 a 8`: no está listo.

---

## Definition of Done

Un Prompt Maestro está listo cuando:

- representa un caso de negocio validado;
- todos los bloques están completos;
- no contiene contradicciones;
- las entradas críticas están identificadas;
- el proceso es explicable;
- la salida es verificable;
- existen restricciones y manejo de incertidumbre;
- los casos críticos fueron probados;
- la versión y evidencias están documentadas;
- una persona responsable aprobó los cambios.

---

## Actividad práctica

1. Aplica el checklist al Prompt Maestro del laboratorio ILC16.
2. Identifica tres riesgos.
3. Selecciona dos patrones reutilizables.
4. Elimina instrucciones duplicadas.
5. Construye siete casos de prueba.
6. Califica el prompt con la matriz.
7. Ajusta el diseño hasta alcanzar al menos 17 puntos.
8. Registra la nueva versión y sus evidencias.

---

## Resumen ejecutivo

Los checklists reducen omisiones y los patrones evitan diseñar cada GPT desde cero. Juntos convierten la ingeniería de prompts en una práctica repetible, auditable y orientada a calidad.