---
nav_order: 2
---
# 2 On Agile Development

Agile is a set of guidelines on how to deliver quality software, skipping
unproductive or inefficient parts that do not deliver value and focusing on a
fast release cycle. The set of principles of Agile focus on lightweight
processes, an incremental approach to software delivery, and a strong focus on
people and direct communication rather than paperwork.  In other words, minimum
viable burocracy to deliver minimum viable products in small, achievable and
measurable steps, new feature after new feature. 

On paper, Agile is an excellent way to get things done.  Unfortunately, no plan
can face direct conflict with the enemy.  I've seen plenty of mistakes made by
companies pretending or claiming to use Agile, while in fact they use anything
but Agile, completely neglecting the advantages of Agile by compromising on its
assumptions.

Don't get me wrong, I am a strong Agile supporter. What I mean is that the
whole concept of Agile is often corrupted in its application by managers and
executives due to the strong disconnection between what Agile methodologies
*are* and what these people *think they are*. 

The typical scenario is the following: upper management and executives decide
to "go agile" because it is sold as a more effective and faster way to deliver
results. Lower management and teams realise that in order to implement an
agile framework, they would need not only to rewire how the external interactions work,
but also their framework against the "accepted company practices" in terms of
deadlines, meeting schedules, manufacturing process, stakeholder availability,
and Gantt charting labeling from upper management. In addition to that,
fundamental tools such as information emitters are not provided, nor are
whiteboards or walls to arrange post-its, or closeness of team members.
The result is that:

1. Executives and upper management claim they are doing Agile while in reality
   the company is not. This percolates to job announcements from HR. New hires think
   they are joining an Agile system while they are not.
2. Middle and low management (if uninformed or inexperienced) are led to believe Agile doesn't work or cannot work,
   or (if informed) that what the company is doing is not Agile, but a hodgepodge of tragedy.
3. Team is caught in the mess that originates from this, and starts to either
   dismiss Agile practices or resign altogether.

The result is that Agile has become a buzzword that is both hated,
misunderstood, and pointed as a cargo cult, not because of what Agile actually
is, but because of all the people who botched it so badly.

So let's focus first on what Agile is: a set of principles for development.
Agile means to plan for requirements to change, because they will, so stay 
lightweight and flexible to minimise the cost associated to these changes,
and strongly encourage those who dictate the requirements to stay in the loop.
That's it. Nothing more. Do you want to distill it down even further? Here is is:
*Talk to your customers, talk to your teammates, get things done*. 
Everything else (Scrum, Kanban, etc) is prescriptive methodology that dictates
how to apply Agile principles in the real world.  Here is when things tend to
go wrong.

## Scrum

There are many implementation of development methodologies that follow Agile
principles, the most commonly used is probably Scrum. As an implementation, it
details specific guidelines on how to organise your development process, as
well as the general flow of information and execution within the development
team. 

For those unfamiliar with Scrum, the idea is to deliver the product
incrementally in batches of work called Sprints (lasting from two to four weeks
each), feature by feature, via the interaction of three entities: 

1. The Product Owner (PO), a single person acting as a proxy for the
   customer. The PO is responsible for the direction of the product, the priorities of the features,
   and the general translation of user requirements in a "language" developers can understand.
   In other words, the PO is the person that developers need to inquire directly and without hindrance 
   for questions about the features.
2. The Scrum Team (ST), who estimates the effort required to deliver the
   product increment satisfying the requests of the PO, as well implement them during
   the Sprint. The team composition is as variegated as it needs to be: a team dedicated
   to UI development might have both coders and visual designers.
3. Finally, the Scrum Master (SM) is a single person organising and monitoring
   the Scrum process, orchestrating the so-called Scrum "ceremonies" (AKA
   meetings), checking progress metrics and promoting the removal of impediments.

Every project needs to satisfy the holy trinity of parameters: time, features
and resources.  Mathematics teaches us that you can not enforce constraints on
all three. If you have fixed resources (team, technical skills, development
tools) and fixed time (deadline), the the features will need to be left
floating. If on the other hand the project has fixed resources and fixed
features, the flexibility must be in the delivery time. You can't cheat this
fundamental law of nature. Scrum defines a process that allows the PO to focus
on what matters and promotes the release of a working product at the end of
every sprint.  While not perfect, this product targets the fundamental
needs of the customer first, so that feedback and productivity can be achieved
as soon as possible.

From what I have seen, Scrum works well in driving delivery and focusing
effort, but has its drawbacks.  Most of these drawbacks arise from these
factors, the first three of which are not strictly Scrum's fault:

1. Incorrect application of Scrum as a whole.
2. Incorrect application of aspects of Scrum.
3. Scrum not being the right framework for the task.
4. Scrum not being overly prescriptive on some crucial duties.


## Incorrect application of Scrum as a whole

As a first step we are going to analyse a few patterns of incorrect application
of Scrum as a whole.  This is normally the result of misunderstanding of the
fundamentals behind it, or the inability ior unwillingness to transform the
company's established process into the new strategy, while at the same time
being pressured into the change from decisions above or from the perceived
gains that such transition will bring, without being willing to accept the 
change in mindset andprocess, as well as the associated costs.

### Scrumwashing

The biggest incorrect use of Scrum I've witnessed is what I call Scrumwashing.
It is a process that adds a veneer of appearance of doing Scrum, and is
generally performed unconsciously by those who do not understand how to
practice it. Briefly said, the company and process structure remains exactly
the same and people's roles are renamed: upper managers become Product Owners,
middle managers and Team leads become Scrum Masters, but they keep operating in
the same way, possibly waterfall.

### Scrumfall

Related, but different from Scrumwashing is Scrumfall, that is, Scrum + waterfall.
Scrumfall does implement Scrum "correctly", but applies the sprint to individual 
waterfall phases. There are sprints to write the specs, then sprints to write
the design, then sprints to perform the implementation. 

### Water-Scrum-Fall

Once again related to the previous two, Water-Scrum-Fall starts with a drafting
of the specs that are signed off, followed by development performed with a
Scrum methodology, followed by the final acceptance by the customer. I've
witnessed this method in consulting companies, where the deliverable is decided
upfront and agreed upon at contract signing. In general, the customer is not
willing to provide any guidance or feedback during the development. They just
want the contract fulfilled according to the request, even if the request makes
no sense.  The Team is not consulted before the final sign-off to see if the
specs are achievable or make any sense, and the final product is generally the
result of interpreting these specs so that, at least on paper, it satisfies the
requirements.



## Incorrect application of aspects of Scrum

In other cases, Scrum is applied, but with caveats which undermine its core
strengths. These are generally the result of inexperienced Scrum Masters and
Product Owners, or when Scrum is applied in a context where software production
must interact with other aspects of the business having different leading time
or feedback and production cycles, typically manufacturing and research.

### Use end of sprint as a deadline

In this scenario, Scrum is understood not as an incremental process, but as a
fixed time/fixed goal project, typically of one Sprint. The end of Sprint is
considered the deadline for the fixed, non-negotiable effort. This leads to a
situation where the Team has no control over the features to deliver, and no
control over the time. As you can't cheat nature, something has to give: either
the project will be late, or corners will be cut, generally in code quality and
testing.

### Absentee Product Owner

This is a very common situation. The Product Owner is nowhere to be seen. It
can happen that either the PO is unaware of being so, or is just too busy.
Unfortunately the job of the Product Owner does not complete with the
occasional end of sprint/beginning of sprint period.  The Team needs to
understand what needs to be done from the User Story. If the request is
unclear, or some aspects require discussion during implementation, the Product
Owner must be available. Failure to do so will end up delaying the Story, or
implementing the Story incorrectly.

### Absentee Team

In general, the Product Owner should not disrupt the Team during the Sprint unless
directly summoned. The Product Owner is pulled by the Team, never pushed on the Team.
However, a situation can occur when the Team requires the Product Owner, but when the
Product Owner is available, the Team is not. This is due to a disruption of the
Team by other forces, which is a poor practice in itself. The consequence of
this is that Team and Product Owner never have the chance to interact directly, and
if this can be brought to the extreme when someone from the Team, or even the Scrum Master,
becomes a proxy for the Product Owner. 

A similar situation can occur not because the Team is actually absent, but because
the Product Owner does not have time, and asks for a restricted one-to-one
meeting with the proxy to "keep things short". The proxy now has to propagate
the information from the Product Owner to the Team, and has become basically a
secondary Product Owner, except has no idea apart from the extremely narrow set of
information provided by the real Product Owner.

### Team too large

Another mistake I've seen in some cases is to have a Scrum Team that is too large.
I've seen "Scrum Teams" of 20 people, way, way above the optimal of around 6 people.
More people means poor integration and a higher chance of unproductive communication.
Daily standups become longer, and what one part of the Team does is likely not
relevant to the other part. These large teams reflect poor planning in dividing tasks,
scope, and competences of the team.

### Poor subdivision of competences

This antipattern presents itself in two ways: poor allocation of people, and
poor assignment of tasks.  

For the first case, poor allocation of people, a Team should have all the
competences required to achieve the goal of the Sprint. If a team is given a
task, but knows nothing about the technical details on how to achieve that
task, they simply can't progress.  The likely scenario will be that they have
to interact with an expert outside the team, which may or may not be available.
A proper way to conduct the team would be to include the external expert in the
Team. Typical examples of this situation is when a Team of developers needs to
develop an application frontend, but has no support from a UI designer or the
backend expert. These two should be part of the team, either fully or
partially.

The second case is corollary to the first, but is related to how individual tasks
are assigned during a Sprint. Some Scrum teams operate so that anybody can grab
any available tasks and get to work. Reality is however different. 
Some parts of the code may be better known by one or two elements of the team, either
because they already worked on it, or because they have a technical background or
seniority that allows them to understand it better. The most effective way to deliver
a result is for these people to take those tasks. If another member were to
pick it, coding will require more time, reviews will require more back and
forth, and overall the effectiveness of the team will be less than what it
would have been if the task was taken by the right person. Nevertheless, one
also has to consider load balancing and information sharing. Proper assignment
of tasks is a collective decision of the team that cannot be performed at
random or "when you are free take the next task".

### Team has no clue about the application

Another frequently seen antipattern is when the application has been developed
by someone else (likely contractors, or another team), and has been dropped
like a steaming pile of garbage on the Team's table. The Team, who
knows nothing about the internals of the application, is now asked to plan the
next sprint without knowing anything of the application, and to commit to
fixing it for the end of the sprint. The results will be disastrous. Teams and
team members are not interchangeable at will, and knowledge of the internals
and the required consistency in a piece of software is important information
that is never transported from one team to another easily. Some companies
try to mitigate this issue with massive amounts of documentation, but while
documentation is a fundamental tool, excessive use of it adds more burden to
the process, and moves the problem from understanding the code to understanding
the documentation against the code. 

At the end of the day, brain to brain data transfer is a fundamentally slow
process, Agile acknowledges this, and highlights the fact that face to face,
direct communication is the mechanism with the highest bandwidth and lowest
latency. 

### The imaginary "Team Lead" role

This scenario is the result of Scrumwashing traditional job descriptions 
into a Scrum framework. Scrum makes no prescription about the Team composition,
except for a statement generally expressed as "a team of motivated, self-organising
individuals". Nevertheless, payroll, resumes and job openings need cool-sounding
titles, and in some cases the Team Lead figure emerges. The Team Lead ends up
being a catch all for tasks and a blame magnet for failures, must organise
the Team operations like a Scrum Master, decide priorities and interact with
the customers like a Product Owner, code like a Team member. Oftentimes this
figure is the result of an absentee Product Owner who intends his contribute
to development as "This is what I need done. It's all top priority. It need it
now. Good bye".

While the Team Lead figure can be a Scrum Master with enhanced competences that
focuses on the technical side of the Team, a Scrum Master cannot also be a Product
Owner. The obvious reason is that the Team and the PO are pulling in different
directions. The PO knows what's needed. The Team knows what's possible.
Consensus between these two forces is orchestrated by a negotiation, but this
negotiation is harder to achieve when these two roles reside on the same person.
The Team ends up seeing the Team lead as "the boss", rather than the technical guide
and organiser, and this influences decision making and willingness to speak openly.

### Using the User Story template religiously

This is a minor issue, but I've seen it occur in some companies, especially in environments
that are inexperienced in Scrum. 

A common Scrum User Story template is the "As a ... I want ... so that ...". The intent 
is to capture the software feature and its target. A simple application of the above template
to a music player could say, For example

```
*As a* User, *I want* to search songs *So that* I can find the song that interests me.
```

I have seen this format followed religiously and verbatim. Nothing less, nothing more.
This results in poor readability and stifled communication. The point of the rule is to
ensure that the critical information given above is present for a story to be valid.
The same story, rewritten:

```
Users need to be able to search songs, for example by typing the name of the song
in an input area, and obtain a list of the matching ones as they type.
```

While this seems trivial, it is not only a petty lexical and formatting
requirement. The User Story must be human readable, and must address the "As a
I want So that" need, but also leave space for ease of readability, as well as
broader explanatory power.  Artificially constraining your story to a rigid
template of sterile points is not the goal. The goal is to communicate intent
clearly and start a conversation between the User and the Team.


## Scrum not being the right framework for the task

In some contexts, Scrum is simply not the right framework, or need to consider the
larger context in which it is performed. We'll explore a few of the circumstances that
might undermine a Scrum approach.

### IT support

IT engineers normally have to deal with two types of work: on demand
"first-come first-serve" issue resolution, and administration of
infrastructure. Scrum is clearly not indicated for the first type of work.
Imagine your IT person accepting your request and telling your problem will be
first prioritized. Then, if deemed of sufficient priority it will be addressed
and finalised in two weeks time. For this kind of activity, Kanban is a better
strategy exactly because it focuses on a first-come first-serve handling.

Different is however the topic of administration of infrastructure. Depending
on the infrastructure, and the strategies implemented by IT, a Scrum approach
might be appropriate, for example to develop administrative tools and scripts.
The result is that, in some cases, IT might have to work with both a Kanban and
a Scrum style in parallel, which might introduce its own challenges for
personnel allocation.

### Highly regulated industries or consulting

Another environment in which Scrum might not be appropriate (with caveats) is
highly regulated industries such as those involved in medical devices,
aviation, finance, and pharmaceuticals. These industries have a strong burden
of paperwork to address regulatory requirements. A typical scenario is the
addition of a new feature to software that can, in case of failure, potentially
injure or kill. This modification cannot just be included in the next sprint
and performed. Instead, appropriate assessments of the impact of the change
must be performed and signed off, the change must be approved and tracked, the
code modified, test protocols updated, test reports written and signed off, and
a new release must be done, together with the associated documentation. 

Scrum can, in a sense, be used within the above scenario if the development is
ongoing and the change can be inserted into the production chain, but the
documentation burden represents a deliverable in itself, and generally it is a
deliverable that requires long time and the involvement of multiple people that
may not be part of the team.

Consulting also offers a challenging environment for a Scrum setup. Individual
consultants are generally hired by a company to focus on a particular task. If
the consultant is not involved in a Scrum team, Scrum makes no sense for a single person,
although some concepts of it can be applied to streamline the problem and solve
it bit by bit, as well as doing demos along the way. 

In the case of consulting companies, generally there's no negotiation from the
team. The team is handed a consulting contract where the requirements have been
specified by the customer or agreed as part of a larger project. The Team can,
however, internally use Scrum to organise the process, but it is unlikely that
the customer will be available for further inquire, making the job of the
Product Owner and the Team much harder. This is normally due to the fact that
either the customer believes their side of the involvement has been satisfied
and just want the result, or because the customer's internal responsibilities
for the project are poorly defined and nobody is really responsible for taking
decisions. These projects normally fail to deliver a quality product.


### Integration with long round trip time (e.g. manufacturing)





inability of management to handle a mixed software-hardware company


Company in eternal panic mode.

Among the various issues I've seen happen in practice,

- people still involved in other tasks
- short sprints and late planning.
- sprints always leak
- fluid teams aimed at the feature.
- code quality in an agile mindset.



## Scrum not being prescriptive on crucial duties


Who is responsible for creating the team?
Who does end user support, or bug verification?

Refactoring and technical stories.

documentation duties.


## The untold dark consequences of Scrum

In all instances of use of Scrum I've seen, the code quality has always been
abysmal.  I am unwilling to assign to Scrum or Agile practices the
responibility for such failure, but it is worth stressing out a few important
points.

Scrum favors the resolution of user stories, that is, goals that provide
benefit for the Product Owner, and by proxy, the end user. It does not,
however, address the need for stories that keep velocity high. Retrospectives
may (and often do) consider procedural shortcomings and how to address them,
but another part of the retrospective discussion is generally
code quality, lack of documentation, deceiving interfaces, false dependencies,
lack of expertise.

The truth is, there are two customers to the codebase: 

- the end user which produces positive value (money earned) when its needs are satisfied. 
- the development team, which produces negative value (money spent) when its needs are not satisfied.

Scrum puts all emphasis to the first customer, and completely hides under the rug the second 
"anti-customer". The idea is that needs for the developers to improve the codebase are supposed to
be rolled into the first stories as "refactoring costs". This never really happens. If you can solve
a story with 1 story point with a hack, and refactoring it to proper and more flexible design requires 
10 story points, we all know which solution will be picked. Code quality goes down another notch,
until code debt after code debt you will be code bankrupted.

The other issue is that very often top-level products end up requiring meta-products. A typical
example is a common library shared by different products. However, without coordination and decision
making, the end result is that the team will deliver the same boilerplate again and again, or worse,
different teams will invent the same boilerplate in two different (and obviously incompatible) ways.
Since this meta-product is never coming up in a user story, there will be an intrinsic lack of
well-integrated meta-products in Scrum driven developments, not because of Scrum itself, but because
of how people use Scrum.

It is my opinion that the following adjustments should be made to Scrum:

- A backlog should be made of User Stories, created by the Product Owner, and Developer Stories, created
  by the development team.
- Every sprint must allocate a defined proportion of User and Developer Stories, depending on how strong 
  is the need for cleanup. Strong cleanup sprints can have 20% User and 80% developer stories. Feature
  driven sprints the reverse. Sprint allocation to developer stories should never be under 20%.
- When a meta-product is identified (typically at the end of the sprint), it should be extracted 
  promptly as a dependency before it escalates further. The longer is the delay, the more painful will 
  be the extraction, up to the point that no extraction will be possible.



every user story starts with 3 points, base
overall task. nothing specific. no points: only easy/medium/hard
change tasks as things go on.

sistema a catena di montaggio non funziona. Dovresti portare una feature da prototype a deployment, senza interruzioni.

bad decisions are there to stay. Nobody will refactor them. Some trivial stuff gets copied around again and again.
the design piles up layer upon layer of bad decisions. we create our own problems, and solve them with other problems.
tragedy of the commons


# On code ownership

8. Do you track progress with a physical medium?

Nothing is more frustrating not to know how far you are, what needs to be done, what is still pending.
I've seen plenty of times when things pile up due to urgency.

We are sensory driven animals. We manipulate objects and having objects represent what needs to be done
is essential.

- Issues are generally not measurable in achievement. "Cleanup this" is not measurable. We can clean it up for an hour or for three days.
- certainty of tasks: A person who picks up a task must be clear on what to do


- Excessive bickering over technicalities.

- death by a thousands papercuts.
- unclear dependencies of the various stages of the sprint.

- Excessive use of github issues as a "notebook" introduces a lot of notification noise. A developer has a development track. We should not keep creating issues just for us as reminders. While I understand that the goal is to keep PR small, I fear it decreases understandability instead of increasing it.

- Development model makes it complex to keep the code forward, New branches must depend on still not merged branches, meaning that often we end up with conflicts.
- hard to know the progress and the remaining work to be done for the specific
  milestone. GitHub tracker is too primitive.
- Prioritization and scheduling is pretty much left to random. PM should prioritize and assign issues, remind of the status.
- bad management of the issue tracker. keep pushing non-milestone tasks from milestone to milestone, instead of leaving them for slack time after the release. The issue list for a milestone should contain what it's expected from the customer for that iteration, that is, the goals (user story), plus the individual tasks on how to achieve that. This way we can know how far we are from customer completion.

- disorganized, complex workflow, limited by the rate of review to get features into the main branch.
- As above, the fact that these issues are constantly added to the milestones means that it's pretty much impossible to know how far we are from reaching the goal.

- throw software at a problem instead of a person.
