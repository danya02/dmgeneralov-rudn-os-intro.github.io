---
title: Markup languages, LaTeX
subtitle: Choice topic for week 19

# Summary for listings and search engines
summary: Choice topic for week 19

# Link this post with a project
projects: []

# Date published
date: '2022-05-14T18:30:00Z'

# Date updated
lastmod: '2022-05-14T18:30:00Z'

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
  - Week 19

categories:
  - Topical
  - Week 19
---

A markup language is a way of writing text in a format that is suitable for machine processing and often contains, in addition to the text, instructions for displaying that text.
There are many different markup languages ​​that work well for different tasks.

We will consider the LaTeX language, which is most often used for writing scientific papers.
It is an extension of the TeX layout language, invented by Donald Knuth in 1978.
Backslashes are used to call commands, and curly braces are used to specify arguments:

```tex
This text is \emph{in italics}.
This text is in \textbf{bold}.
\begin{large}This text is larger than usual.\end{large}
\begin{Large}This text is even larger than usual.\end{Large}
\begin{LARGE}This text is STILL larger than usual.\end{LARGE}
\begin{huge}This text is huge.\end{huge}
\begin{Huge}This text is Huge.\end{Huge}
```

One of the most famous features of the LaTeX language is the ability to enter complex mathematical formulas. For example, this code:

```latex
\begin{equation}
\Delta M_i^{-1} = - \alpha \sum_{n=1}^N D_i \left[ n \right] \left[ \sum_{j \in C \left[ i \right]}^{} F_{ji} \left[ n -1 \right] + Fext_i \left[ n^{-1} \right] \right]
\end{equation}
```

...displayed as follows:

![Equation](eqn.png)

(This expression is the title of [one of Aphex Twin's tracks](https://www.youtube.com/watch?v=M9xMuPWAZW8).)

Because of this capability, LaTeX remains the gold standard for formatting mathematical texts, and it is not uncommon for other document authoring environments (such as Microsoft Word) to copy some of the syntax.
Some programs even use the LaTeX engine as part of their work -- for example, Pandoc uses it to convert documents to PDF, and [Manim's programmable animation library](https://www.manim.community/) uses it to display mathematical formulas in SVG format.

LaTeX also has a wide standard library that allows you to use it to display pictures, graphs, code blocks, and more. Thus, LaTeX is one of the most important markup languages ​​for scientific documents, and it is worth knowing for anyone who plans to write documents with mathematical formulas or other complex display elements.
