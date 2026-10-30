# Project proposal helper

A Claude skill that helps you go from an interest or a rough idea to a project proposal
for the **Vanderbilt AI Studies project board** and, for AI 1010, the instructor meeting
before building an ambitious final project.

It's for AI 1010, AI minor, MSAI and MSDS students proposing **their own** project. To
browse projects other people have posted, use the board itself:
<https://bit.ly/vanderbilt-ai-projects>.

New to the board? Read the student guide first:
[onboarding/student-guide.md](onboarding/student-guide.md)
([PDF](onboarding/student-guide.pdf)).

## Use it in Claude Desktop

Open the **Claude Desktop app**, select the **Code** tab, and ask:

> Use the project-proposal skill from https://github.com/vanderbilt-ai-studies/project-proposal to help me develop my AI 1010 final project.

Claude can handle the skill setup and guide you through developing your idea, creating
your private project repo, and writing its README. Tell it what you care about or bring
an idea you already have.

**Skill repository:** [vanderbilt-ai-studies/project-proposal](https://github.com/vanderbilt-ai-studies/project-proposal)

## AI 1010: three phases, three steps each

| Set up | Build | Test and improve |
| --- | --- | --- |
| 1. Define the problem | 1. Plan the work | 1. Test the actual solution |
| 2. Define success | 2. Build a working piece | 2. Diagnose and revise |
| 3. Prepare the project | 3. Inspect and steer | 3. Try it with someone and share |

Testing can send you back to building or setup. Permissions, privacy, and source judgment
apply throughout. Claude helps you focus on your current phase and next step.

Set up includes your private repo, proposal README, board entry, and project consult.
Begin implementation after the consult and agreement on the plan. See the
[phase guide](.claude/skills/project-proposal/references/process-and-assessment.md)
for the details. Other programs retain their own project requirements.

## Write issues that steer the development agent

When you begin drafting, reviewing, or splitting development issues, this helper
calls its bundled [agent-issue-authoring skill](.claude/skills/project-proposal/references/agent-issue-authoring/SKILL.md).
It uses your project's purpose, specification, actual files, and decisions to help
define a bounded outcome, observable acceptance criteria, checks, and stopping
conditions. It does not start implementation merely because you ask for a draft.

Read the [one-page guide and canonical skill repository](https://github.com/vanderbilt-ai-studies/agent-issue-authoring).
The full issue helper ships inside the project-proposal skill folder, including
its references, so it works when that folder is copied on its own. For AI 1010,
implementation still follows your consult and the agreed plan; an issue backlog
is not a prerequisite for the meeting.

## What you get

A conversation that helps you:

1. explore what you would attempt if technical implementation no longer stopped you
2. connect the ambition to your expertise and what AI makes possible
3. plan a demonstration of the central promise, with materials, evidence, and realistic time
4. once the purpose, intended user, initial approach, and name are established, have Claude
   **create the private project repository in `vanderbilt-ai-studies`**, generate and push
   its initial **`README.md`**, and develop that README into the proposal guiding your work
5. reuse that proposal for the **Submit a Project** entry, including the repository URL
   in **Full Details**, and prepare questions for the instructor meeting

**AI 1010: swing for the fences.** Your project can be software built with AI, skills,
an agent workflow, an interactive experience, or another agreed creation. No predictive
dataset or model training is required. Read the
[final-project description](.claude/skills/project-proposal/references/ai1010-final-project.md).
AI 1010 is **agent-forward**: agents can help draft, plan, build, test, and revise.
You define the ambition, approve the decisions, and judge the evidence. Give the agent a
clear objective and have it loop toward that objective: plan, act, test, inspect, revise,
and repeat until the agreed criteria are met or it reaches an agreed limit or blocker.
Grading emphasizes
**process over the finished outcome**: problem definition, agent direction, source judgment,
meaningful tests, diagnosis, and iteration. See the
[process and assessment guide](.claude/skills/project-proposal/references/process-and-assessment.md).
Every ambitious feature need not work to demonstrate strong learning; polished output alone
is not enough. Other programs retain their own requirements for methods, depth, and evaluation.

It never submits anything for you. Sign in at the [project board](https://bit.ly/vanderbilt-ai-projects), choose **Submit a Project →
"A student, for myself"**, and paste each section in. A person reviews every student
proposal.

**Sharing your proposal means adding your project to the [project board](https://bit.ly/vanderbilt-ai-projects).** Put the private
organization repository link in the board entry's **Full Details**. The one-page proposal
lives in your project's README and guides your work; you do not need a separate document.

AI 1010 students: add the board entry before your **15-minute instructor/team meeting**.
When your README and board entry are ready,
[sign up for your AI 1010 project consult](https://calendly.com/d/d3nk-8tg-2kt/ai-1010-project-consults).
Complete the meeting and agree the project plan **before implementation begins**. Creating
the private repo and writing its README are preparation for that meeting. Follow the
board's submission/booking order and the currently posted course dates; board acceptance
alone does not replace this conversation.

---

*Maintainers:* this repository distributes `.claude/skills/project-proposal/`, including
the AI 1010 course guidance. Keep any maintained infrastructure copy in sync. The board's
separate deployed reviewer is `app/chatbot/review_prompt.md` in the infrastructure repo;
changing this skill does not change that service. Review and align that prompt separately
rather than claiming the helper guarantees board approval.
