---
layout: page
title: "ProvGen: Provenance-Aware Semantics for Synthesized Programs"
description: A provenance-aware operational semantics for LLM code synthesis. Under review.
importance: 1
---

A provenance-aware operational semantics that treats LLM code synthesis as a first-class effect. Every synthesis step produces a value paired with a structured provenance capsule, capturing model identity, prompt hash, tool invocations, retrievals, and environment assumptions. A satisfaction relation and a proved Reproduction Soundness theorem link capsule requirements to consistent re-evaluation.

A prototype wraps real LLM calls, emits capsules alongside generated files, and supplies a CI-ready checker that flags environment drift with precise witnesses. Experiments over 60 synthesis events show sub-millisecond capture overhead and 100% accurate detection of non-reproducible replays.

**Status:** Under review

**Stack:** program semantics, LLM provenance, reproducibility, effect systems, Python
