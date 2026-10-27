# Direct agents and show how you learned

Use Claude Desktop's **Code** tab to specify, direct, test, and improve an agent-built
solution. Agents can help at every stage: drafting the proposal and specifications,
writing guidance and issues, building the solution, creating and running tests, analyzing
failures, and preparing your account of the work. You do not need to write the code
by hand. Your responsibility is to approve the important decisions, inspect the evidence,
and explain why you accepted or rejected a result.

Keep the ambition from [Swing for the fences](ai1010-final-project.md). The purpose of
this process is to make a serious attempt possible and learn from what actually happens.
Create your private organization repo and proposal README, add the project to the board
with its repo link in Full Details, and complete the project consult before implementation.
A finished specification, working prototype, or completed test suite is not a prerequisite
for that conversation.

## Use the repository to direct the work

After the consult, ask Claude to help establish:

| Record | Purpose |
| --- | --- |
| `README.md` | Begins as your proposal. Keep it concise and current: ambition, what you attempted, how to try it, findings and limits, with links to details. |
| `SPEC.md` | The user need, intended behavior, sources and assumptions, environment, boundaries, and observable acceptance criteria. Link criteria to cases you will test. |
| `CLAUDE.md` | Persistent guidance for the development agent: what to read, the issue to work on, how to test, limits on changes, and when to stop and report. |
| GitHub issues | Bounded work with a goal, relevant context, acceptance criteria, and a boundary. Link the issue to the specification and evidence. |
| `tests/` and `results/` | Repeatable cases, checks or procedures, actual observed results, and enough context to reproduce and interpret them. Adapt folders to the solution. |

Read the proposed specification and agent plan. Correct assumptions and decide which
criteria actually express your goal. Delegate a bounded issue, review the work and tests,
and ask the agent to revise and retest. After review, have it commit and push; check GitHub
for the saved work. Close an issue when its completion conditions are met and keep
unresolved work visible. Do not lower the ambition simply to get a green test report.

An instruction you can adapt in Claude Desktop:

> Your objective is to implement the capability in this issue and meet its SPEC.md
> acceptance criteria. Read CLAUDE.md, make a plan, and work toward that objective in a
> loop: act, run the tests, inspect the evidence, revise, and repeat. Continue until the
> agreed criteria are met or you reach our iteration or usage limit or a blocker. Stay
> within the issue's boundaries, preserve the criteria and observations, and report
> evidence of what you achieved and anything unresolved so I can review it.

## Test the actual solution

Define success before judging a result. Each meaningful test identifies its criterion,
starting inputs and state, expected behavior, and how you will judge it. Include realistic
cases and a situation that could expose a weakness. Use a comparison appropriate to your
idea; this need not be a predictive-model benchmark.

**Loop with an objective.** Give the agent a clear objective from the specification,
observable success criteria, and a way to evaluate its progress. Ask it to plan, act,
inspect the result, revise its approach, and keep working toward that objective. The
loop ends when evidence supports meeting the agreed criteria or it reaches an agreed
limit or blocker; running more steps alone is not progress.

**Automating tests is encouraged.** Tests and feedback help the agent judge each attempt
and decide what to do next in that loop. Direct skill tests, computer use of an interface,
and documented manual trials can all be appropriate. Test the chosen environment rather
than assume a successful build works everywhere. Let Claude handle code and commands
while you inspect the choices and evidence in the desktop app.

Run the actual version under test, capture its output or actions, and evaluate those
observations. For skills, use a fresh or isolated test session with intended inputs and
resources; keep the builder's conversation and sample answers out. For an ongoing
interaction, record the starting state. An evaluator should cite evidence against the
criteria, not simply repeat the builder's claim of success.

Check the checks: can they reject an inadequate result? Explain what an automated check
can and cannot establish, and inspect meaning or quality where a mechanical test cannot.
A canned output, a file's existence, or a clicked button alone does not establish that the
solution works. Re-evaluating an old output does not test a newly revised solution.

Preserve observed failures. Connect a failure or feedback to a diagnosis, a reasoned
revision, and a new run; rerun other affected cases to check for regressions. If a
criterion itself was mistaken, explain the correction and retain the earlier evidence.
Do not invent a bug or make an arbitrary change just to manufacture iteration. Feedback
can also support a reasoned no-change decision. A peer trial can help answer questions about the actual experience.

Record a blocked run as blocked, including the attempted setup, evidence, and next step.
An unavailable account or tool is not a passing test. At an iteration or usage limit,
have the agent report unresolved results for your judgment.

## How the work will be assessed

**Assessment emphasizes process over the finished outcome.** We will look at how well
you turned an ambitious idea into work an agent could carry out, tested the attempt,
interpreted evidence, and used it to improve your approach.

| Area | Evidence we will examine |
| --- | --- |
| Problem and specification | A meaningful ambition, a clear user need, observable success, sources, assumptions, and boundaries that guide real work. |
| Agent direction | Decisions you approved or corrected, persistent guidance, and bounded issues that help an agent carry out the specification. |
| Source judgment | Relevant context selected and checked; missing or conflicting information handled honestly. |
| Testing and evaluation | Meaningful tests of the actual solution, checks capable of finding failures, and your understanding of their limits. |
| Diagnosis and iteration | Observations connected to reasoned decisions, revisions and retests, or an evidenced explanation for leaving something unchanged. |
| Repository evidence and explanation | A current README linked to specifications, issues, meaningful pushed commits, tests, observed results, and clear limits. |

Functionality is evidence to investigate and explain, not a substitute for this process.
Every ambitious feature need not succeed for you to demonstrate strong learning. A
failed experiment or blocked capability can still provide assessable evidence when you
show what you tried, what happened, how you responded, and what you learned. Do not claim
an untested capability works. A polished product, large codebase, long chat, or high count
of issues and commits is not by itself evidence of learning.

Submit the creation in its actual state with instructions or a demonstration, and use
the README to lead us through the important decisions and their supporting records.
Identify what AI did and the judgments you made. An unsupported account of effort or an
untested idea alone cannot establish a strong process; failed work does not automatically
earn full credit. Detailed rubric weights and levels remain to be set.

This approach adapts the [Career Services repository workflow](https://github.com/vanderbilt-ai-studies/career-services-project/blob/main/docs/repository-process.md),
[testing guidance](https://github.com/vanderbilt-ai-studies/career-services-project/blob/main/docs/testing.md),
and [assessment guidance](https://github.com/vanderbilt-ai-studies/career-services-project/blob/main/docs/assessment.md)
for the final project.
