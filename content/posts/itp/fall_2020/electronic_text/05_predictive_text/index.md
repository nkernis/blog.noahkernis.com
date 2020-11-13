+++
slug = "05_predictive_text"
title = "Predictive Text"
date = "2020-11-09T20:20:54-05:00"
author = "Noah Kernis"
tags = ["itp",  "electronic_text"]
description = "Bideological administrats"
showFullContent = false
+++

## Thinking

The assignment for this project:

> Use predictive models to generate text: either a Markov chain or a neural network, or both. How does your choice of source text affect the output? Try combining predictive text with other methods we’ve used for analyzing and generating text: use neural network-generated text to fill Tracery templates, or train a Markov model on the output of parsing parts of speech from a text, or some other combination. What works and what doesn’t? How does neural network-generated text “feel” different from Markov-generated text? How does the length of the n-gram and the unit of the n-gram affect the quality of the output?

## The plan

This past weekend was the 2020 presidential election. 

After the election was called for Biden on Saturday, a New York Times [interview](https://www.nytimes.com/2020/11/07/us/politics/aoc-biden-progressives.html) with Alexandria Ocasio-Cortez came out quickly. Then, on Sunday, a New York Times [interview](https://www.nytimes.com/2020/11/08/us/politics/conor-lamb-democrats-biden.html) with Conor Lamb came out.

Each presents a different perspective and diagnosis of the election. A major topic that comes up in both is the loss of seats in the House for Democrats. They both make claims on reality - how things "really" are. That it's just "common sense". Subjective assertions that suddenly become concrete. Narratives seem to just emerge although someone has to drive the interviews.

Especially with news about politics, reading these articles can cause feeling a mix of dissonance and anxiety (Or is that just me then?).

I want to try and play with their language. The people interviewed and the person interviewing them. See if can recreate an interview article that generates similar feelings. 

## The code

*Note: the post continues inside the embed below*

{{< gist nkernis 127110f411648e9a6eeee92bce6422cc >}}

[predictive_text.ipynb](https://gist.github.com/nkernis/127110f411648e9a6eeee92bce6422cc)

I also tried using aitextgen. I think training on the limited text I had didn't work well. The text generated was way to close to the original. I also didn't try a ton of messing with parameters because the markov chains were working well for me.

[colab notebook](https://colab.research.google.com/drive/1rZFSYyScnAV1YUcthM47F046IbUxkxoc?usp=sharing) (requires being logged into nyu google account)

## An article

### Short article

{{< figure src="img/00_short_article.png" alt="" caption="[ I thing policies you. ]" >}}

### Long article

{{< figure src="img/01_long_article.png" alt="" caption="[ Bideological administrats ]" >}}

