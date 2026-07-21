# 07 – Gobierno y Escalamiento del GPT

## Objetivo del capítulo

En este capítulo aprenderás a transformar un MVP validado en una capacidad sostenible, gobernada y escalable dentro de la organización.

Al finalizar podrás:

- definir criterios para decidir si un GPT debe escalarse;
- establecer propietarios, responsabilidades y niveles de aprobación;
- diseñar controles de seguridad, privacidad y uso responsable;
- organizar el versionamiento y la gestión de cambios;
- implementar monitoreo operativo, de calidad, adopción, costo y riesgo;
- preparar un roadmap de evolución desde MVP hacia operación controlada.

---

## 1. Del MVP a una capacidad organizacional

Un GPT que funcionó correctamente durante un piloto todavía no es una solución institucionalizada.

Para escalar debe demostrar que puede operar de forma:

- útil;
- segura;
- repetible;
- medible;
- mantenible;
- auditable;
- económicamente sostenible.

El escalamiento no consiste únicamente en habilitar el GPT para más usuarios. También implica establecer gobierno, responsabilidades, controles, soporte y mecanismos de mejora continua.

> Escalar un GPT no significa ampliar su alcance sin límites. Significa aumentar su uso manteniendo control sobre calidad, riesgo y valor.

---

## 2. Flujo ILC hacia el escalamiento

```text
Caso de negocio
      ↓
GPT Canvas
      ↓
Prompt Maestro
      ↓
Configuración del GPT
      ↓
Pruebas y validación
      ↓
MVP controlado
      ↓
Evaluación de evidencias
      ↓
Decisión de escalamiento
      ↓
Gobierno y operación
      ↓
Mejora continua
```

Cada etapa debe dejar evidencia suficiente para justificar la siguiente.

---

## 3. Decisiones posibles después del MVP

Al finalizar el piloto, el equipo no debe asumir automáticamente que el GPT pasará a producción.

Existen cuatro decisiones principales.

### Escalar

Se recomienda cuando:

- las métricas cumplen o superan las metas;
- no existen riesgos críticos abiertos;
- los usuarios demuestran adopción;
- el beneficio es observable;
- existe un propietario responsable;
- la operación puede sostenerse.

### Mejorar y repetir

Se recomienda cuando:

- el caso de negocio sigue siendo válido;
- existen fallas corregibles;
- algunas métricas no alcanzaron la meta;
- se requiere ajustar conocimiento, instrucciones o experiencia;
- el riesgo puede mitigarse.

### Pausar

Se recomienda cuando:

- faltan datos o capacidades necesarias;
- existe dependencia de una decisión externa;
- la organización no cuenta todavía con controles suficientes;
- el costo o esfuerzo necesita reevaluarse.

### Cancelar

Se recomienda cuando:

- el problema no es relevante;
- el GPT no genera valor;
- el riesgo es inaceptable;
- la solución no supera al proceso actual;
- no existe adopción;
- el costo es desproporcionado.

---

## 4. Matriz de decisión de escalamiento

Utiliza una escala de 1 a 5 para evaluar cada dimensión.

| Dimensión | Pregunta | Peso sugerido |
|---|---|---:|
| Valor | ¿El GPT genera un beneficio medible? | 20 % |
| Calidad | ¿Las respuestas cumplen los criterios de aceptación? | 20 % |
| Adopción | ¿Los usuarios lo utilizan y desean seguir usándolo? | 15 % |
| Riesgo | ¿Los riesgos están identificados y controlados? | 20 % |
| Operación | ¿Existe soporte, monitoreo y propietario? | 15 % |
| Sostenibilidad | ¿El costo y mantenimiento son razonables? | 10 % |

### Fórmula sugerida

```text
Puntaje total = Σ (puntaje de dimensión × peso)
```

### Interpretación

| Puntaje | Recomendación |
|---:|---|
| 4.0 – 5.0 | Escalar |
| 3.0 – 3.9 | Mejorar y repetir |
| 2.0 – 2.9 | Pausar |
| 1.0 – 1.9 | Cancelar o rediseñar |

La matriz orienta la decisión, pero no reemplaza la evaluación de riesgos críticos. Un solo riesgo crítico no mitigado puede impedir el escalamiento aunque el puntaje total sea alto.

---

## 5. Modelo de gobierno del GPT

Todo GPT escalado debe contar con responsables claramente definidos.

### Propietario de negocio

Responsable de:

- validar que el GPT continúe resolviendo el problema;
- priorizar mejoras;
- aprobar cambios funcionales;
- supervisar adopción y valor;
- decidir sobre continuidad o retiro.

### Propietario técnico

Responsable de:

- configurar y mantener el GPT;
- gestionar versiones;
- controlar archivos de conocimiento;
- ejecutar pruebas técnicas;
- revisar integraciones y capacidades.

### Responsable de conocimiento

Responsable de:

- validar documentos fuente;
- controlar vigencia y calidad;
- retirar información obsoleta;
- mantener glosarios y reglas del negocio;
- aprobar actualizaciones de conocimiento.

### Responsable de riesgo o cumplimiento

Responsable de:

- revisar privacidad, seguridad y uso responsable;
- aprobar restricciones;
- evaluar incidentes;
- validar controles;
- establecer condiciones de escalamiento.

### Usuarios y validadores

Responsables de:

- utilizar el GPT dentro del alcance autorizado;
- revisar resultados antes de decisiones relevantes;
- reportar errores;
- proteger la información;
- aportar retroalimentación.

---

## 6. Matriz RACI sugerida

| Actividad | Negocio | Técnico | Conocimiento | Riesgo | Usuario |
|---|---|---|---|---|---|
| Definir alcance | A/R | C | C | C | C |
| Aprobar Prompt Maestro | A | R | C | C | I |
| Actualizar conocimiento | C | C | A/R | C | I |
| Ejecutar pruebas | A | R | C | C | C |
| Aprobar escalamiento | A | C | C | R | I |
| Monitorear operación | A | R | C | C | I |
| Gestionar incidentes | A | R | C | R | I |
| Retirar el GPT | A/R | C | C | C | I |

Leyenda:

- **R:** Responsable de ejecutar.
- **A:** Responsable final de aprobar.
- **C:** Consultado.
- **I:** Informado.

---

## 7. Controles mínimos antes de escalar

### Identidad y acceso

- definir quién puede utilizar el GPT;
- aplicar el principio de mínimo privilegio;
- evitar acceso público cuando el caso usa información interna;
- revisar periódicamente usuarios y permisos;
- retirar accesos cuando cambien las funciones.

### Protección de información

- clasificar la información utilizada;
- evitar datos sensibles no autorizados;
- anonimizar o enmascarar cuando corresponda;
- definir qué información puede ingresarse;
- establecer reglas para archivos y conversaciones.

### Conocimiento

- utilizar fuentes aprobadas;
- registrar propietario y fecha de actualización;
- controlar versiones;
- retirar documentos obsoletos;
- probar contradicciones entre fuentes.

### Comportamiento

- mantener restricciones explícitas;
- evitar decisiones críticas completamente autónomas;
- establecer Human in the Loop;
- definir respuestas ante incertidumbre;
- bloquear solicitudes fuera de alcance.

### Evidencia y auditoría

- registrar versiones del Prompt Maestro;
- mantener resultados de pruebas;
- documentar aprobaciones;
- conservar hallazgos e incidentes;
- registrar cambios relevantes.

---

## 8. Versionamiento del GPT

Un GPT escalado debe gestionarse como un producto versionado.

### Esquema recomendado

```text
Versión mayor.menor.parche

Ejemplo: 2.3.1
```

- **Versión mayor:** cambia el propósito, alcance o arquitectura.
- **Versión menor:** agrega una capacidad o mejora relevante.
- **Parche:** corrige un error sin modificar el alcance principal.

### Registro de cambios

```markdown
## Versión 1.2.0

- Fecha:
- Responsable:
- Motivo del cambio:
- Secciones modificadas:
- Archivos de conocimiento actualizados:
- Riesgos revisados:
- Pruebas ejecutadas:
- Resultado:
- Aprobador:
```

No deben realizarse cambios directos en una versión operativa sin registro, pruebas y aprobación proporcional al impacto.

---

## 9. Gestión de cambios

Todo cambio debe seguir un flujo controlado.

```text
Solicitud de cambio
      ↓
Análisis de impacto
      ↓
Clasificación del riesgo
      ↓
Modificación en versión de prueba
      ↓
Pruebas funcionales y de regresión
      ↓
Aprobación
      ↓
Publicación
      ↓
Monitoreo posterior
```

### Cambios que requieren mayor control

- modificación del propósito;
- acceso a nuevas fuentes;
- uso de información sensible;
- incorporación de acciones o integraciones;
- ampliación a nuevos usuarios;
- eliminación de restricciones;
- automatización de decisiones;
- cambio de propietario.

---

## 10. Monitoreo del GPT

El monitoreo debe cubrir más que disponibilidad técnica.

### Valor

- tiempo ahorrado;
- productividad;
- reducción de errores;
- volumen atendido;
- impacto económico estimado.

### Adopción

- usuarios activos;
- frecuencia de uso;
- recurrencia;
- tareas completadas;
- abandono.

### Calidad

- respuestas aceptadas;
- respuestas corregidas;
- fallas por tipo;
- consistencia;
- cumplimiento del formato.

### Riesgo

- respuestas fuera de alcance;
- exposición de información;
- intentos de evasión de restricciones;
- decisiones incorrectas;
- incidentes y escalaciones.

### Operación

- disponibilidad;
- tiempos de respuesta;
- incidencias;
- actualizaciones pendientes;
- vigencia del conocimiento.

### Costo

- consumo estimado;
- costo por usuario;
- costo por caso;
- costo de soporte;
- relación entre costo y beneficio.

---

## 11. Tablero mínimo de seguimiento

| Indicador | Meta | Resultado | Estado | Tendencia | Responsable |
|---|---:|---:|---|---|---|
| Respuestas aceptadas | ≥ 85 % | Pendiente | Sin evaluar | — | Producto |
| Errores críticos | 0 | Pendiente | Sin evaluar | — | Riesgo |
| Usuarios activos | ≥ 70 % del piloto | Pendiente | Sin evaluar | — | Negocio |
| Ahorro por tarea | ≥ 30 % | Pendiente | Sin evaluar | — | Negocio |
| Incidentes de seguridad | 0 | Pendiente | Sin evaluar | — | Seguridad |
| Documentos vigentes | 100 % | Pendiente | Sin evaluar | — | Conocimiento |

Estados recomendados:

- Verde: cumple la meta;
- Ámbar: desviación controlable;
- Rojo: incumplimiento relevante;
- Gris: sin evidencia suficiente.

---

## 12. Gestión de incidentes

Un incidente es cualquier evento que compromete calidad, seguridad, cumplimiento o continuidad.

Ejemplos:

- respuesta con información confidencial;
- recomendación peligrosa o incorrecta;
- incumplimiento de restricciones;
- uso no autorizado;
- fuente de conocimiento obsoleta;
- cambio no aprobado;
- comportamiento inconsistente;
- indisponibilidad prolongada.

### Flujo de atención

1. Registrar el incidente.
2. Clasificar severidad.
3. Contener el impacto.
4. Suspender el GPT si es necesario.
5. Analizar causa raíz.
6. Corregir.
7. Ejecutar pruebas de regresión.
8. Aprobar la reapertura.
9. Documentar lecciones aprendidas.

### Severidad sugerida

| Nivel | Descripción | Acción |
|---|---|---|
| Crítica | Daño, exposición o incumplimiento grave | Suspensión inmediata |
| Alta | Impacto significativo o repetitivo | Corrección prioritaria |
| Media | Error controlable con revisión humana | Plan de mejora |
| Baja | Problema menor de experiencia o formato | Incorporar al backlog |

---

## 13. Escalamiento por etapas

No es recomendable pasar de un piloto pequeño a toda la organización en un solo paso.

### Etapa 1. Piloto controlado

- pocos usuarios;
- alcance limitado;
- supervisión cercana;
- medición intensiva.

### Etapa 2. Área o proceso

- más usuarios del mismo dominio;
- soporte definido;
- conocimiento estabilizado;
- métricas operativas.

### Etapa 3. Múltiples áreas

- perfiles de acceso diferenciados;
- gobierno formal;
- catálogo de GPTs;
- estándares comunes;
- mayor control de costos.

### Etapa 4. Capacidad empresarial

- portafolio gestionado;
- ciclo de vida institucional;
- monitoreo centralizado;
- integración con arquitectura y seguridad;
- operación y mejora continua.

---

## 14. Criterios de retiro

Un GPT también debe tener condiciones para ser retirado.

Considera retirarlo cuando:

- dejó de resolver un problema vigente;
- existe una solución mejor;
- el propietario ya no existe;
- el conocimiento no puede mantenerse;
- el riesgo aumentó;
- la adopción es insuficiente;
- el costo supera el beneficio;
- permanece sin uso durante un periodo definido.

El retiro debe incluir:

- comunicación a usuarios;
- revocación de accesos;
- respaldo de documentación;
- conservación de evidencias necesarias;
- cierre de integraciones;
- registro de la decisión.

---

## 15. Ficha de gobierno ILC

```markdown
# Ficha de Gobierno del GPT

## Identificación
- Nombre:
- Versión:
- Estado:
- Área:
- Fecha de aprobación:

## Responsables
- Propietario de negocio:
- Propietario técnico:
- Responsable de conocimiento:
- Responsable de riesgo:
- Equipo de soporte:

## Alcance autorizado
- Usuarios:
- Procesos:
- Datos:
- Fuentes:
- Capacidades:

## Controles
- Acceso:
- Privacidad:
- Seguridad:
- Human in the Loop:
- Auditoría:

## Monitoreo
- Indicadores de valor:
- Indicadores de calidad:
- Indicadores de adopción:
- Indicadores de riesgo:
- Indicadores de costo:

## Gestión de cambios
- Frecuencia de revisión:
- Flujo de aprobación:
- Pruebas obligatorias:

## Continuidad
- Soporte:
- Escalamiento de incidentes:
- Condiciones de suspensión:
- Condiciones de retiro:
```

---

## 16. Checklist antes de escalar

### Valor

- [ ] El beneficio fue medido.
- [ ] Las metas del MVP fueron evaluadas.
- [ ] Existe una recomendación sustentada.

### Propiedad

- [ ] Existe propietario de negocio.
- [ ] Existe propietario técnico.
- [ ] Existe responsable de conocimiento.
- [ ] Existe responsable de riesgo.

### Calidad

- [ ] Los casos críticos fueron aprobados.
- [ ] Se ejecutaron pruebas de regresión.
- [ ] No existen fallas críticas abiertas.

### Seguridad y cumplimiento

- [ ] La información fue clasificada.
- [ ] Los accesos están definidos.
- [ ] Las restricciones están activas.
- [ ] Existe revisión humana donde corresponde.

### Operación

- [ ] Existe soporte.
- [ ] Existe monitoreo.
- [ ] Existe gestión de incidentes.
- [ ] Existe control de versiones.

### Sostenibilidad

- [ ] El costo fue estimado.
- [ ] La relación costo-beneficio es razonable.
- [ ] El conocimiento puede mantenerse.
- [ ] Existe un roadmap de evolución.

---

## 17. Laboratorio práctico

Utiliza el GPT desarrollado durante el taller y prepara su propuesta de escalamiento.

### Entregables

1. Resultado de la matriz de escalamiento.
2. Decisión recomendada.
3. Ficha de gobierno.
4. Matriz RACI.
5. Tablero mínimo de indicadores.
6. Flujo de gestión de cambios.
7. Plan de escalamiento por etapas.
8. Riesgos pendientes y mitigaciones.
9. Condiciones de suspensión o retiro.

### Pregunta de cierre

> ¿Qué debe cambiar en la organización para que este GPT deje de ser una demostración y se convierta en una capacidad sostenible?

---

## 18. Definition of Done

El bloque de gobierno y escalamiento se considera completo cuando:

- existe una decisión sustentada con evidencia;
- los responsables están identificados;
- el alcance autorizado está documentado;
- los controles mínimos están definidos;
- el GPT posee versión y registro de cambios;
- las métricas tienen metas y propietarios;
- existe un proceso de incidentes;
- el escalamiento será gradual;
- se conocen las condiciones de suspensión y retiro;
- el GPT puede operar sin depender exclusivamente de su creador.

---

## Resumen ejecutivo

El éxito de un GPT empresarial no se demuestra únicamente cuando genera una buena respuesta. Se demuestra cuando la organización puede utilizarlo de forma repetible, segura, medible y sostenible.

La metodología ILC completa el ciclo al conectar el caso de negocio, el diseño, el Prompt Maestro, la configuración, las pruebas y el MVP con un modelo de gobierno que permita decidir cuándo escalar, mejorar, pausar o retirar la solución.

> Un GPT sin gobierno es un experimento. Un GPT con responsables, controles, métricas y mejora continua puede convertirse en una capacidad organizacional.
