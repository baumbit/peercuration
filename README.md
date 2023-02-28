# Peercuration

## TL;DR
Peercuration makes it possible to mitigate proliferation of spam in decentralized social media networks. It is a simple mechanism that works like this. A node in a network, query its trusted peer nodes for their individual score of a hash, and then calculate an average score. The hash is a mathematically derived identifier for a digitally encoded resource. The score is a value between 0 and 1. This mechanism provides the means of creating a sorted list of digital resources (such as images, videos, social media comments, etc.), which makes it possible to weed out bad content from good and thus produce a curated list.

## The problem
In the early 2020 it was impossible to ignore how many people had become aware of the power of "the algorithm". Elon Musk boosted the outcry against "the Twitter algorithm" on Twitter and argued that it should be open sourced. Other people made it clear that merely making code open source was not enough, and social networks needed to be decentralized, so as to put an end to centrally controlled content distribution. People argued that Facebook streams, YouTube video lists, where designed to captivate people by creating "hits of dopamine" and did not have the best of the users as heart. True or not, all content platform need some way to filter through all the content and decide which content should have the highest priority and which content should be deleted.

## Spam
While decentralization of social media solves some of the issues related to centrally controlled content distribution, it opens the doors further to other issues such as spam. In an open network, it is difficult to prevent bots from creating a never ending stream of spam. While heavily modereated social media platforms such as Reddit, may be critized for censoring comments, at least spam and content that do not belong in the stream, is weeded out by moderators. In an open network, this fix is incompatable with the ethos of decentralization.

## The Solution: Peercuration
We propose a solution to this problem which we call Peercuration. Inspired by concepts such as "Wisdom of crowds" and "Web of trust", the general idea behind Peercuration, is that you as a user knows the best which other users you want to trust and follow. Afterall, you probably do not want someone else to tell you what content you should prefer to consume or not.

When everyone in a network establish connections with those they trust the most, then together they create a web of trust. This trust can be leveraged to weed out spam and moderate content. The only thing needed is for everyone to create a score content they consume and this information is then used to create an average score. Content with the best score can be prioritized for download and display in user interfaces, and content with the lowest score might even be blocked from propagation.

## The curation mechanism
It is possible to mathematically derive a numerical representation (called a hash) of all digital resources such as images, comments, JSON objects, etc., which is smaller than the resource itself. A score between 0 and 1 can then be tied to this hash. It is a good idea to great a floor (zero) and a ceiling (one), because this way no node in the network can sque the average score in either direction. A hash and a score can easily be stored in a HashMap or similar, thus it is easy and fast to find out what score a hash has.

As a node on the network, you have your own oppinion on what the appropriate score of a specific content is. This is the score you should share with your peers, when they are asking you for your score. Sure you could lie and always send the lowest or the highest score no matter what the content is, but such bad behaviour will be punished when your peers finds out that your scoring tends to overlap poorly with their own preferences. Or more bluntly put; if you start sending spam to your peers are likely to stop asking you for content, block you and maybe even drop the conncetion they have with you. You are pushed out from the web of trust and now on your own. Hence good behaviour is rewarded and bad behavour punished.

Note, what is considered bad or good is fully subjective. If you peers do not like your scoring, you are probably better of if you find another group of peers that share your preferences.

And this is how digital resources gets sorted in the network. Different content will gravitate to different parts of the overall network and only that content which everyone agrees on is spam, will be dropped by everyone. Content that everyone feels is the most valuable, will be propagated the most and persist the longest in the network.

