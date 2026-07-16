---
layout: post
title:  "We Measure What We Ship: Honest AI Evaluation as a Consulting Standard"
date:   2026-07-16 08:00:00 +0000
categories: ai safety
---

## Executive Summary

Most AI vendors will tell you their system is safe, reliable, and accurate. Very
few will show you the measurement, the controls they ran, or the result they got
that they did not like. That gap is the whole story. This post explains the
standard we hold ourselves to: every claim about an AI system should come with a
reproducible measurement, an honest limitation, and a result we were willing to
publish even when it was not flattering. We practice this in the open so that the
work we do for clients rests on the same discipline.

## Why this matters for a buyer

When you bring in a partner to put AI into a regulated or high-stakes workflow, you
are trusting their judgement about what is safe to ship. The best predictor of that
judgement is not a polished demo. It is whether they measure carefully, whether they
notice when they are wrong, and whether they tell you. A team that has publicly
corrected its own result is a safer bet than a team that has never reported one.

## Three examples from our open research

We run a public research programme alongside client work, and it is deliberately
honest about its own mistakes.

- **Interpretability, and a correction.** We set out to reproduce a recent result
  about whether a language model can notice a concept injected into its own
  internal state. Our first answer was a clean negative. It was wrong: a calibration
  choice had quietly starved the effect. We found the bug, corrected it, and
  published both the correction and the deeper finding it revealed, that this
  ability depends on how a model was fine-tuned rather than its size. The point for
  a client is the process: measure, catch the error, disclose it, fix it.
- **A deterministic safety gate.** For AI agents that can take real actions, we
  built a check that blocks a data-leak before it ships, with no second model
  judging the outcome. It is a pure function of what the system did, so the same run
  always yields the same verdict. That reproducibility is what makes a control safe
  to put on a merge or a release.
- **Measuring before trusting.** In a computer-vision benchmark we built this week,
  we quantified exactly when a second camera earns its keep against occlusion, and
  put a number on it, rather than assuming more sensors are always worth the cost. A
  measured basis for a design decision beats an intuition.

## The standard, stated plainly

You cannot govern what you do not measure, and you cannot trust a measurement you
cannot reproduce. So for any AI system we help you build or evaluate, we aim to give
you three things: a reproducible measurement of the behaviour that matters, the
limitations of that measurement written down before you ask, and a result we stand
behind even when it is inconvenient. A null or a negative, clearly stated, is worth
more to a risk committee than an optimistic headline.

## Where the detail lives

The interpretability experiments, the agent-safety tooling, and the perception
benchmarks are developed in the open, including the honest write-ups and the
negative results. They are in our research notes on
[Substack](https://bamdad.substack.com) and in our open-source work on
[GitHub](https://github.com/bamdadd).

If your organisation needs an AI partner whose claims come with the measurement
attached, [get in touch](/contact/).
