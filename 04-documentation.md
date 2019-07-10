---
nav_order: 4
---
# 4 On Documentation

Documentation is often touted as the savior of the software company. The idea
is that documentation carries the knowledge required for anyone to understand
and pick up the software, reducing "bus factor" and allowing reuse. While I
would not call this a fallacy, I might argue that it might become a fallacy
under some constraints. Often, you will hear people complain that "we need
documentation" or "if this were documented the problem would not happen" but I
don't believe it in full. I instead state that **more documentation will not
solve, and might even be potentially damaging**. This is nothing new, but it's
worth digging further.

The first point to investigate is that documentation is only as useful as it is:

- **concise**: delivers the right amount of information in the shortest number of words.
- **correct**: outdated information is deceiving and damages trust in the rest of the documentation.
- **scoped**: is attached as close as possible to the entity it documents, and offers the correct 
  amount of information.
- **discoverable**: it can be found easily and its existence must be inferred and discovered
  naturally.
- **consistent**: concepts are clear and well defined, and their definition remains unchanged.
  Established language is respected, rather than reinvented. E.g. if a document is a specification document,
  it should be called as such, not "master plan" or "project strategy". The documentation is kept updated against
  changes, or written so that changes to the code minimise the impact to the documentation.
- **straightforward**: the more indirection is needed to understand a document, 
  the less usable it is.

The second point is that documentation promotes a RTFM attitude within the
team, where the answer to every question is "it's in the documentation".  This
discourages fast exchange of knowledge and a culture of improving communication
skills via a high bandwidth two-way medium. Of course one has to weight this factor
against scalability, so the proper caveats must be considered.

The requirements given aim at delivering good documentation. Violating them leads
to heavy, unfocused documents with poor value. They also apply to all forms of
documentation: 

- code comments, which includes actual comments as well as any documentation strings for API, functions, classes and properties.
- tutorials, reference, installation guides
- troubleshooting
- regulatory requirements documentation
- internal guides (typically wiki pages)



## 4.1 Concise

Concise documentation

When writing some information, ask yourself: is it relevant for later understanding? If not, remove it.
later If something does not propel 
Concise, correct, well-organised, discoverable, and close to the
relevant place documentation will.** 
Enforce consistency of API naming, least surprise principle, proper naming, orthogonal behavior, minimalistic code, use of well-understood design patterns. Train as appropriate. 


## 4.2 Correct

## 4.3 Scoped

Documentation as part of the software component (versioned, tracked, “near” to the code)

## 4.4 Discoverable

Location and organization of documentation is critical for discoverability.
Documentation that is not easily discoverable is useless, which means that proper titles, proper tagging,
consistent keywords and a correct hierarchical classification is fundamental. 

Search engines vs information organisation.

reduce noise by removing old stuff.
Maintaining a well-organised documentation is a major task that requires discipline.

## 4.5 Consistent

example of writing installation instructions to follow the on-screen instructions. Better longevity.
Periodic refactoring of documentation layout in case of discoverability shortcomings and cleanup of outdated information.

## 4.6 Straightforward

Documentation should generally be self-contained, without having to depend on external documents for understanding.
This does not mean that documents should not have pre-requisites for understanding. It means that all the information
should be available within the document itself as much as possible.




- methods, functions and classes: in the code
- software packages: in the repository
- release and deployment processes: in the repository

Most companies rely on tools such as wiki or confluence to keep their
documentation.  The general trend of these tools is that they become black
holes where information is hard to find, strongly duplicated, lacks a review
process, makes it hard for interested people to learn about it, and encourages
to disconnect documentation from code. The tendency to create poorly organised
or flat hierarchies ends up creating poor signal to noise ratio. Information
literally disappears, swallowed in noise, in these tools if not properly
maintained and editorialised by a *mess manager*.

- spreading information that now have to be kept synchronised.

## How we write

A separate but related issue is the quality of documentation. Not everybody is able to
write quality documentation. I developed overall criteria to assess the quality of documentation

- if a picture requires a textual explanation, it is not working.
- the language of presenting information (top to bottom diagrams, pointed lists, flowing information).


# Regulatory documentation

Regulatory documentation has an important role in some industries.  Most of the
times, this documentation is technical but need to be handled, reviewed, and
commented by non-technical people. 

- word programming
- word burden and red tape
- word itself (bugs), updating the templates, have dumb templates. The Office.
- regulatory vs non-regulatory documentation. difficulty to find it.


- develop common language within team
- poor communicaiton and organization of info


## Types of documentation required:

Solid, but essential documentation for:
- General development environment setup (used by IT for onboarding)
- Component specific dev environment setup
- deployment and release process of the software component
- Fundamental API usage (not API reference, unless a project requirement) 
- if component is used by external teams.
- Code documentation
- Docstrings are where the reference API is described.

Most programmers browse code and learn API with their IDE, not with browser.
If browser-oriented reference API is convenient or desirable, generate via standard tools (sphinx/doxygen).
Reduce use of wiki tools such as Confluence/MediaWiki to reduce synchronization burden. Code documentation lives with code.

- Spending excessive amout of time in documenting the code when the design is prone to change. 
The code is the documentation. 
I understand that excessive turnover of the developers may want 
to keep information stored somewhere, 

but it's probably better to focus on keeping competences 
and teams together so that projects are not handed out to some new random person/group every time.
