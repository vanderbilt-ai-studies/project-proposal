# The bar a student proposal has to clear

Every submission to the board is read first by a model and then, for a student's own
proposal, always by a person. Both apply the rules below. This file is the student-facing
version of `app/chatbot/review_prompt.md`; when that prompt changes, change this.

The reviewer is **not** judging whether the idea is good. They are deciding whether the
posting is complete, honest and safe, and whether the project can be done. A modest project
that clears the bar is approved. An ambitious one that does not is sent back with a note.

## 1. What gets a proposal sent back

| Flag | What it means | How the draft avoids it |
|---|---|---|
| **incomplete** | A field with no content: placeholders ("TBD", "will figure out"), a description that restates the title, details too thin to tell what the student would do day to day. Also: **no time commitment anywhere**, since a student sees no schedule fields. | Say the hours a week and the number of weeks in the details. Describe the work, not the topic. |
| **unclear** | From the posting alone you cannot answer: what will the student build, investigate or produce? | One sentence: "I will hand in ..." |
| **mismatch** | The posting contradicts itself: scope that cannot fit the time, dates that do not make sense, claims of no experience needed beside a hard requirement. | Check the scope against the hours stated. |
| **data** | The work touches patient or health records, identifiable student records, personnel or financial records, anything under an NDA or export control, or human subjects without a mention of IRB. Flagged even when it sounds handled, so a person checks. | Prefer data that raises none of these. If it does, name it and say how it is handled. Never leave it implicit. |
| **contact** | Asks anyone to email a personal address, send a CV off-platform, pay for anything, or hand over personal information. | Leave contact details out entirely. The board handles contact. |
| **unsafe** | Purpose is to harm, deceive, surveil people without consent, or evade a legal or safety control. | Do not draft it. Say why. |
| **criteria** | Clear and honest, but the project fails the bar below. | Reshape it before submitting. |

## 2. What is not a problem

Do not "fix" these; the reviewer is told not to flag them.

- Being a beginner. Most AI 1010 students are first-years. A proposal that says so is fine.
- A modest or unglamorous project. "Sort these 40,000 images" is a good project.
- Informal writing and typos.
- Overlapping another project on the board.
- Not naming a supervisor. Student proposals are self-supervised by design; the AI 1010
  check-in is the oversight. Do not add a supervisor to make it look complete.

## 3. The bar for every proposal

All five must hold.

1. **It fits the time.** Roughly a semester at the hours stated, with something useful
   inside the first month so that a struggling project still ends with a partial result.
2. **The materials exist now.** Data, access, accounts, hardware, in hand at the start.
   "We'll have the dataset in October" is the single most common way a student project dies.
3. **A named person will meet them.** For a student's own proposal this is satisfied by the
   student and the check-in. Nothing to add.
4. **There is something to show at the end.** A tool, an analysis, a decision, a write-up.
   A negative result counts when it is stated clearly with evidence.
5. **Real use of AI or data science.** Raw data collection with no modelling, analysis or
   evaluation is not a project for this board.

## 4. The stricter bar for a graded semester project

When the student answers **Yes** to "Is this your semester final project?" (AI 1010) or
"Is this your Capstone project?" (MSDS), all of the above **and**:

6. **Doable by someone who started this semester.** The core of the work within reach of a
   capable beginner who is getting help. Not "they'll pick it up".
7. **The AI or data work is the point.** A web app with a sentiment API on the side is a
   web-development project. The interesting decisions are in the modelling, the data, or the
   evaluation.
8. **The deliverable is defined now.** One sentence, before starting. Discovering the goal
   along the way is a research posture and does not survive a deadline and a grade.
9. **Nothing hangs on an external approval.** IRB, a data-sharing agreement, a partner's
   sign-off. If it might not arrive, the project cannot depend on it.
10. **Individually assessable.** A student proposal is solo, so this holds automatically.
    Do not propose a team.
11. **Small enough that failure is informative.** The likely bad outcome is "this approach
    did not work, and here is the evidence", never "there is nothing to show".

## 5. Self-check table

Fill this in for the student before handing over the draft. One line per row.

| # | Criterion | Met? | Where the draft shows it |
|---|---|---|---|
| 1 | Fits the time, first-month milestone | | |
| 2 | Materials in hand now | | |
| 4 | Deliverable in one sentence | | |
| 5 | AI / data science is real work | | |
| 6 | Doable by a beginner (graded only) | | |
| 7 | The AI/data work is the point (graded only) | | |
| 9 | No external approval on the critical path (graded only) | | |
| 11 | Failure would still be informative | | |
| – | Time commitment stated in the details | | |
| – | No sensitive data, or named and handled | | |
| – | No contact details or off-platform steps | | |

## 6. A worked example

An AI 1010 student who runs, uses Strava, and cannot find a project about running on the
board. Their own export is data in hand; nothing here needs approval or touches anyone
else's records. Each block maps to one form field.

**Title**

> What actually predicts my running pace: two years of my own Strava data

**Short description**

> Use two years of my own Strava runs plus historical weather to find out which factors
> explain my pace, and whether a model can predict a run's pace better than my own recent
> average.

**Full details**

> I have run with Strava since fall 2024 and have about 380 recorded runs. The question I
> want to answer is simple and personal: what actually explains how fast I run on a given
> day? I assume it is heat and sleep. I would like to find out whether that is true.
>
> Data in hand today: my full Strava export (a CSV of every activity plus one GPX file per
> run, downloaded this week), which gives date, distance, moving time, elevation gain, and
> per-second heart rate for roughly 300 of the runs. For weather I will use the Open-Meteo
> historical API, which is free and needs no account, to pull temperature, humidity and wind
> for each run's start time and location. I have already pulled a week of it to confirm it
> works. All of this is my own data. It contains my home location, so I will strip
> coordinates before anything leaves my laptop and will not publish the raw files.
>
> The work is a supervised regression problem with a small dataset, which is where the
> interesting decisions are. I will build features from each run (distance, elevation per
> km, temperature, humidity, days since last run, a rolling four-week volume), fit a
> baseline that predicts pace from my trailing average, then compare linear regression,
> a regularised model and gradient-boosted trees using time-ordered cross-validation so I
> never train on the future. I will report error in seconds per kilometre, look at which
> features matter, and check for leakage such as heart rate, which is measured during the
> run and would not be available before it.
>
> Deliverable: a written report with the cleaned dataset description, the model comparison,
> and a plain-English answer to what predicts my pace, plus the notebook that reproduces
> every figure.
>
> By the end of the first month I will have the cleaned, joined dataset and the baseline
> with its error, so even if nothing beats the baseline I have a result. I expect to spend
> five to seven hours a week for the twelve remaining weeks of the semester.
>
> If no model beats my trailing average, that is itself the finding: day-to-day pace is
> mostly training load and not weather, and I will show the evidence for it.

**Tags**

> regression, time-series, feature-engineering, sports, personal-data

**Is this your semester final project?**

> Yes. It is scoped for one person over twelve weeks, the data is in hand, and the
> deliverable is defined.

Why it clears the bar: the data exists now and is the student's own; the deliverable is one
sentence; the modelling and evaluation decisions are the substance; the first-month
milestone is a baseline with an error number; the time is stated even though the form has no
box for it; the likely negative result is named and still worth handing in; the only
sensitivity (home location) is named and handled.
