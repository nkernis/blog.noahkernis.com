+++
slug = "electronic_text"
title = "Making a Poem Generator"
date = "2020-08-29T17:32:59-04:00"
author = "Noah Kernis"
tags = ["itp", "electronic_text"]
description = "*a being of plastic*"
showFullContent = false
+++

For this assignment, we were asked to look at some early versions of poem generators and then to create our own, starting from one of the examples. 

After reviewing the generators and reading more about their histories and makers, I had some ideas. I was interested in exploring the creation and consumption of text as input/output. Unix streams are the closest analogy I can think of - and in reality is the practical experience I am thinking of.

In this situation, some process can accept text as an input and return text as an output. This allows for 'piping' information to one process from another. The process together create the final result. A poem that is generated, consumed, or 'read' by another generator, which then outputs a final poem for human consumption is interesting to me. 

This new 'hidden' poem is then written exclusively for another generator and not a human. How many times can the cycle run before the entire piece loses all sense? In the end, is this just an overly complex way to create a Dada like poem? What is the relationship between the final output and the hidden poem?

For my first experiment, I decided to start with the poem generator, *A House of Dust*. This one stuck out to me for a number of reasons. First, after reading more about the generator, I learned Alison Knowles and James Tenney where part of the Fluxus community, and that they were working with Nam Jun Paik. I have found myself returning to Paik time and time again in the past few years, so I was instantly drawn to this work becuase of it's proximity to him. Second, the simplicity of the code itself, and the way Knowles described it: `a house of (list material) (list location) (list light source) (list inhabitants)` ([source](https://blog.calarts.edu/2009/09/10/alison-knowles-james-tenney-and-the-house-of-dust-at-calarts/)). After reading the other examples of generators, I found this to be more common when describing abstractly the poem generators, but this was the first time I saw it and it definitely stood out. The simple form defines what can produced. Maybe a bit of stretch, but describing a poem in this way reminded me of a joke:

> A new inmate at a prison is eating their first lunch. Suddenly, someone screams "347" and everyone in the lunchroom starts laughing. The same things happens again and again, but each time a different number is said. Eventually the new inmate asks someone what's going on. The person replies, "oh, well you see, we have been here so long we have already told each other all the jokes we know, so instead of wasting time telling them, we have assigned them all numbers and refer to them that way." The new inmate thinks they get it and stands up and says "45!" No one laughs. The person turns to them and says, "you told it wrong."

For me, the collective pool of jokes is kind of like the collective pool of words any collection of humans may share. When the poem generator is described in terms of the words it can draw on, without referencing any specific word, it is in a way, a similar abstraction. A big difference is one is referring to a known body of jokes while the other refers to a process that can produce many, if not infinite, iterations of the final piece. But they both require thinking about something implied by the more abstract reference. 

I guess I was struck by the relationship of the description of the process, to implementation, to what is actually produced. And how that abstract description can render so much. My experience working as DevOps Engineer meant I spent a lot of time thinking about systems (I also am interested in them generally, but my work was practical and taught me different things). One of the major themes I took away was that complexity is created from many simple things, happening together (these often have a relationship and may interact in multiple ways). So, for this, I want to use the early, simple generators to create complexity by feeding text through the system one or more times. 

Below is a link to code that created the final poem. The text of this post sorta ends here and picks up in the code linked to.

[poetry_generator.ipynb](https://gist.github.com/nkernis/e7cfa374d16fe16f320ed25a638db427)

Here is a version of a poem produced by this code

```
a ambition of dust
     in southern france
          pants for electricity
                fervently inhabited by french and german speaking people

                a for speaking by french pants people southern
          dust in france
     and fervently ambition
of electricity inhabited german

a craving of sand
     in a hot climate
          attracts candles
                eagerly inhabited by people who love to read

                read sand who of inhabited craving hot attracts
          candles climate
     eagerly people by a
to love in a

a eagerness of dust
     in a cold, windy climate
          hopes for natural light
                tenderly inhabited by collectors of all types

                inhabited hopes eagerness windy natural a of
          types dust of a
     tenderly cold, for climate all
in by light collectors

a longing of sand
     by the sea
          longs for all available lighting
                curiously inhabited by very tall people

                very curiously inhabited a sand for
          available longs people the by
     longing sea of
by lighting all tall

a ambition of paper
     in a place with both heavy rain and bright sun
          thirsts for candles
                burningly inhabited by people who love to read

                rain inhabited sun place a thirsts burningly of
          people with heavy
     paper a candles love both by ambition read for bright
and in to who

a yearning of discarded clothing
     in a hot climate
          thirsts for natural light
                beautifully inhabited by french and german speaking people

                french climate and in inhabited clothing german for
          people hot light by
     thirsts speaking beautifully a
a natural of discarded yearning

a thirst of roots
     inside a mountain
          hungers for candles
                burningly inhabited by people who eat a great deal

                eat burningly great who by roots inside a mountain
          a people of
     for thirst candles
a inhabited hungers deal
```