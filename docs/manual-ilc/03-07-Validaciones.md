# 03.07 – Validaciones del Prompt Maestro

## Objetivo

Una de las diferencias entre un prompt improvisado y un **Prompt Maestro profesional** es que este último incorpora mecanismos para validar la calidad de la información antes, durante y después de generar una respuesta.

Las validaciones permiten que el GPT detecte información incompleta, inconsistente o ambigua antes de producir un resultado, reduciendo errores y aumentando la confiabilidad.

---

## ¿Qué son las validaciones?

Las validaciones son reglas que el GPT debe ejecutar para verificar que:

- la información recibida sea suficiente;
- los datos sean consistentes;
- no existan contradicciones;
- el resultado cumpla el formato esperado;
- la respuesta tenga calidad antes de entregarse.

No forman parte del conocimiento.

No forman parte del proceso.

Son una **capa de control de calidad**.

---

## ¿Por qué son importantes?

Sin validaciones, un GPT suele:

- inventar información faltante;
- asumir datos incorrectos;
- producir respuestas inconsistentes;
- mezclar conceptos;
- entregar resultados difíciles de reutilizar.

Con validaciones, el GPT aprende a detenerse cuando detecta problemas.

---

## Momento donde actúan

Las validaciones pueden ejecutarse en tres momentos.

### Antes

Verifican la entrada.

Ejemplos:

- ¿Todos los datos requeridos existen?
- ¿Falta algún archivo?
- ¿Se entiende la solicitud?

### Durante

Controlan el procesamiento.

Ejemplos:

- ¿Existe contradicción entre documentos?
- ¿Hay datos duplicados?
- ¿Hay campos vacíos?

### Después

Revisan el resultado final.

Ejemplos:

- ¿Se respetó el formato?
- ¿La respuesta atiende la solicitud?
- ¿Hay secciones incompletas?

---

## Tipos de validaciones ILC

### 1. Validación de completitud

Comprueba que toda la información necesaria esté disponible.

```text
No continúes si faltan datos obligatorios.
Solicita la información faltante.
```

### 2. Validación de consistencia

Busca contradicciones entre datos, documentos o instrucciones.

```text
Si dos documentos contienen información distinta,
indica la inconsistencia.
No inventes cuál es correcta.
```

### 3. Validación de formato

Verifica que el resultado siga la estructura definida.

Puede incluir:

- Markdown;
- tabla;
- JSON;
- lista;
- documento ejecutivo.

### 4. Validación de restricciones

Comprueba que no se violen las reglas del Prompt Maestro.

Ejemplos:

- No responder temas legales.
- No modificar datos.
- No generar código.
- No exponer información confidencial.

### 5. Validación de confianza

El GPT debe identificar cuando no posee suficiente evidencia.

```text
Si el nivel de confianza es bajo,
indica claramente la incertidumbre.
```

---

## Patrón ILC recomendado

```text
Validar entradas
      ↓
Validar contexto
      ↓
Validar restricciones
      ↓
Generar respuesta
      ↓
Validar formato
      ↓
Validar calidad
      ↓
Entregar resultado
```

---

## Ejemplo comparativo

### Prompt débil

```text
Resume este documento.
```

Problemas:

- no verifica que el documento exista;
- no valida que sea legible;
- no controla el idioma;
- no define longitud;
- puede resumir información parcial.

### Prompt Maestro con validaciones

```text
Antes de generar el resumen:

1. Verifica que exista un documento adjunto.
2. Verifica que el contenido pueda leerse.
3. Identifica el idioma principal.
4. Si existen páginas ilegibles, notifícalo.
5. Si falta información crítica, solicita aclaración.

Luego genera el resumen.

Finalmente valida que el resultado:

- cubra todas las secciones relevantes;
- no invente información;
- mantenga un tono ejecutivo;
- tenga como máximo una página;
- indique cualquier limitación detectada.
```

---

## Qué hacer cuando una validación falla

Cuando una validación falla, el GPT debe aplicar una respuesta controlada.

### Regla general

```text
Si una validación crítica falla:

1. Detén el proceso.
2. Explica el problema con claridad.
3. Indica qué información falta o es inconsistente.
4. Solicita únicamente los datos necesarios para continuar.
5. No inventes información para completar el resultado.
```

### Validaciones críticas y no críticas

| Tipo | Comportamiento esperado |
|---|---|
| Crítica | Detener el proceso y solicitar corrección |
| No crítica | Continuar, pero declarar la limitación |
| Informativa | Registrar una advertencia sin bloquear |

---

## Antipatrones

Evita los siguientes errores:

- validar solo al final;
- asumir datos faltantes;
- ignorar inconsistencias;
- corregir información sin evidencia;
- ocultar errores encontrados;
- aplicar controles ambiguos como “verifica que esté bien”;
- continuar a pesar de una falla crítica;
- declarar confianza alta sin evidencia suficiente.

---

## Plantilla reutilizable

```text
## Validaciones

Antes de responder, verifica:

- que la información obligatoria esté disponible;
- que los datos sean legibles y consistentes;
- que no existan contradicciones sin resolver;
- que las restricciones estén siendo respetadas;
- que el formato solicitado sea viable.

Antes de entregar, verifica:

- que la respuesta cubra el objetivo;
- que no se haya inventado información;
- que el formato de salida sea correcto;
- que las conclusiones estén sustentadas;
- que las limitaciones estén declaradas.

Si una validación crítica falla,
detén el proceso y solicita la información necesaria.
```

---

## Checklist de calidad

Antes de dar por terminado un Prompt Maestro, confirma que:

- [ ] se validan todas las entradas obligatorias;
- [ ] existen controles de consistencia;
- [ ] se comprueba la legibilidad de archivos y datos;
- [ ] se verifican las restricciones;
- [ ] se controla el formato de salida;
- [ ] se evita inventar información;
- [ ] se solicita aclaración cuando corresponde;
- [ ] se declara la incertidumbre;
- [ ] se revisa la calidad antes de entregar la respuesta;
- [ ] se distingue entre errores críticos y advertencias.

---

## Laboratorio práctico

Mejora el siguiente prompt incorporando validaciones:

```text
Analiza este contrato y dime los riesgos.
```

Incluye al menos:

- validación de existencia del archivo;
- validación de idioma;
- validación de páginas ilegibles;
- validación de cobertura;
- validación del formato del informe;
- validación del nivel de confianza;
- tratamiento de contradicciones;
- regla para información faltante.

### Resultado esperado

El Prompt Maestro debe impedir que el GPT emita conclusiones firmes cuando:

- el documento esté incompleto;
- existan secciones ilegibles;
- falten anexos relevantes;
- la evidencia sea insuficiente;
- la solicitud exceda el alcance definido.

---

## Resumen ejecutivo

Las validaciones convierten un GPT en un sistema más confiable, controlado y predecible. En la metodología ILC representan una barrera de calidad que opera antes, durante y después de la generación de una respuesta.

Un Prompt Maestro no solo define **qué debe hacer** el GPT. También establece **cómo comprobar que lo hizo correctamente**, cuándo debe detenerse y cómo debe comunicar una limitación.