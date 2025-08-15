---
title: "Who's Washing the Dishes Tonight?"
date: 2025-08-15
---
Hi there!
This is my very first project using R with 0 previous coding experience. Why R? I've had a bit of exposure to the coding language through some of my extracurriculars involving biostatistical research. Although other coding languages never appealed to me, I saw first-hand how R could be used to perform complex tasks to answer questions about problems that I'm interested in!
With all of that being said, I present to you my own rendition of a wheel of fortune: "Who's Washing the Dishes Tonight?". My younger brother and I always bicker about who will do the dishes, so I wanted to solve this problem by having a computer decide for us!
However, as you will notice soon, the computer isn't completely unbiased. I may or may not have tipped the odds in my favour. ;)

I started this project by learning basic commands like "sample", if-else statements, concatenanting, replicating and using a table. This taught me how to roll two dice, which built the groundwork for my project. 

1) I started by outlining my variables
> randomizer <- 1:2
> probability <- c(0.25, 0.75)

2) I moved to creating the weighted "coin".
<pre> ```r  rolling <- function() { spin <- sample(randomizer, size=1, prob=probability) if (spin == 1) { print("Jessica") } else { print("Christopher") } } ``` </pre>
> rolling <- function() {
> spin <- sample(randomizer, size=1, prob = probability)
> if (spin==1) {
> print("Jessica")
> }
> else {
> print("Christopher")
> }
> }

3) To test:
>  rolling()

4) Proof of efficiency:
>  proof <- replicate(50, rolling())
> table(proof)

And there you go! I'm not too sure how to better format the code and my results, but I hope you enjoyed reading this small blog! Now I'll only have to do the dishes 25% of the time!
