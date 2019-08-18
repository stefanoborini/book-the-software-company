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

Documentation is only useful if it fulfills the following criteria:

- **concise**: delivers the right amount of information in the shortest number of words.
- **correct**: outdated information is deceiving and damages trust in the rest of the documentation.
- **scoped**: is attached as close as possible to the entity it documents, and offers the correct 
  amount of information.
- **discoverable**: it can be found easily and its existence must be inferred and discovered
  naturally.
- **consistent**: concepts are clear and well defined, and their definition
  remains unchanged.  Established language is respected, rather than
  reinvented. E.g. if a document is a specification document, it should be called
  as such, not "master plan" or "project strategy". The documentation is kept
  updated against changes, or written so that changes to the code minimise the
  impact to the documentation.
- **straightforward**: the more indirection is needed to understand a document, 
  the less usable it is.

The take home message of the above points is that documentation should not
waste other's people time.

## 4.1 Concise

Concise documentation addresses the point quickly, takes no diversions, leads
the reader to conclusions through clean, well-defined steps.  When writing some
information, ask yourself: is it relevant for later understanding?  If not,
remove it. 

## 4.2 Correct

Nothing damages trust in the documentation like incorrect information.
"If this is wrong" - asks the reader - "what else can it be?".  Documentation
that outdates quickly is typically relative to code or features that are under
development, so the documentation update process must be connected to the code 
change. Typically, this means that a pull request must address both code and 
documentation.

## 4.3 Scoped

Documentation is part of the software component, and therefore must follow the
same process relative to versioning and tracking of changes. The documentation
must live near the code (e.g. committed in the same repository), not in a
separate document store (e.g. as a docx document on sharepoint)

## 4.4 Discoverable

Location and organization of documentation is critical for discoverability.
Documentation that is not easily discoverable is useless, which means that
proper titles, tags, consistent keywords and a correct hierarchical
classification is fundamental, and must be kept consistent throughout project
renaming, groups formed and dismantled, people quitting and joining.

Companies tend to address the documentation chaos by using an internal search engine,
but unfortunately it's not necessarily the best solution. The problem with a search 
engine is that you must know the question to get answers. Typical phrases that you can
hear in companies with a documentation discoverability issue are

- "I remember we have a document with a picture of the overall design, but I can't find it"
- "Do you know if we have a document that describes who is responsible for that component's maintenance?"
- "There should be a document for it, but I can't find it anymore, because I don't remember which keyword I used to find it."
- "I could not find the document because we always use the acronym, but that document had it in extended form"

Search engines index words, but can't provide effective search functionality for
pictorial representations, or complex concepts. It requires you to know the question,
and ask it right, to get to the answer you need.

On the other hand, information organisation allows to discover the questions
and thus their answers. Moreover, the structure allows people to discover
related knowledge. Unfortunately, there are two fundamental problems with
documentation organisation:

- Maintaining a well-organised documentation is a major task that requires discipline and context.
- Create a proper organisation model is difficult, prone to inconsistencies, and may not fit
  everyone's mental model of the topic.

It is therefore not surprising that the general approach in companies is to
throw the documentation into a big pile and pray to the search engine gods to
save them.

An additional point to consider is the naming convention of the documents,
typically as titles or identification codes. These can be useful and are generally a
must in large companies where documentation proliferates, but may add a layer of indirection
that makes onboarding of new team members harder. It is not clear, for example, that the document
DD-0234 contains the design for the main component of your application. While it's inevitable that
these names will be part of your company lore, it is important that they are kept alive.
For example, if the main component is redesigned, the new design document
should be DD-0234v2, rather than, say, DD-0472.

## 4.5 Consistent

example of writing installation instructions to follow the on-screen instructions. Better longevity.
Periodic refactoring of documentation layout in case of discoverability shortcomings and cleanup of outdated information.
reduce noise by removing old stuff.

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

later If something does not propel 
Concise, correct, well-organised, discoverable, and close to the
relevant place documentation will.** 

Enforce consistency of API naming, least surprise principle, proper naming, orthogonal behavior, minimalistic code, use of well-understood design patterns. Train as appropriate. 


## How we write

The second point is that documentation promotes a culture within the
team where the answer to every question is "it's in the documentation". 
This discourages fast exchange of knowledge and a culture of improving
communication skills via a high bandwidth two-way medium. Of course one 
has to weight this factor against scalability, so the proper caveats 
must be considered.


A separate but related issue is the quality of documentation. Not everybody is able to
write quality documentation. I developed overall criteria to assess the quality of documentation

- if a picture requires a textual explanation, it is not working.
- the language of presenting information (top to bottom diagrams, pointed lists, flowing information).


# Regulatory documentation

Regulatory documentation has an important role in some industries.  Most of the
times, this documentation is technical but need to be handled, reviewed, and
commented by non-technical people. 

For some regulatory documentation, an additional requirement applies to support
traceability of attribution and changes, typically involving a sign off process. 
We will not explore this further, as it ties with regulatory requirements that 
might be different depending on the targeted market.


- word programming
- word burden and red tape
- word itself (bugs), updating the templates, have dumb templates. The Office.
- regulatory vs non-regulatory documentation. difficulty to find it.


- develop common language within team
- poor communicaiton and organization of info


## Types of documentation required:

The requirements given above aim at delivering good documentation. Violating these
requirements lead to heavy, unfocused documents with poor value. They also apply to all forms of
documentation: 

- code comments, which includes actual comments as well as any documentation strings for API, functions, classes and properties.
- tutorials, reference, installation guides
- troubleshooting
- regulatory requirements documentation
- internal guides (typically wiki pages)


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

- big concepts need a high level picture. No space to see it or poor tools to represent them.
