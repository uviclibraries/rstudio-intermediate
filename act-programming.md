---
layout: default
title: 4-If Statements, Loops, Custom Functions
nav_order: 5
parent: Workshop Activities
---

# If Statements, Loops, Custom Functions
If statements and loops help implement logical operations in any programming language. We'll learn how to write these operations in R through basic examples.
A function groups operations into a single line of code which can be used repeatedly with different inputs.

1. **If Statements**
- An if statement in R has the following syntax:
```
if (<condition>) {
  <statement1>
}
```

<img src="http://www.trytoprogram.com/images/if.jpeg" alt="if" style="float:right;">
 
If the condition is True, then `statement1` is executed. If the condition is False, `statement1` is ignored and nothing happens. Try running this block of code which will print out a message if x is smaller than 10:
```
x <- 5
if (x < 10) {
  print("x is smaller than 10!")
}
```
In this case, we can extend this statement to include an `else` clause to execute another statement if the condition `x < 5` is False.
```
x <- 10
if (x < 5) {
  print("x is smaller than 10!")
} else {
  print("x is larger than or equal to 10!")
}
```
<img src="https://eecs.oregonstate.edu/ecampus-video/CS161/template/chapter_4/chapter4_images/4_08.png" alt="if" style="float:right;">

How about checking more conditions? Use `else if`! Any guesses which message the code will print out?
```
x <- 12
if (x < 5) {
  print("small x")
} else if (x < 10) {
  print("medium x")
} else if (x < 15) {
  print("large x")
} else {
  print("very large x")
}
```
<img src="https://eecs.oregonstate.edu/ecampus-video/CS161/template/chapter_4/chapter4_images/4_09.png" alt="if" style="float:right;">

2. **Loops**
A for loop runs some specific lines of code for a number of times.
<img src="https://cdn.techbeamers.com/wp-content/uploads/2019/01/C-For-Loop-Flowchart.jpeg" alt="if" style="float:right;">

`c(1:3)` is a vector containing integers `[1,2,3]`. The loop below will execute `statement` for a total of 3 times, one time each for i=1, 2, 3.
```
for (i in c(1:3)) {
  <statement1>
}
```
From Activity 3, we have a `score` variable containing test scores of 8 students. Suppose that we want to add 20 more points for each student. This can be achieved efficiently with a for loop. 
`length(score)` calculates the length of vector `score` which is the number of times we need to iterate through the loop (8 times).
`i` serves as an index and is a variable that is local/valid to only this for loop. We can also use `i` within the loop.
```
# score <- c(70, 62, 67, 69, 90, 72, 75, 80)
lenscore <- length(score)
for (i in c(1:lenscore) {
  score[i] <- score[i] + 20
}
score
```

3. **Custom Functions**


[NEXT STEP: Interactive Data Dashboard With RShiny](act-4.html){: .btn .btn-blue }
