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
- creation of the software product.
- documentation of the software product.
- testing of the software product.
- handling of the infrastructure to perform testing, possibly hardware.
- handling the strategy for versioning and releases of the software, and their interactions.
- deployment of the software product, either in house, off-site (e.g. with third parties), or in the cloud.
- interaction of the software product with your core business.
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
requirement, failing to organise your runtime will eventually lead to broken
installations with hard to reproduce bugs or random crashes.

You therefore need a proper process in place to manage, build, maintain,
deliver, update, and track your runtime effectively, and ensure that your
company uses your runtime's software packages.

# Creating and maintaining the software

On top of the runtime, you create your software product. Creating software goes
well beyond the writing of code. Code, in fact, can be said to be almost the
trivial part. The surronding infrastructure needed to create production-ready
code is large and pretty much required with no exceptions. The following
components are needed:

- A version control system to keep track of changes and allow developers to modify the code
in an organised and reliable way.
- A bug tracking system to ensure that defects are recorded, tracked, and addressed.
- A process tracking system, to ensure that features are properly recorded, prioritised,
and managed within a team or across teams, as well as managing official releases timelines.
- An IDE that simplifies and provides support for coding, refactoring, testing, and debugging.
- Quality assurance tools such as linting and code review to allow for
  automatic and manual feedback, as well as approval of changes.

As you can see, the amount of infrastructure needed keeps growing, and requires
considerale attention and skills. While some improvisation and liberties can be
taken at a very small scale, even a single developer will eventually need all
of the above.

Creating software will also require support programs, such as sketching
applications to visualise user interface prototypes, and physical objects such
as whiteboards, post-its, screens to show various types of information, from
technical (build status, performance records, failure rates) to management
(process track, burndown charts). 


# Documenting the software

Software is useless to others if not properly documented. A large number of
software packages have gained massive market share also due to an effective and
punctual documentation.  Even if the software is for internal use only,
effective documentation minimises chances of error and delivers transfer of
knowledge from one team to another. In some cases, documentation might be a
legal or regulatory requirement as well, and must comply with these practices.

Documentation in general has different level of scope in software, and is
addressed to different actors:

- the user, who is anybody interested in simply using a given component.
  This might be the end user, in case of an application, or a software developer
  that uses this component for another software
- and the developer, who is interested in developing the component itself.

The user needs to know how to deploy and install either a released or a
development level version of the software. Generally, the user will deploy the
component in an already configured system or environment, which must be clearly
described in the documentation.

On the other hand, the developer needs a lot more details, such as the required
tools and environment for development, how to setup local testing, code
conventions and best practices followed, overall design and code organization,
build scripts, external dependencies and libraries (and the aforementioned
runtime).  When into the code, the developer needs to know details about
subsystems, classes (in particular their interface and state), and functions
(typically their parameters, returned values, side effects and computational
cost)

All of this requires support tools. Inline code documentation can be extracted
to generate reference documents.  Documentation of design needs UML modeling
tools. Documentation must be reachable and searchable, potentially online,
and it must be directly connected to the version of the code it refers to.

# Testing the software

No software can be produced without bugs. Software will need to be tested at
different levels, from individual routines and classes, to their integration,
up to the final application deployment, usage, and functional behavior on all
the targeted platforms. Tools such as unit test runners, mock libraries,
performance evaluation and memory leak detection are needed to ensure quality.
When the software controls physical hardware, testing also requires the
presence of rigs specifically designed to service test operations and emulators.
Hardware testing rigs may require special attention for the testing setup, 
and might require, for example, firmwares specifically designed for testing.

Tests will have to be classified according to different criteria, for example
if they take a long time, or if they require a specific platform or hardware
rig. Tests should be fully automatic, so an additional need might be to
eliminate or work around steps that are supposed to require human interaction
without compromising the nature of the test itself.

# Handling the testing infrastructure

Testing will be executed by different actors, some of them humans, other ones computers.
Typically, the human will run unit tests on its machine to remove trivial mistakes and check
overall soundness of the subsystem it is working on, but in a large system, testing may take
time or required infrastructure that the single developer might not have or be willing to provide.
For this reason, a testing infrastructure takes care of running the tests at various stages of
integration.

This infrastructure must be automatic, reliable and fast. If a user creates a new change,
the infrastructure must provide a quick evaluation of the correctness of the tests associated
to the change with no intervention from the user. Periodically, it also has to execute more complex
tests, dispatching the test execution to the appropriate machine out of a pool
of executors, keeping into account parameters such as:

- machine properties: operating system, memory, graphics adapter.
- process load: assign the execution of testing so that machines are properly balanced
- attached rigs: machines that provide access to hardware rigs should only run tests that are actually using these rigs.
- cost: depending on the testing infrastructure, an excessive availability of executors can increase costs due to licensing terms.

# Handing the network and cloud infrastructure

Every company needs a network, and networks are fragile, require configuration,
protection from attack both from the inside and outside, and automation of common tasks
such as addition and configuration of new hardware, centralised authentication of users
and services, internal and guest wifi access, firewall settings. In addition to the internal
network, cloud services such as AWS need to be considered, setup, administered, and accounted.

# Handling the database and general data storage

Another critical component of the software company infrastructure are databases in their various
implementations and use.
Typically, databases can hold from straightforward data such as addresses of
your customer, to massive datasets about medical data, oil drilling, or
pharmaceutical trial results. Some of these data may be under specific
regulatory requirements. All of them need a backup strategy, because pretty
much all of them are business critical and will disrupt your company if something goes
wrong.  Some of them may need replication to ensure its reliable availability
in case of failures or downtimes of the main server.

Development of software accessing the database needs a platform similar to the
live database for testing before deployment to the production database,
therefore an additional testing database must exist. Similar considerations
about regulatory requirements may apply to this database.

Databases also generally require fine tuned access control, so that only the
relevant parties have access to the contained data.

schema migration strategy, downtime scheduling.

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


