# Inline Spoilers on Reddit

The stacked bar charts show the number of spoilers `>! annotated like these !<` in Reddit comments and submissions each month (more precisely the number of comments containing such spoilers).

This visualization was originally created for my [master's thesis](https://www.inf.uni-hamburg.de/en/inst/ab/lt/teaching/theses/completed-theses/2020-ma-hatzel-spoiler.pdf), where I detected spoilers using neural networks.
I found these graphics to be pretty neat but I didn't get to around to publishing them individuall at the time, so the data is a bit out of date.

I based it all on Reddit dumps from pushshift.io which I processed [using Spark](https://github.com/hatzel/spoiler-data-processing).
While Reddit introduced 'official' spoiler tags at some point, before that various different ways of encoding spoilers were to be found, as far as I know all of them are handled.
Unlike post-level spoiler information this 'inline' tagging is (or at least was) not actually easily acessible (e.g. via API) and I had to [extend a Markdown parser](https://github.com/hatzel/markdown-spoilers) to extract the tags from raw Markdown.

The actual visualization was created using the latex package pgfplots, mostly for consistent font sizes etc. in the actual thesis.

Some interesting observations in the data:

* A peak in the StarWars subreddit in late 2015 relate to the Force Awakens release
* Red Dead Redemption 2's release is also clearly visible
* I wasn't able to explain the September 2018 peak.

For some further analysis check out the section 4 of the [thesis itself](https://www.inf.uni-hamburg.de/en/inst/ab/lt/teaching/theses/completed-theses/2020-ma-hatzel-spoiler.pdf).
