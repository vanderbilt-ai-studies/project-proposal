# Project proposal helper

A Claude skill that helps you go from an interest or a rough idea to a project proposal
for the **Vanderbilt AI Studies project board**, written to pass review the first time.

It's for AI 1010, AI minor, MSAI and MSDS students proposing **their own** project. To
browse projects other people have posted, use the board itself:
<https://bit.ly/vanderbilt-ai-projects>.

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

1. find an idea, if you don't have one yet
2. check it has data you can use today, a clear deliverable, and real AI work
3. scope it to a semester, with a first-month milestone
4. draft every field of the **Submit a Project** form, ready to paste
5. check the draft against the same bar the reviewer uses

It never submits anything for you. You sign in at the board, choose **Submit a Project →
"A student, for myself"**, and paste each section in. A person reviews every student
proposal.

AI 1010 students: once your project is approved, book your 15-minute check-in from the
board.

---

*Maintainers:* the source of truth is `.claude/skills/project-proposal/` in the AI Studies
infrastructure repo. Change it there, then copy it here.
