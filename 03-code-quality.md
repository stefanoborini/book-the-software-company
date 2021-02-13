---
nav_order: 3
---

# 3 On code quality

In this section, we are going to discuss code quality. We will discuss how to establish, maintain
and promote it, as well as evaluating its cost against the evolving backdrop of the market and
the company's goals. The golden rule to establish within the company is to strive for code quality
as a product in its own right.

Code quality is probably the source of most attrition and loss of productivity
in the software company, and for good reasons: it has strong notes of
subjectivity, potentially sparking inconsistencies to be dealt with, as well as
feud wars between developers of different factions, but these notes of
subjectivity often have a foundation on sensible and objective strategies to
minimise mistakes and maximise extensibility in response to business pressure. 
They are not for naught, and should never be dismissed. Only managed.

In fact while code quality may have subjective connotations, lack of it
has objective and tangible effects on the costs associated to software
development, which is why poor code quality is often referred as *technical debt*.
If code quality degrades, the company will eventually reach a state of
technical bankruptcy. Your developers will spend all of their working time
fighting with the inconsistencies, bad choices, irrationality, unexpected side
effects of your code, unable to do any progress toward the shipping of the 
features that bring money into the business. 

When this happens, there's no way back. Bad code will pile and compound over
bad code. Code complexity will arise to fight human induced complexity, leading
to an unstable, frail codebase where nothing can be refactored, because too
many hacks and counter-hacks to compensate for the hacks will create a
super-system of dependencies and unexpected behaviors that only a focused,
dedicated time investment can disentangle. You will never get clearance to
proceed on such tasks. Business will say no, because the net benefit is
negative: at the end of the journey, you will have the exact same features for
a massive cost. It's cheaper to just kick the can yet another time. Business
does not see the internals. It only sees the resulting features. It does however
see that a feature that may be trivial to implement or required to close a sale
will require months rather than weeks to be implemented, but you can be
guaranteed they will not blame the problem on the lack of budgeting that
allowed this mess to be generated in the first place.

Bad code, poorly designed interface and classes will haunt you forever.  Their
consequences have far reaching implications that are hard or even impossible to
fix, especially if these APIs become the backbone of your business. Most of
these APIs were initially dismissed as "a prototype" or "just internal tool",
but the reality of development is that an APIs, be it internal or external,
is a dependency that other components will have.  Occasionally, the business
will pressure developers and managers into releasing to the public (either
general or to internal teams) APIs that never received the proper design attention
and polish.  Once the gates are open, there's no easy turning back, because the
general customer now depends on these poorly designed APIs, and any change will
have to be managed with a deprecation strategy. Needless to say, this is
additional workload that will never be prioritized.  The API will remain
broken, and the problem will escalate.

Some companies, notably those in regulated industries, have requirements for
compliance to standards, testing, code styleguides, design patterns, uniformity
of behavior, consistency of interface, and adherence to well known best
practices and idioms. Unfortunately, these requirements are often addressed by
requiring traceability, rather than code investigation, through massive amounts
of documentation to support changes. While this is commendable and certainly
required, it leaves developers with little to no time to actually address the
issue at the code level, either because of lack of time, or because fixing the
problem for good would require to touch so much code that the amount of
documentation to justify it would pile higher than the roof, reducing the
available time even more.

With the above statements, I hope I convinced you it's important to sort out
code quality immediately, aggressively and correctly, because complex
refactoring is generally unfeasible. I've seen many companies, and not in 
a single one refactoring practices were effectively and seriously undertaken.

## Use of inferior tools impacting code quality

Code quality can be deeply compromised by inferior tools, either directly or
indirectly. For example, use of an inferior review tool can make the review
process slow and clumsy, as well as not give any guarantee that what is merged
is actually what gets reviewed. Poor IDEs without automatic code formatting,
refactoring tools, or type checking can increase the amount of errors and
inconsistencies. Using inferior, poorly designed third party libraries can
force the propagation of these bad practices (for example, by developers
imitating or copying this code), the introduction of workarounds, or writing
lots of code to address the shortcomings of the library or toolkit in use. 

Proper tools must therefore be considered on all aspects, from infrastructure
to coding to testing. This is not only a business factor (good tools tend to be
expensive) but also a developer factor (developers tend to have their own tools
and stick with them). In general, it is recommended to leave the IDE to the
preference of the developer, because proficiency in the IDE is the most
important factor in developer productivity. Other tools, such as review tools,
version control, continuous integration systems, the choice is more open and
a proper assessment should be done. There's plenty of products, both opensource
and commercial, that are technically excellent and should be chosen according to
ease of use, integration with other tools, cost, and last but not least popularity.
In fact, a popular tool is more likely to be known by new hires, thus reducing
onboarding costs, and any problem that may arise with the tool is likely to have
been solved by someone and is just a google search away.

## Quality of code layout

Code is generally not contained in a single file. Instead, it is subdivided in files and folders
according to some schema. A proper choice of this schema is fundamental for two reasons:

- Improving discoverability: Code layout that groups routines and classes into
  properly named files and directories makes the discovery of existing
  functionality easier. In other words, a developer has easier time finding a
  functionality they need, resulting in faster development and reduced chance of
  re-creating what is already available..
- Removing phantom dependencies: Properly organised code tends not to have "phantom 
  dependencies", that is, dependencies that exist not because of a real,
  model-driven dependency between entities, but because classes or functions are
  organised improperly. These phantom dependencies are generally solved by moving
  these functions and classes "where they belong"

Therefore, proper naming of files and directories, and proper code
organisation across the files is a factor to consider when aiming for code
quality.

When it comes to naming modules, some names are a louder signal that poor code
organisation is present in the codebase. The most prominent is probably
"utilities" or "utils". A module with such name is guaranteed to become a catch
all for any functionality, from string parsing to network connectivity. These
modules tend to grow to unreasonable sizes, creating poorly discoverable
entities with a large list of imports.  

Another name that raises alarms is "globals", a module where global variables
(generally for configuration) are stored. This module also tends to attract a
mixture of unrelated information, as well as becoming a single entity that gets
imported or included by many, if not all, of the files in your project. Never
use these names. General purpose routines should be classified at least
according to the topic they handle, for example networking, security, or string
manipulation.

A recommended strategy when choosing a layout is not to reinvent it if it
already exists: many languages or development frameworks use a conventional and
well established layout, as well as conventional names for the various modules
and the entities contained therein. For example, React projects typically use a
split between Components and Containers. Django separates models and views in
specific subpackages. File names are generally chosen to match the main class
contained in the file. Using these established conventions promote clear
communication of intent to other coders via a shared vocabulary of terms, and
is therefore strongly encouraged.

No matter the final choice, it is important not to lose focus of the two main
driving forces: discoverability and removal of phantom dependencies. Excesses
can be bad in both direction, and being overly specific on a layout convention
can be as detrimental as the lack of it.

## Quality of code formatting and ordering

Entering into the organisation and layout of the code itself within the file,
there are also important rules to follow. These rules once again focus on 
human factors.

A file should generally contain one main class plus a handful of support
classes, routines, and data in support to the main class. This kind of layout
is generally favored to ensure the file remains small and easy to navigate. A
large file containing many unrelated classes and functions, in fact, can become
a problem for the following reasons:

- A particular identifier string can be used in many different classes. Running a text search
  for this identifier will possibly match outside of the class you are
  refactoring or debugging, making these tasks harder.
- The file will contain many potentially unrelated or loosely related functions
  and classes, each with their own potential dependencies on other modules.
  When imported by external code, having a large module will trigger these
  imports, leading to potentially unnecessary dependencies and side effects.
- A large file is most likely to lead to merge conflicts if two or more developers
  are working on it.
- Finally, a large file makes it harder to see how the various entities are organised
  inside it.

The latter point, in particular, is conventional to communicate importance and intent 
of the various parts. A typical layout is:

- Standard imports at the top
- followed by imports of modules that are part of the current code base.
- Followed by the main public class this module contains and exports (AKA the "linchpin class") 
- Followed by public functions this module exports
- Followed by private (internal only) classes and functions.

While this common convention is a mild convention, it helps in keeping the code organised and
communicate intent, putting main, front facing functionality before internal one.

---------------------

## Quality of API documentation

## Accuracy of design of routines, classes, modules.

## Accuracy of design of interface elements, such as APIs, web APIs, file formats.


## Establishing a culture of quality

%s methodology for manufacturing should be applied to software as well.
5s is a workplace organisation strategy that focus on the following points:

- Sort: 
- Set in order:
- Shine
- Standardise
- Sustain:

## Establishing standards

- common code conventions and unwritten rules.
- implement things locally, then cleanup and promote globally.

## Code ownership policies

- code ownership: tragedy of the commons, bystander effect.
6. Do you have loose, but full code ownership?

Any software developer or manager has his own opinion on this one. Code ownership
has always been a hot topic. Those in the field of Agile tend to favor collective code ownership.
I propose that every brain works in a different way, and establishes different
rules and conventions to build something. Those who claim shared code ownership encourage sharing of
these conventions, but in practice, for large codebases, these conventions are too many.
Some redundancy is good, but in practice you should leave the code in the hands and brain
of the person who built it first. He knows the rules of its own universe, he aderes to them
and is hopefully more consistent than a bunch of people acting on it.

Coding is not wikipedia. Wikipedia does not rely on logic to build a meaningful narrative.
Coding requires correctness and logical consistency.

- code conflicts arise from poor management. 
- schizophrenic development: many different brains with no clear, uniform mindset lead to confusing, schizophrenic code.

## Quality of internal tools 

Any technology product builds on previously established tools. In the startup phase,
these tools are external ones, either opensource or commercial products. As the startup
grows, so does the need for specialized tools, such as a deployment infrastructure, a
specialized library for core business tasks, classes and functions to reduce boilerplate,
documentation. You must invest in these tools because they increase the velocity of
development, yet investment in these tools is considered waste because it does not generate
revenue. Truth is, your developers are customers too, and specifically they are customers 
that consume money. The more they have to fiddle with your own broken tools, the less
efficient they will be. Invest in your tools, or your ability to deliver will be crushed 
under their ineffectiveness.


## Make it, use it, bin it

Sooner or later, something of your hardly implemented solutions will be implemented better
by some external product. It is time to move away from your internal product. You are delegating
problems. I've seen plenty of times when stubborn developers clinged to their own file format
when HDF5 offered the experience of a full research team whose goal is to deliver the most
performant file format for scientific storage. Your business is in developing scientific
software, not in developing file formats. Ditch your file format. It made sense 10 years ago,
now it's time to move on.

This is also important because people working for you are not only here for the money. They are
also here to learn new techniques. Using internally developed tools does not enrich their curriculum,
and if they don't want to become irrelevant on the job market, they are not going to like it.

- write code that is overly complex in response to needs for genericity that is not there, in the name of flexibility, but end up being inflexible due to the complexity of the resulting design.
- Complexity for the sake of complexity. Inability to keep things simple and lean.

- implementing the same things twice in parallel 
- solving big problems without addressing user-centric fundamental (e.g. installation)

# Disorganized notes 

Code quality must be analysed under various aspects:

- Quality of code layout 
- Quality of code formatting and ordering
- Quality of API documentation
- Accuracy of design of routines, classes, modules.
- Accuracy of design of interface elements, such as APIs, web APIs, file formats.

