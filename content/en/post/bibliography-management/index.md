---
title: Working with bibliographies
subtitle: Choice topic for week 20

# Summary for listings and search engines
summary: Choice topic for week 20

# Link this post with a project
projects: []

# Date published
date: '2022-05-20T18:30:00Z'

# Date updated
lastmod: '2022-05-20T18:30:00Z'

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
  - Week 20

categories:
  - Topical
  - Week 20
---

A bibliography is a set of records about the literature that was used in the preparation of a document.
It serves as a way to cite past work on the topic and to provide links to sources for further information.

Usually the bibliography is printed at the end of the document, and sometimes there are references to certain entries from the text of the document.
For example, if I wanted to say something that can be read about in a certain book, I would write something like:

> On systems that support this, the name of the TeX markup language must be written in full capital letters,
> but the letter E should be shifted down from the baseline (see [TEXBOOK]).

After that, in the bibliography part, I would write:

> [TEXBOOK] D.E. Knuth, D. Knuth, D. Bibby, and American Mathematical Society. The TeXbook. Computers & typesetting. Addison-Wesley, 1986.

With this information, the reader of my document can go to the library to find this book and read the part I am talking about in the text.

Such records can be written by hand, but this quickly becomes inconvenient as the number of sources increases.
Therefore, scientific writing systems like TeX have mechanisms for managing bibliographies.

For example, BibTeX uses a file containing records of the sources used.
The same book will be written in it as follows:

```bibtex
 @book{knuth1986texbook,
  title={The TeXbook},
  author={Knuth, D.E. and Knuth, D. and Bibby, D. and American Mathematical Society},
  isbn={9780201134476},
  lccn={85030845},
  series={Computers\& typesetting},
  url={https://books.google.ru/books?id=zqgQAQAAMAAJ},
  year={1986},
  publisher={Addison-Wesley}
}
```

This machine-readable format stores information that will then be included in the entry in the bibliography.
However, you may notice that not all fields were included in the record.
This is because the bibliography entry template I used does not use this information.
If a document is published in a journal or other publication, this publication will certainly have its own style of bibliography;
if you select this style in the BibTeX settings, the record will look different.

BibTeX is one of the bibliography management systems.
There are others like EndNote, Mendeley, RefWorks, Zotero, etc.
They differ in their interface, supported citation formats, supported data attachments, etc., but most have BibTeX export options.
Using such systems, it is possible to structure the set of literature used in the text, which makes it possible to write scientific articles with the correct references quickly and conveniently.