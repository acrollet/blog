+++
title = "Creating a WatchOS app in a morning"
date = 2024-12-15T20:22:38-07:00
tags = ["productivity", "AI", "chatgpt", "claude"]
description = "Coding with LLMs for fun and no profit."
+++

Ever since I started [running more slowly]({{< ref "/posts/on-enjoying-running" >}}), I've wanted a very specific running app. This app would be very minimal, letting me focus on the act of running rather than staring at a display to maintain a certain heartrate zone. It's possible that something like this exists, but I couldn't find it. I noodled on the idea of building that app, but it felt like it would take more effort than I wanted to expend. (This was based on bitter experience with abortive past side projects)

So, I decided to timebox the project. On a day off in October, I decided to see if I could start coding that morning and use the app on a run that afternoon. The basic structure was designed by ChatGPT[^1], starting from this prompt:

```
I want to create a WatchOS workout app. It should have a very simple UI and minimalist design.
It will be focused on running within a certain heartrate zone. When opened, the app should
prompt the user to start a workout and allow selecting a zone, defaulting to the previous selection,
or zone 2 if there is no previous selection. While working out, the app should only display the
elapsed time, current zone and current heartrate. Haptics should be used to alert the user when
above or below zone.
```

With some back and forth including clarifications and requests for additional features I didn't think of initially, I quickly had a functional prototype. This turned out to be a good way to flesh out and improve the idea while keeping the whole project in context. ChatGPT's output was very good overall.[^2] The only glaring mistake was hallucinating a non-existent Swift API for heart rate zones.[^3]  I then used [aider](https://aider.chat) with [Claude Sonnet](https://www.anthropic.com/news/claude-3-5-sonnet) to continue iterating. Long story short, the app was functional enough to use that afternoon after about 4 hours of work.[^4]

I've been using the app for most of my runs since then. After a few sessions of bug fixes and functional + UI improvements, I decided to release [ZoneFlow](https://apps.apple.com/us/app/zoneflow/id6739025069) on the app store. I don't have any illusions that it will be used by more than a few people, but it gives me extra motivation to maintain the app.

## Learnings

- Using LLMs took away almost all of the pain of dealing with a new language & framework
- Using Claude to generate initial versions of the promotional text & [help page]({{< ref "/ZoneFlow" >}}) etc. was a huge time saver and might have made the difference between bothering to publish the app or not
- If you clearly express the problem you're trying to solve, advanced models may be able to provide an entire solution without advanced [prompt engineering techniques](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)


[^1]: `o1-preview`
[^2]: You can see the chat transcript [here](https://chatgpt.com/share/675f7072-46e0-8005-bfe1-27fe3efc2bd2)
[^3]: A fairly classic case of an LLM providing a seemingly plausible answer rather than saying "I can't do that, Dave"
[^4]: About 2 of those hours were spent futzing with XCode!

