---
layout: page
title: Fórmula do Ponto de Atenção
permalink: /dashboard/ponto-de-atencao/
lang: pt-BR
---

# Fórmula do Ponto de Atenção — riskScore

**Última atualização:** 14 de maio de 2026

## O que é o Ponto de Atenção?

O **Ponto de Atenção** é uma métrica do dashboard que identifica quais tópicos escolares merecem acompanhamento mais próximo. Ele combina três fatores para gerar um escore entre 0 e 1, onde **valores mais altos indicam maior necessidade de intervenção pedagógica**.

## A Fórmula

```
riskScore = (difficultyScore × 0.5) + (quizErrorRate × 0.4) + (trailErrorRate × 0.1)
```

### Componentes

| Fator | Peso | Descrição |
|-------|------|-----------|
| **difficultyScore** | 50% | Dificuldade reportada pela criança (escala 1–5, normalizada de 0.0 a 1.0) |
| **quizErrorRate** | 40% | Taxa de erro nas questões do quiz (percentual de respostas erradas) |
| **trailErrorRate** | 10% | Taxa de erro no jogo educativo (trail) |

## Por que essa proporção?

A dificuldade pesa **mais (50%)** que a taxa de erro porque:

1. **Sorte pode mascarar defasagem** — Uma criança pode acertar 100% de um quiz super difícil em uma única sessão apenas por sorte ou ajuda momentânea, mas não necessariamente domina o tópico.

2. **Uma sessão não valida aprendizado** — Quando um tópico é muito difícil, você precisa de múltiplas tentativas para validar que o conhecimento é real.

3. **Taxa de erro só importa se confiável** — Se a criança está errando 11% mas após apenas 2 sessões, isso mostra progressão gradual. Dificuldade alta com 0% de erro em uma sessão é mais preocupante.

### Analogia

Imagine dois cenários no final da semana:

- **Criança A:** tira 100% em uma prova **muito difícil** em um único dia (dificuldade 5/5, zero erros)
- **Criança B:** tira 89% em uma prova **mais fácil** após treinar **2 vezes** (dificuldade 4/5, 11% de erro)

Qual é mais preocupante? A Criança A, porque pode ter tido sorte, e não há evidência de que o aprendizado se consolidou.

## Exemplo prático

Comparando dois tópicos no dashboard:

### Obras Literárias

| Métrica | Valor | Cálculo |
|---------|-------|---------|
| Dificuldade reportada | 5.0/5 | 1.0 |
| Taxa de erro (quiz) | 0% | 0.0 |
| Taxa de erro (trail) | 0% | 0.0 |
| **riskScore** | — | (1.0 × 0.5) + (0.0 × 0.4) + (0.0 × 0.1) = **0.50** |

### Sistema Digestivo

| Métrica | Valor | Cálculo |
|---------|-------|---------|
| Dificuldade reportada | 4.0/5 | 0.8 |
| Taxa de erro (quiz) | 11% | 0.11 |
| Taxa de erro (trail) | 0% | 0.0 |
| **riskScore** | — | (0.8 × 0.5) + (0.11 × 0.4) + (0.0 × 0.1) = **0.444** |

**Resultado:** Obras Literárias (0.50) aparece com maior risco do que Sistema Digestivo (0.444), mesmo com menor taxa de erro, porque a dificuldade muito alta com performance perfeita em poucos encontros é um sinal de alerta mais forte.

## Como interpretar o riskScore no app

- **0.0–0.25:** Tópico sob controle — criança está segura e progredindo
- **0.25–0.50:** Atenção moderada — pode precisar de mais prática ou esclarecimento
- **0.50–0.75:** Alerta — recomendamos reforço imediato
- **0.75–1.0:** Intervenção urgente — criar sessão de estudo ou reforço com a criança

## O que o app recomenda fazer

Quando um tópico entra em Ponto de Atenção, o Geninho sugere:

1. **Aumentar frequência de sessões** — mais exposição ao conteúdo
2. **Usar o chat da IA** — fazer perguntas sobre o tópico (Premium)
3. **Revisar o plano de estudos** — pode precisar de abordagem diferente
4. **Monitorar nas próximas sessões** — escore deve baixar com prática consistente

## Notas importantes

- O **riskScore é dinâmico** — atualiza a cada nova sessão, quiz ou jogo concluído
- A métrica **não é punitiva** — um risco alto significa que a criança precisa de suporte, não que "falhou"
- **Contexto importa** — um tópico novo sempre terá risco mais alto no início; é normal
- **Discussão em família** — use o Ponto de Atenção como base para conversar com a criança sobre dificuldades e estratégias
