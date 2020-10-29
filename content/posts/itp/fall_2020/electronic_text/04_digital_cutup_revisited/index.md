+++
slug = "digital_cutup_revisited"
title = "Digital Cutup - Revisited"
date = "2020-10-24T17:39:56-04:00"
author = "Noah Kernis"
tags = ["itp", "electronic_text"]
description = "The chef said to, \"cut them smaller\""
showFullContent = false

+++

## Thinking

The assignment for this project:

> The digital cut-up revisited. In assignment #2, the tools available to you for cutting up and rearranging texts relied only on information present in the character data itself. Since then, we’ve learned several methods for incorporating outside information concerning syntax (i.e. with spaCy) and semantics (i.e., word vectors) into what we “know” about a text in question. Adapt your original digital cut-up assignment, making use of one of these new sources of information. What new aesthetic possibilities are made available if the unit of the cut-up can be a type of syntactic unit (instead of words, lines, characters), and if stretches of text can be algorithmically selected not at random, but based on their meaning?

### Last time

So, the last time I did this ([Elements of Circumstance](https://blog.noahkernis.com/posts/itp/fall_2020/time/elements_of_circumstance/)), most of my effort went into creating a collection of strings I could then randomly pick from, based on a word I was interested in. 

I was pleased with the results last time. However, it didn't quite achieve what I had in mind. I wanted the text produced to *feel* like it was ruminating on the 5W's, time, and space. To sort of, go down a rabbit hole of thinking.

### This time

This time, I'm going to do a little bit of work to create a corpus to pull from, and then use vectors, calculated by spaCy, to find similar meaning sentences in these corpus's.

Here are some of thinking notes:

```
~> vector relationships of 5W's (something more than just themselves?)
    ~> calc distance and point between two or three 
        ~> Can vectors be used to ask questions? ~> *distributional semantics* (spaCy vectors)
~> structure of the sentences I wrote (5 for each W)
~> use vectors to break down a sentence?
    ~> pull out the 5Ws? replace them with something?
    ~> how to abstract it?
~> time as an actor ~> analyze text and fill these in?
    ~> does that "reveal" anything?
~> new form and structure
```

## The plan

After some thinking, I came up with three things to try. Hopefully, this will lead to output that feels a little more like someone trying to think about the 5Ws, space, and time. 

1. explore vectors for 5Ws
    - what is the average W?
2. explore sentence meaning between texts
    - pull sentences from one text and find a similar meaning one in the other texts from the group
3. go back and forth between texts
    - pull sentence with 5W, time, or space in it
    - manipulate the pulled sentence then find a similar meaning one in the other text
    - repeat with all the terms

## The code

*Note: the post continues inside the embed below*

{{< gist nkernis 47117471da3bbfec823af0cb8c05caa7 >}}

[link to digital_cutup.ipynb](https://gist.github.com/nkernis/47117471da3bbfec823af0cb8c05caa7)

## Structure in a poem

I wanted to highlight the structure of one of the texts produced. This a good example of how the random tabs can change how the reading.

Although you could read this left to right, because of things like proximity, I feel like I should read the terms on the left as one block and the sentences on the right separately.

{{< figure src="img/00_poem_structure.png" alt="" caption="[ Example Structure in Output Text ]" >}}

## A poem

*ask yourself honestly*

```
			But what he says about thinking in trains, and
			concentration, and so on, is not for me.

					what

		Our knowledge of things where we are not, and of
		things when we are not, is essentially the same—
		an inference (sometimes a mistaken inference)
		from brain impressions, including memory, here
		and now.

				where

		For myself, I know nothing more "actual," more
		bursting with plain common-sense, applicable to
		the daily life of plain persons like you and me
		(who hate airs, pose, and nonsense) than Marcus
		Aurelius or Epictetus.

			who

	The stationary observer and the aviator disagreed
	as to whose cigar lasted the longer time.

who

								For myself, I know nothing more "actual,"
								more bursting with plain common-sense,
								applicable to the daily life of plain
								persons like you and me (who hate airs,
								pose, and nonsense) than Marcus Aurelius
								or Epictetus.

							who

					Our knowledge of things where we are not, and
					of things when we are not, is essentially the
					same— an inference (sometimes a mistaken
					inference) from brain impressions, including
					memory, here and now.

							when

			Everything--the whole complex movement of the
			universe--is as simple as that--when you can
			sufficiently put two and two together.

	when

	Thus we have a suitable analogy for a circle
	whose circumference is less than π times its
	diameter.

					who

			And you would be able to tell us why, as the
			natural result of cause and effect, the longest
			straight street in London is about a yard and a
			half in length, while the longest absolutely
			straight street in Paris extends for miles.

							why

		Just as we picture different kinds of two-
		dimensional space as differently curved surfaces
		in our ordinary space of three-dimensions, so we
		are now picturing different kinds of four-
		dimensional space-time as differently curved
		surfaces in a Euclidean space of five
		dimensions.

		time

									It is as well not to chatter too much
									about what one is doing, and not to
									betray a too-pained sadness at the
									spectacle of a whole world deliberately
									wasting so many hours out of every day,
									and therefore never really living.

				who

							Just as we picture different kinds of two-
							dimensional space as differently curved
							surfaces in our ordinary space of three-
							dimensions, so we are now picturing
							different kinds of four-dimensional space-
							time as differently curved surfaces in a
							Euclidean space of five dimensions.

			space

						And when you have done, ask yourself
						honestly whether you still dislike poetry.
```
