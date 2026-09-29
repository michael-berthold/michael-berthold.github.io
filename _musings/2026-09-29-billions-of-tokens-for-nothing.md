---
title: Billions of Tokens for Nothing - The Cost of Context
date: 2026-09-29
excerpt: "Agentic setups expand the types of problems AI can help with. But it often also results in an exploding token usage..."
author_line: "By Michael R. Berthold"
lang: en
seo_title: "Billions of Tokens for Nothing."
seo_description: "A musing on how more powerful agents results in token usage explosion - and what we can do about it."
---

Agentic setups allow AI to solve complex problems by designing and following a plan and using a variety of tools or even other agents. This massively expands the types of problems AI can help with. But it often also results in an exploding token usage - for context the AI usually doesn't need.

<!-- more -->

## How little context does AI actually need?

With AI agents becoming widespread, this problem is growing. Agents don't just take in context once per prompt — they load it, analyze it, and hand it along across many steps. Research on token consumption in coding tasks shows how big the effect is. A Microsoft Research study found that agentic tasks can consume up to 1,000 times more tokens than classic code reasoning — driven mostly by input tokens, not output tokens. And more tokens do not automatically lead to better results. A second study on agentic software engineering tasks reaches a similar conclusion and describes a "communication tax": agents keep passing existing information along without a significant impact on the quality of the outcome.

## A large context window is not a free pass

A large context window makes it tempting to simply put everything in — the entire repository, the full document collection, the complete conversation history. That may be fine for a single call. In a production agent system, however, it quickly turns into a massive cost block. Take a repository of 500,000 tokens that ends up in the context over 10,000 interactions: that's billions of processed tokens — even if nothing in the repository has changed.

And it's not only about money. The well-known "Lost in the Middle" study by Liu et al. showed that language models don't make equally good use of relevant information across long contexts; when the key information sits in the middle of a long input, quality drops noticeably. Anthropic, too, now describes context as a limited resource and recommends providing as few — but as information-rich — tokens as possible. More context does not automatically mean more intelligence. Often it simply means more ballast.

## Condensation, not just retrieval

What companies need, then, is not more context but better-prepared context. Retrieval-Augmented Generation (RAG) is a first filter: rather than putting every document into the context, it searches for content that matches a given request. But RAG only filters raw material. If it returns ten documents of 20,000 tokens each, 200,000 tokens still land in the context — and, with variations, again on every similar call.

The next step is therefore condensation, or abstraction: a compact essence is generated once from large amounts of raw material, and only this essence goes into the context from then on. Based on it, the AI decides which details it really needs — which components exist, how they relate to one another, which parts are relevant — and only then loads specific files or documents.

## Context engineering: context becomes infrastructure

Anthropic defines context engineering as the systematic curation and maintenance of the information a model receives during inference. It's not just the prompt that matters, but the entire state an agent sees. The guiding rule: the best context is not the largest possible one, but the smallest one that still carries just enough information for the next decision.

A semantic layer answers the question "What is this?" It describes terms, types, and their meaning — for example, that different labels refer to the same business concept. A knowledge graph answers the question "What is it connected to?" It maps the relationships between entities: a service uses an API, one component depends on another. Both produce a structure that is more compact — and more useful to the AI — than the raw original data or documents.

For source code, this role is played by a context compiler. A coding agent doesn't need to read the whole repository at every step; what it needs first is a map — architecture, modules, dependencies, APIs, data flows. The compiler creates this essence once, and the AI navigates along it afterwards instead of copying raw data over and over again. As long as the repository doesn't change, the essence stays stable, and the expensive analysis doesn't have to be repeated.

The same principle applies to skills, the essence layer for tools and procedural knowledge. An agent doesn't need to know every tool detail all the time. A skill first conveys when a capability is relevant; the details of exactly how to use the tool follow only when they're needed.
## Context becomes hierarchical

Ultimately, this leads to a hierarchical structure: at the top, a very compact summary; below it, more detailed summaries of individual areas; and only at the very bottom, the complete raw data. The AI works its way down step by step instead of diving straight into raw data with every request. Increasingly, this hierarchy can be generated by AI itself: expensive processing once, cheap use a thousand times over.

## The new optimization question

For a long time, the AI industry optimized for ever-larger context windows — and that was important progress. But for companies, window size must not become a goal in itself. A context window isn't free storage; it's a resource that has to be processed again and again. Anyone who feeds an agent huge amounts of raw material may end up paying for billions of tokens of information it never — or only rarely — needs.

The key question is therefore no longer "How many tokens fit into the context?" but rather "How little context does the AI need to decide for itself which information it needs next?" Put differently: provide as much raw material as possible, but present pre-processed background information that makes it possible to navigate that raw material — ideally generated once and reused many times.

