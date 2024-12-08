+++
title = "Burndown charts are fake"
date = 2024-12-08T12:31:40-07:00
draft = true
tags = ["agile", "yelling at clouds", "productivity"]
+++

![Fake burndown chart, with Overestimates on the Y axis and Arbitrary Time on the X axis](feature-burndown.png "This tells me as much as any burndown chart I've seen. (Created with Claude's assistance)")

Wikipedia says the following things about [burndown charts](https://en.wikipedia.org/wiki/Burndown_chart).[^1] In my opinion, they are nearly all false!

> A burndown chart or burn-down chart is a graphical representation of work left to do versus time. The outstanding work (or backlog) is often on the vertical axis, with time along the horizontal. A burndown chart is a run chart of remaining work. It is useful for predicting when all of the work will be completed. It is often used in agile software development methodologies such as Scrum. However, burndown charts can be applied to any project containing measurable progress over time.

Burndown charts are actually a representation of **estimated effort** versus time. In order for this to be the same as **work left to do**, the following things must all be true:

* The estimates must be reasonably accurate
* The tasks being estimated must represent a valuable deliverable

Estimates are almost always over-estimates, because all the available incentives point in that direction. If all tasks were estimated completely accurately,[^2] the burndown chart would show work remaining at about half of all sprint demos. We are human, and we want Number To Go To Zero. Therefore, teams will do what they have to to make this happen.

> Remaining work can be represented in terms of either time or story points (a sort of arbitrary unit).

In practice, most teams estimate in terms of time. We'll give Wikipedia this one.

> Burn charts can be used to present the project's team velocity. Velocity is a measure that represents the productivity rate, within a predefined interval, for which deliverables are created, validated and approved.

Wrong again, because velocity is just a total of the team's estimates for a given interval. Need your velocity to look better? Just bump your estimates, add team members, or work some overtime.

In short, burndown charts are fake because they say nothing about value delivered. On a high-functioning team that aggressively prioritizes work according to value, there will be some relationship. _But there is no way to tell by looking at the chart._


A final note: I truly believe that teams are doing the best they can within the framework they have been given. Value is a messy concept and hard to measure, so leaders tend to fall back on more amenable concepts. [Goodhart's law](https://en.wikipedia.org/wiki/Goodhart%27s_law) is undefeated.


[^1]: If you don't know what burndown charts are, you are (1) a blessed soul, and (2) probably don't need to keep reading
[^2]: Yes, that's impossible, but work with me
