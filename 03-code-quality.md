---
nav_order: 3
---

# 3 On code quality

Code quality may be subjective, but the hard truth is that there's good code, and bad code. Unfortunately, 
there is no metric for taste, but there are metrics on other factors, such as compliance to

- standards
- code styleguides
- design patterns
- uniformity of behavior
- consistency of interface
- adherence to well known practices and idioms.

You should sort out code quality immediately.

, because refactoring, the practice of cleaning up code, is generally
unobtainable. I've seen many companies, and not in a single one refactoring was effectively practiced. The 
general motivation for this 

If code quality degrades you will eventually reach a state of technical
bankruptcy. Your developers will spend all of their working time fighting with
the inconsistencies, bad choices, irrationality, unexpected side effects of
your code, unable to do any progress. When this happens, there's no way back.
Bad code will pile and compound over bad code. Code complexity will arise to
fight human induced complexity, leading to an unstable, frail codebase where
nothing can be refactored, because too many hacks and counter-hacks to compensate
for the hacks will create a super-system of dependencies and unexpected behaviors
that only a focused, dedicated time investment can disentangle. You will never get
clearance to proceed on such tasks. Business will say no. 

Unfortunately, bad code, poorly designed interface and classes will haunt you
forever.  Their consequences have far reaching implications that are hard, if
not impossible to fix, especially if these APIs become the backbone of your
business. Most of these APIs were initially dismissed as "a prototype" or "just
internal tool", but the reality of development is that internal APIs never stay
internal, and the business will pressure developers and managers in releasing
to the public (either general or to internal teams) entities that never received
the proper design and polish required for a proper software tool or application.
Once the gates are open, there's no turning back, because the public now depends on
these poorly designed APIs, and any change will have to be managed with a deprecation
strategy. Needless to say, this is additional workload that will never be prioritized.
The API will remain broken, and the problem will escalate.

# Inferior tools

Code quality can be deeply compromised by inferior tools, either directly or
indirectly. For example, use of an inferior review tool can make the review
process slow and clumsy, as well as not give any guarantee that what is merged
is actually what gets reviewed.

Using inferior, poorly designed third party libraries can force the propagation
of these bad practices (for example, by developers imitating or copying this
code), the introduction of workarounds, or writing lots of code to address the
shortcomings of the library or toolkit in use. 

# On code organisation

Code is generally not contained in a single file. There are general practices
to organise code so that is follows these requirements:

- discovery: Code layout that groups routines and classes into properly named files and directories makes the discovery of 
  functionality easier. A developer has an easier time finding the functionality that is relevant for his or her task,
  resulting in faster development and reduced chance of re-creating existing functionality.
- isolation: Properly organised code tends not to have "artificial dependencies", that is, dependencies that exist not because
  of a real, model-derived dependency between entities, but one that exists
  just because classes or functions are organised improperly. These dependencies are generally solved by moving these functions
  and classes "where they belong", but this may break imports from external code.

There are names for modules that are a signal and a trap for proper code
organisation, the most prominent is probably "utilities". A module with such
name is guaranteed to become a catch all for any functionality, from string
parsing to network connectivity. These modules tend to grow to unreasonable
sizes, creating poorly discoverable entities with a large list of imports.
Another one is "globals", where global variables (generally for configuration)
are stored. These also tend to attract a mixture of unrelated information, as
well as becoming a single entity that gets imported or included by many, if not
all, of the files in your project. Never use these names. General purpose routines
should be classified at least according to the topic they handle, for example networking,
security, or string manipulation.


- implement things locally, then cleanup and promote globally.
- common code conventions and unwritten rules.
- code ownership: tragedy of the commons, bystander effect.


12. Do you keep up with technology?

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

2. Do you invest in your own tools?

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

- write code that is overly complex in response to needs for genericity that is not there, in the name of flexibility, but end up being inflexible due to the complexity of the resulting design.
- Complexity for the sake of complexity. Inability to keep things simple and lean.

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
- implementing the same things twice in parallel 
- solving big problems without addressing user-centric fundamental (e.g. installation)

# Disorganized notes 

%s methodology for manufacturing should be applied to software as well.
5s is a workplace organisation strategy that focus on the following points:

- Sort: 
- Set in order:
- Shine
- Standardise
- Sustain:
