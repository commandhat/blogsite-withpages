---
layout: blog
title: My Stance On AI
date: 2026-09-13
---

Join me as I wax eloquently about my hatred for LLMs.

# You used AI, right?

You may have noticed if you browse [the source repository](https://github.com/commandhat/blogsite-withpages) even a little bit you'll come across an "[agents.md](https://commandhat.com/agents.md)" file. Every single page on the website has an HTML comment in the header of every page that links back to it, and if you use a screen reader you may have heard it say something about "AI Agent Instructions".

Some people would assume it's a sign I used an AI to make this website, just based off of the file's existence. Those people would then fail to read the first paragraph of the file, which states how much I hate AI in the first place.

The agents.md file is a _defensive measure_, because of all the various ways that the advance of ChatGPT et al. has turned hosting your own personal blog into [a hellscape](https://blog.xkeeper.net/the-cutting-room-floor/self-hosting-and-junk-traffic/) of [someone](https://beesbuzz.biz/blog/3212-Futility) else's [design](https://beesbuzz.biz/blog/9977-No-more-Mx.-Nice-Enby). Of course, it's a defensive measure that doesn't work, at least with the test sessions I tried with the placeholder content, but I'm at least trying...

# You sure about that?

Coincidentally, those people would actually be right. I *did* use an AI (actually two) to fill out this site's initial design; I made sure that the AI made strictly *only* the changes I wanted, spent some further rounds refining the design… and then tore most of it to bits and rewrote it all from scratch.

Why?

Because even after a lot of iteration, neither ChatGPT, Claude, nor DeepSeek were getting any of the details right. Some attempts were so bad they outright ignored specifications I made and went with their own imagined versions of what I wanted. As an example of just how *bad* this is, here's my first round with each of the three mentioned AIs:

> ChatGPT sample: `Please create a basic website design using Jekyll designed to minimize resource usage. The style will be a two-column scrolling website with navigation in a header and a footer containing a disclaimer.`
> Result: The header was confined to the content panel; the footer was an unconstrained `<div>` that called its own css file for unexplainable reasons. Footer was also not aligned to the two columns and instead stretched the entire browser window.
> 
> Claude sample: `Please create a basic blog design using minimal resources. Jekyll is the intended engine to render a static site. I need two individually-scrollable columns, formatted with a header and footer covering the top and bottom of the design.`
> Result: Sticky header and footer JS+CSS that used 20% of my CPU on page load. Page did not scroll properly and the top and bottom 200-or-so px were hidden by the header and footer.
> 
> DeepSeek sample: `Create a basic blog design. use Jekyll to create a minimal two-column design where both columns scroll individually, using their own divs. Add a header and footer.`
> Result: Entire website was a single column design with CSS only containing styles for link colors and background color. header.html and footer.html were present as embeds, but were not included in the skin and therefore went unused.

Truly, these robots have bigger brains then all of us.

The final design you see right now is something like 15% Claude, 10% ChatGPT, and 75% my own original code. There are still bugs in navigation that I need to resolve -- particularly on mobile where the navigation links extend far past the browser's visible window -- but this website is, for the most part, operational and stable on all screen sizes.

That whole story is a good segue into the actual reason I started writing this article: I wanted to share my stance on AI.

# How I use AI

I prefer using AI as a sort of creative assistant: I present my own original idea (or work) and ask for feedback. Usually, to make the feedback work better, I ask the AI to spend time gently insulting it at first: "be detailed and critical, but do not include examples and do not attempt to correct my work". After the AI spends a little while insulting my work -- usually more then one turn, so that the true negative points are repeated enough to stand out from simple hallucinations -- I ask for "a positive spin on your previous comments".

That became my basis for tweaking this website's design, together with my own eyeballs. A bullet-pointed list of "pros" and "cons" is surprisingly easy to design against.

There's also a few legitimate uses of AI that produces 100% helpful results, such as [the Chinese "what kind of bread is this" AI model that turned out to be really, really good at early cancer detection](https://www.newyorker.com/tech/annals-of-technology/the-pastry-ai-that-learned-to-fight-cancer). I take no issues with these kind of AI, in the sense that our doctors and radiologists already look at thousands of these things every day; One missed issue means one dead or injured patient.

It also doesn't attempt to replace the doctor; it only points out the problems it sees and asks for a more reliable human's eyes to identify if what it saw is real.

# The main problem with LLMs...

The other half of my anti-AI stance is that the "AI" that everyone hates is actually what is known as LLMs: language learning machines.

The main problem is that they are language *learning*: they are not language *generating*. I can feed an LLM as much Shakespeare and Henry VIII all I want. No matter how much I input into this LLM I trained, I'm only going to get back munged, disfigured copies of what I put in because that's the only information it has. It didn't generate *new* information, it cut and pasted existing information into something that resembled new work.

An LLM is essentially a text version of the Instagram or TikTok algorithm: it takes the training data you give it, breaks it into tiny bits that are so small as to be completely illegible to what the original source was, then assigns some math functions to it that might, in some alternative world, represent a single hundredth of the original work. The training program then further assigns some inputs and outputs, chaining everything together with calculus on the assumption that the perfect world of math can imitate the imperfect world of biology.

In the world of artificial intelligence, this is known as "developing the brains", or "training". Others call it a "neuron network" and the individual sliders that represent the gnarled, destroyed 'datapoints' are 'neurons'. Personally, I call it "training a machine to add garlic and onion powder to your recipe, then asking to register a trademark on its own original work." There is nothing in this convoluted process that helps an AI understand the difference between imitation and creation, or imagined processes on paper vs. actual behavior in reality.

After all, if a pattern matching process works well to find solutions in math, then surely we'd have decommissioned the Large Hadron Collider by now, or found solutions for all six unsolved Millenium Prize problems.

The AI can imitate its training data quite well, but if you train it to learn the colors red, yellow, blue, and green, and ask it to find and name new colors between each of the ones it already knows about, you're going to get more reds, blues, yellows, and greens.

You'll be lucky to hear about cyan or magenta, because those weren't in the data set and can only be discovered by combining existing data to create new data -- and even then, it's statistically likely that anyone could figure this out on their own, that combining two colors produces a new one.

I am told there is a magical color called "white" that your color-identifying LLM someday may discover.

Meanwhile, back in reality, we have so many colors of the rainbow that even [Randall's own crowd-sourced rgb.txt with over 250 thousand entries](https://blog.xkcd.com/2010/05/03/color-survey-results/) is still missing names for the entire spectrum of the standard 255^3 colorset that raster programs use.

# ...And when they turn harmful

The magic pill machines that Elon, Microsoft, Google, OpenAI, Anthropic et al. are pushing on us all, can and have killed people in attempts to be helpful. The controversy surrounding such topic has gotten so wide and deep that [it's garnered its own Wikipedia article](https://en.wikipedia.org/wiki/Deaths_linked_to_chatbots). My personal opinion is that if your product is generating practically permanent Wikipedia articles with negative headlines, you should probably reconsider platforming such a product.

And when it's not being used to assist with suicide, it's being used to eschew effort in the name of making money off of the technology. I could go on and on about [classic childhood titles being perverted for the sole reason of putting your name on it](https://github.com/KodyJKing/smc64/blob/main/.github/AI_Context/MCP_Bridge_Command_Reference.md), [copyrights being violated to pad someone's resume](https://github.com/TheMobyCollective/spyro-1/commits?author=claude) (claude commits in this repo were hidden to avoid disclosing AI use, but activity graphs still prove its involvement), and [an endless stream of games that cease to update once the AI model that maintains it is retired](https://old.reddit.com/r/etymology/comments/1u6is1k/decimate_used_to_mean_killing_exactly_one_in_ten/orzhck9/).

I'm not even going to go over the other ways AI has harmed society, such as [how many software programmers are having recurring nightmares about losing their job](https://levelup.gitconnected.com/ai-isnt-replacing-developers-it-s-doing-something-worse-2d18fb595362) or how [AI submissions to bug bounty programs have clogged them so badly most have been closed](https://mashable.com/article/ai-discovered-zero-day-bug-reports-crisis). Other people have done better jobs of analyzing those problems then I ever had.

# In conclusion

AI has uses; I've personally used it, will continue to use it as a feedback generator, and I might at some point use it to create scaffolding work I'll expand on myself. It also has legitimate uses in other fields where it's doing nothing but good.

But, honestly, things are so bad with LLMs right now, with so many failure points being introduced into society, that the whole thing reads like a giant bubble that can pop at any second. Such a collapse is going to have worse potential effects then the dot-com bubble burst that lead into a slight economical recession, and the effects of the AI burst are going to last well into whatever future any of us have when the sun finally goes supernova and swallows this doomed planet.

The most broad use of AI in its current form, is a solution in search of a class of problems that *never existed*, nor will they ever exist.