---
layout: post
title:  "AI Safety and Reliability: A Compliance Requirement, Not a Research Luxury"
date:   2026-07-14 10:00:00 +0000
categories: ai safety
---

## Executive Summary

Most enterprises now run generative AI in production. Far fewer can answer a
regulator's simplest follow-up question: how do you know what it does, and how do
you prove it did not do something it should not have. For finance, healthcare, and
legal organisations, that gap is not a research curiosity. It is an audit finding
waiting to happen. This post outlines how we treat AI safety and reliability as a
measurable, gateable engineering discipline rather than a promise, and why that
matters most in regulated environments.

## The emerging risk

Traditional software fails in ways you can reproduce. A large language model, and
especially an AI agent that can call tools, fails in ways that are probabilistic,
context-dependent, and easy to miss in a demo. Three failure modes matter for
regulated clients:

- **Data leakage through the model.** An agent that reads an untrusted document
  (an email, a web page, a customer upload) and later takes a sensitive action
  (sends, deletes, pays) can be steered by instructions hidden in that content.
  This is the prompt-injection to data-exfiltration path, and it maps directly
  onto GDPR, HIPAA, and confidentiality obligations.
- **Silent unreliability.** Agents loop, retry, swallow errors, and truncate
  context without failing loudly. The output still looks plausible. In a clinical
  or financial workflow, plausible-but-wrong is the expensive case.
- **Unmeasured behaviour change.** Teams adjust prompts, guardrails, or model
  versions and assume the behaviour improved. Without measurement, they are
  trading one unknown for another.

## Why traditional QA is not enough

A pass or fail test suite assumes deterministic behaviour. AI systems are not
deterministic, so a single green run tells you very little. Worse, many teams
evaluate AI with another AI as the judge. That is fine for exploration during
development. It is unusable as a merge-blocking control: the same input can score
differently across runs, model versions, and provider outages, and every check
costs a model call. A compliance gate cannot be probabilistic.

## A measurement-first approach

Our position is simple. You cannot govern what you do not measure, and you cannot
gate on a control that is not reproducible. In practice that means:

- **Measure interventions before trusting them.** When you steer or guardrail a
  model, quantify the effect on the target behaviour, the side effects on
  unrelated capabilities, and the point at which the intervention degrades output.
  A change that "looks better" is not evidence.
- **Deterministic safety checks in the pipeline.** Reliability and data-flow
  checks should be a pure function of what the system did, with no model call in
  the path, so the same trace yields the same verdict every time. That is what
  makes a check safe to fail a build or block a release on.
- **Information-flow awareness.** Flag any run where untrusted input reaches a
  sensitive action without passing a review or sanitisation step. This is a
  security control expressed as data flow, and it is exactly the pattern that
  turns a clever demo into a breach.
- **Honest evaluation.** Report uncertainty, controls, and limitations. A null or
  negative result, clearly stated, is more valuable to a risk committee than an
  optimistic headline.

## What this looks like in a regulated environment

For a bank, a health provider, or a law firm, the deliverable is not a smarter
model. It is evidence. A safety and reliability layer that produces reproducible,
auditable verdicts gives you three things regulators and boards actually ask for:
a record of what the system did, a check that runs in CI and blocks known-bad
behaviour before it ships, and a measured basis for saying an AI change is an
improvement rather than a hope.

This is engineering discipline applied to a probabilistic system. It is the same
mindset we bring to continuous delivery in regulated environments, applied to the
newest and least understood part of the stack.

## Where the depth lives

The techniques behind this, interpretability of model internals, evaluation of
steering interventions, and deterministic detection of agent failure modes, are
areas we actively research in the open. If you want the technical detail, the
experiments, the tooling, and the honest write-ups including the negative results,
they live in our research notes on
[Substack](https://bamdad.substack.com) and in our open-source work on
[GitHub](https://github.com/bamdadd).

If your organisation is putting AI into a regulated workflow and needs a safety and
reliability story that survives an audit, [get in touch](/contact/).
