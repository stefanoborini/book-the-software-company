---
nav_order: 1
---
# 1 The Software Company

If your company creates software of any kind, from basic scripts to complex applications, it is a software company.
It is irrelevant that its core business is not software. While this seems to be a trivial point to make, my personal
experience with multiple companies from manufacturing to pharmaceuticals points at how often this fundamental
concept is downplayed.

As a software company, you carry a set of requirements to meet the goals of handling software. You need to handle the software
production chain, which generally can be represented as follows:

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


# Other
- Excessive involvement of developers in secondary tasks
- General communication problem
- Putting a business critical project in the hands of a completely different team on a different location, with no chance for one of the new developers to get an introduction to the code base.
- Excessive bickering over technicalities.
- disorganized, complex workflow, limited by the rate of review to get features into the main branch.
- Development model makes it complex to keep the code forward, New branches must depend on still not merged branches, meaning that often we end up with conflicts.
- Unclear roles and process in handling issues.
- unclear dependencies of the various stages of the sprint.
- hard to know the progress and the remaining work to be done for the specific
  milestone. GitHub tracker is too primitive.
- Technologies that we use are overdesigned or redundant, no training given, huge money sinks because they don't behave like expected.
- Prioritization and scheduling is pretty much left to random. PM should prioritize and assign issues, remind of the status.
- Excessive use of github issues as a "notebook" introduces a lot of notification noise. A developer has a development track. We should not keep creating issues just for us as reminders. While I understand that the goal is to keep PR small, I fear it decreases understandability instead of increasing it.
- As above, the fact that these issues are constantly added to the milestones means that it's pretty much impossible to know how far we are from reaching the goal.
- It's often unclear who is the expert in this or that technology if one has a problem with it.
- the production pipeline is constantly interrupted due to poor forward thinking. e.g. in the decision on how to present multiple tracks in the alignment view and which code should be responsible for it, these things should already be discussed and ready for the beginning of the milestone. There's no product owner responsible for this high level decision.
- bad management of the issue tracker. keep pushing non-milestone tasks from milestone to milestone, instead of leaving them for slack time after the release. The issue list for a milestone should contain what it's expected from the customer for that iteration, that is, the goals (user story), plus the individual tasks on how to achieve that. This way we can know how far we are from customer completion.
- It's not always clear who is doing what, when.
- solving big problems without addressing user-centric fundamental (e.g. installation)
- members enter and exit the team on-demand without any minimal planning/expected need.



