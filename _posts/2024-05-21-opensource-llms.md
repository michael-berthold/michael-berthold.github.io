---
title: Open Sourcing LLMs - is it really all about Ethics?
author: Michael Berthold
---

Should GenAI be open source? That debate typically focuses on the risks of giving
everybody with sufficient compute resources the ability to run LLMs. The pro-arguments
center on the reproduction of published results (and proper benchmarking/comparing of
different models) as well as the typical open source \"everybody can check the code and
find issues\" claims. The con-arguments cite the risk of putting this type of powerful
and potentially dangerous technology into evil peoples hands and claim that we need ways
to control who has access and be able to protect the technology so it ca not be used for
bad (unethical, illegal, ...) purposes.

<!-- more -->

This is a legit debate and if (and that is a big if!) all those big players were really
bought into the responsible-use cause of the debate, I would side with them. If (and this
is the other big if), we could guarantee nobody could actually get access to their code
and their models. History shows that they will eventually all sneak out though.

In order to open another line of argument why the big players shy away from open sourcing
their models, we need to dive a bit deeper into what that would actually mean.

The code to train large AI models is mostly open source anyway. The larger players in the
field probably all made small modifications and additions to that code that they would need
to open source as well to make their approaches completely reproducible.

This code is then used, together with massive amounts of data to actually train a model. In
order to reproduce, we would also need to know exactly which data was used. Most of it is
\"out there\" but knowing which pieces were used for training is important. Potentially some
other data (confidential/artificially generated) was used as well to bias the model one way
or the other. We would need to get access to that as well.

The resulting model is then a pretty gigantic set of numbers (the typically cited billions
parameters a model consists of). Sharing this set of parameters allows others to use the
model without having to go through the extremely compute-intensive process of training it.
The raw code to apply the model to new input is also primarily open source and just like
during training, everybody probably made a few small modifications/additions that would
need to be shared as well in order to reproduce the published results or use the model
yourself.

And now we are getting to the interesting part: over the course of the last months/years,
the big players have gotten tons of user feedback on where their models made mistakes,
produced nonsense, or outright wrong, unethical, or illegal output. Some of those problems
were fixed with adjusting the model itself or the way it was trained. But quite a bit of it
was fixed by adding safeguards around the model itself. And this safeguarding infrastructure
is the truly interesting part - open sourcing this would allow everybody to see what kind
of mechanisms were put in place to avoid certain outputs to be produced. And only with that
knowledge can we truly reproduce their claims.

So in a nutshell we have five pieces:
- already open source code to train the model (plus minor modifications/additions)
- the actual data used for training
- the billions of numbers describing the model
- already open source code to use the model (plus minor modifications/additions)
- confidential infrastructure and code to safeguard the model and filter incoming
  data / outgoing responses 

The success of a commercial company focusing on GenAI depends on the quality of the
responses of their model. A large part of that relies on the first four pieces. Others
have access to those pieces as well and - given enough compute power - can easily
train and offer similar models. However, the last part, the safeguarding infrastructure,
s a massive competitive advantage - many mistakes during the early days are now not
accepted anymore. If you come to the game late, you will always have to play catchup
because your competitor already used massive community feedback to improve their
safeguarding, investing lots of engineering effort. In that light, isn't it interesting
to observe how many of the late entrants are struggling with model quality? Their models
ikely aren't worse - their safeguarding setup is!

So would making the safeguarding code open source be useful? Absolutely, it would make
it transparent what kind of safeguarding rules are applied. Would it hurt their commercial
advantage? You bet.
