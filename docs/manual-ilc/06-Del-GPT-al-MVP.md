# 06 – Del GPT al MVP

## Objetivo del capítulo

En este capítulo convertirás un GPT configurado y probado en un **Producto Mínimo Viable (MVP)** que pueda utilizarse con usuarios reales, medir su desempeño y generar evidencia para decidir si debe mejorarse, escalarse o detenerse.

Al finalizar podrás:

- distinguir entre una demostración, un prototipo y un MVP;
- definir el alcance mínimo del GPT;
- seleccionar usuarios piloto y escenarios reales;
- establecer indicadores de adopción, calidad, eficiencia y riesgo;
- organizar un piloto controlado;
- recopilar evidencias para decidir el siguiente paso.

---

## 1. ¿Qué es un MVP de GPT?

Un MVP de GPT es la versión más pequeña de una solución de IA generativa que permite comprobar, con usuarios y casos reales, si el GPT resuelve un problema relevante de forma suficientemente útil, segura y repetible.

Un MVP no busca demostrar que el GPT puede hacerlo todo. Busca validar las hipótesis más importantes con el menor esfuerzo razonable.

> Un MVP no es un GPT incompleto. Es un GPT deliberadamente acotado para aprender rápido y con evidencia.

---

## 2. Demostración, prototipo y MVP

| Nivel | Propósito | Usuarios | Datos | Evidencia esperada |
|---|---|---|---|---|
| Demostración | Mostrar una posibilidad | Equipo creador | Ejemplos preparados | Interés inicial |
| Prototipo | Probar funcionamiento | Equipo interno | Datos controlados | Factibilidad técnica |
| MVP | Validar valor y uso | Usuarios piloto | Casos reales autorizados | Valor, calidad, adopción y riesgo |

Un GPT que funciona correctamente con un ejemplo preparado todavía no es un MVP. Para serlo debe usarse en un contexto real, con criterios de éxito definidos y evidencia observable.

---

## 3. Del caso de negocio al MVP

El flujo ILC llega al MVP mediante una secuencia trazable:

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
Medición y decisión
```

Cada etapa reduce incertidumbre:

- El caso de negocio valida relevancia.
- El GPT Canvas define el diseño.
- El Prompt Maestro estructura el comportamiento.
- La configuración implementa el GPT.
- Las pruebas verifican calidad y seguridad.
- El MVP valida valor en uso real.

---

## 4. Hipótesis que debe validar el MVP

Antes de iniciar el piloto, documenta las hipótesis.

### Hipótesis de problema

El problema ocurre con suficiente frecuencia y genera una dificultad relevante para los usuarios.

### Hipótesis de solución

El GPT puede apoyar la tarea con un nivel de calidad aceptable.

### Hipótesis de adopción

Los usuarios entienden cómo utilizar el GPT y están dispuestos a incorporarlo en su trabajo.

### Hipótesis de valor

El uso del GPT genera una mejora medible, por ejemplo:

- menor tiempo de atención;
- menor esfuerzo manual;
- mayor consistencia;
- reducción de errores;
- mejor acceso al conocimiento;
- aumento de productividad.

### Hipótesis de riesgo

El GPT puede operar dentro de las restricciones de seguridad, privacidad y negocio definidas.

---

## 5. Definir el alcance mínimo

El MVP debe concentrarse en el proceso o escenario con mayor valor y menor complejidad inicial.

### Incluye

- uno o pocos tipos de usuario;
- un conjunto limitado de tareas;
- fuentes de conocimiento autorizadas;
- formatos de entrada controlados;
- una salida principal;
- casos de prueba representativos;
- medición básica de resultados.

### No incluye todavía

- todos los procesos del área;
- integraciones complejas no necesarias;
- automatización total;
- decisiones críticas sin revisión humana;
- acceso masivo a toda la organización;
- conocimiento no validado;
- múltiples versiones sin control.

### Regla práctica

Si el MVP requiere resolver todos los casos, integrar todos los sistemas y atender a todos los usuarios antes de comenzar, el alcance no es mínimo.

---

## 6. Ficha del MVP ILC

Utiliza la siguiente ficha antes de iniciar el piloto.

```markdown
# Ficha del MVP

## Identificación
- Nombre del GPT:
- Versión:
- Área propietaria:
- Responsable del producto:
- Responsable técnico:

## Problema
- Problema priorizado:
- Usuarios afectados:
- Situación actual:

## Hipótesis
- Hipótesis de problema:
- Hipótesis de solución:
- Hipótesis de adopción:
- Hipótesis de valor:
- Hipótesis de riesgo:

## Alcance
- Incluye:
- No incluye:

## Usuarios piloto
- Cantidad:
- Perfiles:
- Criterios de selección:

## Escenarios
- Escenario 1:
- Escenario 2:
- Escenario 3:

## Indicadores
- Calidad:
- Tiempo:
- Adopción:
- Satisfacción:
- Riesgo:

## Duración
- Fecha de inicio:
- Fecha de cierre:

## Criterio de decisión
- Escalar:
- Mejorar y repetir:
- Pausar:
- Cancelar:
```

---

## 7. Selección de usuarios piloto

Los usuarios piloto deben representar el uso real, pero participar dentro de un entorno controlado.

Selecciona personas que:

- conozcan el proceso;
- realicen la tarea con frecuencia;
- puedan comparar el resultado con el método actual;
- entreguen retroalimentación concreta;
- comprendan que están probando una versión inicial;
- respeten las reglas de seguridad y uso responsable.

Evita seleccionar únicamente al equipo que construyó el GPT. Su conocimiento previo puede ocultar problemas de usabilidad que aparecerán con usuarios nuevos.

---

## 8. Escenarios reales de validación

El MVP debe probarse con escenarios representativos.

Incluye al menos:

1. **Caso normal:** información completa y solicitud habitual.
2. **Caso incompleto:** faltan datos obligatorios.
3. **Caso ambiguo:** la solicitud puede interpretarse de más de una manera.
4. **Caso límite:** alta complejidad o gran cantidad de información.
5. **Caso restringido:** el usuario solicita algo fuera del alcance.
6. **Caso con contradicción:** dos fuentes contienen datos diferentes.
7. **Caso adversarial:** intento de ignorar instrucciones o extraer información no autorizada.

El objetivo no es comprobar solamente cuándo funciona, sino también cómo responde cuando no debe continuar.

---

## 9. Indicadores del MVP

Un MVP debe medir varias dimensiones. No basta con preguntar si a los usuarios les gustó.

### Calidad

- porcentaje de respuestas aceptadas sin cambios;
- porcentaje de respuestas aceptadas con ajustes menores;
- cantidad de errores críticos;
- cobertura de criterios de aceptación;
- nivel de consistencia entre respuestas similares.

### Eficiencia

- tiempo promedio antes del GPT;
- tiempo promedio con el GPT;
- ahorro estimado por tarea;
- reducción de pasos manuales;
- volumen de casos atendidos.

### Adopción

- usuarios activos;
- frecuencia de uso;
- porcentaje de usuarios que repiten;
- número de tareas completadas;
- abandono durante la interacción.

### Experiencia

- facilidad de uso;
- claridad de las respuestas;
- utilidad percibida;
- confianza del usuario;
- satisfacción general.

### Riesgo

- respuestas fuera de alcance;
- exposición de información sensible;
- incumplimiento de restricciones;
- alucinaciones relevantes;
- decisiones incorrectas no detectadas;
- necesidad de intervención humana.

---

## 10. Métricas y línea base

Para demostrar mejora necesitas comparar el desempeño del GPT con la situación actual.

Ejemplo:

| Indicador | Línea base | Meta MVP | Resultado |
|---|---:|---:|---:|
| Tiempo promedio por caso | 30 min | ≤ 15 min | Pendiente |
| Respuestas aceptadas | 70 % | ≥ 85 % | Pendiente |
| Errores críticos | 5 % | 0 % | Pendiente |
| Satisfacción | 3.2/5 | ≥ 4/5 | Pendiente |
| Usuarios que repiten | No aplica | ≥ 70 % | Pendiente |

La meta debe definirse antes de ejecutar el piloto para evitar reinterpretar los resultados después.

---

## 11. Human in the Loop

Durante el MVP, las decisiones relevantes deben mantener supervisión humana.

El usuario o especialista debe:

- revisar la respuesta antes de usarla en un proceso crítico;
- confirmar datos sensibles o regulatorios;
- corregir resultados incorrectos;
- registrar hallazgos;
- escalar casos no contemplados;
- decidir cuando existe incertidumbre alta.

El GPT recomienda, organiza o genera borradores. La responsabilidad final permanece en las personas y en el proceso de negocio.

---

## 12. Plan de ejecución del piloto

### Fase 1. Preparación

- confirmar versión del GPT;
- congelar el Prompt Maestro del piloto;
- validar archivos de conocimiento;
- definir usuarios y escenarios;
- establecer métricas y línea base;
- comunicar restricciones;
- preparar registro de evidencias.

### Fase 2. Inducción

- explicar el objetivo del MVP;
- enseñar cómo iniciar una conversación;
- mostrar ejemplos correctos;
- explicar qué información no debe ingresarse;
- indicar cómo reportar errores;
- aclarar que el GPT no reemplaza decisiones críticas.

### Fase 3. Ejecución

- utilizar el GPT en casos autorizados;
- registrar entradas y resultados según las políticas aplicables;
- medir tiempos;
- clasificar respuestas;
- documentar errores, dudas y mejoras;
- recoger retroalimentación de usuarios.

### Fase 4. Evaluación

- consolidar métricas;
- comparar contra la línea base;
- analizar riesgos;
- identificar patrones de fallo;
- priorizar mejoras;
- recomendar una decisión.

---

## 13. Registro de evidencias

Utiliza una tabla similar a la siguiente:

| ID | Escenario | Resultado esperado | Resultado obtenido | Estado | Hallazgo | Severidad | Acción |
|---|---|---|---|---|---|---|---|
| MVP-001 | Caso normal | Informe completo | Informe completo | Aprobado | Ninguno | Baja | Ninguna |
| MVP-002 | Datos faltantes | Solicitar información | Asumió un valor | Fallido | No aplicó validación | Alta | Ajustar prompt |

Estados recomendados:

- Aprobado;
- Aprobado con observaciones;
- Fallido;
- Bloqueado;
- Fuera de alcance.

Severidad recomendada:

- Crítica;
- Alta;
- Media;
- Baja.

---

## 14. Retroalimentación de usuarios

Las preguntas deben generar información accionable.

### Preguntas sugeridas

1. ¿Qué tarea intentaste realizar?
2. ¿La respuesta fue útil para completar la tarea?
3. ¿Qué parte fue correcta?
4. ¿Qué parte tuviste que modificar?
5. ¿Qué información faltó?
6. ¿La respuesta fue fácil de entender?
7. ¿Confiarías en usarla nuevamente con revisión humana?
8. ¿Cuánto tiempo ahorraste?
9. ¿Qué riesgo o preocupación identificaste?
10. ¿Qué mejora tendría mayor impacto?

Evita depender solamente de preguntas generales como “¿Te gustó?”.

---

## 15. Criterios de decisión

Al finalizar el MVP, el equipo debe tomar una decisión explícita.

### Escalar

Aplica cuando:

- las métricas principales alcanzan la meta;
- no existen riesgos críticos abiertos;
- los usuarios muestran adopción;
- el valor está respaldado por evidencia;
- existe un propietario responsable;
- se cuenta con capacidad para operar y mejorar el GPT.

### Mejorar y repetir

Aplica cuando:

- el valor potencial está confirmado;
- existen fallos solucionables;
- las métricas están cerca de la meta;
- se requieren cambios de prompt, conocimiento o experiencia;
- no existen riesgos críticos sin tratamiento.

### Pausar

Aplica cuando:

- faltan datos o documentos esenciales;
- no existe disponibilidad de usuarios;
- hay dependencias técnicas no resueltas;
- el contexto organizacional impide continuar temporalmente.

### Cancelar

Aplica cuando:

- el problema no es relevante;
- la solución no genera valor suficiente;
- los riesgos superan los beneficios;
- el GPT no alcanza calidad mínima después de iteraciones razonables;
- existe una alternativa más simple o efectiva.

---

## 16. Criterios mínimos para pasar a una siguiente etapa

Antes de ampliar el alcance, verifica:

- [ ] El problema fue confirmado con usuarios reales.
- [ ] El GPT resuelve los escenarios prioritarios.
- [ ] Las respuestas cumplen los criterios de aceptación.
- [ ] No existen errores críticos abiertos.
- [ ] Las restricciones se aplican correctamente.
- [ ] El manejo de incertidumbre funciona.
- [ ] El conocimiento utilizado está autorizado y vigente.
- [ ] Los usuarios comprenden las limitaciones.
- [ ] Existe evidencia de ahorro, calidad o valor.
- [ ] Se definió un propietario del GPT.
- [ ] Existe un plan de soporte y mejora.
- [ ] Se registró una decisión formal.

---

## 17. Antipatrones

Evita estos errores:

### Llamar MVP a una demostración

Mostrar una respuesta preparada no valida uso real.

### Medir solo satisfacción

Un GPT puede resultar atractivo y, al mismo tiempo, producir errores relevantes.

### Cambiar el prompt durante el piloto sin registrar versiones

Esto impide saber qué versión generó cada resultado.

### Ampliar el alcance demasiado pronto

Agregar usuarios, documentos y tareas antes de estabilizar el caso principal aumenta la complejidad.

### Ignorar resultados negativos

Los errores son evidencia para mejorar o detener la iniciativa.

### Automatizar decisiones antes de validar

Primero debe demostrarse calidad y control con supervisión humana.

### No asignar propietario

Sin una persona o área responsable, el GPT se degrada y queda sin mantenimiento.

---

## 18. Entregables del MVP

Al finalizar, conserva como mínimo:

1. GPT Canvas actualizado.
2. Prompt Maestro versionado.
3. Configuración del GPT.
4. Inventario de conocimiento utilizado.
5. Matriz de casos de prueba.
6. Ficha del MVP.
7. Registro de evidencias.
8. Métricas y comparación con línea base.
9. Hallazgos y riesgos.
10. Backlog de mejoras.
11. Recomendación de decisión.
12. Acta o aprobación del responsable.

---

## 19. Laboratorio ILC

### Actividad

Convierte el GPT priorizado por tu equipo en un MVP controlado.

### Paso 1. Define las hipótesis

Escribe una hipótesis de problema, solución, adopción, valor y riesgo.

### Paso 2. Acota el alcance

Define claramente qué incluye y qué no incluye el MVP.

### Paso 3. Selecciona usuarios

Identifica entre tres y cinco usuarios piloto representativos.

### Paso 4. Diseña escenarios

Prepara como mínimo siete casos:

- normal;
- incompleto;
- ambiguo;
- límite;
- restringido;
- contradictorio;
- adversarial.

### Paso 5. Define métricas

Incluye al menos:

- una métrica de calidad;
- una de eficiencia;
- una de adopción;
- una de experiencia;
- una de riesgo.

### Paso 6. Ejecuta y registra

Documenta cada interacción, el resultado y los hallazgos.

### Paso 7. Presenta una decisión

Selecciona una opción:

- Escalar;
- Mejorar y repetir;
- Pausar;
- Cancelar.

Sustenta la decisión con evidencia.

---

## 20. Plantilla de informe ejecutivo

```markdown
# Informe de Resultados del MVP

## 1. Resumen ejecutivo

## 2. Problema validado

## 3. Alcance del MVP

## 4. Usuarios y escenarios

## 5. Resultados de métricas

## 6. Comparación con línea base

## 7. Hallazgos principales

## 8. Riesgos y controles

## 9. Retroalimentación de usuarios

## 10. Backlog de mejoras

## 11. Decisión recomendada

## 12. Próximos pasos
```

---

## Resumen ejecutivo

El MVP es la etapa donde el GPT deja de ser una configuración prometedora y comienza a demostrar valor en el trabajo real. Su propósito es aprender con usuarios, medir resultados y reducir incertidumbre antes de ampliar inversión, alcance o automatización.

En la metodología ILC, un MVP exitoso no se define únicamente porque el GPT responde. Se define porque existe evidencia de que responde con calidad suficiente, aporta valor, mantiene controles adecuados y puede evolucionar de manera responsable.
