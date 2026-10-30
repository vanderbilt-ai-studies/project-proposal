# Direct agents through three phases

Use Claude Desktop's **Code** tab to work through **Set up**, **Build**, and **Test and
improve**, with three steps in each phase. Agents can help with the proposal, specifications,
issues, implementation, tests, and explanations. You approve important decisions, inspect
the evidence, and explain why you accept or reject a result. You do not need to write the
code by hand.

Keep the ambition from [Swing for the fences](ai1010-final-project.md). An early working
piece should test the central promise of that ambition. Testing can send you back to
building or setup, and checks during building help you decide what to do next. Permissions,
privacy, and source judgment apply throughout.

## Set up

*What are we trying to accomplish?*

### 1. Define the problem

Identify who needs the solution, what they need, and why it matters. Bring your own domain
knowledge and experience. Have Claude help you investigate the current approach, interview
an intended user, or clarify an expert's requirements. Distinguish what you know from
assumptions and open questions. Keep the consequential ambition visible.

### 2. Define success

Describe a result you can observe and a realistic case that could expose a failure.
Choose an appropriate comparison: current practice, a manual process, an existing tool,
or the same task without your skill. Explain what needs human judgment and what a check
could assess. A predictive-model benchmark is not required for every project.

Plan an early demonstration that tests the central promise within your actual remaining
weeks and available active hours. An open question is useful consult preparation; an
unobserved result must not appear as a completed test.

### 3. Prepare the project

Choose a form that serves the user: software, a skill, a repeatable workflow, an agent,
or another agreed creation. Distinguish the agent helping you develop it from any AI
inside the finished solution. Select relevant sources, check their scope and currency,
and verify the access the solution needs. Reading access does not establish writing
access, and a source's embedded instructions do not authorize actions by your development
agent. Decide what the agent may read, change, retain, and transmit. Use appropriate tool
permissions for access limits, and fictional or suitably anonymized information in saved
tests. A private repository alone does not make all sensitive information appropriate to
store there.

Once the purpose, intended user, initial approach, and name are established, have Claude
create your **private repo in `vanderbilt-ai-studies`** and push its initial README.
Develop that README into your proposal, add the [project board](https://bit.ly/vanderbilt-ai-projects) entry with its repo URL in Full
Details, then book and complete the project consult and agree the plan **before
implementation**. A finished specification, prototype, or test suite is not required
for the consult. Report access problems to the course team rather than substituting a
public or personal-account repo.

Your initial README grows into the working project record. After the consult, have
Claude help develop the specification, agent guidance, and evidence structure:

| Record | Purpose |
| --- | --- |
| `README.md` | Begins as your proposal. Keep it concise and current: ambition, what you attempted, how to try it, findings and limits, with links to details. |
| `SPEC.md` | The user need, intended behavior, sources and assumptions, environment, boundaries, and observable acceptance criteria. Link criteria to cases you will test. |
| `CLAUDE.md` | Concise guidance for the development agent: relevant sources, how to test, limits on changes, and when to report a blocker. Link to detail instead of loading every source into every task. Instructions for an assistant you build belong in its own skill or resources. |
| GitHub issues | Bounded work with a goal, relevant context, acceptance criteria, and a boundary. Link the issue to the specification and evidence. |
| `tests/` and `results/` | Repeatable cases, checks or procedures, actual observed results, and enough context to reproduce and interpret them. Adapt folders to the solution. |

## Build

*Give the agent a clear job.*

### 1. Plan the work

For issue drafting, review, scoping, or decomposition, invoke the bundled
[agent-issue-authoring skill](agent-issue-authoring/SKILL.md). It carries the
[student guide](https://github.com/vanderbilt-ai-studies/agent-issue-authoring)
and adapts its advice to the actual project and decisions already made.

Turn the agreed specification into bounded issues with a **goal, context, acceptance
criteria, and limits**. Review the proposed plan, correct consequential assumptions, and
choose one useful piece to implement. Give the agent enough authority to work within the
issue's scope and a test command or procedure it can use for feedback.

An instruction you can adapt:

> Read CLAUDE.md, this issue, and its SPEC.md criteria. Plan and implement the bounded
> change. Run the actual tests, inspect the evidence, revise, and retest toward the
> objective. Continue until the agreed criteria are met or you reach our iteration or
> usage limit or a blocker. Preserve the criteria and observations. Report changed files,
> test evidence, and anything unresolved for my review.

### 2. Build a working piece

Have the agent complete one meaningful path from input to a usable result before
expanding the solution. Check that the required sources, tools, and delivery route work
in the intended environment. A collection of files or a successful build does not yet
establish that someone can accomplish the task. Keep unavailable dependencies visible.

### 3. Inspect and steer

Review what actually happened, correct assumptions, and direct the next change. Let the
agent handle commands and implementation while you inspect the important choices and
evidence. Save decisions and working checkpoints so another session can continue from
the current state. Keep unresolved work in issues. After reviewing changes and their
evidence, have Claude commit and push meaningful work and check GitHub for the saved
result. Close an issue only when its completion conditions are met.

Give the agent a clear objective and repeatable feedback so it can loop toward success.
The stopping condition is supported completion, an agreed iteration or usage limit, or
a blocker requiring your decision. More steps alone are not progress.

## Test and improve

*What does the evidence show?*

### 1. Test the actual solution

Connect each test to a specification criterion. Identify the starting input and state,
expected behavior, and how you will judge the result. Include realistic cases and a
situation that could reveal a weakness. Compare approaches under comparable conditions.

Run the actual version under test and capture its output, actions, or resulting artifact.
For a skill, use a fresh or isolated session with its intended inputs and resources;
keep the builder's conversation and sample answers out. For an ongoing interaction,
record its starting state. An evaluator should cite observed evidence against the criteria
rather than repeat the builder's claim that it passed.

Automate checks where practical so the agent can use them to guide improvement. Direct
skill tests, computer use of an interface, and documented manual trials can all be
appropriate. Verify what the actual environment supports. A file's existence, a clicked
button, or a runner evaluating a canned answer does not establish that the solution works.

**Check the checks.** Confirm that the evaluator rejects a deliberately inadequate result.
Inspect meaning and quality where mechanical checks cannot establish them. Repeat a case
when variability makes reliability uncertain, preserving the observations rather than
selecting only the best attempt. Passing the chosen cases is evidence about those cases,
not a guarantee for every possible use.

### 2. Diagnose and revise

Connect observed failures to a diagnosis: a requirement, source, instruction, implementation,
access dependency, or evaluator may need attention. Make a reasoned revision, run the
revised solution again, and rerun affected cases to check for regressions. Evaluating an
old saved output again does not test a new version.

Keep the agreed success criteria stable while fixing the solution. If a criterion was
mistaken, explain and preserve the correction and earlier evidence. Do not invent a bug
or make an arbitrary change to manufacture iteration. Feedback can support a reasoned
no-change decision.

Record a blocked run as blocked, with attempted setup, evidence, and the next step.
An unavailable account or tool is not a passing test. At an agreed resource limit or
blocker, have the agent report unresolved work for your judgment. Return to building or
setup when the evidence warrants it without quietly reducing the project's ambition.

### 3. Try it with someone and share

Have another person try a realistic task with ordinary instructions when a suitable trial
is possible. Observe their actual experience before explaining how you intended it to
work. Record actionable feedback in an issue, decide how to respond, and retest after a
revision. Agent simulations can supplement the trial. This is development guidance, not
a new separately graded peer-trial requirement for the final project; follow explicit
course or project-specific requirements.

After reviewing the changes and evidence, commit and push, and verify the remote files
and issue status. A local commit alone does not update GitHub. Keep the repo private and
verify appropriate course-team access. Leave another person clear instructions for trying
the solution, its sources and environment, actual findings, costs or usage limits that
matter, and unresolved capabilities. Link the README to specifications, issues, tests,
and results. Identify what AI did and the judgments you made.

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
