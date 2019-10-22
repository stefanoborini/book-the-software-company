---
nav_order: 1
---
# 1 The Software Company

As we established in the introduction, if your company creates software of any
kind, from basic scripts to complex applications, it is a software company.  It
is irrelevant that its core business is not software. While this seems to be a
trivial point to make, my personal experience with multiple companies from
manufacturing to pharmaceuticals points at how often this fundamental concept
is downplayed.

A software company carries a set of requirements to meet the goals of handling
software. You need to handle the software production chain, which generally can
be represented as follows:

- handling of the runtime the software depends on (compilers, libraries etc).
- software, its creation and its maintenance
- documentation of the software
- testing of the software
- handling of the infrastructure to perform testing, possibly hardware.
- versions and releases of the software, and their interactions.
- deployment of the software, either in house, off-site (e.g. with third parties), or in the cloud.
- interaction of the software with your core business
- interaction of software development process with your core business process.

We will investigate each of these points in more details.

# Handling the runtime

When you want to develop some software, you have to rely on external components
of various nature, such as interpreters, compilers, or libraries. These
components are either commercial products or opensource, and have different
level of quality, documentation, bug tracking and user support. They might be
pre-built as a binary, or need to be built from source within your company,
therefore needing a well-known, reproducible build chain to ensure the quality
and reliability of the resulting artefact. 

If you want a running product, you need to take care of your runtime as if it
were a product in itself. You must keep track of its changes, its affecting
bugs, any backward compatibility breakages, platform inconsistencies or
differences and so forth. This is not only a loose recommendation, it is an
actual regulatory requirement in some industries, and a massive one in some
cases where human life may be in danger. Even when not a regulatory
requirement, not organising your runtime will eventually lead to broken
installations with hard to reproduce, random crashes, or unexpected bugs
appearing or reappearing.

You therefore need a proper process in place to manage, build, maintain,
deliver, update, and track your runtime effectively, and ensure that your
company uses your runtime's software packages, and not else.

# Creating and maintaining the software

On top of the runtime, you create your software. Creating software goes well beyond the
writing of code. Code, in fact, can be said to be almost the trivial part. The surronding 
infrastructure needed to create production-ready code is large and pretty much required with
no exceptions. The following components are needed:

- A version control system to keep track of changes and allow developers to modify the code
in an organised and reliable way.
- A bug tracking system to ensure that defects are recorded, tracked, and addressed.
- A process tracking system, to ensure that features are properly recorded, prioritised,
and managed within a team or across teams, as well as managing official releases timelines.
- An IDE that simplifies coding and provides support during coding, refactoring, testing, and debugging.
- Quality assurance tools such as linting and code review to allow for
  automatic and manual feedback, as well as approval of changes.

As you can see, the amount of infrastructure needed keeps growing, and requires
considerale attention and skills. While some improvisation and liberties can be
taken at a very small scale, even a single developer will eventually need all
of the above.

Creating the software will also require support programs such as sketching
applications to visualise user interface prototypes, and physical objects such
as whiteboards, post-its, screens to show various types of information, from
technical (build status, performance records, failure rates) to management
(process track, burndown charts). 


# Documenting the software

Software is useless if not properly documented. A large number of software packages 
have gained massive market share also due to an effective and punctual documentation.
Even if the software is for internal use only, effective documentation minimises chances
of error and delivers transfer of knowledge from one team to another. In some cases,
documentation might be a legal or regulatory requirement as well, and must comply with these
practices.

Documentation in general has different level of scope in software, and is addressed to different
actors. Typically the actors are the user, who is interested in using a given component,
and the developer, who is interested in developing it. The first needs to know how to deploy
and install either a released or a development level version of the software. Generally, the user
will deploy the component in an already configured system or environment, which must be clearly
described in the documentation.

On the other hand, the developer needs a lot more details, such as the required tools and environment
for development, how to setup local testing, code conventions and best practices followed, overall design and
code organization, build scripts, external dependencies and libraries (and the aforementioned runtime).
When into the code, the developer needs to know details about subsystems, classes (in particular their interface
and state), and functions (typically their parameters, returned values, side effects and computational cost)

All of this requires support tools. Inline code documentation can be extracted
to generate reference documents.  Documentation of design needs UML modeling
tools. Documentation must be reachable and searchable, potentially online,
and it must be directly connected to the version of the code it refers to.

# Testing the software

No software can be produced without bugs. Software will need to be tested at different
levels, from individual routines and classes, to their integration, up to the final application
deployment, usage, and functional behavior on all the targeted platforms. Tools such as unit test
runners, mock libraries, performance evaluation and memory leak detection are needed to ensure quality.
When the software controls physical hardware, testing also requires the presence of rigs
specifically designed to service test operations. 

# Handling the testing infrastructure

- A test infrastructure that verifies the functionality and soundness of the committed code to ensure
quality.

# Handing the network and cloud infrastructure

databases (production, testing) 

# Version and release the software
- A build infrastructure that creates software releases for final delivery.
- Version planning and release management to organise official releases

# Deploy the software

- Storage of built code, also known as artifacts.

creating installation scripts that are adequate for the target platform, smooth out
unexpected circumstances and differences in the target machine (proxy, antivirus, 
ACL).

# Handle deprecation, upgrades and migration.

of file formats, database schema changes.

# Interaction of the software with the core business

- In some cases, infrastructure for measuring performance, logging of events,
  and watchdogs to ensure immediate response in case of failure.

# Interaction with the development process with the core business process


