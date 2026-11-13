# Learning Lab · UXplosion

CSEN 909 Milestone 3 coded web prototype, based on the supplied project description and UXplosion Milestones 1 and 2.

## Project links

- **GitHub repository:** https://github.com/hamsashouman/UXplosion-HCI-Milestone3
- **Deployed prototype (team-provided link):** https://hamsashouman.github.io/UXplosion-HCI-Milestone3/

The deployed link may show an older version until the updated `dist/` files are published. Verify it in a private/incognito browser session before submission.

## Run locally

No installation or build is required. Extract the ZIP. Open a terminal in its folder and run:

```sh
python -m http.server 8000 --directory dist
```

On Windows, use `py -m http.server 8000 --directory dist` if Python is available as `py`. On macOS/Linux, `python3` may be used. Open http://localhost:8000 in your browser.

The interface uses HTML, CSS and JavaScript only. Google Fonts is optional: system sans-serif fonts are used if unavailable.

## Deploy

Upload this folder to a public repository in your own GitHub account. For a static host, set the publish/output directory to `dist` and leave the build command empty. Alternatively deploy the contents of `dist` through any static host. Verify the deployed link in a fresh browser before submitting it.

The privately hosted review copy is not evidence of public examiner access. Configure the final submitted deployment audience deliberately.

## Demo sequence

Use Help & support → Reset example workspace to restart. Student: Upload an exam → choose subject/language → sample or real file preview → submit. Teacher: Assessment review → correct OCR question 2 to 12 → confirm answers → override marks → confirm grades → decide gap and support flag → edit and release feedback. Student: notification → confirmed marks and feedback. Teacher: Support plans → create goal/target/activity/date → complete activity → save → review later sample → record outcome.

## Walkthrough Video

A 2–4 minute recorded demonstration of the
UXplosion Milestone 3 prototype is available here:

[Watch or download the walkthrough](YOUR_RELEASE_URL)

## Included files

- dist/index.html, style.css, app.js: runnable prototype.
- submission/UXplosion-Six-HTDs.drawio: six editable HTD pages, preserving Milestone 2 task numbering.
- submission/HTD-Task-Designs.md: the same task actions and plans in text.
- submission/Walkthrough-Script.md: timed 2–4 minute recording script.
- submission/Submission-Checklist.md: remaining submission steps.

## Implemented interactions

Student dashboard, Mathematics sample and exam language selection (English/German), file validation (PNG/JPG/WEBP/PDF, maximum 10 MB), preview, submission, status, released grades, question marks, feedback, practice recommendations, notifications and progress. Teacher dashboard and student profile entry, side-by-side sample OCR editing, grading explanations and mark overrides, independent gap/flag decisions, evidence timeline across assessments, feedback editing and release, support-plan goal/measurable target/activity/date/completion and follow-up outcome.

## What makes UXplosion different

The Milestone 2 teacher interview identified a limitation of grade-only tracking: a learner can improve in overall marks while repeatedly misunderstanding the same concept. The prototype demonstrates two human-in-the-loop responses:

1. **Evidence-Based Learning Gap Tracker:** a timeline of exact question-level misconceptions across teacher-confirmed assessments. Current AI-suggested gaps remain separate until the teacher reviews the verified answer, acknowledges the evidence, and confirms or dismisses the suggestion. Historical confirmed evidence is retained when a new suggestion is dismissed.
2. **Learning Gap Intervention Planner (Support plans):** a teacher specifies an improvement goal, a measurable target (3, 4, or 5 correct comparisons out of five), an activity, and a follow-up date. Once the activity is marked complete, the teacher reviews clearly labelled fictional follow-up evidence and records an outcome. The prototype validates recorded outcomes against both activity completion and the chosen target.

These are simulated interface workflows, not live student assessment or automated diagnosis. The teacher makes the final decisions.

## Prototype boundaries

All AI extraction, grading and historical matching are simulated. Actual uploaded files are local previews only and never transmitted. Uploaded file contents are not interpreted; the teacher review remains explicitly labelled sample data. File previews exist only until refresh; thereafter a sample scan is displayed. Prototype decisions persist in browser localStorage. Student/teacher switching demonstrates views without authentication and is not a security boundary. A new exam can be uploaded after the current exam is released. Earlier released exams remain accessible in the student and teacher assessment histories. Historical quiz examples are fictional. The runnable demonstration focuses on Mathematics; other subjects are outside this packaged sample. Historical grades and evidence are fictional examples, not research results.

## Merged safeguards (10 November 2026)

The merged build uses the expanded assessment history, German samples, responsive layouts, evidence acknowledgement, measurable support targets, and editable HTDs from the revised LearningLab version, while restoring the following checks from the earlier UXplosion build:

- **Teacher-controlled release:** the release function itself refuses publication unless an exam has been submitted, OCR verified, grades confirmed, and both learning-gap and support-flag suggestions confirmed or dismissed. Confirmed learning-gap evidence must also have been acknowledged.
- **Intervention consistency:** outcome recording requires a completed activity and a reviewed follow-up. An outcome cannot be marked Successful below its measurable target, or Requires further support when the displayed gap is Resolved. If an already-successful plan is changed to incomplete or its new target is unmet, the outcome reverts to Ongoing.
- **Assessment history:** newly released exams are archived when another starts, preserving grades and feedback. This replaces the older single-demo reset behavior, rather than discarding prior results.

The website source download inside `dist/` is regenerated from this merged source.

## Validation

JavaScript syntax checked with Node. The revised LearningLab source reported Chromium testing for the core workflow. This merged build was independently syntax-checked and exercised with focused regression tests for the restored release and intervention safeguards. The deployed website was not updated by packaging this ZIP; verify the final hosted link and downloadable source after deployment.

## Team Members

**Team Name:** UXplosion  
**Course:** CSEN 909 – Human Computer Interaction  
**Project:** AI-Powered Personalized Assessment and Learning Gap Detection for Children  
**Milestone:** 3 – Interactive Prototype

| Team Member | Student ID | Tutorial | Email |
|---|---|---|---|
| Malak Amr Abdelmonem Elarnaouty | 58-0357 | T-01 | malak.elarnaouty@student.guc.edu.eg |
| Hamsa Ahmed Shoumann | 58-3186 | T-12 | hamsa.shouman@student.guc.edu.eg |
| Aly Walid Aly Amin Youssef | 58-1992 | T-08 | aly.amin@student.guc.edu.eg |
| Malak Wael | 58-0773 | T-08 | malak.waelabdelhami@student.guc.edu.eg |
| Mohamed Alaa | 58-9368 | T-08 | mohamed.elmetwaly@student.guc.edu.eg |

## Attribution

Created with assistance from ChatGPT. Submit the full conversation and all other AI prompts used, as required by the course. The source includes no real pupil records or private team contact details.

## Fixes in this revision

- Repeatable assessment uploads after teacher release, with archived grades, answers, and feedback.
- Student-facing learning focus and supportive explanation of teacher-confirmed support flags.
- Follow-up target checking: cannot mark an intervention Successful when the example result falls below the measurable target.
- Explicit selection and teacher confirmation of fictional follow-up scenarios.
- Assessment title field, upload-file reset, and mobile layout checks.
- German sample paper, OCR text and grading prompts use German throughout.
- Question 2 grading suggestion and default mark follow the verified answer (12 is correct; 17 is not).
- Teacher must explicitly acknowledge reviewing evidence before confirming the current learning gap.
- Support plans have a separate measurable target and revised HTD labels.
- The website source download is bundled in `dist/uxplosion-milestone3-source.zip`.
- This ZIP updates the local source package; it does **not** automatically update the already hosted ChatGPT site.


### Assessment history and student dashboard
The progress chart and summary cards use the same three fictional historical results and any additional teacher-released assessments. A teacher-confirmed fictional follow-up is shown as a labelled example. Notifications persist in browser storage and remain linked to archived assessments. German sample submissions provide German default feedback, which the teacher can edit.
