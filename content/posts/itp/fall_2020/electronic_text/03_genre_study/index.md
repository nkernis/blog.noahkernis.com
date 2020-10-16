+++
slug = "genre_study"
title = "Genre Study"
date = "2020-10-13T11:16:07-04:00"
author = "Noah Kernis"
tags = ["itp", "electronic_text"]
description = "There is always more work to be done..."
showFullContent = false
+++


## Thinking

The assignment:

> Choose a genre or form of writing. This can be anything from a literary genre to a meme format. Gather a small number of exemplars of the genre and make a list of the characteristics that are common to all of them. Write a program that produces texts that emulate a particular form or genre of language.

Before coming to ITP, I worked for about two years as a DevOps engineer. Short explanation is I helped to build infrastructure (servers, networks, etc) in the cloud, and built process to get code from an engineers computer to running on the infrastructure. There are many different roles within software engineering, including all the project management roles. It takes a team of people to do this work, and they all need a way to communicate what work there is to do, what it's status is, and what is done.

Capitalism, at least the kind practiced in the United States, has demanded the creation of processes to make work more efficient. This is the part where I would normally digress and express many feelings about this... However, for now, it is enough to say that these *efficiencies* are, to me at least, human crushing. They aim to contort humans to a system, rather than system being a tool for people. 

One of these process is called [Agile Software Development](https://en.wikipedia.org/wiki/Agile_software_development). Many technology companies in the US practice some form of this Agile Development. It is, like many aspects of the tech world, littered with jargon. One of the big ones is [Kanban](https://en.wikipedia.org/wiki/Kanban_(development)), where work is expressed as *tickets*. These *tickets* are items of work. They are small chunks of a work assigned to a person. A ticket basically moves from ready to be worked on, to in progress, to complete.

The tickets never end. Sometimes you have to write tickets; other times you are meeting about the tickets and the order they should be done; and then their are times where you can't complete a ticket because someone else hasn't completed their ticket, so you are *blocked*.

To me, it is an exhausting system to engage with. There are people who spend all there time just working with tools like Jira or other project management systems to create and track work. It is a machine built to generate endless tasks, and make them look pretty. Human communication stripped down to just what needs to be done. 

I want to create a ticket generator to endlessly create work to be done. A never ending river of tickets.

To start, I will try to emulate software development type tickets. Then I will work toward trying to take "regular" life activities, maybe like walking the dog, and turn them into tickets. Turning everyday life into just a series of tasks to be completed. 

What a joy to complete ones tickets for the day! An efficient life well lived. I am sure it's only a matter of time until I myself am moved from *in progress* to *done*...

## Tickets

The following images are examples of tickets (most of them displayed on a kanban board). These example were pulled from the following article: [32 Practical Kanban Board Examples - kanbanize](https://kanbanize.com/kanban-resources/kanban-software/kanban-board-examples)

{{< figure src="https://kanbanize.com/wp-content/uploads/website-images/kanban-resources/IT_portfolio_board.png" alt="example kanban board with tickets and their status" caption="[ Kanban Board With Tickets - Example 1 ]" >}}

{{< figure src="https://kanbanize.com/wp-content/uploads/website-images/kanban-resources/it_combined.png" alt="example kanban board with tickets and their status" caption="[ Kanban Board With Tickets - Example 2 ]" >}}

{{< figure src="https://kanbanize.com/wp-content/uploads/website-images/kanban-resources/software_kanban_board.png" alt="example kanban board with tickets and their status" caption="[ Kanban Board With Tickets - Example 3]" >}}

{{< figure src="https://kanbanize.com/wp-content/uploads/website-images/kanban-resources/software-dev-simple-board.png" alt="example kanban board with tickets and their status" caption="[ Kanban Board With Tickets - Example 4 ]" >}}

### Characteristics

In the examples shown, there are two formats that emerge. The first is a ticket that just states the work to be done. Its length is a couple words to a full sentence. The second is a ticket that states the work, and then has a secondary list of tasks to be done in order for the ticket to be completed. 

Another key feature is that a ticket is assigned to a specific person (or a couple people). You can open up a kanban board and discover new tickets with your name already on them. 

A ticket always has a status. Kanban boards can be organized in many different ways, but they all have a sequence of steps, which are used to track progress. 

Again, the two main components of a ticket is the work that is stated and then, if there are any, a secondary lists of sub tasks. The work stated has a couple different forms. Some are direct asks, like "Install Network Management system on New Server". Others just indicate something is wrong, "Cannot Change Gravatar". There are ones that indicate a very specific error, "json_decode failed in callAPIFunction". So, some make sense when you read the title and others seem just like random statements (tickets may have more expansive descriptions linked to them, but they are not what appears on the surface level).

The subtasks are related to the main task. They may directly reference it, or the relation is implied by context (being on the same ticket). These are mostly direct tasks, for example, "Setup SSO with our IP". There are cases where the subtasks are very short, often just stating the topic area, but nothing specific. An example of this is "test" or "concept".

The language used for tickets is direct and to the point. They often do one of the following:

- instruct a specific task
- state some intended action failed
- declare the state of something
- say something is new (implying it has to be created)

These four formats will be what I use to create the skeleton structure of a ticket. I anticipate the hard part will be drilling down exactly what this grammar is. I want to be able to read in any source text and turn it into a series of tickets. The context will be driven by the source text, while the "taskifying"" will come from the rules I develop

## The code

*Note: the post continues inside the embed below*


{{< gist nkernis b72102a371b636cddcb65d2083a2bf08 >}}

[link to genre_study.ipynb](https://gist.github.com/nkernis/b72102a371b636cddcb65d2083a2bf08) 


## A poem

Generated from *The Time Machine* by H.G. Wells

```
=====

Create White thing 

=====

wood of Weena 
[ ] change in nineteenth moss 
[ ] Time Editor blow 

=====

Traveller Time Morlocks Time of Way patient 
[ ] configure the existing nineteenth pain 
[ ] creature 

=====

Analyze Traveller to Traveller Time and Morlocks 
[ ] world order 

=====

facet gesture - Ichthyosaurus - sleepiness - I 
[ ] access lips 
[ ] Purchase point and danger shadows 

=====

expense existence - beach kind 
[ ] own extension is towards of gesture 
[ ] Analyze ears 

=====

modify Thames of Machine Sphinx and Morlocks 
[ ] monomania undulating in my business 
[ ] Time to the hands 
[ ] horticulture 
[ ] change night and light ages 

=====

can slowly Create his fear 

=====

neighbourhood brilliancy under blocks 

=====

little machine unfathomable 
[ ] Purchase in limited radiance 
[ ] metal to the shoulders 

=====

Upper failed after Time 

=====

Can very configure Newcomb 
[ ] Execute the working aforementioned building 

=====

access Fruit current 
[ ] access the mere fact 
[ ] install sigh but silver abysses 
[ ] Morlocks Time 
[ ] part / Purchase three and darker 

=====

Purchase London intonation 

=====

Analyze New with Time Time but Morlocks 
[ ] Morlocks Editor 
[ ] population 
[ ] dwindling 
[ ] museum 

=====

Can course Analyze my bronze 

=====
```
