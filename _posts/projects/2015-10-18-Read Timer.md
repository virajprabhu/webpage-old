---
layout: project
title: "Read Timer"
excerpt: A chrome extension to learn your read speed and provide estimates of article read times.
date: 2015-10-18
---

A light week at work coupled with a niggling urge to build something led a colleague and me to pick up something we felt we'd like to use - a read timer. The said read timer would provide a reasonably accurate estimate of the time it would take to read a blog article without having to scroll all the way down (and thus decide if it was worth it). Personally, it appealed to me on several fronts - 
<ul>
	<li> It was a small project and would be easy to put out in a short timeframe.</li>
	<li> It seemed useful.</li>
	<li> There were subtle complexities such as parsing the page well enough to identify only the article and ignore ads, navigational text, comments, images etc.</li>
	<li> The aspect of <i>learning</i> the user's speed seemed like a challenging problem. </li>
	<li> I really needed something to do. </li>
</ul>

So off we set.

We'd originally got the concept from <a href="www.medium.com">Medium</a> that does this for all its articles, presumably manually. Apart from <a href="https://getpocket.com/">Pocket</a>, some basic google-fu revealed the existence of services such as <a href="https://www.readability.com/">Readability</a>, <a href="https://www.instapaper.com/">Instapaper</a>, <a href="http://embed.ly/">Embedly</a> etc. that were devoted to providing 'Read Later' functionalities to archive articles to be read later in a simple, clean format. Readability and Embedly have even put out API's.<br/>

We decided to go the non-API way (we weren't going to pay for full access), and building a chrome extension seemed like a natural starting point owing to the ease of use (or so we believed - the <a href="https://developer.chrome.com/extensions">chrome extensions API</a> was its own can of worms). A week later, we have a (mostly) functional browser action chrome extension that uses the <a href="https://github.com/mozilla/readability">Mozilla Readability.js</a> project and can:
<ul>
	<li> Provide an estimate of the total time it will take to read the current article.</li>
	<li> Provide an estimate of the remaining time based on the user's position in the article.</li>
	<li> Learn the user's speed based on time spent reading each page, This is a highly experimental feature and far from stable/reliable at this stage.</li>
	<li> Is reasonably well documented and completely open source. <a href="https://github.com/virajprabhu/read-timer">Here's</a> the code. Feel free to contribute! </li>
</ul>

There are still a couple of bugs/UX issues we want to iron out before publishing a 1.0 release to the store. We'd really like to do better with the learn feature and also improve the parsing. Another ambitious feature would be to factor in the complexity of an article and the nature of content (say, a comic) while providing an estimate - there are a ton of such possibilities. We're planning to explore a few of them in the coming weeks, and welcome all sorts of contribution in code, opinions or otherwise!

EDIT: The extension is live! Check it out <a href="https://chrome.google.com/webstore/detail/read-timer/ojcneamhcbpginfcagjnmeeegbhpngdk?utm_source=chrome-app-launcher-info-dialog"><b>here.</b></a>