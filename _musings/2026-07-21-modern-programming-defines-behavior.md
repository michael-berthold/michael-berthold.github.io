---
title: Modern Programming Will Specify Behavior, Not Code.
date: 2026-07-21
excerpt: "Describing behavior will replace writing code when it comes to using AI to develop future applications..."
author_line: "By Michael R. Berthold"
lang: en
seo_title: "Modern Programming Will Specify Behavior, Not Code."
seo_description: "A musing on how describing behavior will replace writing code."
---

I recently tried vibe coding two applications myself. As so often happens when you work with AI, it was a mix of wow and ow moments.
The first experience was impressive: the AI built the app, added user authentication upon request, added embedded AI features, and
even suggested an improvement for the guest mode I wanted at the end. Just awesome. But even then, I had this nagging feeling: what
did the AI really do? I had no idea - I just saw the result.

With the second experiment we did not get past the login screen. The AI never managed to figure out the authentication process of
the underlying system the app needed to access. It kept suggesting improvements and workarounds that supposedly fixed the errors
but eventually we ended up in a loop. It never worked.

What do both of these experiences have in common? In both cases I had no chance of discussing what the AI thought I wanted – we kept
talking about the outcome and in one case that worked out nicely. But in the other case, we simply could not align.

The problem was not that the AI could not code. The problem was that we never established a shared understanding of the intended behavior.

<!-- more -->

There is the obvious solution for this: show me the code and we will figure it out together. But that is not the promise of vibe coding.
We do not want to end up turning everybody into a code writer – also because, ideally, the AI picks different coding languages underneath
the hood for different types of problems – no human will ever be proficient in all of them. We do want to keep talking about *what* we want
to build and let the AI worry about the *how*, the code.

The question we face is a different one: how can we talk to an AI in a more systematic way than just an informal conversation so that both
sides develop, over time, a shared understanding of the desired behavior?

Software engineering had that problem for decades – users tended to have all sorts of ideas in mind about what they wanted but expressed it
poorly. And at the end, the delivered program did not really do what they truly wanted. Which is why we invented requirement documents and
software specifications.

### Beyond Spec Driven Development.

Someone recently claimed that AI will allow us to turn specifications into code and I totally agree with that. I just think that those
specifications will look different to what we are used to. They will be more of a mix of a requirement document and a specification
– probably even in a type of language that will be ideally suited for a human to understand all facets of the program they are asking
the AI to build. And we will, obviously, not be expected to write those things – let’s call them “behavior specifications” – from scratch,
but we will create and improve them together.

The big difference compared to today is that in my second experiment, we could have stopped talking about the "I still get an error when
trying to login" but I could have asked: "hey, what do you think I want you to do for the login part of this app". We could have expanded
this document describing the desired behavior together, instead of me complaining about the outcome and the AI fiddling with the code.
While doing that, I would have understood what the AI was trying to do and could have helped correct some of the mistakes in the underlying
assumptions. Or maybe it would have even figured it out itself, being forced to systematically describe what it was trying to do.

There is another interesting side effect, of course. We need our AI to translate this behavior specification into code – and reliably so.
Ideally, when we feed in the same document, we get the same code. Or, maybe a tad bolder: we get code that is guaranteed to fulfill the
specification, that is, code that exhibits the intended *behavior*.

### AI will do the coding for us -- if we tell it *what* we want.

In the end, AI will act as a compiler, translating well-specified behavior into an executable program. This has lots of interesting side
effects: we may be able to ask the AI to translate the same document for different underlying languages, operating systems, or hardware.
We can also validate proper translation through separate AIs by adding “unit tests” derived from other behavior specifications with
corresponding implementations.

But it goes both ways: this type of document can also be used by the AI to identify open questions and potential conflicts so it
can proactively ask the human for additional information. As more such documents become part of the AI training material, they will
be able to identify common patterns and flag ambiguities or unusual assumptions in a given behavior specification.

### Computer Science continues to do what it does best: Keep abstracting.

Programming will evolve to another level of abstraction once we figure out what a suitable AI- and human-compatible behavior
specification language looks like *and* come up with reliable ways to make an AI translate this into actual computer code.
We have abstracted away the need to write the “how” and worry about technical details and replaced it with the ability of
simply describing the “what”.

For that we need a language that retains maximum human expressiveness while remaining minimally ambiguous – that tension is one
of the reasons why informal prompting for program generation breaks down for more complex but also for enterprise-grade problems.
Note that we may still have - previously written by our specilists in the IT department - a more technical specification document
underneath the hood, outlining architectual and more technical requirements. But the user more concerned about the actual
behavior will not need to worry about that.

What will this look like in the future? People will learn to communicate about a program’s functionality in a suitably intuitive
yet formal language. They may still communicate with the AI in a colloquial tone, but they can go to that behavior specification
as a “reliability layer” at any time to double-check that the AI really understood what they wanted.

In the end, this feels quite similar to formal specification languages and other formal software engineering methods from the past.
But AI will finally make these methods practical because humans no longer need to author them alone. The future of programming
will no longer be editing source code, but creating structured descriptions of desired behavior that AI can translate into working
software.


