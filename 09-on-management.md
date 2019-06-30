---
nav_order: 9
---
# 9 On Management


This section wants to dig deeper into management and execs strategy when it comes to integrating 
the software company into a more articulated and complex business. Note that this does not necessarily
imply a failure of the business (although I've seen cases where this was indeed the case). It will
however consider issues that may compromise, ruin, or introduce a general feeling of poor satisfaction,
and thus poor loyalty to the company.

The important take home message of this whole chapter can be summed up in a
single phrase: **your company is a brain, and developers are its neurons.
Creating an environment that makes them leave, or dismissing them, is
equivalent to a lobotomy.**

Why such importance on software developers? Because software developers don't
follow a rulebook.  They know intimate detail of the infrastructure that keeps
your business and production chain running at all times. Their knowledge of the
system complexity and interactions is what keeps the show running and takes
years to acquire. While you may claim that this is a general principle to any
part of the company, remember that a single misguided intern can bring your
whole company down, or much worse: check, for example, Knight Capital Group's
460 million dollars loss, ma.gnolia total data loss, Aexecor's delivery of
28000 tons of coal to their doorstep, the explosion of the Ariane 5, or the
most recent Boeing 737 Max crashes. 

A rather disturbing comment on the topic is that, from my personal experience,
software development and their staff is not kept in high respect in businesses that
are not focused on a software product. Sentiment can drift from mild disinterest to
contempt. My feeling is that Execs don't know how to treat software because software
is a young industry (especially compared to manufacturing), and there is no
established literature or best practices to handle software development in a
larger product driven company. Execs therefore improvise, or get married to a
formula that has proven to work in traditional contexts, and lack the will to take
the risk or willingness to attempt something that strays too far from the established
literature, lest they piss off venture capitalists or other execs with a more conservative
attitude. Nobody gets fired if you follow the book to the letter, and if the book fails,
it's the book's fault.

Another factor worth pointing out is that software is intangible, both in its
complexity and in its quality. If a mechanical engineer were to produce a
perfectly machined mechanical piece that moves smoothly, anybody would
recognise its quality and state of achievement. On the opposite side of the
spectrum, if an electronic engineer were to produce a jumbled mess of wires and
connectors, anybody would recognise the poor level of completeness of this
prototype. Software? Its parts are invisible, its quality and readiness
ephemeral. If it gets the job done, it's considered done, regardless of its
safety, stability and reliability.  Right now, there are hundreds of thousands
of software components out there that are the equivalent of the jumbled mess of
wires that can burn at any moment and can't be changed at short notice. They
are all in production, all managing mission critical or business critical
operations. And execs and managers are absolutely fine with that.

In the political fight between venture capitalists, execs and management, the developers
are in the middle. They get tired, their warnings ignored, their technical debt becoming 
larger and larger until the code is technically bankrupt. Everything is hanging on a
thread, everything is impossible to understand, modify, fix. Everything is set in stone
due to legacy or dependency. Developers wait for the other shoe to drop, fighting fires
every day, being kicked here and there according to business pressure, and hope that 
they are out of the way when their awful code will eventually break. It's not their problem
anyway: due to how people are managed, it won't be them to suffer the cost of their poor
code. It will probably be the intern, or the new hire, or a colleague. 

This is why I encourage people to have some form of loose ownership of code.
People have to suffer through their mistakes. If they write bad code, they have
to suffer the consequences of their bad code. If business pressure forces them to write
bad code, they have to think very carefully about their estimates, as well as creating
code that will become a future nightmare for themselves just to please the annoying
deadline. Their debt should be their debt alone, it should not be transferred to others.

Which brings me to the topic of consultants.

## On consultants

## On product owners

A product owner is the person responsible for the direction and feature
prioritisation of an application.  When it comes to creating a product, product
owners is responsible for the "what (needs to be done)", and the team is
responsible for the "how (to do it)". The main problem of Product Owners is
that they want everything, perfect, right now. Unfortunately some product
owners seem generally oblivious to one of the main rules of the universe, the
law of motion: ``space = velocity * time``. This is generally known as the
"project management triangle", albeit with different names. I prefer the
``s=vt`` formulation because it's a more realistic expression of the problem.

The law of motion tells you that, in order to cover some distance, you need
time and velocity. The rather trivial point out of this equation is that once
you fix one term, the remaining ones are constrained.

Velocity depends on many different factors: your team effectiveness, how good
are your tools (internal or external), how complex and research-glazed is the
task you have to address, new hires entering the team, context switches, but
barring disruptive shifts in tasks, your team's velocity is pretty much a
constant. You can maximise this constant through consistency and skills, and
ironically enough, very few management actions improve this number.  Reorganise
the team, the velocity decreases. Developers are interrupted, the velocity
decreases.  Use inferior tools, you guessed it, velocity decreases. 
Add junior team members, the velocity decreases or even drops to zero.
The only actions that management can do to improve velocity is to remove
obstacles and ensure a reliable output from a well-oiled team that knows what
is doing. As Sun-Tzu said: know yourself (your skills) know the enemy (the
current code, tools and problem to solve).

Now that we established that velocity is a constant, the only option we have is
on space (the features) and time (how much time the team has to implement
them). Either you choose one, or the other. You can't choose both.

Some companies try to do creative management, such as menacing team of
layoffs, or proposing incentives. None of these will change velocity. It will
just increase time (they will work overtime), but this affects velocity (people
are tired, introduce more bugs, skip over important details) so the net result
is less motivated individuals and a lousy product.



## On managers

Managers are human calendars. They have two main responsibilities:

- organise people time so that no conflicts arise.
- take decisions to remove impediments.



- developers are not interchangeable
- splitting of tasks across teams
7. Do you encourage removing obstacles?

employee has a problem and can't solve it. What should he do? Spend one hour in front of the
screen trying to figure it out. ask the other guy who in 5 minutes knows the problem and fixes it.
Disruption.



5. Do you plan ahead?

Employees get sick, or leave. Do you account for that?
Do you account how to react to the increase in amount of employees? who trains them?
who buys and installs their computers? 

- Undefined long term strategic goal, both in scope and in excessive verbosity of the presentations that dilute the key points.

- constant panic mode is indicative of poor initial technical planning

9. Management hires developers and treat developers all the same. Do you have a technical lead and a project manager?

- strong reluctance of the executive to finance improvement of our tools, offloading these tasks to either "side projects" or as "consequences" of other development. Leaving this to personal initiative leads to unresponsiveness and uncoordination.
  management pet projects that don't address the business need.
- Excessive involvement of developers in secondary tasks
- Putting a business critical project in the hands of a completely different team on a different location, with no chance for one of the new developers to get an introduction to the code base.
- Unclear roles and process in handling issues.
- the production pipeline is constantly interrupted due to poor forward thinking. These things should already be discussed and ready for the beginning of the milestone. There's no product owner responsible for this high level decision.

- running out of spare capacity to improve the process
- everything priority one, therefore switch context all the time
- what is your business? don't develop things that are not your business. buy them.


## 9.1 on Jira

I argued with myself for a long time where to put this section. Management,
communication, or general principles.  I decided to choose management because
this tool is definitely addressed to management.

Jira is, for better or worse, the unfortunate standard of project management tools in the industry. Other tools exist,
but by far Jira is, if not the most common, the most commonly known. Unfortunately it is also deeply flawed as a tool.

Stripped out of its poor UI, Jira is a relational database with a fancy
interface to describe table views.  It does not provide a solution for project
management. Rather, it provides a generic tool that you can use to do project
management. The difference may seem unimportant, but the reality is that the
claimed "flexibility" of Jira masks an unwillingness by Jira's development team
to create a well-researched workflow, and puts the burden on your company to
devise this workflow.

The consequences of this are:

- Jira has no standardized workflow or terminology. Knowledge and use cannot be
  ported between companies or even departments or groups of the same company,
  because each company, department, or group may invent their own redundant, deceiving
  terminology that is meaningful only locally within the group.

- Jira provides tons of plugins that add functionality to dialogs, boards, and issues. 
  These plugins, as well as the need to configure and setup appropriately the boards,
  introduce irrelevant options (that need occasional dummy data), complex
  and redundant workflows to create issues, misconfigured boards, incorrect or
  obsolete terms, teams or classifications that cannot be removed (because
  historically relevant) and pollute the selection dialogs. All of this adds
  even more lack of skill portability and makes extremely hard to onboard a new
  team member.

- The nature of Jira as a database and boards as views mean that issue will
  only appear if they match a query. The result is that, either to
  misclassification or obsolescence of the board in favor of a different one
  after a reorganisation, entries will be forgotten, disappear, or never appear.

- Jira has massive UI shortcomings and bugs that have been requested for
  years to be fixed, and are still unsolved. The UI is slow and
  counterintuitive, cluttered with confusing choices and obtuse behavior that
  reject your input unless you learn all its needs and workarounds and scales poorly
  to large number of issues.


In other words, if before installing Jira you have one problem, that is, doing
project management, when you install Jira you have three problems: managing
Jira buggy interface and behavior, coming up with usage and practices to map
your business to Jira's way, and manage the chaos that Jira usage eventually
produces.

Jira is just one of the many management tools available out there, but it's the
most relevant example for the topic of management tools and their overall
quality. The tool does not make the management, the tool supports the management.
Poor management cannot be fixed no matter how excellent the tool is, but an
excellent management can become extremely inefficient due to poor tools. The
tool is the language by which management organises and coordinates the effort
across the team and the rest of the company. A good language means nothing
if what is said is utter nonsense, and no philosopher can express ideas relying
only on unstructured guttural sounds.
