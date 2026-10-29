# Proposal guidance and meeting readiness

This reference contains the updated AI 1010 course guidance and shared proposal checks.
It does **not** assert that the separate board's deployed review prompt has been updated.
That prompt lives in the infrastructure application at `app/chatbot/review_prompt.md`.
If board feedback conflicts with current course guidance, preserve the student's ambition,
identify the conflict, and bring it to the instructor. Do not promise a pass, quietly change
the course assignment, or mark graded work as ungraded to bypass review.

## 1. AI 1010 — swing for the fences

The [final-project description](ai1010-final-project.md) is the course framing. Look for an
ambitious creation that makes something consequential possible in an area the student cares
about. Technical complexity and long hours are not substitutes for ambition. Prior coding
experience, model training, a dataset, a live model in the product, or worldwide originality
are not required. Software built with AI can qualify through the student's specification,
context, direction, decisions, testing, and judgment.

The proposal becomes the project's **README.md**, guiding the student's work as it develops.
Every project begins as a **private repo in `vanderbilt-ai-studies`**. Sharing the proposal
means adding the project to the [project board](https://bit.ly/vanderbilt-ai-projects), with its **repository URL in Full Details**, before
the **instructor scoping meeting**. It is ready for that conversation when
it explains the vision, why AI changes the opportunity, a possible approach, meaningful
evidence, and the questions needing instructor help. Open design questions are legitimate;
fabricated access, materials, time, or results are not. The meeting agrees the execution
plan; the student need not arrive with a finished implementation specification or prototype.

## 2. Shared proposal checks

Apply these without making the student abandon a strong idea merely because its approach
needs thought. For other programs, add the methods and depth their requirements call for.

- **Meaning and output.** Explain who benefits, what becomes possible or is investigated,
  and what someone could try or assess at the end. For AI 1010 this is a creation and a
  demonstration of its central promise; a generic topic or an essay about AI is insufficient.
- **Substantive work.** For AI 1010, make the student's application of course concepts,
  domain expertise, important decisions, and judgment visible. Agents can help write and
  build throughout; do not require unaided prose or hand-coded implementation. For data-science work, make
  the methods and evaluation substantive. Do not dismiss a web application merely because
  its final output is software rather than a predictive model.
- **Credible execution.** Identify available sources/tools, uncertain access, actual remaining
  time, and an early demonstration that tests the vision. Hours are the student's realistic
  estimate, not a fixed course quota. Avoid default first-month or twelve-week promises.
  If time is not yet known, ask before presenting a completed board submission; a meeting
  draft may label it as a question.
- **Evidence.** Give concrete signs of success, an appropriate comparison, and a situation
  that might expose weakness. Explain who judges quality and what needs verification.
  Do not claim a result the student has not observed or infer a cause from failure to beat
  a predictive baseline.
- **Permissions and responsibility.** Name sensitive health, student, personnel, financial,
  NDA, location, or human-subject information and proposed handling. Confirm appropriate
  permission rather than assuming personal possession or anonymization solves everything.
  Avoid dependencies on an uncertain approval. A board data flag calls for human review;
  it is not itself proof the student has done something wrong.
- **Ownership and assessment.** The student can explain their own contribution and choices.
  For AI 1010, grade the quality of problem definition, agent direction, source judgment,
  tests, diagnosis, iteration, and repository evidence before the finished outcome. A
  blocked run or unresolved feature can still show strong process when evidenced honestly.
  A polished product or a count of issues/commits does not by itself show that learning.
  See [process and assessment](process-and-assessment.md); do not invent numeric weights.
  The board's own-proposal path is solo. Team arrangements, reuse of another assignment,
  and credit for an extension are course decisions, not claims the helper can approve.
- **Honesty and contact.** Keep personal contact details and off-platform recruitment out
  of the board draft. Do not help plan projects whose purpose is harm, deception,
  nonconsensual surveillance, or evasion of safety controls. Never invent facts to make a
  proposal appear complete.

Being a beginner, informal writing, or overlap with another idea is not a defect. For AI
1010, if a proposal lacks ambition, ask what more consequential capability the student
would actually want to create. Do not guarantee grades or impose a technical novelty test.

## 3. AI 1010 meeting self-check

Use a compact check with evidence from the draft and a useful next question. Distinguish
**ready to discuss**, **factual gap**, and **decision for the meeting** rather than treating
every uncertainty as a rejection.

| Area | What to look for |
|---|---|
| Ambition | A meaningful new capability and a stretch the student can explain |
| Opportunity | What AI enables and what the student's knowledge contributes |
| Approach | A plausible creation and early demonstration; a plan to direct agents through a specification, persistent guidance, and bounded issues after the consult |
| Evidence | Concrete criteria, a comparison and difficult case; actual tests, preserved observations, and a plan to diagnose, revise, and retest |
| Questions | The actual uncertainties the instructor can help resolve |
| Practical preparation | A realistic time estimate or an explicit question, relevant permissions, and student ownership |
| Repository and README | Private repo in `vanderbilt-ai-studies`; proposal committed and pushed as root README.md |
| Board sharing | Project added to the [project board](https://bit.ly/vanderbilt-ai-projects); repository URL included in Full Details |
| Next step | Once the README and board entry are ready, [book the project consult](https://calendly.com/d/d3nk-8tg-2kt/ai-1010-project-consults); agree the plan before implementation and keep the README current |

For other programs, check the applicable shared criteria and program-specific methods,
evaluation, output, and time. A model verdict is not human project approval.

## 4. Worked AI 1010 example

This is an illustrative proposal, not facts to copy into a student's submission. In this
example the student has said they have their own application notes, public career guidance,
and four weeks at five hours per week. They have created a private organization repo named
`career-counselor`. That example URL below is illustrative, not a verified existing project.
Use a real student's actual repository, materials, and calendar.

**Title**

> A career counselor that learns from what happens between appointments

**Short description**

> Create a career-guidance workflow that turns a student's changing experiences into
> better next steps, so each conversation builds on the last instead of starting over.

**Full details**

> I want career guidance to grow with me as I try things, change my mind, and learn what
> matters to me. My ambition is a counselor that connects those experiences across time
> and helps me take the next step. I know what it feels like to receive advice that sounds
> reasonable but does not connect to my actual situation; I want that experience to shape
> what I build.
>
> I propose a skill-based workflow that uses public career-planning guidance and a saved
> record the user can inspect and correct. AI makes it possible to interpret an account
> of an interview or activity and connect it with earlier goals. I would decide what
> questions it should ask, which guidance it should use, and how to judge its suggestions.
> I have my own application notes and public guidance available. I will test shareable
> examples with fictional histories and keep my personal notes out of the repository.
>
> The demonstration will follow a user through two conversations with a meaningful change
> in between. I will compare the second conversation with the same request made without
> the saved history. Success means that the guidance accurately uses relevant prior
> information, responds when a goal changes, and proposes an action grounded in the user's
> stated situation. A deliberately conflicting history will test whether it asks for
> clarification instead of making assumptions. I will judge the results against these
> criteria rather than accept the agent's claim that it works.
>
> I have four weeks available and can spend about five hours per week. After the meeting,
> my first checkpoint will test whether retained information actually improves a later
> conversation. I will have Claude help draft SPEC.md and CLAUDE.md, turn the criteria into
> bounded issues, and build and test the workflow. I will review its plan and test evidence,
> save observed failures, and direct revisions and fresh retests. My final creation will
> include the workflow in its actual state, instructions, a demonstration or attempted run,
> and evidence of revisions and limits. I need help deciding what information should be
> saved and what would make the advice trustworthy enough to act on. This proposal is my
> project's README, which I will update as the work develops. I will add the project to the
> board before the meeting and agree the plan with the instructor before implementation.
>
> Project repository: https://github.com/vanderbilt-ai-studies/career-counselor

**Tags**

> career-guidance, agent-skills, workflows, memory, evaluation

**Submission setting**

Select Yes for the AI 1010 semester-final-project question when submitting this example.
This setting is separate from domain tags and is not a paragraph to paste into the proposal.

Why it prepares a useful meeting: the vision is meaningful, the student contributes
experience and judgment, and the demonstration tests the central promise. The sources,
time, evidence, and open questions are explicit. The final architecture is still a topic
for discussion; nothing claims that a live integration or a completed test already exists.
