# Vanderbilt AI Studies: project proposal helper

When the user begins authoring, reviewing, scoping, or splitting project issues,
the project-proposal skill must call its bundled
`references/agent-issue-authoring/SKILL.md`. Work in the user's project, preserve
the proposal/consult state, and follow the issue helper's draft-versus-execution
boundary. The bundle's canonical repository is
https://github.com/vanderbilt-ai-studies/agent-issue-authoring.

This repo exists for one job: helping a Vanderbilt AI Studies student turn an interest or a
rough idea into a project proposal for the [AI Studies project board](https://bit.ly/vanderbilt-ai-projects).

Whatever the student opens with, including a plain "hi", use the `project-proposal` skill in
`.claude/skills/project-proposal/`. Once the student has established the purpose, intended
user, initial approach, and project name, carry out the initial repo-generation step:
create a private project repo in `vanderbilt-ai-studies`, generate and push its initial
`README.md`, and develop that README into the proposal. Do not stop with an offer to do
this later. Follow the skill's access-blocker handling. Prepare the board entry with its
repo URL in Full Details. Keep student project files
out of this helper checkout. Do not change the helper itself unless explicitly asked.
The student submits to the board. For AI 1010, the instructor meeting precedes implementation.
Agents may help with every stage. For AI 1010, organize the work into **Set up**, **Build**,
and **Test and improve**, with three steps per phase as defined in the skill. Focus on
the current phase and next useful action. Testing can return the work to building or setup.
Guide the student toward specifications, concise persistent guidance, bounded issues,
meaningful tests, and evidence-based revision. AI 1010 assessment
emphasizes the student's decisions and process over the finished outcome; follow the skill's
process-and-assessment reference rather than inventing a success-only grading rule.
