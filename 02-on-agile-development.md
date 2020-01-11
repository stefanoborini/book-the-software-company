---
nav_order: 2
---
# 2 On Agile Development

Agile is a set of guidelines on how to deliver quality software, skipping
unproductive parts that do not deliver value and focusing on a fast release
cycle. The set of principles of Agile focus on lightweight processes, an incremental
approach to software delivery, and a strong focus on people rather than paperwork.
In other words, minimum viable burocracy to deliver minimum viable products in
small, achievable and measurable steps.  On paper, it's an excellent way to get
things done. Unfortunately, no plan can face direct conflict with reality.
I've seen plenty of mistakes of companies pretending or claiming to use
Agile, while in fact they use anything but Agile, completely neglecting 
the advantages of Agile by compromising on its assumptions.

Don't get me wrong, I am a strong Agile supporter (and I put my money on it, as
I have an Advanced Certified Scrum Master certification). What I mean is that
the whole concept of Agile is often corrupted in its application by managers
and executives due to the strong disconnection between what Agile methodologies
are and what these people think they are. The typical scenario is the following: 
upper management and executives decide to "go agile" because someone sold them
the idea that it's a better and faster way to achieve results. Lower management
and teams realise that in order to do agile, they would need not only to rewire
how the external interactions work, but also their framework against the
"accepted company practices" in terms of deadlines, meeting schedules,
manufacturing process, stakeholder availability, and Gantt charting labeling
from upper management. In addition to that, fundamental tools such as
information emitters are not available, nor are whiteboards or walls to arrange
post-its, or closeness of the team members.
The result is that:

1. executives and upper management claim they are doing agile while in reality the company is not. 
   This percolates to job announcements from HR.
2. middle and low management (if uninformed or inexperienced) are led to believe Agile doesn't work or cannot work
   or (if informed) that what the company is doing is not Agile, but a hodgepodge of tragedy.
3. team is caught in the mess that originates from this, and starts to either dismiss Agile practices or quit altogether.


So much for the high level view. Going into more detail, 


There are many implementation of development methodologies that follow Agile principles
the most commonly used is probably Scrum. As an implementation, it details specific guidelines
on how to organise your workday, as well as the general flow of information and execution
within the development team. 

I am going to analyse Agile practices under two aspects: management, and technical.
Agile practices has a strong consequences on both.






The best way to explain these mistakes is by giving actual examples, and
explain what assumptions are violated and what is the consequences of violating
those assumptions.

## Scenario 1: use end of sprint as a deadline.

In some cases, the end of sprint is seen as an opportunity to enforce a deadline

Among the various issues I've seen happen in practice,

- people still involved in other tasks
- short sprints and late planning.
- end of sprints are not project deadlines.
- sprints always leak
- fluid teams aimed at the feature.
- code quality in an agile mindset.

## Scenario 2: Absentee product owner

There are issues to be solved, but nobody knows where they are. The product owner is not aware of
being the product owner, and is unavailable for questions, being too busy. The team has to understand 
what needs to be done from the open story, but the request is unclear.

## Scenario 3: Absentee team

The reverse of the above is when the team is unavailable to receive input from the product owner, normally
because they are involved in other tasks, or the product owner keeps requesting a meeting between him
and the team lead to "keep it short". The team lead now has to propagate the information from the product
owner.

## Scenario 4: Team has no idea of the application

Seen many times: the application has been developed by someone else, and has been dropped like a steaming pile
of garbage on the team's table. The team, who knows nothing about the internals of the application, is now asked 
to plan the next sprint without knowing anything of the application, and to commit to fixing it for the end
of the sprint.

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
