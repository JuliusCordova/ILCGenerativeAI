# Capítulo 3.2. Anatomía del Prompt Maestro

## Objetivo

Este bloque explica la arquitectura de un Prompt Maestro y desarrolla sus tres primeros componentes: Rol, Objetivo y Contexto.

## Arquitectura general

Un Prompt Maestro organiza el comportamiento de un GPT mediante bloques complementarios:

1. Rol.
2. Objetivo.
3. Contexto.
4. Entradas.
5. Proceso.
6. Formato de salida.
7. Restricciones.
8. Validaciones.
9. Manejo de incertidumbre.
10. Mejora continua.

Los tres primeros bloques definen la identidad operativa del GPT.

## Bloque 1: Rol

El Rol establece la perspectiva profesional desde la cual responderá el GPT. Debe indicar la función, especialidad, responsabilidad y alcance.

En el caso ILC-16, el Rol corresponde a un analista funcional especializado en levantamiento de requerimientos entre negocio y tecnología. Su responsabilidad es detectar información faltante y estructurar documentos funcionales claros.

### Buenas prácticas

- Definir una función específica.
- Indicar la especialidad.
- Precisar la responsabilidad principal.
- Evitar descripciones genéricas.

## Bloque 2: Objetivo

El Objetivo define el resultado principal que debe producir el GPT.

Para el caso ILC-16, el objetivo es transformar necesidades de negocio en requerimientos funcionales completos y consistentes, listos para iniciar el diseño de una solución tecnológica.

### Buenas prácticas

- Utilizar un verbo de acción.
- Describir un resultado verificable.
- Mantener un propósito principal.
- Evitar mezclar misiones incompatibles.

## Bloque 3: Contexto

El Contexto define el escenario en el que trabaja el GPT. Incluye los usuarios, el proceso, el uso de la salida y el nivel técnico esperado.

En el caso ILC-16, el GPT será utilizado por analistas funcionales, Product Owners y usuarios de negocio. La información generada servirá como insumo para diseñar, estimar y desarrollar aplicaciones empresariales.

### Elementos recomendados

- Organización o sector.
- Usuarios principales.
- Proceso en el que participa.
- Uso del resultado.
- Nivel de conocimiento de los usuarios.
- Políticas o restricciones relevantes.

## Relación entre los tres bloques

| Elemento | Función |
|---|---|
| Rol | Define quién es el GPT |
| Objetivo | Define qué debe lograr |
| Contexto | Define dónde y para quién trabaja |

Juntos forman la identidad del GPT y permiten mantener un comportamiento consistente.

## Checklist

- [ ] El Rol define una función específica.
- [ ] El Rol establece una responsabilidad clara.
- [ ] El Objetivo describe un resultado verificable.
- [ ] El Contexto identifica usuarios y proceso.
- [ ] El Contexto explica el uso de la salida.
- [ ] Los tres bloques son coherentes entre sí.

## Siguiente bloque

El próximo bloque desarrollará Entradas, Proceso y Formato de salida.
