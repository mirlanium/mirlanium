---
title: "The manifold hypothesis and what generative models actually learn"
date: 2026-04-12
excerpt: "On the geometry of learned representations and why video generation is harder than it looks."
---

There's an elegant tension at the heart of generative modeling: we assume data lives on a low-dimensional manifold embedded in high-dimensional space, then build architectures that must discover this manifold without ever being told its shape.

In video generation, this becomes particularly acute. A single frame already occupies a complex manifold — but a sequence of frames must trace a path along a temporal sub-manifold that respects physics, occlusion, lighting, and the causal structure of the world.

The question I keep returning to: is temporal consistency an emergent property of learning the right manifold, or must it be imposed externally through architectural priors? My work with Orbis and LSA suggests it's somewhere in between — the manifold provides the skeleton, but you need explicit signals to prevent the model from taking shortcuts through regions of the space that look plausible frame-by-frame but collapse over time.

This connects to active inference in an interesting way. If a world model is performing something like free energy minimization, then temporal consistency isn't a constraint — it's a consequence of accurate prediction. The jitter we see in naive video generation isn't a rendering artifact; it's a failure of the model's internal physics.
