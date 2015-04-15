---
layout: post
title: 'Seven Languages in Seven Weeks: Erlang, Day 2'
date: '2012-11-04T20:29:00.002-08:00'
author: Yevgeniy Brikman
tags:
- Seven Languages in Seven Weeks
- Software Engineering
modified_time: '2012-11-04T20:29:36.156-08:00'
blogger_id: tag:blogger.com,1999:blog-5422014336627804072.post-5833130757249896035
blogger_orig_url: http://brikis98.blogspot.com/2012/11/seven-languages-in-seven-weeks-erlang_4.html
---

After learning some basic Erlang syntax on [Day 
1](http://brikis98.blogspot.com/2012/11/seven-languages-in-seven-weeks-erlang.html), 
I take on the second Erlang chapter, which introduces some more interesting 
concepts. 

## <span style="font-size: x-large;">Erlang, Day 2: Thoughts 

I'm finding it very easy to dive into Erlang. After going through the Prolog 
and Scala chapters of this book, as well as making heavy use of Scala at work, 
the functional constructs used in Erlang feel natural. I've grown very fond of 
pattern matching in the last few months and have found it to be a very 
powerful tool for expressing complex concepts in a very concise and readable 
manner. Erlang's heavy reliance on pattern matching makes me happy. 

However, the syntax does feel slightly clunky: I constantly forget to end 
lines with dots and separating clauses of control structures with semi-colons 
gets annoying. I suspect this is something you get used to. Moreover, the end 
result, at least in the dead-simple code snippets I've looked at so far, is 
pleasantly readable. 

## <span style="font-size: x-large;">Erlang, Day 2: Problems 

## List lookup 
<b> 
</b>Consider a list of keyword-value tuples, such as [{erlang, "a functional 
language"}, {ruby, "an OO language"}]. Write a function that accepts the list 
and a keyword and returns the associated value for the keyword. 

My implementation: 

<script 
src="https://gist.github.com/4015266.js?file=list_lookup.erl"></script> 
## Shopping list price 
<b> 
</b>Consider a shopping list that looks like [{item, quantity, price}, ...]. 
Write a list comprehension that builds a list of items of the form [{item, 
total_price}, ...] where total_price is quantity times the price. 

My implementation: 

<script 
src="https://gist.github.com/4015266.js?file=shopping_list_price.erl"></script> 
Sample usage: 

<script 
src="https://gist.github.com/4015266.js?file=shopping_list_sample_usage.txt"></script> 
## Tic-tac-toe 
<b> 
</b>Write a program that reads a tic-tac-toe board presented as a list or a 
tuple of size nine. Return the winner (x or o) if a winner has been 
determined, cat if there are no more possible moves, or no_winner if no player 
has won yet. 

My implementation: 

<script 
src="https://gist.github.com/4015266.js?file=tic_tac_toe.erl"></script> Sample 
usage: 

<script 
src="https://gist.github.com/4015266.js?file=tic_tac_toe_sample_usage.txt"></script> 
My first tic-tac-toe solution was a bit more complex, using recursion to scan 
all rows, columns and diagonals. However, I found that for a 3x3 board, the 
simple pattern matching approach, while somewhat verbose, was much easier to 
read. 
<div> 