# 03.09 – Mejora Continua del GPT

## Objetivo

Un GPT empresarial no debe considerarse terminado después de su primera publicación. Debe evolucionar con base en evidencia, retroalimentación de usuarios, cambios del proceso y nuevos riesgos identificados.

La mejora continua convierte al GPT en un producto vivo, medible y gobernable.

---

## ¿Qué significa mejora continua?

La mejora continua es el ciclo mediante el cual se observa el comportamiento del GPT, se identifican oportunidades, se priorizan cambios, se prueba una nueva versión y se valida si la modificación produjo una mejora real.

No consiste en cambiar el prompt constantemente. Consiste en mejorar de forma controlada, trazable y basada en evidencia.

---

## Principio ILC

> No se mejora lo que no se observa, no se mide y no se prueba.

El ciclo recomendado es:

```text
Observar
   ↓
Registrar
   ↓
Analizar
   ↓
Priorizar
   ↓
Modificar
   ↓
Probar
   ↓
Validar
   ↓
Versionar
```

---

## Fuentes de mejora

Las mejoras pueden originarse en:

- comentarios de usuarios;
- respuestas incorrectas o incompletas;
- preguntas que el GPT no pudo resolver;
- cambios en políticas o reglas de negocio;
- nuevos documentos de conocimiento;
- resultados de pruebas;
- incidentes de seguridad o privacidad;
- métricas de uso y satisfacción;
- nuevas oportunidades de automatización.

---

## Qué elementos pueden evolucionar

### Prompt Maestro

Puede ajustarse el rol, contexto, proceso, restricciones, validaciones o formato de salida.

### Conocimiento

Pueden actualizarse documentos, políticas, procedimientos, glosarios y ejemplos.

### Casos de prueba

Deben incorporarse nuevos escenarios reales, casos límite y errores observados.

### Experiencia de usuario

Pueden mejorarse los mensajes iniciales, preguntas aclaratorias, tono y estructura de respuesta.

### Integraciones

El GPT puede evolucionar desde una interacción manual hacia acciones, APIs, automatizaciones o agentes.

---

## Métricas recomendadas

La mejora debe evaluarse mediante indicadores definidos.

| Dimensión | Métrica sugerida |
|---|---|
| Calidad | Porcentaje de respuestas aceptadas sin corrección |
| Precisión | Respuestas correctas frente al total evaluado |
| Completitud | Porcentaje de respuestas que cubren todos los criterios |
| Eficiencia | Tiempo ahorrado por interacción |
| Adopción | Usuarios activos y frecuencia de uso |
| Satisfacción | Valoración promedio de los usuarios |
| Seguridad | Número de incidentes o incumplimientos |
| Escalamiento | Casos resueltos sin intervención adicional |

No todas las métricas aplican a todos los GPTs. Deben seleccionarse según el caso de negocio.

---

## Registro de retroalimentación

Toda observación relevante debe registrarse con una estructura mínima:

```text
Fecha:
Usuario o área:
Caso de uso:
Entrada utilizada:
Respuesta generada:
Resultado esperado:
Problema identificado:
Severidad:
Mejora propuesta:
Responsable:
Estado:
```

Esto permite diferenciar una percepción aislada de un patrón recurrente.

---

## Clasificación de mejoras

### Correctiva

Corrige un error, una omisión o una respuesta insegura.

### Preventiva

Reduce la probabilidad de que ocurra un error futuro.

### Evolutiva

Agrega una nueva capacidad o amplía el alcance aprobado.

### Experiencial

Mejora claridad, tono, facilidad de uso o presentación.

### Técnica

Optimiza conocimiento, integraciones, rendimiento, seguridad o trazabilidad.

---

## Priorización

Las mejoras deben priorizarse considerando:

- impacto en el negocio;
- frecuencia del problema;
- nivel de riesgo;
- cantidad de usuarios afectados;
- esfuerzo de implementación;
- dependencia de datos o integraciones;
- urgencia regulatoria u operativa.

Una forma simple de priorizar es utilizar la siguiente escala:

| Prioridad | Criterio |
|---|---|
| Crítica | Riesgo de seguridad, privacidad, cumplimiento o daño significativo |
| Alta | Error frecuente que afecta una decisión o proceso importante |
| Media | Mejora relevante de calidad, eficiencia o experiencia |
| Baja | Ajuste cosmético o mejora de conveniencia |

---

## Control de versiones

Cada cambio relevante debe generar una nueva versión.

Ejemplo:

```text
GPT: Asistente de Contratos
Versión: 1.2.0
Fecha: 21/07/2026
Cambio: Se agregó validación de vigencia contractual.
Motivo: Se detectaron respuestas basadas en cláusulas vencidas.
Responsable: Equipo Legal.
Resultado de pruebas: 10 de 10 casos aprobados.
```

Se recomienda utilizar versionamiento semántico:

- `1.0.0`: primera versión estable;
- `1.1.0`: nueva capacidad compatible;
- `1.1.1`: corrección menor;
- `2.0.0`: cambio importante de alcance o comportamiento.

---

## Ciclo de prueba antes de publicar

Antes de liberar una mejora:

1. Actualiza el Prompt Maestro o la fuente de conocimiento.
2. Ejecuta los casos de prueba existentes.
3. Agrega el caso que originó la mejora.
4. Evalúa exactitud, formato, restricciones y seguridad.
5. Compara la nueva versión con la anterior.
6. Documenta resultados.
7. Publica solamente si cumple los criterios de aceptación.

---

## Criterios de aceptación

Una mejora debe considerarse aprobada cuando:

- resuelve el problema identificado;
- no deteriora casos previamente correctos;
- mantiene las restricciones definidas;
- supera los casos de prueba críticos;
- no introduce riesgos adicionales;
- cuenta con evidencia de validación;
- queda registrada en el historial de versiones.

---

## Mejora continua dentro del Prompt Maestro

El GPT puede incorporar una regla como la siguiente:

```text
Al finalizar una tarea, identifica únicamente cuando sea relevante:

- información que mejoraría el resultado;
- datos faltantes que deberían incorporarse en futuras interacciones;
- patrones repetitivos que podrían automatizarse;
- limitaciones detectadas;
- oportunidades para mejorar el proceso.

No modifiques tus propias instrucciones ni amplíes tu alcance.
Presenta las mejoras como recomendaciones para revisión humana.
```

La mejora continua no significa que el GPT se reconfigure solo. Los cambios deben ser evaluados y aprobados por una persona responsable.

---

## Gobierno de cambios

Para GPTs empresariales se recomienda definir:

- propietario del GPT;
- responsable funcional;
- responsable técnico;
- aprobador de cambios;
- frecuencia de revisión;
- repositorio de versiones;
- conjunto oficial de pruebas;
- procedimiento de reversión.

Los cambios críticos no deben pasar directamente a producción.

---

## Antipatrones

Evita:

- cambiar instrucciones sin registrar la razón;
- aceptar toda sugerencia de usuario como requisito;
- publicar sin ejecutar pruebas de regresión;
- ampliar el alcance sin aprobación;
- eliminar restricciones para obtener respuestas más completas;
- reemplazar conocimiento oficial por información no validada;
- medir solo cantidad de uso y no calidad;
- permitir que el GPT cambie sus propias reglas.

---

## Plantilla reutilizable

```markdown
## Mejora continua

### Indicadores
- [Indicador 1]
- [Indicador 2]
- [Indicador 3]

### Fuentes de retroalimentación
- [Usuarios]
- [Pruebas]
- [Métricas]
- [Incidentes]

### Frecuencia de revisión
[Semanal / mensual / trimestral]

### Flujo de mejora
1. Registrar observación.
2. Clasificar impacto y riesgo.
3. Priorizar cambio.
4. Actualizar artefactos.
5. Ejecutar pruebas.
6. Aprobar o rechazar.
7. Versionar y publicar.

### Responsables
- Propietario:
- Responsable funcional:
- Responsable técnico:
- Aprobador:

### Regla
El GPT no puede modificar autónomamente sus instrucciones, conocimiento, restricciones ni alcance.
```

---

## Checklist

Antes de cerrar esta sección del Prompt Maestro, confirma que:

- existen indicadores de calidad y valor;
- se registra la retroalimentación;
- las mejoras se clasifican y priorizan;
- existe un responsable del GPT;
- los cambios pasan por pruebas;
- se ejecutan pruebas de regresión;
- cada versión queda documentada;
- existe un procedimiento de reversión;
- el GPT no puede autoaprobar cambios;
- la mejora está conectada con el beneficio de negocio.

---

## Laboratorio

Selecciona uno de los casos de uso del taller y diseña su mecanismo de mejora continua.

Incluye:

1. tres métricas de calidad;
2. dos métricas de valor;
3. formato de registro de retroalimentación;
4. responsables de aprobación;
5. frecuencia de revisión;
6. cinco casos de prueba de regresión;
7. criterio para publicar una nueva versión;
8. mecanismo de reversión.

Como ejercicio adicional, simula una respuesta incorrecta del GPT y documenta todo el recorrido desde la detección hasta la publicación de la corrección.

---

## Resumen ejecutivo

La mejora continua permite que un GPT permanezca útil, seguro y alineado con el negocio. La evolución debe basarse en evidencia, métricas, pruebas y control de versiones. En la metodología ILC, el GPT no se mejora de manera improvisada: se observa, se evalúa, se modifica, se valida y se publica bajo supervisión humana.