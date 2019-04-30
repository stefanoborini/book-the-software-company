---
nav_order: 1
---
# 1 The Software Company

If your company creates software of any kind, from basic scripts to complex applications, it is a software company.
It is irrelevant if its core business is not software. While this seems to be a trivial point to make, my personal
experience with multiple companies from manufacturing to pharmaceuticals point at how often this fundamental point
is ignored.

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
- extremely uncomfortable tables, both for height, and for transmission of vibrations between employees.
- the production pipeline is constantly interrupted due to poor forward thinking. e.g. in the decision on how to present multiple tracks in the alignment view and which code should be responsible for it, these things should already be discussed and ready for the beginning of the milestone. There's no product owner responsible for this high level decision.
- bad management of the issue tracker. keep pushing non-milestone tasks from milestone to milestone, instead of leaving them for slack time after the release. The issue list for a milestone should contain what it's expected from the customer for that iteration, that is, the goals (user story), plus the individual tasks on how to achieve that. This way we can know how far we are from customer completion.
- It's not always clear who is doing what, when.
- Complexity for the sake of complexity. Inability to keep things simple and lean.
- solving big problems without addressing user-centric fundamental (e.g. installation)
- members enter and exit the team on-demand without any minimal planning/expected need.
