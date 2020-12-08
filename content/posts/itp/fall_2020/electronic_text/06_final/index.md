+++
slug = "final"
title = "Final Project - Frames"
date = "2020-12-07T17:59:46-05:00"
author = "Noah Kernis"
tags = ["itp",  "electronic_text"]
description = "*They poisoned the words, don't speak them!*"
showFullContent = false
draft = true
+++

## Thinking

For my final project I am going to explore frames, a topic I have been researching for my thesis. The main source for my initial research into frames is ["The ALL NEW Don't Think of an Elephant!: Know Your Values and Frame the Debate"](https://www.amazon.com/ALL-NEW-Dont-Think-Elephant/dp/160358594X), by George Lakoff.

Lakoff offers the following as a definition for frames,

> Frames are mental structures that shape the way we see the world. As a result, they shape the goals we seek, the plans we make, the way we act, and what counts as good or bad outcomes of our actions. (xi - xii)

Frames effect how we interpret the world. When an idea is new and hard to understand, Lakoff says that is because we lack a frame to understand it. We can either learn and develop a frame, or reject the idea. Another important point is that frames are structures in our brains. they are made up of patterns of neurons firing. 

When it comes to words, Lakoff writes,

> We also know frames through language. All words are defined relative to conceptual frames. When you hear a word, its frame is activated in your brain. (xii)

Words activate frames, and the more a frame is activated, the stronger it becomes. Lakoff says this is why when discussing the opposition in politics, people should avoid using the other parties language. That language is meant to activate frames that that party has chosen to connect to their values. Also, negating a frame actually activates that frame. That's why the book is titled "don't think of an elephant", saying it still invokes the image of an elephant. Lakoff says that images can also activate frames.

I drew an illustration to help myself better understand frames:

{{< figure src="img/00.jpeg" alt="" caption="[ They poisoned the words ]" >}}

There are two things in this image that I would like to experiment with for this final project. First, the sentence in the center of the TV. How does the language of political news coverage activate frames? The choice of words effects how political events are interpreted. 

Second, is the TV itself. One of the central ideas I am currently thinking about a lot for my thesis is how U.S. politics has been mediated through TV for over 70 years. We experience a lot of modern politics on tv through news, debates, and press conferences. This has expanded to the internet in many forms including twitter, tikok, anonymous message boards, youtube, and new forms of socials media apps. 

I am interested in how the physical devices themselves - a TV, laptop, or phone - may activate a frame within people. That frame may be an expectation or idea about the sphere in which they are interacting. That sphere is often refereed to as "the internet". There are many examples in U.S. popular culture of what is expected from the internet. Many of them depict the internet as a harsh and cruel place.

If so much of U.S. politics happens through devices that activate the idea of another sphere (the internet), and we expect bad things in that sphere, how do those devices effect our political discourse and beyond?

## The plan

I want to generate something that plays with how one word can invoke a frame, and the consequence of that. How can I effect how a sentence is interpreted?

The final idea I came up with includes three parts:

1. pick keywords from an article
2. generate a short sentence trained on the article
3. print the generated sentence out, surrounded by a "frame" made of one of the keywords picked from the article

For the final output I will pick a few articles, run them through my generator, pick two pieces from each articles, and then combine them into a small zine.

## The code

*Note: the post continues inside the embed below*

{{< gist nkernis 6fbce7130b1a2c74dc7e0659b518282a >}}

[predictive_text.ipynb](https://gist.github.com/nkernis/6fbce7130b1a2c74dc7e0659b518282a)

## A final piece

I created a final zine that was made from generating outputs from 5 articles and selecting ones I liked. The pdf can be viewed [here](https://blog.noahkernis.com/posts/itp/fall_2020/electronic_text/final/pdf/Not_News_Zine.pdf).

This is an example of what the generator makes: 

```
                           e      p
                            p    e
                             t  c
                              ac
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
accept                                                accept
accept                                                accept
accept                                                accept
accept                                                accept
accept                                                accept
accept      But the law and new ideas?                accept
accept                                                accept
accept                                                accept
accept                                                accept
accept                                                accept
accept                                                accept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
acceptacceptacceptacceptacceptacceptacceptacceptacceptaccept
      accept                                    accept      
      accept                                    accept      
      accept                                    accept      
      accept                                    accept
```