---
title: Scientific programming languages
subtitle: Choice topic for week 21

# Summary for listings and search engines
summary: Choice topic for week 21

# Link this post with a project
projects: []

# Date published
date: '2022-05-28T18:30:00Z'

# Date updated
lastmod: '2022-05-28T18:30:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
  - admin

tags:
  - Topical
  - Week 21

categories:
  - Topical
  - Week 21
---

Scientific programming is a field of programming that relies on the use of computers for research purposes.
His tasks are often very different from industrial programming --
while there is often a focus on code readability and maintainability, here the speed with which the program design can be iterated is more important.

Because of this feature, many programming languages ​​are poorly suited for scientific programming.
For example, Rust, with its focus on the formal correctness of all memory usages, often slows down the developer,
and Java and other strictly object-oriented languages ​​require a more fundamental architecture than is often possible in scientific programming.

One of the languages ​​that is very often used in scientific programming is Python.
It is very popular, has an easy-to-learn syntax, allows many different approaches to solving architectural problems,
and also integrates into libraries written in C and C ++, which are faster and implement the most complex parts of the algorithms.
This makes the Python language convenient for gluing different data together and processing it in different ways, which is exactly what is useful in scientific programming.

Other languages ​​that are often used for working with data -- R, Julia, and Ada -- have simple syntax, a rich type system, and links to C/C++ code,
and all these features also make them useful in scientific programming.

Among other options, functional languages ​​like Haskell, F#, and Clojure allow algorithms to be described in a more declarative style --
don't say what calculations are to be done, but instead state the formulas that need to be calculated in the end.

Rarer programming paradigms like logic programming -- as implemented in Prolog and Erlang, for example -- are rarely used in industrial applications,
but in scientific programming they are often useful.
In logic programming, the programmer specifies statements about terms -- for example, "If something is a cat, then it is an animal",
"If something is an animal, then it is alive or dead", "If something is alive, then it is not dead", "There is something called Barsik", "If something is called Barsik, then it is a cat" and "If something is called Barsik, then it is not dead".
After that, you can ask questions like "What things are animals?", "What things are alive and dead at the same time?", "Is Barsik a cat and alive?" etc.
This kind of reasoning is often called logical propositions, and most programs are difficult to translate into a form that consists entirely of logical propositions.
However, in scientific programming, there are often questions that can be framed as logical statements, and such languages ​​help with this.

Thus, scientific programming has tasks that often differ from industrial tasks, so the set of languages ​​and paradigms that find application in scientific programming is very wide.