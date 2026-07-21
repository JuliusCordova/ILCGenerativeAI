# Capítulo 3.5. Formato de salida del Prompt Maestro

## Objetivo

Este bloque explica cómo definir la estructura, el nivel de detalle y las reglas de presentación que debe seguir un GPT al entregar sus resultados. El Formato de salida convierte una respuesta generada por IA en un entregable consistente, legible y reutilizable.

## Bloque 6: Formato de salida

El Formato de salida responde una pregunta fundamental:

> ¿Cómo debe presentar el GPT el resultado final?

Si el Rol define quién es el GPT, el Objetivo establece qué debe lograr, las Entradas indican qué información necesita y el Proceso determina cómo debe trabajar, el Formato de salida especifica cómo debe organizar y comunicar el entregable.

En el caso ILC-16, este bloque permite que los requerimientos funcionales mantengan una estructura estable, independientemente del usuario que realice la solicitud o del tipo de proceso analizado.

## Por qué el formato es parte del diseño del GPT

Una instrucción como la siguiente resulta insuficiente:

```text
Genera un requerimiento funcional claro y completo.
```

Aunque define una intención, no establece:

- qué secciones debe contener el documento;
- en qué orden deben aparecer;
- qué información es obligatoria;
- cómo distinguir hechos, supuestos y pendientes;
- qué nivel de detalle se espera;
- cómo presentar tablas, listas o criterios de aceptación;
- qué hacer cuando no existe información suficiente.

Cuando el formato no está definido, el GPT puede entregar respuestas correctas pero difíciles de comparar, revisar, aprobar o reutilizar.

## Del texto libre al entregable controlado

### Salida sin formato explícito

```text
El usuario necesita mejorar el inventario. Se recomienda implementar alertas,
reportes y controles de stock. También deberían definirse responsables y reglas.
```

La respuesta puede ser útil, pero mezcla problema, solución, alcance y recomendaciones sin una estructura verificable.

### Salida con formato explícito

```markdown
# Requerimiento funcional

## 1. Resumen ejecutivo

## 2. Problema de negocio

## 3. Objetivo

## 4. Alcance

## 5. Actores

## 6. Funcionalidades

## 7. Reglas de negocio

## 8. Excepciones

## 9. Criterios de aceptación

## 10. Supuestos, riesgos y pendientes
```

Esta estructura facilita la revisión, la trazabilidad y la comparación entre entregables.

## Características de un buen formato de salida

| Característica | Descripción |
|---|---|
| Estructurado | Divide el resultado en secciones claramente identificadas. |
| Consistente | Mantiene el mismo orden y criterios para solicitudes similares. |
| Completo | Incluye los elementos necesarios para cumplir el objetivo. |
| Legible | Utiliza títulos, tablas, listas y párrafos breves. |
| Verificable | Permite comprobar si cada sección contiene información suficiente. |
| Adaptable | Puede ajustarse al tipo de usuario o nivel de madurez del caso. |
| Accionable | Presenta información que puede utilizarse para decidir o ejecutar. |
| Transparente | Diferencia información confirmada, supuestos y pendientes. |

## Componentes del Formato de salida

Un formato bien diseñado debe especificar, como mínimo, cinco elementos.

| Elemento | Pregunta que responde |
|---|---|
| Estructura | ¿Qué secciones debe contener el entregable? |
| Orden | ¿En qué secuencia deben presentarse? |
| Contenido mínimo | ¿Qué debe incluir cada sección? |
| Estilo | ¿Cómo debe redactarse y visualizarse? |
| Tratamiento de vacíos | ¿Qué debe hacer el GPT cuando falta información? |

## Estructura recomendada para el caso ILC-16

El siguiente formato puede utilizarse para generar un requerimiento funcional empresarial.

```markdown
# Requerimiento funcional: [nombre de la iniciativa]

## 1. Resumen ejecutivo

## 2. Problema de negocio

## 3. Objetivo del requerimiento

## 4. Contexto y situación actual

## 5. Alcance

### 5.1 Incluye

### 5.2 No incluye

## 6. Actores y usuarios

## 7. Funcionalidades requeridas

## 8. Reglas de negocio

## 9. Excepciones y escenarios alternativos

## 10. Datos e integraciones

## 11. Requisitos no funcionales

## 12. Criterios de aceptación

## 13. Dependencias

## 14. Riesgos

## 15. Supuestos

## 16. Información pendiente de validar

## 17. Recomendación del siguiente paso
```

La estructura puede ampliarse o simplificarse según la complejidad del caso, pero no debe eliminar información crítica sin explicarlo.

## Sección 1: Resumen ejecutivo

Debe presentar una visión breve del problema, el objetivo, la solución esperada y el impacto buscado.

### Reglas recomendadas

- utilizar entre tres y cinco párrafos breves;
- evitar detalles técnicos innecesarios;
- destacar el valor para el negocio;
- indicar si el documento es preliminar o final;
- declarar cualquier limitación crítica.

### Ejemplo

```text
La iniciativa busca mejorar el control de inventario mediante alertas de stock,
visibilidad consolidada y reglas de reposición. El objetivo es reducir quiebres,
sobrestock y trabajo manual. El requerimiento se encuentra en estado preliminar
hasta validar los umbrales de reposición y las fuentes de datos disponibles.
```

## Sección 2: Problema de negocio

Debe explicar la situación actual y su impacto.

Debe incluir, cuando exista información:

- proceso afectado;
- usuarios involucrados;
- síntomas del problema;
- causas conocidas;
- impacto en tiempo, costo, calidad, riesgo o experiencia;
- evidencia disponible.

El GPT no debe presentar una hipótesis como si fuera una causa confirmada.

## Sección 3: Objetivo del requerimiento

Debe expresar el resultado esperado de manera concreta.

### Patrón recomendado

```text
Implementar [capacidad] para [usuario o proceso], con el propósito de [resultado de negocio], manteniendo [condiciones o restricciones relevantes].
```

### Ejemplo

```text
Implementar un mecanismo de monitoreo de inventario para los responsables de almacén, con el propósito de anticipar quiebres de stock y reducir reposiciones manuales.
```

## Sección 4: Contexto y situación actual

Debe describir cómo funciona hoy el proceso.

Puede incluir:

- pasos actuales;
- sistemas utilizados;
- responsables;
- controles manuales;
- puntos de dolor;
- frecuencia de ejecución;
- dependencias conocidas.

## Sección 5: Alcance

El alcance debe dividirse en dos partes.

### Incluye

Lista de capacidades, procesos, usuarios, datos o áreas cubiertas por la iniciativa.

### No incluye

Elementos que se excluyen explícitamente para evitar interpretaciones incorrectas.

### Ejemplo

| Incluye | No incluye |
|---|---|
| Consulta de stock por almacén | Optimización automática de compras |
| Alertas de nivel mínimo | Reemplazo del ERP |
| Reporte de productos críticos | Rediseño físico del almacén |

## Sección 6: Actores y usuarios

Debe identificar quién participa y qué responsabilidad tiene.

| Actor | Responsabilidad | Interacción esperada |
|---|---|---|
| Responsable de almacén | Revisar alertas y validar stock | Consulta y actualización |
| Jefe de operaciones | Supervisar indicadores | Consulta y aprobación |
| Administrador del sistema | Mantener parámetros | Configuración |

Cuando un rol no esté confirmado, debe marcarse como pendiente.

## Sección 7: Funcionalidades requeridas

Cada funcionalidad debe redactarse de forma clara, independiente y trazable.

### Plantilla recomendada

```text
FR-[número] — [nombre de la funcionalidad]

Descripción:
El sistema debe [comportamiento esperado].

Actor principal:
[rol]

Entrada:
[dato o evento]

Resultado:
[respuesta, acción o estado esperado]

Reglas relacionadas:
[identificadores]
```

### Ejemplo

```text
FR-01 — Generar alerta de stock mínimo

Descripción:
El sistema debe generar una alerta cuando el stock disponible de un producto sea igual o menor al umbral configurado.

Actor principal:
Responsable de almacén.

Entrada:
Stock disponible y umbral mínimo.

Resultado:
Alerta visible con producto, almacén, cantidad disponible y fecha de detección.

Reglas relacionadas:
RN-01 y RN-02.
```

## Sección 8: Reglas de negocio

Las reglas deben ser concretas y verificables.

### Plantilla recomendada

```text
RN-[número] — [nombre]

Si [condición], entonces [acción o resultado].
```

### Ejemplo

```text
RN-01 — Activación de alerta

Si el stock disponible es menor o igual al stock mínimo configurado, entonces el producto debe clasificarse como crítico.
```

## Sección 9: Excepciones y escenarios alternativos

Debe registrar condiciones que modifican el flujo normal.

| Identificador | Situación | Comportamiento esperado |
|---|---|---|
| EX-01 | No existe umbral configurado | Mostrar el producto como pendiente de parametrización. |
| EX-02 | La fuente de datos no responde | Informar indisponibilidad y registrar el incidente. |
| EX-03 | Existen datos contradictorios | No consolidar el resultado y solicitar validación. |

## Sección 10: Datos e integraciones

Debe mostrar qué información necesita la solución y de dónde proviene.

| Dato | Fuente | Frecuencia | Responsable | Estado |
|---|---|---|---|---|
| Stock disponible | ERP | Cada 15 minutos | Operaciones TI | Confirmado |
| Stock mínimo | Catálogo maestro | Diario | Planeamiento | Pendiente |

No deben inventarse nombres de sistemas, tablas, API o frecuencias cuando no han sido confirmados.

## Sección 11: Requisitos no funcionales

Debe incluir únicamente los requisitos relevantes para el caso.

Categorías frecuentes:

- seguridad;
- disponibilidad;
- rendimiento;
- privacidad;
- auditoría;
- accesibilidad;
- mantenibilidad;
- interoperabilidad;
- escalabilidad;
- recuperación ante errores.

### Ejemplo

```text
RNF-01 — Tiempo de respuesta

Las consultas de inventario deben responder en un tiempo objetivo menor a cinco segundos bajo la carga esperada.
```

Cuando el valor objetivo no esté confirmado, debe indicarse como pendiente y no asumirse.

## Sección 12: Criterios de aceptación

Los criterios deben permitir verificar si una funcionalidad fue implementada correctamente.

### Formato Given-When-Then

```gherkin
Dado que un producto tiene un stock disponible de 8 unidades
Y su stock mínimo configurado es 10
Cuando el sistema actualiza la información del inventario
Entonces debe clasificar el producto como crítico
Y debe generar una alerta para el responsable del almacén
```

### Reglas recomendadas

- cada criterio debe ser observable;
- debe evitar términos ambiguos como rápido, fácil o adecuado;
- debe relacionarse con una funcionalidad o regla;
- debe incluir escenarios positivos y excepciones relevantes;
- no debe depender de información no confirmada sin declararlo.

## Secciones 13 a 16: Dependencias, riesgos, supuestos y pendientes

Estos conceptos deben presentarse de manera separada.

| Categoría | Definición | Ejemplo |
|---|---|---|
| Dependencia | Elemento externo necesario para avanzar | Disponibilidad de una API del ERP. |
| Riesgo | Evento posible que puede afectar el resultado | Datos de stock desactualizados. |
| Supuesto | Condición considerada válida sin confirmación completa | Cada producto tiene un umbral mínimo. |
| Pendiente | Información o decisión aún no resuelta | Confirmar frecuencia de actualización. |

Mezclarlos reduce la claridad y puede convertir una suposición en una falsa certeza.

## Sección 17: Recomendación del siguiente paso

La salida debe terminar con una acción concreta.

Ejemplos:

- validar el alcance con el responsable de negocio;
- confirmar las fuentes de datos;
- revisar los criterios de aceptación;
- estimar esfuerzo y dependencias;
- preparar una sesión de refinamiento;
- construir un prototipo;
- aprobar el requerimiento para desarrollo.

## Reglas de estilo

El Prompt Maestro debe indicar cómo redactar el entregable.

### Recomendaciones

- utilizar Markdown;
- emplear títulos jerárquicos;
- usar tablas cuando faciliten la comparación;
- mantener párrafos breves;
- evitar lenguaje promocional;
- utilizar términos consistentes;
- numerar funcionalidades, reglas y criterios;
- escribir fechas en formato completo cuando sean relevantes;
- evitar abreviaturas no explicadas;
- adaptar el nivel técnico a la audiencia.

## Nivel de detalle

El formato también debe especificar cuánta profundidad se espera.

| Nivel | Uso recomendado | Características |
|---|---|---|
| Ejecutivo | Decisión y priorización | Resumen, impacto, alcance, riesgos y próximos pasos. |
| Funcional | Refinamiento de requerimientos | Funcionalidades, reglas, actores, escenarios y criterios. |
| Técnico | Diseño e implementación | Datos, integraciones, seguridad, rendimiento y operación. |

El GPT puede generar una combinación de niveles, pero debe señalar claramente la audiencia principal.

## Tratamiento de información faltante

Cuando falte información, el GPT no debe completar los vacíos con datos inventados.

Debe utilizar alguno de los siguientes estados:

- **Confirmado:** validado por el usuario o una fuente confiable.
- **Supuesto:** utilizado provisionalmente para avanzar.
- **Pendiente:** requiere respuesta o decisión.
- **No aplica:** no corresponde al caso.
- **No disponible:** no se cuenta con información.

### Ejemplo

| Campo | Valor | Estado |
|---|---|---|
| Frecuencia de actualización | Cada 15 minutos | Supuesto |
| Responsable de aprobación | Por definir | Pendiente |
| Fuente principal | ERP corporativo | Confirmado |

## Formato de borradores

Cuando el usuario solicite una versión preliminar, la salida debe indicarlo visiblemente.

```markdown
> **Estado del documento:** Borrador para validación
>
> Esta versión contiene supuestos y campos pendientes. No debe considerarse aprobada para desarrollo.
```

Además, debe incluir una sección específica de información pendiente.

## Formato de respuesta conversacional y formato documental

El GPT puede operar en dos modos.

### Modo conversacional

Se utiliza durante la recopilación y validación de información.

La respuesta debe ser breve y centrarse en:

- confirmar lo comprendido;
- identificar vacíos;
- formular preguntas específicas;
- mostrar avances parciales cuando aporten valor.

### Modo documental

Se utiliza cuando la información crítica es suficiente para construir el entregable.

La respuesta debe seguir la estructura completa definida en este capítulo.

No debe mezclarse una larga conversación de descubrimiento con el documento final.

## Formato recomendado para el bloque del Prompt Maestro

```text
FORMATO DE SALIDA

1. Entrega el resultado en Markdown.
2. Utiliza la siguiente estructura:
   - Título del requerimiento.
   - Resumen ejecutivo.
   - Problema de negocio.
   - Objetivo.
   - Contexto y situación actual.
   - Alcance incluido y excluido.
   - Actores y usuarios.
   - Funcionalidades numeradas.
   - Reglas de negocio numeradas.
   - Excepciones.
   - Datos e integraciones.
   - Requisitos no funcionales.
   - Criterios de aceptación.
   - Dependencias.
   - Riesgos.
   - Supuestos.
   - Pendientes de validación.
   - Siguiente paso recomendado.
3. Utiliza tablas cuando faciliten la comparación.
4. Redacta funcionalidades, reglas y criterios de forma verificable.
5. Diferencia información confirmada, supuestos y pendientes.
6. No inventes valores para completar campos vacíos.
7. Si el documento es preliminar, identifícalo como borrador.
8. Mantén un lenguaje profesional, claro y adecuado para la audiencia.
9. Verifica que todas las secciones relevantes estén completas antes de entregar.
```

## Antipatrones

### Entregar un bloque de texto continuo

Dificulta la lectura y oculta omisiones.

### Usar títulos sin contenido mínimo

Una estructura vacía no garantiza calidad. Cada sección debe tener criterios claros.

### Mezclar hechos y supuestos

El lector puede interpretar información provisional como confirmada.

### Presentar recomendaciones como requisitos aprobados

Una propuesta del GPT no debe convertirse automáticamente en una decisión de negocio.

### Incluir detalles técnicos inventados

No deben asumirse tecnologías, integraciones, volúmenes o niveles de servicio.

### Utilizar criterios de aceptación ambiguos

Frases como “el sistema debe ser rápido” no permiten validar el resultado.

### Entregar una versión final con pendientes críticos ocultos

Cuando falte información esencial, el estado del documento debe reflejarlo.

## Lista de verificación

Antes de aprobar el bloque Formato de salida, comprueba lo siguiente:

- [ ] La estructura del entregable está definida.
- [ ] El orden de las secciones es lógico.
- [ ] Cada sección tiene un contenido mínimo esperado.
- [ ] El nivel de detalle corresponde a la audiencia.
- [ ] Se especifica el estilo de redacción.
- [ ] Se define cómo presentar tablas, listas y numeración.
- [ ] Se diferencian hechos, supuestos y pendientes.
- [ ] Se indica qué hacer cuando falta información.
- [ ] Las funcionalidades y reglas pueden trazarse.
- [ ] Los criterios de aceptación son verificables.
- [ ] Se identifica claramente el estado del documento.
- [ ] La salida termina con un siguiente paso útil.

## Laboratorio práctico

### Actividad

Diseña el Formato de salida para un GPT que documenta oportunidades de automatización en una empresa.

El formato debe incluir, como mínimo:

1. nombre de la oportunidad;
2. problema actual;
3. proceso afectado;
4. usuarios involucrados;
5. tareas manuales;
6. frecuencia y volumen;
7. impacto esperado;
8. propuesta de automatización;
9. datos y sistemas involucrados;
10. riesgos;
11. supuestos;
12. criterios de éxito;
13. información pendiente;
14. recomendación del siguiente paso.

### Criterios de revisión

El resultado debe:

- ser comprensible para negocio y tecnología;
- distinguir información confirmada de supuestos;
- permitir comparar varias oportunidades;
- facilitar una decisión de priorización;
- evitar completar datos inexistentes;
- mantener una estructura reutilizable.

## Resultado esperado

Al finalizar este capítulo, debes poder diseñar una salida que sea:

- consistente;
- verificable;
- legible;
- trazable;
- adaptable a la audiencia;
- útil para tomar decisiones;
- segura frente a información incompleta.

## Resumen

El Formato de salida no es una decisión estética. Es un mecanismo de control que transforma la respuesta del GPT en un entregable profesional y repetible.

Un buen formato define:

1. qué secciones debe incluir la respuesta;
2. qué información mínima debe contener cada sección;
3. cómo debe presentarse el contenido;
4. cómo deben tratarse los vacíos y las incertidumbres;
5. cómo debe verificarse la calidad antes de la entrega.

En la metodología ILC, este bloque conecta el trabajo interno del GPT con el documento que finalmente recibe y utiliza el usuario.