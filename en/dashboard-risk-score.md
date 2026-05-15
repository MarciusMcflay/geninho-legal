---
layout: page
title: Attention Point Formula
permalink: /en/dashboard/attention-point/
lang: en
---

# Attention Point Formula — riskScore

**Last updated:** May 14, 2026

## What is the Attention Point?

The **Attention Point** is a dashboard metric that identifies which school topics deserve closer monitoring. It combines three factors to generate a score between 0 and 1, where **higher values indicate greater need for pedagogical intervention**.

## The Formula

```
riskScore = (difficultyScore × 0.5) + (quizErrorRate × 0.4) + (trailErrorRate × 0.1)
```

### Components

| Factor | Weight | Description |
|--------|--------|-------------|
| **difficultyScore** | 50% | Difficulty reported by the child (scale 1–5, normalized from 0.0 to 1.0) |
| **quizErrorRate** | 40% | Error rate in quiz questions (percentage of incorrect answers) |
| **trailErrorRate** | 10% | Error rate in the educational game (trail) |

## Why this proportion?

Difficulty weighs **more (50%)** than error rate because:

1. **Luck can hide gaps** — A child can score 100% on a very difficult quiz in a single session just by luck or momentary help, but that doesn't necessarily mean they've mastered the topic.

2. **One session doesn't validate learning** — When a topic is very difficult, you need multiple attempts to validate that the knowledge is real and lasting.

3. **Error rate only matters if reliable** — If the child is making 11% errors but only after 2 sessions, that shows gradual progress. High difficulty with 0% errors in one session is more concerning.

### Analogy

Imagine two scenarios at the end of the week:

- **Child A:** scores 100% on a **very difficult** test in a single day (difficulty 5/5, zero errors)
- **Child B:** scores 89% on an **easier** test after practicing **twice** (difficulty 4/5, 11% error rate)

Which is more concerning? Child A, because they may have been lucky, and there's no evidence the learning has solidified.

## Practical Example

Comparing two topics on the dashboard:

### Literary Works

| Metric | Value | Calculation |
|--------|-------|-------------|
| Reported difficulty | 5.0/5 | 1.0 |
| Error rate (quiz) | 0% | 0.0 |
| Error rate (trail) | 0% | 0.0 |
| **riskScore** | — | (1.0 × 0.5) + (0.0 × 0.4) + (0.0 × 0.1) = **0.50** |

### Digestive System

| Metric | Value | Calculation |
|--------|-------|-------------|
| Reported difficulty | 4.0/5 | 0.8 |
| Error rate (quiz) | 11% | 0.11 |
| Error rate (trail) | 0% | 0.0 |
| **riskScore** | — | (0.8 × 0.5) + (0.11 × 0.4) + (0.0 × 0.1) = **0.444** |

**Result:** Literary Works (0.50) appears with higher risk than Digestive System (0.444), even with a lower error rate, because very high difficulty with perfect performance in few encounters is a stronger warning signal.

## How to interpret riskScore in the app

- **0.0–0.25:** Topic under control — child is confident and progressing
- **0.25–0.50:** Moderate attention — may need more practice or clarification
- **0.50–0.75:** Alert — we recommend immediate reinforcement
- **0.75–1.0:** Urgent intervention — create a study or reinforcement session with the child

## What the app recommends doing

When a topic enters Attention Point status, Geninho suggests:

1. **Increase session frequency** — more exposure to the content
2. **Use the AI chat** — ask questions about the topic (Premium)
3. **Review the study plan** — may need a different approach
4. **Monitor in the next sessions** — score should decrease with consistent practice

## Important Notes

- The **riskScore is dynamic** — updates with each completed session, quiz, or game
- The metric **is not punitive** — a high risk means the child needs support, not that they "failed"
- **Context matters** — a new topic will always have higher risk initially; that's normal
- **Family discussion** — use the Attention Point as a basis for talking with the child about difficulties and strategies
