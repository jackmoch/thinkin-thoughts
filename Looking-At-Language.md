# Looking At Language

## Overview

My goal here is to open up a discussion about the distinction between syntax and
semantics, particularly how we can get bogged down in the former and lose sight 
of the latter. 

## Intro

Why do we build programming languages? 

In my opinion and experience, a programming language offers an interface into a
very powerful set of constructs. In order to leverage these constructs we build 
abstractions, and these abstractions allow us to interact with the lower level
constructs without having to spend too much time focusing on on the minutia and
details of the mechanisms that control them. 

Before a language designer even begins to think of the syntax with which a
user can control the constructs, I believe they would want to flesh out the 
general abstractions they want to offer to their users. This core list of 
abstractions can live totally separate from the syntax, which eventually be
designed around the abstractions, and can be referred to as a language's
value propositions.

The power in defining a set of value propositions that a language can offer via
its abstractions is that they can live and be discussed outside of the context 
of syntax. 

This gets a little "meta" but that means we can define a language with which we
can talk about...defining languages. Stay with me.

## Syntax vs Semantics

Think about this question: "What is a for-loop?"
This can be answered without ever mentioning anything about how it's invoked. 

A for-loop is an abstraction that allows a user to `do x thing` for each element
in a collection. 

That is _totally_ different from the question: "How do I write a for-loop?" 

This is the separation of syntax and semantics at it's most basic level. 

## The Language of Language

A language used to talk about language is something we interact with every day.

Does your language have:
- for-loops
- while loops
- variables
- objects
- types
- dictionaries 
- arrays 
- etc

These all fit into the "vocabulary" of defining a language. It's an abstraction
that enables us to discuss programming languages without getting too deep into
the weeds. From a high level, we can talk about the general purpose abstractions
our language does or doesn't provide. 

## Unique Constructs

I've never written a programming language and think it would be disingenuous to
act like I was some type of expert in the field. But as a programmer I have 
certainly interacted with these constructs and seen firsthand the variations 
across languages in what constructs are available. 

To give an example, Clojure makes changing variables in place a bit obtuse, and
this was an intentional design decision. In doing so, they force a user to 
_acknowledge_ that they are about to engage in a mutation.

They facilitate this pattern with a construct called an `atom`. When you update 
an atom in Clojure, you use functions like `swap!` or `reset!`. These functions 
are appended with a bang to let the user know _you are about to mutate 
something!_ I found this to be a somewhat novel construct and something I 
couldn't draw a clear parallel to in other languages, so I would define it
as a _value proposition_ that is unique to Clojure. 

Perhaps a more portable and approachable example would be something like, is
the language automatically garbage collected, or does the language implement
a strict type system? 

## Zooming In

Although I'm sure there are a good amount of other unique constructs that 
are novel to their respective languages, I think a more common comparator 
would be the implementations of these constructs. 

This can be something as simple as: if I run the "same" for-loop in two 
different languages, which is more efficient, which is more memory intensive?

I think this is a good opportunity to point out that value propositions do
not translate to _right_ and _wrong_. They are about tradeoffs, not correctness.

This begins to get at the crux of the conversation, namely, different languages 
have different value propositions. This is not a qualitative assessment of how 
_good_ or _bad_ a language is, but rather an honest look at the value 
propositions the language has to offer and where that is or is not useful.

## Applying Value Propositions 

Now that we've clearly defined the line between syntax and semantics and opened 
the conversation to the differences between what languages have to offer we can 
begin to apply that knowledge. 

In a practical capacity, this means deciphering what types of constructs or 
value propositions are best suited to solve the particular problem at hand.  

Here is where I feel programmers can start to get in their own way by placing a 
higher level of importance on things like familiarity over utility. 

My language of choice is a LISP. What I think a lot of people hear in that
statement is "my language of choice uses a lot of parenthesis" instead of "my
language of choice is built on _list processesing_". To me, this is a prime
exemplification of focusing on syntax over semantics and missing the forest for
the trees.

## Conclusion

I know I know, you spent all of this time reading and you've gotten to the end
only to discover this was all an intricately placed trap to convince you parens
aren't as scary as you think.

I promise that is not my intention. I feel this is a topic that I encounter 
often due to the nature of LISPs, but I think the general concepts port quite
well across a variety of contexts. 

When we compare frameworks, libraries, tools, cloud environments, you name it:
are we _really_ focusing on what they have to _offer_, or do we sometimes get 
lost in how familiar, comfortable, or easy they are to use?

Now obviously there needs to be a balance. I don't care how amazing the value 
propositions of Brainfuck are, nobody is about to use that language to build a 
system because it is basically unintelligible. 

But I think it is extremely important to recognize both the strengths and the
shortcomings of the tools we are using when we are building technology. If we 
can have honest conversations that focus on the value propositions, the 
constructs that different languages have to offer, and determine what is 
_most important_ for the problem at hand, I truly believe we can build more
usable, functional, reliable software and grow together as a community while 
doing so. 
