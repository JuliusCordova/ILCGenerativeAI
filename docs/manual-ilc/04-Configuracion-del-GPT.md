# 04 – Configuración del GPT

## Objetivo

Este capítulo explica cómo transformar el Prompt Maestro aprobado en una configuración funcional dentro del constructor de GPTs.

El objetivo es mantener la trazabilidad entre el caso de negocio, el GPT Canvas, el Prompt Maestro y el GPT que será probado como MVP.

---

## Flujo ILC

```text
Caso de negocio
      ↓
GPT Canvas
      ↓
Prompt Maestro
      ↓
Configuración del GPT
      ↓
Pruebas
      ↓
MVP
```

La configuración no debe introducir comportamientos que no hayan sido definidos y revisados previamente.

---

## Componentes mínimos

La configuración debe incluir:

1. Nombre.
2. Descripción.
3. Instrucciones.
4. Conversaciones iniciales.
5. Conocimiento.
6. Capacidades.
7. Identidad visual.
8. Propietario.
9. Versión y estado.
10. Casos de prueba.

---

## 1. Nombre

El nombre debe ser breve, profesional y orientado al propósito.

### Recomendaciones

- Utiliza entre dos y cinco palabras.
- Evita nombres genéricos como “Asistente IA”.
- Incluye el proceso o resultado principal.
- No prometas capacidades que el GPT no posee.

| Nombre débil | Nombre recomendado |
|---|---|
| Bot de empresa | Asistente de Compras ILC |
| IA de proyectos | Evaluador de Iniciativas |
| GPT financiero | Analista de Presupuesto |
| Ayudante legal | Revisor Documental Legal |

---

## 2. Descripción

La descripción debe indicar:

- a quién ayuda;
- qué información procesa;
- qué resultado genera;
- cuál es su límite principal.

### Plantilla

```text
Ayuda a [USUARIOS] a analizar [ENTRADAS] y generar [RESULTADO], aplicando [REGLAS O CRITERIOS]. No reemplaza la revisión de [RESPONSABLE HUMANO].
```

### Ejemplo

```text
Ayuda al equipo de proyectos a revisar iniciativas, identificar información faltante y preparar una evaluación ejecutiva. No reemplaza la decisión del comité.
```

---

## 3. Instrucciones

Las instrucciones son el núcleo operativo del GPT.

Copia el Prompt Maestro validado y confirma que incluya:

- rol;
- objetivo;
- contexto;
- alcance;
- entradas;
- proceso;
- formato de salida;
- restricciones;
- validaciones;
- manejo de incertidumbre;
- mejora continua.

> El constructor configura; el Prompt Maestro gobierna el comportamiento.

No agregues reglas nuevas en el constructor sin actualizar también el Prompt Maestro.

---

## 4. Conversaciones iniciales

Las conversaciones iniciales muestran al usuario cómo empezar.

### Recomendaciones

- Incluye entre tres y cinco opciones.
- Usa verbos de acción.
- Representa tareas reales.
- Evita solicitudes demasiado generales.
- Incluye una opción para validar información.

### Ejemplos

```text
Analiza este caso y genera [RESULTADO].

Valida si la información está completa antes de continuar.

Compara estas alternativas usando [CRITERIOS].

Identifica riesgos, vacíos y próximos pasos.

Genera una versión ejecutiva para [AUDIENCIA].
```

---

## 5. Conocimiento

La sección de conocimiento contiene los documentos que el GPT utilizará como referencia.

Cada archivo debe ser:

- relevante;
- vigente;
- autorizado;
- legible;
- identificado con versión y propietario;
- libre de duplicidad innecesaria.

### Inventario recomendado

| Archivo | Propietario | Versión | Vigencia | Clasificación | Uso esperado |
|---|---|---|---|---|---|
| [Documento] | [Área] | [Versión] | [Fecha] | [Nivel] | [Uso] |

### Buenas prácticas

- No cargues documentos sin una finalidad definida.
- Retira versiones obsoletas.
- Separa documentos normativos de ejemplos.
- Define qué fuente prevalece cuando dos documentos discrepan.
- Registra los cambios realizados.

---

## 6. Capacidades

Habilita únicamente las capacidades necesarias para el caso de uso.

| Capacidad | Utilizar cuando | Riesgo principal |
|---|---|---|
| Navegación web | Se requiere información pública actualizada | Fuentes no confiables o cambios recientes |
| Análisis de archivos | El caso procesa documentos o tablas | Información sensible o formatos ilegibles |
| Ejecución de código | Se requieren cálculos o transformación de datos | Resultados no validados |
| Generación de imágenes | El resultado requiere contenido visual | Representaciones inexactas |

> Toda capacidad debe tener una justificación de negocio, un responsable y un caso de prueba.

---

## 7. Identidad visual

La imagen y el nombre deben permitir que el usuario identifique rápidamente el propósito del GPT.

Utiliza:

- un icono relacionado con el proceso;
- colores coherentes con la organización;
- una estética profesional;
- elementos que no confundan al GPT con una autoridad humana.

Evita imágenes que impliquen certificación, aprobación oficial o capacidades inexistentes.

---

## 8. Propietario, versión y estado

Todo GPT debe tener un responsable funcional.

| Campo | Ejemplo |
|---|---|
| Nombre | Evaluador de Iniciativas |
| Versión | 0.1.0 |
| Estado | Borrador, Piloto, Aprobado o Retirado |
| Propietario funcional | Oficina de Proyectos |
| Responsable técnico | Equipo de IA |
| Fecha de actualización | AAAA-MM-DD |
| Próxima revisión | AAAA-MM-DD |

### Versionamiento sugerido

```text
0.1.0  Primer prototipo
0.2.0  Ajustes posteriores a pruebas
1.0.0  MVP aprobado
1.1.0  Mejora funcional compatible
2.0.0  Cambio relevante de alcance o comportamiento
```

---

## 9. Visibilidad y acceso

Antes de compartir el GPT, define:

- quién puede utilizarlo;
- qué información puede cargar cada usuario;
- qué grupos tendrán acceso;
- si puede compartirse fuera de la organización;
- cómo se retirará el acceso;
- quién atenderá consultas o incidentes.

No publiques un GPT con documentos internos como recurso de acceso público.

---

## Configuración base reutilizable

```yaml
metadata:
  nombre: "[NOMBRE DEL GPT]"
  version: "0.1.0"
  estado: "Borrador"
  propietario_funcional: "[ÁREA]"
  responsable_tecnico: "[EQUIPO]"

descripcion: >
  Ayuda a [USUARIOS] a analizar [ENTRADAS] y generar [RESULTADO].
  No reemplaza la revisión de [RESPONSABLE HUMANO].

conversation_starters:
  - "Analiza este caso y genera [RESULTADO]."
  - "Valida si la información está completa."
  - "Identifica riesgos y próximos pasos."
  - "Genera una versión ejecutiva."

conocimiento:
  documentos_autorizados:
    - nombre: "[DOCUMENTO]"
      version: "[VERSIÓN]"
      propietario: "[ÁREA]"

capacidades:
  navegacion_web: false
  analisis_archivos: true
  ejecucion_codigo: false
  generacion_imagenes: false

acceso:
  audiencia: "[GRUPO AUTORIZADO]"
  uso_externo: false
```

---

## Validaciones antes de guardar

- [ ] El nombre refleja el propósito.
- [ ] La descripción identifica usuarios, tarea y límite.
- [ ] Las instrucciones corresponden al Prompt Maestro aprobado.
- [ ] Las conversaciones iniciales están dentro del alcance.
- [ ] Los documentos están autorizados y vigentes.
- [ ] No existen versiones duplicadas o contradictorias.
- [ ] Solo están activadas las capacidades necesarias.
- [ ] El GPT tiene propietario funcional.
- [ ] La versión y el estado están registrados.
- [ ] La visibilidad corresponde a la clasificación de la información.
- [ ] Existen casos de prueba definidos.

---

## Antipatrones

Evita:

- cargar todos los documentos disponibles;
- activar todas las capacidades sin necesidad;
- utilizar instrucciones diferentes al Prompt Maestro;
- compartir el GPT antes de probarlo;
- no definir un propietario;
- prometer decisiones automáticas en la descripción;
- mezclar información real con datos de prueba;
- modificar el GPT sin registrar una nueva versión.

---

## Laboratorio

Configura el GPT priorizado por tu equipo.

### Entregables

1. Nombre y descripción final.
2. Prompt Maestro cargado como instrucciones.
3. Cuatro conversaciones iniciales.
4. Inventario de documentos de conocimiento.
5. Capacidades habilitadas y justificación.
6. Propietario, versión y estado.
7. Evidencia visual de la configuración.
8. Lista de casos de prueba pendientes.

### Criterio de finalización

El GPT está listo para pasar a pruebas cuando su configuración es coherente con el Canvas y el Prompt Maestro, sus documentos están controlados, sus capacidades están justificadas y existe un responsable funcional claramente identificado.

---

## Resumen ejecutivo

Configurar un GPT no consiste únicamente en pegar un prompt. Implica convertir el diseño funcional en un producto controlado: con identidad, instrucciones, conocimiento, capacidades, acceso, propietario, versión y pruebas.

En la metodología ILC, la configuración debe mantener trazabilidad con el GPT Canvas y el Prompt Maestro. El resultado de este capítulo es un GPT en estado de borrador, preparado para ingresar al ciclo de pruebas antes de convertirse en MVP.