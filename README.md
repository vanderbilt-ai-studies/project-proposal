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

## Use it with Claude Code

```sh
git clone https://github.com/vanderbilt-ai-studies/project-proposal.git
cd project-proposal
claude
```

The skill is in `.claude/skills/`, so Claude Code loads it as soon as you start it in this
folder. Then just talk to it:

- *"I like music and know a bit of Python. What could I propose?"*
- *"Here's my idea. Is it good enough for my semester project?"*
- *"Help me write my project proposal."*

You can also start it directly by typing `/project-proposal`.

## Use it on claude.ai instead

Download this repo as a ZIP, then zip just the `.claude/skills/project-proposal` folder so
that `SKILL.md` sits at the top of the zip. Upload that zip under **Settings → Capabilities
→ Skills**. If your class Claude Team already has it installed, you don't need to do this.

## What you get

A conversation that helps you:

1. explore what you would attempt if technical implementation no longer stopped you
2. connect the ambition to your expertise and what AI makes possible
3. plan a demonstration of the central promise, with materials, evidence, and realistic time
4. prepare your proposal and questions for the instructor meeting
5. reuse that work to draft the **Submit a Project** fields and check for missing facts

**AI 1010: swing for the fences.** Your project can be software built with AI, skills,
an agent workflow, an interactive experience, or another agreed creation. No predictive
dataset or model training is required. Read the
[final-project description](.claude/skills/project-proposal/references/ai1010-final-project.md).
Other programs retain their own requirements for methods, depth, and evaluation.

It never submits anything for you. You sign in at the board, choose **Submit a Project →
"A student, for myself"**, and paste each section in. A person reviews every student
proposal.

AI 1010 students: share your proposal before your **15-minute instructor/team meeting**.
Complete the meeting and agree the project plan **before you begin building**. Follow the
board's submission/booking order and the currently posted course dates; board acceptance
alone does not replace this conversation.

---

*Maintainers:* this repository distributes `.claude/skills/project-proposal/`, including
the AI 1010 course guidance. Keep any maintained infrastructure copy in sync. The board's
separate deployed reviewer is `app/chatbot/review_prompt.md` in the infrastructure repo;
changing this skill does not change that service. Review and align that prompt separately
rather than claiming the helper guarantees board approval.
