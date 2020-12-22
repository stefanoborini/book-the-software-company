---
nav_order: 1
---
# 1. The Software Company

As we established in the introduction, if your company creates software of any
kind (from basic scripts to complex applications) it is a software company.  It
is irrelevant that its core business is not software. 

While this seems to be a trivial point to make, my experience with multiple
companies (ranging from manufacturing to pharmaceuticals) points at how often
this fundamental concept is downplayed. 

A software company carries a set of additional needs to meet the goals of handling
both the software product and the software production chain, which generally
can be represented as follows:

1. creation and maintenance of the runtime the software depends on (compilers, libraries etc).
2. creation and maintenance of the software development infrastructure.
3. creation of the software product
4. documentation of the software product.
5. testing of the software product.
6. handling of the testing infrastructure, including hardware fixtures required for such task.
7. handling network, databases, file storage, cloud infrastructure.
8. handling the strategy for versioning and releases of the software, and their interactions.
9. deployment of the software product, either in house, off-site (e.g. with third parties), or in the cloud.
10. interaction of the software product with the core business product.
11. interaction of software development process with the core business process.
12. interaction of software product with third party suppliers.
13. interaction of the software product with legal or regulatory requirements.
14. long term support of the software product.
15. deprecation of the software product.

We will investigate each of these points in more details.

## 1.1. Creation and maintenance of the runtime

When you want to develop some software, you have to rely on external components
of various nature, such as interpreters, compilers, libraries, supported
operating systems. All together, these components form your runtime. 
Your software product has direct or indirect dependencies against
this runtime, and cannot run without it.

The components forming the runtime are either commercial products or
opensource, and have different level of quality, documentation, bug tracking
and user support. They might be pre-built as a binary, or need to be built from
source within your company, therefore needing a well-known and reproducible
build chain to ensure the quality and reliability of the resulting artefact. 

If you want a running software product, you must take care of its runtime as if
it were a product in itself. You must keep track of its changes, its affecting
bugs, any backward compatibility breakages, platform inconsistencies or
differences and so forth. This is not only a loose recommendation, it is an
actual regulatory requirement in some industries, and a massive one in some
cases where human life may be in danger. Even when not a regulatory
requirement, failing to organise your runtime will eventually lead to broken
installations with hard to reproduce bugs or random crashes.

You therefore need a proper process in place to reliably manage, build, maintain,
deliver, update, and track your runtime components effectively, and ensure that
the runtime is properly deployed and usable by all interested parties.

## 1.2. Creating and maintaining the software development infrastructure

Creating software goes well beyond writing code. Code, in fact, can be said
to be almost the trivial part. The surrounding infrastructure needed to create
production-ready code is large and pretty much required with no exceptions. The
following components are needed:

1. A version control system to keep track of changes, allow developers to modify the code
   in an organised and reliable way.
2. A bug tracking system to ensure that defects are recorded, tracked, and addressed.
3. A process tracking system, to ensure that features are properly recorded, prioritised,
   and managed within a team or across teams, as well as managing official releases timelines.
4. An IDE that simplifies and provides support for coding, refactoring, testing, and debugging.
5. Quality assurance tools such as linting and code review to allow for
   automatic and manual feedback, as well as approval of changes.

As you can see, the amount of infrastructure needed keeps growing, and requires
considerable attention and skills. While some improvisation and liberties can be
taken at a very small scale, even a single developer will eventually need all
of the above.

# 1.3. Creation the software product

Before coding can take place, some effort must be invested in understanding how
the application should behave, what kind of operations and workflows should
support, and which algorithms are required. These concerns typically need to be
tracked, split, and assigned to different developers with different skillsets
to maximise efficiency and implementation speed, while minimising code
conflicts (when two developers modify the same code for different reasons) 
and communication overhead among developers.

Creating software will also require support programs, such as sketching
applications to visualise user interface prototypes, as well as physical
objects such as whiteboards, post-its, screens to show various types of
information, from technical (build status, performance records, failure rates)
to management (process track, burndown charts). 

An effective IDE is a paramount requirement to achieve maximum effectiveness.
Developers spend years honing their knowledge of various parts of the
programming environment, and the IDE is probably the most important. Through
the IDE, a developer has access to the code, its layout, quick access to the
documentation, debugging, performance tools, interactive linting and error
checking, refactoring tools, and much more. These tools can reduce the time 
to accomplish some tasks that would take hours down to mere seconds.

# 1.4 Documentation of the software product

Software is useless to others if not properly documented. A number of software
packages have gained massive market share also thanks to a comprehensive and
punctual technical documentation. Even if the software is for internal use only,
effective documentation minimises chances of error and delivers transfer of
knowledge from one team to another.

Documentation in general has different level of scope, depending on the final
target: 

- the **User**, who is anybody interested in simply using a given software component.
  This might be the end user, in case of an application, or a software developer
  that uses this component within another software product.
- the **Developer**, who is interested in modifying the component itself.

The User needs to know how to deploy and install either a released or a
development level version of the software. Generally, the User will deploy the
component in an already configured system or environment, which must be clearly
described in the documentation.

On the other hand, the Developer needs a lot more details, such as the required
tools and environment for development, how to setup local testing, code
conventions and best practices followed, overall design and code organization,
build scripts, external dependencies and libraries (and the aforementioned
runtime). The Developer needs to know details about subsystems, classes (in
particular their interface and state), and functions (typically their
parameters, returned values, side effects and computational cost)

All of this requires support tools. Inline code documentation can be extracted
to generate reference documents. Documentation of design needs UML modeling
tools. Documentation must also be reachable and searchable, potentially online,
and it must be directly connected to the version of the code it refers to.

# 1.5 Testing of the software product 

No software can be produced without bugs. Software will need to be tested at
different levels, from individual routines and classes, to their integration,
up to the final application deployment, usage, and functional behavior on all
the targeted platforms. Tools such as unit test runners, mock libraries,
performance evaluation and memory leak detection are needed to ensure quality.
When the software controls physical hardware, testing also requires the
presence of testing rigs specifically designed to service test operations and
emulators. Hardware testing rigs may require special attention for the testing
setup, and might require, for example, firmwares specifically designed for
testing.

Success of tests must be quiet. A successful execution should not notify the
developer, and the resulting log should be compact and minimal.
Therefore, appropriate capturing of output must be performed, and eventually
distilled to pinpoint the probable cause of failure. Tests should also
ensure that the testing system is left in a state that is correct and ready to
operate again, regardless if they succeed or fail.

When test fails, the failure must be:

- **reproducible**: tests must be written so that they ensure the failure is visible at every new invocation. Lack of reproducibility may indicate both a code bug, or a poorly implemented test.
- **precise**: the failure must indicate exactly where a problem has been found.
- **punctual**: the failure reason must be clear.
- **immediate**: the delay between the developer committing the code and the tests to report the error must be as short as possible.
- **noisy**: the failure must be obvious, and produce as much information as possible in order to understand the context that generated the failure.

To reduce confusion among developers and excess of inbox noise, only the person
involved in the failure should be notified of it. 

Tests will have to be classified according to different criteria, for example
if they take a long time, or require a specific platform or hardware
rig. They should be fully automatic, so an additional need might be to
eliminate or work around steps that are supposed to require human interaction
without compromising the nature of the test itself.

Typically, the tests will be executed with different frequencies according to
the above classification. Short, focused unit tests and integration tests may
be performed once per commit or once per development branch. Longer tests may
be executed every night, or as often as possible in a queue.

All the above requirements are addressed through proper infrastructure, proper
analysis of the tests cost and benefits, and good programming practices.

# 1.6. Handling of the testing infrastructure

Testing will be executed by different actors, some of them humans, other ones computers.
Typically, the human will run quick unit tests on its machine to remove trivial mistakes and check
overall soundness of the subsystem it is working on, but in a larger system, testing may take
time or required infrastructure that the single developer might not have or be willing to provide.
For this reason, a testing infrastructure takes care of running the tests at various stages of
integration.

This infrastructure must be automatic, reliable and fast. As said above, if a
user creates a new change, the infrastructure must provide a quick evaluation
of the correctness of the code with no manual intervention from the user.
Periodically, it also has to execute more complex tests, dispatching the test
execution to the appropriate machine out of a pool of executors, keeping into
account parameters such as:

- machine properties: operating system, memory amount, graphics adapter.
- process load: assign the execution of testing so that machines are properly balanced
- attached rigs: machines that provide access to hardware rigs should only run tests that are actually dependent on these rigs.
- cost: depending on the testing infrastructure, an excessive availability of executors can increase costs due to licensing terms.

# 1.7 Handing network, databases, file storage, cloud infrastructure

Every company needs a network, and networks are fragile, require configuration,
protection from attack both from the inside and outside, and automation of common tasks.

Typically, the following tasks will be crucial:

- addition, configuration and removal of new hardware, either server, developer laptops, or other departments' laptops.
- centralised authentication of users and services
- internal and guest wifi access
- firewall settings
- internal network routing
- setup of VPN for employees that need to work from remote, and among company branches.
- setup and maintenance of employees' smartphones
- setup and configuration of cloud services such as AWS
- setup and configuration of watchdogs to verify availability of services, and
  notify the relevant person in case of downtime.

The key characteristic for network management is heterogeneity, and with it
comes the need for specialised training and impedance mismatch between
technologies that require custom solutions and scripts. Regulatory requirements
and legal obligations may add more complexity to the administration of the
network, in particular when it comes to confidentiality, data protection, and
auditing.

Another critical component of the software company infrastructure is the database
in its various implementation and use. Data are often an absolutely business critical 
component, and storage of this data requires appropriate tools. Typically,
databases can hold from straightforward data such as addresses of your
customer, to massive datasets about medical data, oil drilling, or
pharmaceutical trial results. 

To ensure that the company's data is safe even in case of hardware failure or accidental
deletion or corruption, these databases need a backup strategy, because pretty
much all of them are business critical and will disrupt your company if
something goes wrong. Some databases may need replication to ensure its 
availability in case of temporary failures or downtimes of the main server, or to
increase performance.  

Finally, development of software accessing the database will need a "pre-production" 
copy of the live database to test new releases of the software before the final "production" 
deployment. Absence of a "pre-production" database would force the developers to put
untested software on live data, with potentially nefarious consequences in case of bugs.

Like for network, similar considerations about regulatory requirements may
apply to databases, which need appropriate authentication and authorization
mechanisms to ensure that confidential data is not leaked, and only the
relevant parties have access to the contained data.

Finally, an appropriate strategy must be in place for schema migration in case
of changes in the stored data, as well as appropriate downtime scheduling to minimise
disruption of operations.

# 1.8. Handling the versioning and release of the software

Software development moves from release to release, and coordination of the release process
is fundamental to keep order. THe release process must be reproducible and as automatic as possible.
Ideally, every new build that passes tests is a new release that is ready to be used.

Creating a release requires both human and machine support. Machines need to be
set up to build the software and create the releaseable entity, typically on
multiple platforms. Once the build process is performed, the created release is
deployed to a reachable area, such as an artifact storage, where it's made
available for the final smoke test of deployment, either automated or manually
driven. 

Once the releaseable entity is created and tested, humans need to be involved
for both technical and business tasks: 

1. A decision must be taken about the new version number, typically in agreement to semantic versioning guidelines.
1. Release notes must be written, collecting the changes added to the new version.
2. The version control system revision must be tagged on the build corresponding to the release.
3. The final releaseable entity must be deployed somewhere accessible to the interested parties.
4. Interested parties must be notified about the new version, where it can be found, and how it can be installed.

# 1.9. Deploy the software

After release, the software must be deployed, either manually or automatically.
In general, the software is first uploaded on some form of storage endpoint,
which can vary between the trivial webpage, to a more powerful artifact
storage.  Regardless of the storage solution, deployment is the final step that
brings the software product onto the customer's computer. 

Interested parties may now act on the release, typically upgrading, and
potentially incurring in unexpected problems. Therefore, some care needs to be
taken when releasing. For example, releases should not be performed before
festivities or weekends, in order not to leave customers without support in
case of issues. If the released entity is a dependency of another software
product, this software's build process must now include the updated dependency. 

One important distinction is between web applications, where the deployment
happens on computers controlled by the company, and desktop applications, where
the deployment happens on machines that the company generally does not control. 

In the first case, the deployment happens following the procedure for the cloud
or service provider of choice, and might require an intricate coordination between the
development team and the DevOps team to deploy the new component without
compromising the current network of services.

For the second case, heterogeneity is the major problem of these deployments,
and issues may emerge due to interaction of the software with old operating
systems versions, specific hardware configuration, presence of enhanced
security policies, firewalls, antiviruses, or unorthodox setups. These unexpected
circumstances will inevitably lead to support requests and bug reports that
will form the bulk of the issues for the next patch release.

Instances where the company controls desktop machines do exist, but they tend
to be limited to those cases where the company deploys a turnkey solution with
a standardised environment, and preserves full control of the machine through
its lifetime. A typical scanario is a machine controlling high end hardware
(such as a robot or CNC machine), or machines used to assist the operations of
departments of the company itself.

# 1.10. Handle interaction of the software product with the core business process

Additional software may be required in support of the main business product.
For example, the company may need to monitor its product after sale via
event logging, telemetry, usage statistics and watchdogs to ensure immediate
assistance is dispatched with the right replacement parts in case of failure,
notification of reduced performance, or unexpected behavior from software
components deployed internally or externally to the business. 
The infrastructure needed to handle the above requirements must
be maintaned and made reliable across timezones and patterns of use.

Businesses reorganise, extend their product, and change their processes. Some
software may be influenced by these changes and may need to be updated. 
This is generally addressed by improving the software, but this is not always
be possible because of lack of time from the development team compared to the
existing mismatch between the new process and the old use case defined by the
software.  Typically this is addressed by "bending" the use
of the old software to address the new business need, a process that may
generate unintended consequences, corrupted information, dishomogeneous or
non-sensical data, strong dependency on internal conventions, with meta
information generally in data fields not meant to contain data (such as
comments). The consequence is that code consuming this data must now deal
with a much more complex data layout, where a simple typo can lead to unpredictable
results.

# 1.11. Handle interaction between the software development process and the business process.

Another important point is the integration of the software development
lifecycle with the rest of the business, especially when the business product
has high lead times (as in the case of mechanical and electronic products), or
has strict regulatory requirements, such as in the case of medical or
aeronautical industry. Electronic or mechanical support for a feature might
come after a few months of CAD/EDA work, manufacturing, and physical
assembling, while software support for the added feature can in some cases be
ready within a week or two.  However, software development might need the real
hardware to test and evaluate the functionality, and will in fact act as the
entry point for further testing of the whole feature not only at the software
level, but at the electronic and mechanical level. Correct prioritization and
scheduling must be organised to handle the different development cycles and
process heartbeats of each division within the company.


# 1.12. Interaction of the software product with third party entities.

Third party entities can have deep consequences on the software product and
process. Typically these third parties are either part of the "input"
(consultants, external software vendors) or the "output" (e.g. suppliers that
need the company's software, for example to quality control the deliverable
before it is shipped to the company).

Input third parties such as consultants have a direct effect on the software
product.  They have been involved to develop a particular application or
subsystem, for example.  These consultants can achieve large amount of results
fast but leave the company after their expertise is being used. The company
inherits their contribute and needs to support it without having any expertise
in the methodology nor the code, all while being accountable by the rest of the
company is something goes wrong.

External vendors normally provide a well defined software product, often
together with a maintenance or support contract to fix bugs or provide
immediate help in case of unexpected behavior of their software. The use of
their product makes the company fully dependent on the continued use of this
product, and this can have major consequences on future budget. Switching
provider may not be an option. By then, the company will have developed
know-how, automation and documentation strictly bound to that vendor, and
switching will incur major costs or may be downright impossible for technical
reasons.

# 1.13 Interaction of the software product with regulatory requirements

For some industries, such as those involved in commerce, banking, healthcare,
aviation and so on, there are strict regulatory requirements to follow before a
software can be classified as approved for use. In general, these requirements
are satisfied through not only following coding practices, but also ensuring
full traceability of the requirements, tests, changes, deployments, access
rights, associated risks to failures, consequences on human safety and
risk mitigation strategies.

Regulatory documentation will have to be produced and tracked to handle
these requirements, and generally signed either in wet ink or with a
digital signature.

# 1.14. Long term support of the software product

Once the software is released and deployed, a new challenge emerges: not only
the software needs to be improved, but also old software releases must be
supported. This support comes in many different forms:

- support end users still using the old version, triaging their bug reports
- provide patched version of the software for both the old version and the new one.
- organise deployment of patched versions across the business, from the technical, training, 
  and regulatory point of view.
- keep supporting the opening and writing of files produced by the old software version
- handle migrations of database schemas without breaking old software.
- if the software provides an API, extend or deprecate functionalities without
  compromising old client code
- if new hardware, operating systems or dependent libraries are to be supported,
  potentially support different ABI or versions of the dependencies.

Each of these cases has its own special challenges, complexities and remedies.
For example, most of the bug reports will not be actual bugs, but
they will be the result of improper usage. Failure to follow instructions or
read error messages by the end users will not help, nor will poorly defined
steps to reproduce the error condition. Most of the time of the support team
will be spent investigating these obscure reports, to discover that are not
bugs of the software product itself. 

Particular care must be taken, during implementation, not to enter into inescapable
situations with files already on the end user's computers[^1]. 
Refactoring techniques for databases can be used to perform schema migrations,
but proper care and support of advanced features (such as triggers and stored
procedures) may be needed, requiring a different database engine than the one
currently in use.

In other words, at every new release of the software, its surrounding
environment acquires inertia, and changes must be considered not only within
the framework of the software at that specific moment in time, but also its
state in the past and its possible future. This add a potentially large burden
that needs to be taken into account.

[^1]: A real case scenario I've witnessed involved a file, written on customers
computers, that had no version information. In these files, version 1 of the
software wrote a date as day-month-year. Version 2 of the software wrote
month-day-year. With a few exceptions of impossible cases, there is no
practical way to differentiate which format it is used. A hack was devised to
piggyback on the presence of another unrelated information, added in version 2
of the software, to assess the "informal" file format version.  When software
version 3 was released, a version tag was added to the file.  

# 1.15. Deprecation of the software product

Some software is eventually deprecated, not only as old version, but as a whole.
Deprecation is generally performed when the software was supporting a process
no longer practiced, or when a new software product is bought or introduced into
the business to replace the old one. 

Deprecation generally carries its own share of challenges: old data must be migrated,
old deployments must be removed, staff need to be re-trained on the new product.
If the deprecated component is a software library, some applications may have 
a dependency against it. The applications must be modified to remove the dependency
against the deprecated component, or the component simply can't be deprecated in full, 
but will remain active as an obsoleted component.

# Conclusions 

This chapter wanted to bring attention to the following core points: 

1. Any company that writes code is a software company, regardless if its final
business product is software or not.  
2. Being a software company introduces a large number of aspects that need to
be considered to deliver and keep delivering an effective end product.

These points may seem trivial and straightforward to software-oriented readers,
but from my experience a large number of companies developing non-software
products do not believe themselves as software companies. With point 1
dismissed, these companies create a scenario where point 2 is ignored as well,
creating a situation where software and its crafters are relegated to an
unheard voice, with paper thin resources, huge technical burdens and a fragile,
unreliable infrastructure that is keeping the whole business hanging by the
threads.

