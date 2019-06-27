---
nav_order: 5
---

# 5 On company growth

Companies begin their journey in the business as Startups, and eventually, they
go bankrupt. The few that survive, need to grow in size and revenue, start selling
a product, as well as the possible associated services related to the product.

Both phases are delicate and require discussion. During the Startup phase,
foundations are laid down not only for the product, but also for the growth
that will come later. Shaky foundations will eventually lead to poor scaling
up, because new hires need to be trained and keep producing on top of the
established body of knowledge, code, and process that has been defined in the
Startup phase. Not addressing these issues is a joint responsibility of everybody in the company:

- executives need to address higher level organisation and forward planning of the scaling up
- management need to handle and distribute people expertise
- developers need to create code that can be understood and modified with minimal training, as well
  as processes in place to guarantee disaster recovery and mitigation strategies.

Unfortunately, the situation according to my experience is that companies tend
to bite more than they can chew in order to meet VC goals. Due to chronic
understaffing, poor coordination of resources, massive use of consultant that leave 
poorly understood code, quality suffer and all of this will eventually result
in scaling issues, as well as key knowledge leaving due to overwork or lack of
coordination. I have no experience as exec, but my understanding from the
general narrative is that execs may have quotas for how a company of a given
age and investment phase must be: X% staff as sales, Y% staff as development,
Z% as management etc. This is a "one size fits all" approach that poorly
marries with highly technical companies, and indeed spelled disaster when VCs
also don't keep into account that different businesses may have a different
apprach and timeline to market. My guess is that there's no established body of
work to handle these kind of companies, executives are just improvising, and VC
assume they will recover the costs of failures with those few companies that
actually manage to survive either because of luck, or a business that is
actually tailored to this kind of approach.

To add to this, a frequently heard mantra is that every time a company doubles in size, 
it needs to relearn how to communicate. This spans across topics, from documentation
management to actual day to day communication between execs, management and developers.
Processes are put in place to ensure some kind of communication pipeline, but processes
require resources to ensure these processes are followed, and processes don't survive
schizophrenic assignment of tasks. Things will be forgotten, unassigned, improperly
filed, and the process will grind to a confusing halt, possibly forgotten and whose only
remnants will be confusing documents and Jira tickets.


# On publishing job announcements

The first mistake of a software company happens at the job announcement phase.
A job annoucement should explain clearly the critical points that are required
for the job, the position the new hire will fill. I've seen too many job
announcements where it's unclear what kind of person is needed. I suspect there's
some business driven paranoia in not exposing the company to snooping from competitors,
but most of the times, when seeing it from the inside, this lack of clarity arises from
the fact that HR writes the opening according to a template, and the fact that, when
the position is opened, it is not done because there's an actual clear plan on where to
assign the new hire. Instead, the position is opened because the "company needs to grow".
The resulting job opening tends to be unclear and vague on its requirements.

A good announcement should be clear on the position, clear on the salary, and
clear on the tools, frameworks and libraries that will be used on a day to day
basis. A "not unheard of" practice is to include a language or framework that
is not relevant to the job but is there to demonstrate a more general openness.
For example, asking for C++ skills as a requisite for a python position, or
some other lesser used paradigm such as functional languages. While it's
probably a reasonable assumption that these requests may act as a filter, they
are unfair to the candidate and I have personal doubts they actually achieve
their desired goal. What is clearly a wrong practice is to advertise jobs
looking for ninja, pirates or rockstars. The juvenile mindset behind such
advertisements makes it clear that your company is something that only collects
junior developers (because they can't find anything else with their current
skill level), or people with a strong Dunning Kruger effect in action. Job
positions and descriptions have a meaning for the experts in the field, because
they use this classification to understand the type of skills they have to bring
to the table, as well as the expected salary.

Another common mistake is advertising the job on the wrong channels.  Using the
proper channels, keywords and phrasing may make or break the visibility of the
announcement, and with it, the type of candidates that will apply. Developers
tend to join and be part of communities (either online or offline), and you
should target those communities for better results. 

# On Resume screening

Once the resumes start pouring in, you should discard those who clearly don't
have the appropriate experience and they are just "give it a try", both because
they are clearly not appropriate for the position, and because they will,
possibly, choose another company that is a better fit for their skillset if one
comes along. Interviewing is a large time investment, you want to minimise this cost.

Your aim should focus on both general technical skills and technology expertise
in the specific tool, framework, or library you use.  The first gives a sense
of a person that knows a broader vision of the world and is not married to a
concept or framework (which eventually leads to "Cargo culting"), the second
gives you a person that is operational from day one and has already a good
knowledge of the errors and quirks of the technology. You want a person that
has seen them all with that framework or library, so when it's time to solve a
problem, the solution is obvious.

You want to discard anybody who doesn't have code to show online. From new hires,
to old senior developers, a developer has some code he wrote and uploaded somewhere.
Examine this code and verify its quality and compliance with known good practices,
and also verify how much of the code has actually been written by the candidate.

The remaining resumes are people who are good, hopefully, mixed with a lot of
people who are lying.  From my experience, I'd say that one out of three
candidates actively lie on their resume or grossly misrepresent their
expertise, generally through omissions or unclear statements. You want to
filter those out at the phone interview.


# On phone screening

The phone interview is the next obvious step, especially for candidates that are
not nearby, but I think that phone screening should be done regardless. During the
phone interview, apart from the formalities of introduction, the focus should be on
simple questions that someone who used those technologies must necessarily know the 
answer. You should, however, not be all or nothing, especially with people with a certain
seniority, because they might have been proficient in some languages, but their
proficiency fades with time. They may not remember things on the spot, or
remember them incorrectly. Generally, you can see if someone knows what he or
she's talking about after a few seconds. If they are rusty is not necessarily a reason
to reject them.

Technical people like technical questions. It stimulates them. However, you should be
wary of the talkers, for two reasons: first, they might be excessively verbose during their
day to day activities, which leads to long, pointless discussions. Second: they may know
the theory, but not the practical points. Like a musician that knows everything about
harmony and chords and metric, but can't play a single instrument, you want a person
who knows the theory but also can write code.

On the practice of doing code interviews online, I think that their value exists if:

- the code discussion is not about testing the knowledge of a particular algorithm
- the online coding platform is not obnoxious to use or unsuited for the task
- the online coding platform makes it clear that the candidate and only the
  candidate is the one writing the code.
- the code is a topic for conversation to explore the knowledge of the candidate when it comes
  to design strategies, naming, documentation practices.

Coding interviews where you are given 1 hour to create a working implementation
of a periodic game of life that passes the specified testsuite do not test the
candidate flexibility and ability to code. They are testing those who are
already familiar with the algorithm and can write whatever code to make the
tests pass.

You can, however, provide more complex challenges, depending on the seniority.
For example, I found myself extremely pleased when I was given a few days to
create a simple online service with react to perform queries to a third party
server, or when I was asked to talk about the design I would choose for a chess
program. In the first case, you give the candidate time to research the proper
solution, as well as make mistakes. You get a smoother signal on the quality of
the code. In the second case, the question touches many different topics, from 
model-view-controller design, to how to represent the data effectively, disk storage.
It's a conversation topic that evaluates the ability of the candidate to think design,
regardless of the complexities of the algorithm that backs it.

However, offline exercises don't give any guarantee that the candidate is the
person who is actually doing them. it's imperative that this code is then the
topic of a throughout analysis (with potential changes on demand) during the
on-site interview.

# On interviewing on-site

I've seen quite a few interesting development during on-site interviews.  People that
look brilliant on paper, or even on GitHub, are then found unable to code basic
functionalities. I've witnessed candidates interviewed remotely, that are clearly
not the ones writing the code on a shared document, relying on someone else to write it.

The most important question to answer during an interview for a developer is: can this person
write code? Like you would not hire a piano player without asking him to play a tune, you should
not hire a coder without asking him to write some code. If you don't, you are hiring a lot of 
people who claim they can code, but they really don't know how. They will drag the team productivity
down to a halt, and they will eventually produce low quality, hacked up code created by copying and
pasting from the internet without any care or attention.

The questions you are going to ask should also reveal if the person is a scripter or a coder.
Scripters are people that can program, but are not aware of the additional
complexities related to software development.  They trained their expertise in
writing scripts, but have no idea how to organise code (e.g. design patterns)
or address cross-platform compatibility issues. Their code is very linear,
poorly subdivided in responsibility and with very broad scope. Their error
handling is ineffective, approximate or missing altogether. They rarely know
how to program with advanced paradigms such as multithreading or asynchronous
behavior. You should therefore ask questions that allow you to identify the
candidate real level of knowledge.

A very useful guide on this regard is the following test from 
John Sonmez at simpleprogrammer.com. I invite you to read it as it's an exceptional first
step in deciding who is an appropriate candidate.

https://simpleprogrammer.com/joel-test-programmers-simple-programmer-test/

Briefly said and commented, his points are the following:

- *Can you use source control effectively?*: If you don't know how to use
  source control, and especially distributed source control, effectively, you
  have no business in being a programmer. It is a fundamental tool not only for
  history tracking, but for validation, review, testing and debugging.
- *Can you solve algorithm-type problems?*: 
- *Can you program in more than one language or technology?*: Being proficient
  in more than one language or technology does not only show that a candidate
  is dedicated to the profession, but it also shows an understanding of the
  general principles, rather than the "framework of the day", as well as
  broadening the palette of techniques the candidate can use to develop and
  understand other's people code.
- *Do you do something to increase your education or skills every day?*: This
  is controversial in my opinion, because while a candidate should definitely
  improve the general skillset and strive for it, a company should not expect a
  candidate to finish working and then go home and keep studying. People have
  families, and a personal life.  Companies may be skeptical to train their
  employees mostly because, I suspect, they will find better jobs elsewhere. I
  don't agree fully with this, but I suspect that the main point in terms of
  training is to fill a quota for "employee satisfaction". Training of employees
  should be pertinent, and punctual. You can't give an online account to
  employees and then tell them to study whatever they want in their spare time.
- *Do you name things appropriately?*: Naming is a big component of
  development. Choosing the proper name for an entity has a massive effect on
  productivity, discoverability and clarity of the code. It is a skillset that is
  not only a personal choice, but it also arises from established conventions
  from other APIs. Respecting these conventional names is extremely valuable.
- *Can you communicate your ideas effectively?* A confusing, blurred,
  explanation is wasting everyone's time. Presentation of ideas should be
  concise, clear, and to the point. When a person spends minutes trying to
  explain a concept that can be rendered with a single, simple phrase, you know
  that it's not the right candidate. On this, I amend the statement in saying that
  it's not only important for a candidate to be able to express information 
  effectively, but also to organise and classify information effectively.
- *Do you understand basic design patterns?* As 
- *Do you know how to debug effectively?*
- *Do you test your own code?*
- *Do you share your knowledge?*
- *Do you use the best tools for your job?*
- *Can you build an actual application?*

This excellent set of questions can help the hiring process, but as an interviewer it is
your responsibility to ask the candidate the appropriate questions. I am therefore proposing
the following "Test for interviewers".

- *Do you ask relevant questions at the interview?*

I lost count of how many times I've been asked to traverse a tree depth first at a job interview.
The problem I have with this kind of question is that they are irrelevant. I have 10 years
of experience in scientific coding, and never in my own career I had to traverse a tree depth 
first. If I have to, I use networkx. No job position for a senior level coding requires you to be
able to traverse a tree depth first.

- *Is the team involved in the interview process?*

Any hired person must mix well with the rest of the team. If management is excluding 
the team from the decision process, it is disregarding the most valuable contribute in
selecting the candidate, or asking the important questions considering the state of the
current codebase. Does management know we desperately need someone that is a wizard at
gdb, because we are plagued by low level crashes since a year? Will they keep that as 
a checkmark during the interview process?

- *Do you provide the appropriate tools for the interview (laptop, whiteboard)*

- *Do you ask the candidate to show and explain their own code project*
What is then, a relevant question for a job interview? There's only one. "Show me 
and explain me some code you wrote, and eventually add a small feature for me during the
interview". 

- *Do you verify if the candidate is up to date with the language he is going to use?*

- 

- eternal september of junior devs
- you can't cheat nature

