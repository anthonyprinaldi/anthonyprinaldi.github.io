---
title: "When the Map Stops Fitting the Territory"
date: 2026-04-15
permalink: /posts/2026/04/world-model-change/
tags:
  - Reinforcement Learning
  - Artificial Intelligence
  - Cognition
---

## On a difficult problem in machine intelligence — and maybe in thought itself

Imagine you are playing a video game for the first time. Coins are scattered across every level, and collecting them is how you win. You internalize this. The rule becomes invisible — the way grammar becomes invisible once you are fluent in a language. You stop thinking "I should collect coins" and simply reach for them.

Then you load a different game. It looks similar. There are coins. But here, coins only boost your score. What wins the game is something else entirely. For a moment — maybe longer than you'd like to admit — you keep reaching for the coins.

This is not a story about confusion. It is a story about something much more interesting: the moment you realize that your mental model itself is the problem. Not a wrong action within a correct frame, but a frame that no longer fits the world it was built for.

### I. The frame problem, quietly unsolved

Philosophers and AI researchers have long grappled with something called the frame problem — originally a technical question about how a reasoning system knows what doesn't change when an action is taken. If you move a cup, the table remains. But how does a system know that? Every fact about the world would need to be re-verified after every action if you had no shortcut.

The deeper version of this problem is less about facts and more about inference patterns. Frames — what cognitive scientists sometimes call schemas or mental models — are not just repositories of facts. They are the lenses through which facts are gathered in the first place. When you play the first game, you are not merely remembering "coins matter." You are perceiving the world through a structure that makes coins salient, that causes your attention to track them, that shapes what counts as a good move before you have even consciously reasoned about it.

The hard question is not "when is a belief wrong?" It is: when is the entire way you are generating beliefs insufficient?

### II. Why surprise is not enough

The most obvious answer to this question, and the one most AI systems implicitly rely on, is prediction error. When reality surprises you, update your model. This is elegant, and for a certain class of problems it works beautifully.

But consider the structure of the coin problem more carefully. You may finish an entire episode — a whole level, a whole game — having made no prediction errors you could detect in the moment. You collected the coins. The coins were there to collect. Nothing failed. Only at the end, looking at the outcome, do you realize you could have played entirely differently — and better.

This is a crucial distinction. A model can be locally coherent and globally suboptimal. You can be playing the game correctly inside your model while your model misses the game entirely.

> The frame was wrong not because it generated false predictions, but because it was generating the wrong questions.

In reinforcement learning, this manifests as the gap between an agent optimizing well within its learned world model and an agent that recognizes its world model itself needs revision. Current systems are, by and large, good at the former and nearly blind to the latter.

### III. What would genuine frame revision require?

A few things seem necessary, none of them easy.

First, world models need to be modular. A system that can only replace its entire model when something is wrong will be slow, brittle, and prone to forgetting. What you want is something more like a belief architecture with separable components — a causal model where individual mechanisms can be revised surgically when the evidence warrants. You learn that coins don't determine victory; you do not unlearn everything else you know about the game. This is what researchers in causal representation learning are beginning to work toward, and it points toward something like the way the brain appears to store and update knowledge — not monolithically, but in overlapping, recombineable structures.

Second, an agent needs some form of metacognitive access to its own learning process. Right now, in most reinforcement learning research, it is the human researcher who decides that the current algorithm is not working and intervenes — retuning hyperparameters, redesigning reward functions, switching architectures. The agent itself has no representation of its own learning strategy as an object that could be revised. This is the layer that is most conspicuously absent. Systems like **Population-Based Training** or **AutoRL** begin to chip at this from the outside — running many variants and selecting the ones that work — but this is selection pressure, not self-awareness.

Third — and most philosophically interesting — a system would need some way to distinguish between "I am in a familiar situation and should apply my existing frame" and "I am in a situation that superficially resembles a familiar one but may require a different frame entirely." Human beings do this imperfectly but genuinely. We notice the texture of unfamiliarity even when we cannot articulate what is unfamiliar. We have, in some sense, a prior over our own priors.

### IV. The deeper puzzle

What makes this problem philosophically compelling — beyond its technical difficulty — is that it does not have a clean stopping point. If a system can revise its frames, what frame does it use to decide when frame revision is warranted? If you build a meta-model for evaluating your models, you have only pushed the problem up one level. The regress is real.

Human beings seem to escape this regress not through an infinite hierarchy of meta-models, but through something messier and more pragmatic: accumulated experience, social feedback, discomfort, curiosity, the occasional crisis of confidence that forces a step back. We don't have a clean algorithm for frame revision. We have something more like a felt sense that things aren't adding up, combined with the social and emotional capacity to sit with that feeling long enough to let a new frame emerge.

This suggests that the path to machines that can revise their own frames may run not just through better architectures, but through a more serious reckoning with what cognition is actually doing when it does this — and whether the tools of optimization and gradient descent are the right tools for the job at all.

The coin problem is simple. The question it points toward is not.

---