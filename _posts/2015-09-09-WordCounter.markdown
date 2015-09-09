---
layout: post
title:  "Word Counter Design from Class"
categories: wordcounter gitlab
---
# About
This week in class, we built a simple word counter. It was initially implemented entirely in a simple main method that opened a file, looped until the end, and delimited words based on whitespace.

On Wednesday, we identified several aspects of the program that might change, and applied the strategy design pattern to abstract those elements out of the original program. Those were:

1. The source of the file may not always be on my local computer. What if I want to read the words from a file on the web?
1. The definition of a word is subject to change. Whitespace delimited strings are very restrictive; what if I want to support a hyphenated word at the end of the line as part of the first word on the subsequent line?

Our final design looks like this:
<img src="/images/word_counter_architecture.png"/>

You can find the source in the "WordCounter" project in my [EE363 Fall 2015 GitLab Repository](https://gitlab.camp.clarkson.edu/tfanelli/EE363-Fall-2015).
