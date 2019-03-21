---
nav_order: 4
---
# 4 On Documentation

Documentation is often touted as the savior of the software company. The idea
is that documentation carries the knowledge required for anyone to understand
and pick up the software, reducing "bus factor" and allowing reuse. While I
would not call this a fallacy, I might argue that it might become a fallacy
under some constraints. Often, you will hear people complain that "we need
documentation" or "if this was documented the problem would not happen" but I
don't believe it in full.

*More documentation will not solve. Minimal, correct, well-organised, discoverable, and close to the relevant place documentation will.*

Documentation is only as useful as it is
- concise: delivers the right amount of information in the shortest amount of effort.
- correct: outdated information is deceiving and damages trust in the rest of the documentation.
- scoped: is attached as close as possible to the entity it documents, and offers the correct 
  amount of information.
- discoverable: it can be found easily and its existence must be inferred and discovered
  naturally.
- consistent: concepts are clear and well defined, and their definition remains unchanged.
  Established language is respected, rather than reinvented. E.g. if a document is a specification document,
  it should be called as such, not "master plan" or "project strategy".
- straightforward: the more indirection is needed to understand a document, 
  the less usable it is.

These requirements make for good documentation. Violating them leads to heavy,
unfocused documents where understanding is anyone's guess.

Location and organization of documentation is critical for discoverability.

Maintaining a well-organised documentation is a major task that requires discipline.

Documentation also promotes a RTFM attitude within the team, where "everything is in the
documentation". This discourages exchange of knowledge.


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

- word programming
- word burden and red tape
- word itself (bugs), updating the templates, have dumb templates. The Office.
- regulatory vs non-regulatory documentation. difficulty to find it.


- develop common language within team
- poor communicaiton and organization of info
