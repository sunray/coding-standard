# Sunray Coding Philosophy

A coding philosophy to aid in an efficient development workflow resulting from
readable, debuggable, and maintainable code. 

## Table of Contents

  1. [Consistency](#consistency)
  1. [Strict and Predictable Code](#strict-and-predictable-code)
  1. [Minimize The Impact of Change](#minimize-the-impact-of-change)
  1. [Optimize for Readability](#optimize-for-readability)
  1. [Optimize for Code Completion](#optimize-for-code-completion)
  
## Consistency

> If you're editing code, take a few minutes to look at the code around you and
> determine its style. If they use spaces around all their arithmetic
> operators, you should too. If their comments have little boxes of hash marks
> around them, make your comments have little boxes of hash marks around them
> too.

> The point of having style guidelines is to have a common vocabulary of coding
> so people can concentrate on what you're saying rather than on how you're
> saying it. We present global style rules here so people know the vocabulary,
> but local style is also important. If code you add to a file looks
> drastically different from the existing code around it, it throws readers out
> of their rhythm when they go to read it. Avoid this.

&mdash;[Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)

## Strict and Predictable Code

PHP is a dynamically typed language and JavaScript is weakly typed. Careless 
[type juggling](http://php.net/manual/en/language.types.type-juggling.php) can lead
to unpredictable code behaviour and hard-to-find bugs.

Be as strict as possible:

* Use type hints
* Use strict comparisons (=== and !==)
* Use value objects that check their arguments
* Use constants for values that are used more than once

## Minimize the Impact of Change

Bad code is hard to change, unstable, fragile and non-reusable. A small change can 
have unexpected and undetected effects anywhere.

Design your code to minimize the ripple effect of a change.

The [SOLID](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)) principles 
help to achieve this on the level of classes; The lesser known 
[RCC ASS principles](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
do the same for packages, components or even entire systems.


## Optimize for Readability

You write code only once, but it is read (and changed) many times. Write your code so 
that other developers can easily understand it.

Quoting Martin Fowler:

> Any fool can write code that a computer can understand.<br />
> Good programmers write code that humans can understand.

* Prefer simple solutions over complex solutions. No over-engineering. No premature
  optimization. No premature abstraction.
* Be consistent in approach, naming and structure with the rest of the codebase.
* Do not reinvent the wheel.
* Write documentation explaining why the code exists, not what it does. 
* Don't state the obvious.


## Optimize for Code Completion

If your editor can complete your code, you'll likely make less mistakes. And your editor 
can refactor your code later on.

* Use constants instead of string values
* Use value objects instead of associative arrays
* Use exceptions instead of return types
