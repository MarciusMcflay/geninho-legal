---
layout: page
title: Fórmula del Punto de Atención
permalink: /es/dashboard/punto-de-atencion/
lang: es
---

# Fórmula del Punto de Atención — riskScore

**Última actualización:** 14 de mayo de 2026

## ¿Qué es el Punto de Atención?

El **Punto de Atención** es una métrica del panel que identifica qué temas escolares merecen un seguimiento más cercano. Combina tres factores para generar una puntuación entre 0 y 1, donde **valores más altos indican mayor necesidad de intervención pedagógica**.

## La Fórmula

```
riskScore = (difficultyScore × 0.5) + (quizErrorRate × 0.4) + (trailErrorRate × 0.1)
```

### Componentes

| Factor | Peso | Descripción |
|--------|------|------------|
| **difficultyScore** | 50% | Dificultad reportada por el niño (escala 1–5, normalizada de 0.0 a 1.0) |
| **quizErrorRate** | 40% | Tasa de error en las preguntas del quiz (porcentaje de respuestas incorrectas) |
| **trailErrorRate** | 10% | Tasa de error en el juego educativo (trail) |

## ¿Por qué esta proporción?

La dificultad pesa **más (50%)** que la tasa de error porque:

1. **La suerte puede ocultar deficiencias** — Un niño puede obtener 100% en un quiz muy difícil en una sola sesión solo por suerte o ayuda momentánea, pero eso no necesariamente significa que domina el tema.

2. **Una sesión no valida el aprendizaje** — Cuando un tema es muy difícil, necesitas múltiples intentos para validar que el conocimiento es real y duradero.

3. **La tasa de error solo importa si es confiable** — Si el niño está cometiendo 11% de errores pero solo después de 2 sesiones, eso muestra progreso gradual. Dificultad alta con 0% de errores en una sesión es más preocupante.

### Analogía

Imagina dos escenarios al final de la semana:

- **Niño A:** obtiene 100% en una prueba **muy difícil** en un solo día (dificultad 5/5, cero errores)
- **Niño B:** obtiene 89% en una prueba **más fácil** después de practicar **dos veces** (dificultad 4/5, 11% de error)

¿Cuál es más preocupante? El Niño A, porque puede haber tenido suerte, y no hay evidencia de que el aprendizaje se haya solidificado.

## Ejemplo Práctico

Comparando dos temas en el panel:

### Obras Literarias

| Métrica | Valor | Cálculo |
|---------|-------|---------|
| Dificultad reportada | 5.0/5 | 1.0 |
| Tasa de error (quiz) | 0% | 0.0 |
| Tasa de error (trail) | 0% | 0.0 |
| **riskScore** | — | (1.0 × 0.5) + (0.0 × 0.4) + (0.0 × 0.1) = **0.50** |

### Sistema Digestivo

| Métrica | Valor | Cálculo |
|---------|-------|---------|
| Dificultad reportada | 4.0/5 | 0.8 |
| Tasa de error (quiz) | 11% | 0.11 |
| Tasa de error (trail) | 0% | 0.0 |
| **riskScore** | — | (0.8 × 0.5) + (0.11 × 0.4) + (0.0 × 0.1) = **0.444** |

**Resultado:** Obras Literarias (0.50) aparece con mayor riesgo que Sistema Digestivo (0.444), incluso con una tasa de error menor, porque la dificultad muy alta con desempeño perfecto en pocos encuentros es una señal de alerta más fuerte.

## Cómo interpretar riskScore en la app

- **0.0–0.25:** Tema bajo control — el niño está seguro y progresando
- **0.25–0.50:** Atención moderada — puede necesitar más práctica o aclaración
- **0.50–0.75:** Alerta — recomendamos refuerzo inmediato
- **0.75–1.0:** Intervención urgente — crear una sesión de estudio o refuerzo con el niño

## Qué recomienda hacer la app

Cuando un tema entra en estado de Punto de Atención, Geninho sugiere:

1. **Aumentar la frecuencia de sesiones** — más exposición al contenido
2. **Usar el chat de IA** — hacer preguntas sobre el tema (Premium)
3. **Revisar el plan de estudios** — puede necesitar un enfoque diferente
4. **Monitorear en las próximas sesiones** — la puntuación debe disminuir con la práctica consistente

## Notas Importantes

- El **riskScore es dinámico** — se actualiza con cada sesión, quiz o juego completado
- La métrica **no es punitiva** — una puntuación alta significa que el niño necesita apoyo, no que "fracasó"
- **El contexto importa** — un tema nuevo siempre tendrá mayor riesgo inicialmente; es normal
- **Discusión en familia** — usa el Punto de Atención como base para hablar con el niño sobre dificultades y estrategias
