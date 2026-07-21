# 03.08 – Manejo de Incertidumbre

## Objetivo

Un GPT empresarial no siempre dispone de información completa, actualizada o verificable. Por ello, un **Prompt Maestro profesional** debe definir cómo actuar cuando existen dudas, vacíos de información, contradicciones o baja confianza.

El manejo de incertidumbre evita que el GPT complete información por su cuenta, presente suposiciones como hechos o entregue recomendaciones sin evidencia suficiente.

---

## ¿Qué es la incertidumbre?

La incertidumbre aparece cuando el GPT no puede determinar una respuesta confiable con la información disponible.

Puede originarse por:

- datos faltantes;
- instrucciones ambiguas;
- documentos incompletos;
- fuentes contradictorias;
- información desactualizada;
- ausencia de evidencia;
- reglas de negocio no definidas;
- solicitudes fuera del alcance.

La incertidumbre no es un error del GPT. El error ocurre cuando el GPT la oculta o inventa información para continuar.

---

## Principio ILC

> Cuando no exista evidencia suficiente, el GPT debe reconocer la incertidumbre, explicar su causa y solicitar la información necesaria para continuar.

El comportamiento esperado es:

```text
Detectar incertidumbre
        ↓
Identificar la causa
        ↓
Evaluar el impacto
        ↓
Solicitar información o confirmar supuestos
        ↓
Continuar solo cuando exista evidencia suficiente
```

---

## Tipos de incertidumbre

### 1. Información incompleta

Ocurre cuando faltan datos necesarios para ejecutar la tarea.

**Ejemplo**

El usuario solicita evaluar la rentabilidad de un proyecto, pero no proporciona inversión, ingresos estimados ni horizonte de evaluación.

**Comportamiento esperado**

```text
No puedo calcular la rentabilidad con la información disponible.

Necesito, como mínimo:

- inversión inicial;
- ingresos estimados;
- costos operativos;
- periodo de evaluación.
```

---

### 2. Ambigüedad

Ocurre cuando una instrucción admite varias interpretaciones.

**Ejemplo**

```text
Prepara un reporte de ventas.
```

No se especifica:

- periodo;
- región;
- producto;
- nivel de detalle;
- formato esperado.

**Comportamiento esperado**

El GPT debe solicitar la precisión mínima necesaria antes de generar el reporte.

---

### 3. Contradicción

Ocurre cuando dos o más fuentes contienen información incompatible.

**Ejemplo**

- Documento A: presupuesto aprobado de USD 100,000.
- Documento B: presupuesto aprobado de USD 120,000.

**Comportamiento esperado**

```text
He detectado una inconsistencia en el presupuesto aprobado:

- Documento A: USD 100,000.
- Documento B: USD 120,000.

No es posible determinar cuál es el valor correcto sin una confirmación adicional.
```

El GPT no debe elegir automáticamente uno de los valores.

---

### 4. Información desactualizada

Ocurre cuando una respuesta depende de datos que pueden haber cambiado.

**Ejemplos**

- precios;
- regulaciones;
- responsables actuales;
- versiones de productos;
- indicadores financieros;
- políticas internas.

**Comportamiento esperado**

El GPT debe indicar la fecha o vigencia de la información disponible y advertir cuando sea necesaria una verificación adicional.

---

### 5. Baja confianza

Ocurre cuando existe información, pero no es suficiente para sostener una conclusión firme.

**Comportamiento esperado**

El GPT debe diferenciar entre:

- hecho confirmado;
- inferencia razonable;
- supuesto;
- recomendación;
- información no disponible.

---

## Escala de confianza recomendada

El Prompt Maestro puede utilizar una escala simple:

| Nivel | Interpretación | Acción esperada |
|---|---|---|
| Alto | La respuesta está respaldada por información suficiente y consistente | Responder normalmente |
| Medio | Existen datos útiles, pero también vacíos o supuestos menores | Responder señalando supuestos y limitaciones |
| Bajo | La evidencia es insuficiente o contradictoria | No concluir; solicitar información adicional |

Esta escala no debe presentarse como una medición científica. Es una guía operativa para comunicar el nivel de seguridad de la respuesta.

---

## Política de supuestos

Los supuestos pueden utilizarse únicamente cuando:

- no modifican decisiones críticas;
- son explícitos;
- pueden ser validados por el usuario;
- se presentan como provisionales;
- no contradicen la información disponible.

**Formato recomendado**

```text
Supuesto utilizado:
Se asumirá que el periodo de análisis corresponde al último trimestre disponible.

Confirma este supuesto antes de utilizar el resultado para una decisión final.
```

Nunca deben ocultarse los supuestos dentro de la respuesta.

---

## Política de preguntas aclaratorias

El GPT debe formular preguntas solo cuando la información faltante sea relevante para el resultado.

Las preguntas deben ser:

- específicas;
- breves;
- accionables;
- ordenadas por prioridad;
- limitadas a la información realmente necesaria.

**Evitar**

```text
Necesito más información.
```

**Preferir**

```text
Para completar el análisis necesito confirmar:

1. ¿Cuál es el periodo de evaluación?
2. ¿Qué moneda debe utilizarse?
3. ¿La información incluye impuestos?
```

---

## Respuesta parcial controlada

Cuando sea útil, el GPT puede avanzar con la parte verificable de la tarea y separar claramente lo pendiente.

**Ejemplo**

```text
Puedo identificar los riesgos contractuales generales con el documento disponible.

No puedo evaluar el impacto económico porque no se adjuntaron los anexos de precios.
```

La respuesta parcial debe indicar:

- qué pudo completarse;
- qué no pudo completarse;
- por qué;
- qué información permitiría continuar.

---

## Lo que el GPT nunca debe hacer

Ante incertidumbre, el GPT no debe:

- inventar datos;
- completar nombres, fechas o cifras sin evidencia;
- presentar suposiciones como hechos;
- ocultar contradicciones;
- elegir arbitrariamente entre fuentes;
- afirmar certeza cuando no la posee;
- emitir recomendaciones críticas sin sustento;
- continuar una tarea que requiere información obligatoria inexistente.

---

## Patrón ILC para manejar incertidumbre

```text
1. Identificar la afirmación o decisión que requiere evidencia.
2. Revisar si la información disponible es suficiente.
3. Detectar vacíos, ambigüedades o contradicciones.
4. Clasificar el nivel de confianza.
5. Explicar la limitación de forma transparente.
6. Solicitar la información mínima necesaria.
7. Entregar únicamente resultados respaldados.
8. Verificar nuevamente antes de concluir.
```

---

## Plantilla reutilizable

```markdown
## Manejo de incertidumbre

Antes de responder:

1. Verifica si existe evidencia suficiente.
2. Identifica información faltante, ambigua, contradictoria o desactualizada.
3. Diferencia hechos, inferencias, supuestos y recomendaciones.
4. No inventes ni completes información no proporcionada.
5. Si la confianza es baja, detén la conclusión y solicita aclaraciones.
6. Si es posible avanzar parcialmente, indica claramente:
   - qué se pudo completar;
   - qué quedó pendiente;
   - qué información adicional se requiere.
7. Expón todos los supuestos utilizados.
8. Comunica las limitaciones antes de presentar la respuesta final.
```

---

## Ejemplo aplicado

### Prompt inicial

```text
Revisa esta propuesta y dime si debemos aprobarla.
```

### Prompt mejorado

```text
Revisa la propuesta y determina si existe información suficiente para emitir una recomendación.

Antes de concluir:

- valida que estén disponibles el alcance, costo, plazo, beneficios, riesgos y responsables;
- identifica datos faltantes o contradictorios;
- diferencia hechos documentados de inferencias;
- expón cualquier supuesto utilizado;
- asigna un nivel de confianza alto, medio o bajo;
- si la confianza es baja, no recomiendes aprobar o rechazar;
- solicita la información necesaria para completar la evaluación.

Si la información es suficiente, entrega:

1. Resumen ejecutivo.
2. Evidencias favorables.
3. Riesgos y observaciones.
4. Información pendiente.
5. Recomendación fundamentada.
6. Nivel de confianza.
```

---

## Checklist

Antes de finalizar el bloque de incertidumbre, verifica que el Prompt Maestro:

- detecte información incompleta;
- controle instrucciones ambiguas;
- identifique contradicciones;
- diferencie hechos y supuestos;
- comunique el nivel de confianza;
- solicite aclaraciones específicas;
- permita respuestas parciales controladas;
- evite inventar información;
- explique limitaciones;
- impida conclusiones sin evidencia suficiente.

---

## Laboratorio ILC

Mejora el siguiente prompt:

```text
Analiza los resultados y recomienda qué proyecto debemos priorizar.
```

Incorpora reglas para:

- detectar proyectos con información incompleta;
- identificar criterios de evaluación no definidos;
- señalar contradicciones;
- declarar supuestos;
- indicar nivel de confianza;
- solicitar datos faltantes;
- impedir recomendaciones sin evidencia suficiente.

---

## Resultado esperado

Al finalizar este capítulo, el participante podrá incorporar al Prompt Maestro una política explícita para manejar información incompleta, contradictoria o poco confiable.

El GPT resultante no intentará responder a cualquier costo. Sabrá cuándo avanzar, cuándo detenerse, cuándo pedir información y cómo comunicar sus limitaciones de manera profesional.

---

## Resumen ejecutivo

El manejo de incertidumbre protege la calidad y credibilidad de un GPT empresarial. Un GPT confiable no es el que siempre responde, sino el que distingue entre lo que sabe, lo que puede inferir y lo que todavía necesita confirmar.