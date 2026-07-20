# Manual ILC – Construcción de GPTs Empresariales

# Capítulo 2. Conociendo el GPT Canvas

En el capítulo anterior conocimos el problema que queremos resolver. Ahora vamos a diseñar el GPT antes de construirlo.

## 1. ¿Qué es un GPT Canvas?

Un **GPT Canvas** es un plano sencillo que ayuda a ordenar las decisiones más importantes de un GPT.

Piensa en la construcción de una casa:

- El caso de uso explica por qué necesitamos la casa.
- El GPT Canvas es el plano.
- El Prompt Maestro contiene las instrucciones de construcción.
- La configuración convierte el plano en un GPT funcional.

El Canvas evita comenzar directamente en ChatGPT sin tener claridad sobre el objetivo, los usuarios, la información y los límites del GPT.

> **Idea clave:** primero diseñamos el comportamiento; después configuramos la herramienta.

---

## 2. Las preguntas que debe responder el Canvas

Antes de construir un GPT, necesitamos responder estas preguntas:

1. ¿Qué problema queremos resolver?
2. ¿Quién utilizará el GPT?
3. ¿Qué debe hacer?
4. ¿Qué información recibirá?
5. ¿Qué resultado debe entregar?
6. ¿Qué no debe hacer?
7. ¿Cómo sabremos que funciona correctamente?

Si alguna de estas preguntas todavía no tiene respuesta, no significa que el caso sea incorrecto. Significa que debemos conversar con el dueño del proceso antes de construir.

---

## 3. Los bloques del GPT Canvas ILC

| Bloque | Pregunta sencilla |
|---|---|
| Nombre del GPT | ¿Cómo identificaremos al asistente? |
| Problema de negocio | ¿Qué dificultad queremos reducir? |
| Usuarios | ¿Quiénes lo utilizarán? |
| Objetivo | ¿Qué resultado debe ayudar a conseguir? |
| Entradas | ¿Qué información recibirá? |
| Conocimiento | ¿Qué documentos o reglas debe consultar? |
| Actividades | ¿Qué pasos debe realizar? |
| Salidas | ¿Qué debe entregar al usuario? |
| Restricciones | ¿Qué no está autorizado a hacer? |
| Validación humana | ¿Quién revisa o aprueba el resultado? |
| Criterios de éxito | ¿Cómo mediremos que aporta valor? |

---

# 4. GPT Canvas desarrollado: caso ILC-16

## Nombre del GPT

**GPT Estructurador de Requerimientos Negocio–Tecnología**

### Explicación sencilla

El nombre indica claramente qué hace el GPT. Evitamos nombres demasiado creativos que no expliquen su utilidad.

---

## Problema de negocio

Las áreas de negocio envían solicitudes a Tecnología mediante correos, tickets, chats, reuniones o documentos. Muchas solicitudes llegan con información incompleta, términos ambiguos o sin criterios claros para validar el resultado.

Esto genera:

- reuniones adicionales;
- preguntas repetidas;
- diferencias de interpretación;
- retrabajo;
- demoras en la atención;
- requerimientos que cambian durante el desarrollo.

### Ejemplo de solicitud incompleta

> Necesitamos mejorar el módulo de clientes porque está muy lento.

La solicitud expresa una necesidad, pero todavía no indica:

- qué operación es lenta;
- cuánto demora actualmente;
- cuánto debería demorar;
- qué usuarios están afectados;
- desde cuándo ocurre;
- si sucede siempre o en determinados momentos;
- cuál es el impacto para el negocio.

---

## Usuarios

### Usuarios principales

- Analistas funcionales.
- Product Owners.
- Analistas de Tecnología.
- Líderes de proyectos.
- Usuarios de negocio que registran solicitudes.

### Usuario que valida

El dueño del proceso o responsable funcional debe confirmar que el requerimiento representa correctamente la necesidad del negocio.

---

## Objetivo

Ayudar a transformar una solicitud inicial del negocio en un requerimiento funcional claro, ordenado y listo para ser revisado con Tecnología.

El GPT debe:

- comprender la solicitud inicial;
- identificar información faltante;
- formular preguntas sencillas;
- separar hechos, supuestos y dudas;
- organizar reglas de negocio;
- proponer criterios de aceptación;
- sugerir escenarios de prueba;
- preparar una ficha preliminar de requerimiento.

> El GPT no reemplaza al analista funcional. Lo ayuda a trabajar con mayor orden y velocidad.

---

## Entradas

El usuario puede proporcionar uno o varios de los siguientes elementos:

- correo electrónico;
- ticket o registro de atención;
- mensaje de chat;
- minuta de reunión;
- documento Word;
- archivo Excel;
- diagrama o flujograma;
- requerimiento anterior;
- reglas de negocio;
- escenarios de prueba existentes.

### Regla importante

El GPT debe trabajar únicamente con la información entregada o con los documentos autorizados. Cuando falte información, debe preguntarla en lugar de inventarla.

---

## Conocimiento que puede utilizar

Para mejorar sus respuestas, el GPT puede consultar:

- plantilla corporativa de requerimientos;
- glosario de términos del negocio;
- catálogo de sistemas;
- mapa de procesos;
- ejemplos aprobados de requerimientos anteriores;
- políticas de seguridad y privacidad;
- guía para redactar criterios de aceptación;
- estándares de documentación funcional.

### Recomendación ILC

Cada documento debe tener:

- propietario;
- fecha de actualización;
- versión;
- nivel de confidencialidad;
- fecha de próxima revisión.

No debemos cargar documentos antiguos sin saber si todavía son válidos.

---

## Actividades del GPT

El GPT realizará las siguientes actividades:

1. Leer la solicitud recibida.
2. Identificar el objetivo principal.
3. Reconocer usuarios, sistemas y procesos involucrados.
4. Detectar información faltante o ambigua.
5. Formular preguntas de aclaración.
6. Esperar las respuestas del usuario cuando la información sea crítica.
7. Organizar el requerimiento.
8. Identificar reglas de negocio.
9. Separar alcance y fuera de alcance.
10. Proponer criterios de aceptación.
11. Sugerir escenarios de prueba.
12. Señalar riesgos, supuestos y preguntas pendientes.
13. Generar una ficha preliminar para revisión humana.

---

## Salidas esperadas

El GPT debe entregar una ficha con la siguiente estructura:

1. Título del requerimiento.
2. Resumen de la necesidad.
3. Problema actual.
4. Objetivo esperado.
5. Usuarios involucrados.
6. Proceso y sistemas afectados.
7. Alcance.
8. Fuera de alcance.
9. Requerimientos funcionales.
10. Reglas de negocio.
11. Requerimientos no funcionales identificados.
12. Criterios de aceptación.
13. Escenarios de prueba sugeridos.
14. Supuestos.
15. Riesgos.
16. Información pendiente.
17. Fuentes utilizadas.
18. Estado del documento: borrador, en revisión o validado.

---

## Restricciones y guardrails

El GPT:

- no debe inventar requisitos;
- no debe asumir que una información es correcta si no ha sido confirmada;
- no debe aprobar el requerimiento;
- no debe decidir la solución tecnológica final;
- no debe modificar sistemas ni datos;
- no debe exponer información confidencial;
- no debe eliminar preguntas pendientes para que el documento parezca completo;
- no debe presentar supuestos como hechos;
- debe indicar cuando una respuesta requiere validación legal, de seguridad, arquitectura o negocio.

> **Guardrail principal:** cuando falte información crítica, el GPT debe detener la elaboración final y solicitar aclaraciones.

---

## Validación humana

La ficha generada debe ser revisada por:

1. El dueño de la necesidad de negocio.
2. El analista funcional o Product Owner.
3. Tecnología, cuando corresponda.
4. Seguridad, Legal o Datos, si el requerimiento los involucra.

El GPT prepara un borrador. Las personas responsables validan y aprueban.

---

## Criterios de éxito

Consideraremos que el GPT funciona correctamente cuando:

- identifica la información faltante;
- formula preguntas comprensibles;
- no inventa requisitos;
- genera una estructura consistente;
- mantiene trazabilidad con la información original;
- reduce el tiempo de preparación del requerimiento;
- disminuye observaciones durante la revisión;
- el dueño del proceso reconoce el documento como útil y correcto.

### Indicadores sencillos para el MVP

| Indicador | Cómo medirlo |
|---|---|
| Tiempo de preparación | Comparar el tiempo manual con el tiempo usando el GPT |
| Información faltante detectada | Contar preguntas relevantes identificadas por el GPT |
| Requerimientos aceptados en primera revisión | Medir cuántos necesitan pocas correcciones |
| Satisfacción del usuario | Encuesta breve de 1 a 5 |
| Trazabilidad | Verificar que cada afirmación importante tenga una fuente o confirmación |

---

# 5. Vista resumida del Canvas

| Elemento | Definición para el caso ILC-16 |
|---|---|
| Usuario | Negocio, analistas funcionales y Tecnología |
| Problema | Solicitudes incompletas y ambiguas |
| Objetivo | Convertir una necesidad inicial en un requerimiento estructurado |
| Entradas | Correos, tickets, minutas, Word, Excel y diagramas |
| Proceso | Leer, preguntar, organizar, validar y documentar |
| Salida | Ficha preliminar de requerimiento funcional |
| Restricción principal | No inventar información ni aprobar decisiones |
| Validación | Dueño del proceso y analista responsable |
| Éxito | Menos tiempo, menos retrabajo y mayor claridad |

---

# 6. Errores comunes al llenar un GPT Canvas

## Error 1. Definir un objetivo demasiado amplio

**Incorrecto:**

> Ayudar al área de Tecnología.

**Mejor:**

> Transformar una solicitud inicial del negocio en una ficha preliminar de requerimiento funcional lista para revisión.

---

## Error 2. Confundir actividad con resultado

**Actividad:** analizar un correo.

**Resultado:** ficha estructurada con preguntas, reglas, criterios y pruebas.

El Canvas debe dejar claro qué entrega el GPT al final.

---

## Error 3. No definir límites

Un GPT sin límites puede responder con demasiada seguridad o asumir tareas que no le corresponden.

En este caso, el GPT puede estructurar y sugerir, pero no puede aprobar, desarrollar ni decidir la arquitectura.

---

## Error 4. Diseñar el GPT sin participación del usuario

El Canvas debe validarse con la persona que conoce el proceso. Un diseño técnicamente correcto puede ser poco útil si no refleja la forma real de trabajar.

---

# 7. Ahora hazlo tú

Selecciona el caso de uso de tu equipo y completa estas frases:

- El usuario principal es: ______________________________
- El problema que queremos reducir es: __________________
- El GPT ayudará a: _____________________________________
- La información que recibirá será: ______________________
- El resultado esperado será: ____________________________
- El GPT no deberá: _____________________________________
- La persona que validará será: __________________________
- Sabremos que funciona cuando: __________________________

---

# 8. Checklist del capítulo

Antes de avanzar, confirma lo siguiente:

- [ ] El problema está explicado con palabras sencillas.
- [ ] El usuario principal está identificado.
- [ ] El objetivo describe un resultado concreto.
- [ ] Las entradas están disponibles o pueden prepararse.
- [ ] La salida tiene una estructura definida.
- [ ] Los límites del GPT están escritos.
- [ ] Existe una persona responsable de validar.
- [ ] Los criterios de éxito pueden medirse.

---

## Siguiente capítulo

En el próximo capítulo aprenderemos a convertir este Canvas en instrucciones claras mediante el **Prompt Maestro ILC**.