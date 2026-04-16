\---

title: Can we ever trust AI?

author: Michael Berthold

\---



By now, AI models are used broadly: they write code, documents, and movies. They find errors, side effects, and other problems. They build prototypes, plan carefully and even delegate to their colleagues. It seems as if they generally can do pretty much everything humans can do - often faster, better informed, and often even more reliable.

However, when it comes to trusting their outputs, we sometimes still run into a wall. It is usually easy to check if that new AI-generated image displays what it is supposed to show or if the text that it created makes sense. However, when it comes to believing an AI that the insights it generated from massive data sets and all this other information it has access to are valid, it's a different story. Trusting a medical analysis of an AI without humans double checking or at least getting a solid explanation, is unacceptable.

But even if an AI does produce an explanation, it is foolish to trust that. AI is very good at inventing convincing explanations that have nothing to do with the truth. My current favorite example is an AI being asked to find out where a picture was taken. It pointed to the exact location quickly and when asked why, it presented a very plausible explanation based on the objects visible, the type of light and some other elements in the picture. It concluded convincingly that picture could only be taken there. Impressive, isn't it? But when inspecting the logs more carefully, it became clear all the AI had done was to extract the location info from the images metadata. When prompted about this a little more firmly, it finally admitted to having cheated. These types of examples make it hard to trust AIs explanations.

So, if we don't want to trust AI even with an explanation, what do we need to trust it?



<!-- more -->



How do we learn to trust?

But how do we build trust? There are two ways for that, and it probably helps to remind ourselves how we build trust among human colleagues. You typically don't just throw the most critical analysis at a new person you have just met this morning (and have zero recommendations from sources you trust) and simply trust them with your life (or maybe just the life of your company). You may afterwards check those results yourself (or ask someone who you trust to do so) until you are ready to trust the new person. Or you may ask that person to explain how they got to those results so you can sanity check their thinking and their process. If that all makes sense, you will take the risk of trusting those results. But there is another aspect of this: even years later, when you have learned over time that this colleague produces reliably correct reports you will expect them to give you a heads-up when their confidence in a report isn't where it usually is.

Human trust is based on past experiences (directly or indirectly via trusted references), and it is based on the belief that the other side will give you a heads-up about their information confidence level. Both of those ways of building and maintaining trust are hard to do for AI. Current models tend to invent explanations that they didn't even follow (see above), and they also have a tendency to be super confident but also super wrong at the same time.

If trust among humans relies on experience and transparency, how can we adapt these principles to AI systems?



\### How do we learn to trust AI?



How can we learn to trust AI to create critical insights, build enterprise-grade applications, or deal with sensitive information? We need ways to address those two aspects - validating and explaining results - when we work with an AI.

For the validation, we have two alternatives: we can rely on another AI, or we can rely on a human, as in the past. There are already nice setups where a second (or third, fourth...) AI is tasked with sanity checking outputs from the first model. They check for offensive texts, weird images, or other errors but they can also be tasked with questioning the output reliability. As long as we accept less than perfect confidence, this approach works fine. And mind you, you will not get that from your human colleague either. So, this kind of "sanity checking" your AIs output by another AI is likely better than a human double checking it - but, as usual with AI, it may fail in surprising ways. Depending on your tolerance for such surprises, you may or may not want to involve a human after all.

The bigger issue is the aspect of gaining trust through explanation of results. We will need to mimic the way of how we trust an answer by a human colleague: show me (and let me reproduce) how you reach that result. And we do not want an invented explanation; we really want to see the steps the AI took to reach that conclusion. This means we will need to enable AIs to explain how they reached their conclusions in a language that is appropriate for the respective audience. Just like auditors will use different terminology when talking to colleagues or when they communicate with non-experts, the AI will need to have access to different ways of explaining its reasoning. And we will, at times, want to be able to reproduce those results, using those explanations. The language needs to be "executable".

On a side note: the ongoing progress with AI models adds a nasty problem when we talk about "building trust over time": the "brain" that you trusted yesterday may have changed or completely been swapped out for another one earlier today - so you will need to figure out how to trust that new/revised AI all over again.

Which puts even more emphasis on the ability of an AI to truly explain how they got to the results, output, insights without allowing them to invent an explanation just to please us.



\### How can AIs truthfully explain their results?



AI needs to be able to explain what it is doing - and we need to be sure this explanation is really what happened underneath the hood. Image an AI playing music but only get to hear the recording. In order for you to ensure it really played the piano you need to be able to ask the AI which keys it pressed and be sure it can only create acoustic outputs through the actual sound of the piano. Similarly, if your AI produces a forecast based on data, you need to make sure it's doing this through working with the data and not just hallucinations.

So, when the AI explains which keys it pressed, you know it had to do that to produce the music you just heard – it had no other way to create audio. And if you don't trust it (yet), you simply ask: play it on this piano! In this - a bit farfetched example - we expect the AI to use, as tool, two robot hands and an actual piano. For many other tasks, we are solely relying on software tools, but the analogy holds. When it tells you which data it accessed and how it was processed, you can be sure it actually did that. And also here, you can ask: show me so I can reproduce this step-by-step. Some of those explanations may be code: show me the SQL code you used to join that data. Show me the ggplot2 code you used to create this plot. More complex processes required a more abstract explanation: show me the dataflow diagram or the visual workflow. And for many other things, we need a similarly suitable representation that's intuitive enough for a human to be able to understand and reproduce the actual process. That's where we need to invest a lot more effort: define proper mechanisms (languages, if you will) that allow AI and humans to truly collaborate on specific types of work.



\### Where is this going?



In some instances, AI is already trustworthy enough. A few mistakes are easily caught or really don’t cause that much of a problem. In other instance, AI is already way better than humans. We are either happy with that (think: finding loopholes in legal documents - AI isn't perfect but it's already much better at finding issues than us humans) or we will need to learn to accept that AI makes many fewer mistakes than us humans but sometimes really, really stupid ones (think autonomous driving - most of the autonomous cars on the streets today are already way safer than human drivers but they sometimes make outrageous mistakes).

And then there are areas where we will need to figure out how we can find a more systematic way to define what building trust actually looks like. The path forward requires not just better AI, but better ways for humans and AI to collaborate — through transparent processes, reproducible explanations, and shared languages. Only then can we fully harness AI’s potential in domains where trust is non-negotiable.



