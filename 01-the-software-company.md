---
title: The Software Company
nav_order: 1
---
# 1 The Software Company

If your company creates software of any kind, from basic scripts to complex applications, it is a software company.
It is irrelevant that its core business is not software. While this seems to be a trivial point to make, my personal
experience with multiple companies from manufacturing to pharmaceuticals points at how often this fundamental
concept is downplayed.

As a software company, you carry a set of requirements to meet the goals of handling software. You need to handle:

- software, its creation and its maintenance
- handling of the runtime the software depends on (compilers, libraries etc).
- testing of the software
- handling of the infrastructure to perform testing, possibly hardware.
- versions and releases of the software, and their interactions.
- documentation of the software
- interaction of the software with your core business
- deployment of the software, either in house, off-site (e.g. with third parties), or in the cloud.
- interaction of software development process with your core business process.



# On code ownership
- schizophrenic development. 
- certainty of tasks



# Other
- Excessive involvement of developers in secondary tasks
- General communication problem
- Undefined long term strategic goal, both in scope and in excessive verbosity of the presentations that dilute the key points.
- write code that is overly complex in response to needs for genericity that is not there, in the name of flexibility, but end up being inflexible due to the complexity of the resulting design.
- Spending excessive amout of time in documenting the code when the design is prone to change. The code is the documentation. I understand that excessive turnover of the developers may want to keep information stored somewhere, but it's probably better to focus on keeping competences and teams together so that projects are not handed out to some new random person/group every time.
- Putting a business critical project in the hands of a completely different team on a different location, with no chance for one of the new developers to get an introduction to the code base.
- Putting the project in a location that is space limited for additional hires.
- Excessive bickering over technicalities.
- disorganized, complex workflow, limited by the rate of review to get features into the main branch.
- Development model makes it complex to keep the code forward, New branches must depend on still not merged branches, meaning that often we end up with conflicts.
- constant panic mode is indicative of poor initial technical planning
- Poor management tools.
- Unclear roles and process in handling issues.
- unclear dependencies of the various stages of the sprint.
- hard to know the progress and the remaining work to be done for the specific
  milestone. GitHub tracker is too primitive.
- Issues are generally not measurable in achievement. "Cleanup this" is not measurable. We can clean it up for an hour or for three days.
- Technologies that we use are overdesigned or redundant, no training given, huge money sinks because they don't behave like expected.
- strong reluctance of the executive to finance improvement of our tools, offloading these tasks to either "side projects" or as "consequences" of other development. Leaving this to personal initiative leads to unresponsiveness and uncoordination.
- implementing the same things twice in parallel 
- Prioritization and scheduling is pretty much left to random. PM should prioritize and assign issues, remind of the status.
- Excessive use of github issues as a "notebook" introduces a lot of notification noise. A developer has a development track. We should not keep creating issues just for us as reminders. While I understand that the goal is to keep PR small, I fear it decreases understandability instead of increasing it.
- As above, the fact that these issues are constantly added to the milestones means that it's pretty much impossible to know how far we are from reaching the goal.
- It's often unclear who is the expert in this or that technology if one has a problem with it.
- The illness policy makes people come to work while sick, spreading the illness and reducing productivity.
- the production pipeline is constantly interrupted due to poor forward thinking. e.g. in the decision on how to present multiple tracks in the alignment view and which code should be responsible for it, these things should already be discussed and ready for the beginning of the milestone. There's no product owner responsible for this high level decision.
- bad management of the issue tracker. keep pushing non-milestone tasks from milestone to milestone, instead of leaving them for slack time after the release. The issue list for a milestone should contain what it's expected from the customer for that iteration, that is, the goals (user story), plus the individual tasks on how to achieve that. This way we can know how far we are from customer completion.
- It's not always clear who is doing what, when.
- Complexity for the sake of complexity. Inability to keep things simple and lean.
- solving big problems without addressing user-centric fundamental (e.g. installation)
- members enter and exit the team on-demand without any minimal planning/expected need.

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

3. Do you understand s = v * t?

The most basic law of motion tells you that in order to cover some distance, you need time
and speed. The interesting, and rather trivial point out of this equation is that once you 
fix one term, the remaining ones 

Velocity depends on many different factors: your team effectiveness, how good are your tools
(internal or external), how complex and research-glazed is the task you have to address, 
new hires entering the team, context switches, but barring disruptive shifts in tasks, your
team's velocity is pretty much a constant. This leaves 

Menacing your team of layoffs, or proposing incentives will not change
velocity. It will just increase time (they will work overtime), but this
affects velocity (people are tired, introduce more bugs, skip over important
details) so the net result is less motivated individuals and a lousy product.

5. Do you plan ahead?

Employees get sick, or leave. Do you account for that?
Do you account how to react to the increase in amount of employees? who trains them?
who buys and installs their computers? 

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

7. Do you encourage removing obstacles?

employee has a problem and can't solve it. What should he do? Spend one hour in front of the
screen trying to figure it out. ask the other guy who in 5 minutes knows the problem and fixes it.
Disruption.

8. Do you track progress with a physical medium?

Nothing is more frustrating not to know how far you are, what needs to be done, what is still pending.
I've seen plenty of times when things pile up due to urgency.

We are sensory driven animals. We manipulate objects and having objects represent what needs to be done
is essential.

9. Do you have a technical lead and a project manager?

Conflicts arise from poor management. 

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

