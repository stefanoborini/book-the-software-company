---
nav_order: 2
---
# 2 On Agile Development

Agile is a set of guidelines on how to deliver quality software, skipping
unproductive parts that do not deliver value and focusing on a fast release
cycle. The set of principles of Agile focus on lightweight processes, an incremental
approach to software delivery, and a strong focus on people rather than paperwork.
In other words, minimum viable burocracy to deliver minimum viable products in
small, achievable and measurable steps. On paper, it's an excellent way to get
things done. Unfortunately, no plan can face direct conflict with the enemy.
I've seen plenty of mistakes made by companies pretending or claiming to use
Agile, while in fact they use anything but Agile, completely neglecting 
the advantages of Agile by compromising on its assumptions.

Don't get me wrong, I am a strong Agile supporter and Advanced Certified Scrum Master.
What I mean is that the whole concept of Agile is often corrupted in its
application by managers and executives due to the strong disconnection between
what Agile methodologies are and what these people think they are. 

The typical scenario is the following: upper management and executives decide
to "go agile" because someone sold them the idea that it's a better and faster
way to achieve results. Lower management and teams realise that in order to do
agile, they would need not only to rewire how the external interactions work,
but also their framework against the "accepted company practices" in terms of
deadlines, meeting schedules, manufacturing process, stakeholder availability,
and Gantt charting labeling from upper management. In addition to that,
fundamental tools such as information emitters are not provided, nor are
whiteboards or walls to arrange post-its, or closeness of team members.
The result is that:

1. Executives and upper management claim they are doing Agile while in reality
   the company is not. This percolates to job announcements from HR.
2. Middle and low management (if uninformed or inexperienced) are led to believe Agile doesn't work or cannot work
   or (if informed) that what the company is doing is not Agile, but a hodgepodge of tragedy.
3. Team is caught in the mess that originates from this, and starts to either
   dismiss Agile practices or resign altogether.

## Scrum

There are many implementation of development methodologies that follow Agile
principles, the most commonly used is probably Scrum. As an implementation, it
details specific guidelines on how to organise your development process, as
well as the general flow of information and execution within the development
team. 

For those unfamiliar with Scrum, the idea is to deliver the product
incrementally in batches of work called Sprints (lasting from two to four weeks
each), feature by feature, via the interaction of three entities: 

1. The Product Owner (PO), who is a single person acting as a proxy for the
   customer. The PO is responsible for the vision of the product, the priorities of the features,
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
features, the flexibility is in the delivery time. You can't cheat this
fundamental law of nature. Scrum defines a process that allows the PO to focus
on what matters and promote the release of a working product at the end of
every sprint.  While not perfect, this product focuses on the fundamental
needs of the customer first.

From what I have seen, Scrum works well in driving delivery and focusing
effort, but has its drawbacks.  Most of these drawbacks arise from these
factors, the first three of which are not strictly Scrum's fault:

1. Incorrect application of Scrum as a whole.
2. Incorrect application of aspects of Scrum.
2. Scrum not being the right framework for the task.
3. Scrum not being overly prescriptive on some crucial duties.



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
generally performed unconsciously by those who do not understand how to do
Scrum. Briefly said, the company and process structure remains exactly the same
and people's roles are renamed: upper managers become Product Owners, middle managers
and team leads become Scrum Masters, all while they keep operating in the same way,
possibly waterfall.

### Scrumfall

Related, but different from Scrumwashing is Scrumfall, that is, Scrum + waterfall.
Scrumfall does implement Scrum "correctly", but applies the sprint to individual 
waterfall phases. There are sprints to write the specs, then sprints to write the design,
then sprints to perform the implementation. 

### Water-Scrum-Fall

Once again related to the previous two, Water-Scrum-Fall starts with a drafting
of the specs that are signed off, followed by development performed with a
Scrum methodology, followed by the final acceptance by the customer. I've
witnessed this method in consulting companies, where the deliverable is decided
upfront and agreed upon at contract signing. In general, the customer is not
willing to provide any guidance or feedback during the development. They just
want the contract fulfilled according to the request, even if the request is
meaningless.  The team is not consulted to see if the specs are achievable or
make any sense, and the final product is generally the result of interpreting
these specs so that, at least on paper, it satisfies the requirements.

## Incorrect application of aspects of Scrum

In other cases, Scrum is applied, but with caveats which undermine its core
strengths. These are generally the result of inexperienced Scrum Masters and
Product Owners, or when Scrum is applied in a context where software production
must interact with other aspects of the business having different leading time
or feedback and prodcution cycles, typically manufacturing and research.

### Use end of sprint as a deadline

In this scenario, Scrum is understood not as an incremental process, but as a
fixed time/fixed goal project, typically of one Sprint. The end of Sprint is
considered the deadline for the fixed, non-negotiable effort. This leads to a
situation where the Team has no control over the features to deliver, and no
control over the time. As you can't cheat nature, something has to give: either
the project will be late, or corners will be cut, generally in code quality and
testing.

### Absentee Product Owner

There are issues to be solved, but nobody knows where they are. The product
owner is not aware of being the product owner, and is unavailable for
questions, being too busy. The team has to understand what needs to be done
from the open story, but the request is unclear.

### Scenario 3: Absentee team

The reverse of the above is when the team is unavailable to receive input from the product owner, normally
because they are involved in other tasks, or the product owner keeps requesting a meeting between him
and the team lead to "keep it short". The team lead now has to propagate the information from the product
owner.

### Scenario 4: Team has no idea of the application

Seen many times: the application has been developed by someone else, and has
been dropped like a steaming pile of garbage on the team's table. The team, who
knows nothing about the internals of the application, is now asked to plan the
next sprint without knowing anything of the application, and to commit to
fixing it for the end of the sprint.

### Scenario 5: The Team Lead role

This scenario is the result attempts to fit "traditional" job descriptions 
into a Scrum framework. Scrum makes no prescription of the Team composition,
except for a statement generally expressed as "a team of motivated, self-organising
individuals". Nevertheless, payroll, resumes and job openings need cool-sounding
titles, and in some cases the Team Lead figure emerges. The Team Lead ends up
being a catch all for tasks and a blame magnet for failures. It must organise
the team operations like a Scrum Master, decide priorities and interact with
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
The team ends up seeing the Team lead as "the boss", rather than the technical guide
and organiser, and this influences decision making and willingness to speak openly.

## Scrum not being the right framework for the task


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

# Scenario 5: Using the User story template religiously

User stories should tailor to the template "As a ... I want ... so that ...". Some people use this format
religiously, so much that they actually write 

```
*As a*

User

*I want*

to search songs in alphabetical order

*So that*

The appropriate songs are displayed
```

I have two problems with this. First, that it's really hard to read for a ordinary human being.
Second, that it misses the point entirely. In journalism, there's a similar rule, the 5 W of journalism:
Who, What, When, Where, Why. These are established and sensible rules, but open up your daily newspaper
and you will not find articles in the form

```
Who:

Ms. Williamson

What:

Had a car accident

When:

yesterday

Where:

at the crossing in front of the church

Why:

another car ran a red light
```

What one wants to read is a story in this form:

```
Users need to search songs in alphabetical order, and obtain a list of the
matching songs as they type the name they are searching.
```

While this seems trivial, it is not only a petty lexical and formatting
requirement. The user story must be human, and must address the "As a I want So
that" need, but leave space for ease of readability and broader explanatory
power. Artificially constraining your story to a rigid template of sterile
questions is not the goal. The goal is to communicate intent clearly.
Religiously following the template does not achieve that. Enforcing the
following of this template religiously in structure rather than intent is
detrimental, and shows a compliance to the rules typical of people who are
inexperienced.


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
