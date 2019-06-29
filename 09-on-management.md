---
nav_order: 9
---
# 9 On Management

- withhold info until definitive.
- execs may be married to a formula.
- developers as brain cells. making them leave is a lobotomy
- pissing off developers. Grueling tasks
- developers are not interchangeable
- splitting of tasks across teams

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

- Undefined long term strategic goal, both in scope and in excessive verbosity of the presentations that dilute the key points.

- Poor management tools.
- constant panic mode is indicative of poor initial technical planning

7. Do you encourage removing obstacles?

employee has a problem and can't solve it. What should he do? Spend one hour in front of the
screen trying to figure it out. ask the other guy who in 5 minutes knows the problem and fixes it.
Disruption.

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


# on Jira

I argued with myself for a long time where to put this section. Management, communication, or general principles.
I decided to choose management because this tool is definitely addressed to management.

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
