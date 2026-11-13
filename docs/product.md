# Product decisions

[한국어](product.ko.md) · [← README](../README.md)

The decisions that shape Career Workspace, and why. Each one was made as the product owner, often after trying the first version and changing my mind.

## Who it's for

Job seekers in Korea, especially people changing roles or early in their careers, who have plenty of material (old résumés, 자기소개서, certificates, project notes) but no clear picture of what it adds up to, which roles they can reach, or how to present themselves for each.

## The core idea: one unbiased pool, many tailored documents

**Decision:** everything the person has goes into one *career pool* once, and stays there **as given**. No rewriting, no summarising, no role tags or ranking. Tailoring happens only when a document is written for a specific role.

**Why:** the same experience reads differently for a data analyst role and a product manager role. A pool that has already been "optimised" for one direction loses material the other needs.

How it works for the person:
- Drop files of any kind. AI extracts facts into a strict profile with fixed categories (work, projects, education, certificates, skills…).
- A file about something already in the profile fills in the gaps instead of creating a duplicate.
- A value that **disagrees** with one already recorded is never overwritten. It waits for the person's decision, and it shows how many files say each version.
- Every change a file made is logged and can be undone.

## AI proposes, the person decides

**Decision:** AI never silently changes what the person owns.
- Résumé and document edits from AI appear as marked proposals (added in green, removed in red) with 적용 / 취소, one by one or all at once.
- Comments on several lines go to AI together, and the result comes back as one proposal.
- Applying a change never saves by itself. Saving makes a dated version that can be restored.

## AI stays bound to the person's records

**Decision:** in a résumé, facts (organisations, dates, degrees, scores) are copied from the records by code. AI writes only the headline, key strengths and achievement lines, and **every line must cite the records it comes from**; a line that cites nothing is dropped.

**Why:** an AI-written résumé that sounds great but claims things the person can't back up is worse than useless in an interview.

A résumé also holds **only what fits the role**. AI chooses the records that support it and hides the rest (one click shows them again), and nothing is stretched to cover a gap. Instead, a **준비도 (readiness)** score shows what's missing, with a "level up" list of what to do, most important first.

## Fit must never change randomly

**Decision:** role fit and posting scores are **plain matching**, not AI judgement.
- Profile records carry competency tags from one shared vocabulary.
- Fit is tag matching (with years for experience), so the same profile always gives the same fit.
- Scores for job postings are worked out on the person's own computer, without AI.

**Why:** a number that changes each time you ask can't be trusted, and people make real decisions with it.

## Career paths as a ladder, and as a game

- Roles are generic career ladders (e.g. data analyst → senior → lead → head of data), each stage with its own requirements and salary range.
- Stages above the entry are locked until the profile has the experience they ask for, so the list shows the step a person can take *now* and the route ahead.
- The outlook combines official statistics (KOSIS employment and wage data, the national employment forecast), credited as the source requires, with AI research that is clearly labelled as such.
- *My paths* turns the chosen roles into a stage map with requirements as circles and stars, a readiness estimate, and a to-do list.

## Job postings: shared, respectful, fair

- **One collector, not every user scraping:** postings are collected once a day by a single collector and downloaded by every copy of the app. Users make no requests to job sites.
- **Only sources that allow it:** public job boards and company career pages whose terms and robots rules allow collection. Sources that don't welcome it are listed and left alone. Career sites on Workday were dropped because of its terms.
- **Core facts only:** title, company, location, experience, type, dates and a link back to the company's own page, never full descriptions.
- **Fair order:** equally fitting postings are shuffled in each person's own order, so everyone isn't sent to the same few.
- **Legal caution recorded:** a Korean court case on copying job postings was reviewed. Legal advice is planned before any sale.

## Applying: guidance, never automation

**Decision:** the app guides each page of an application form with marks showing what to fill in, but **never types or submits anything** on a site.

- Answers can be copied with one click; the person pastes and submits.
- Known fields (contact details, education, saved essays) are marked instantly by rules with no AI. Only the rest goes to AI, and what AI explains about a form is learned locally as a rule for next time.
- **Login, sign-up and identity-check pages are never sent to AI**, not even their field names. Other pages send field names only, never what's typed.
- Site logins are kept encrypted on the computer. A copied password is cleared from the clipboard after 30 seconds.

## Users never handle an API key

**Decision (changed mid-project):** the first version asked each user for their own AI API key. I replaced it with an account: AI requests go through a small server of mine, so the key never ships in the app, each account has daily and monthly limits, and I can see costs per feature.

## Design: visual, simple, progressive

- Less text, more pictures and chips.
- AI results appear as they arrive (suggestions one by one, files growing in a folder) instead of after a long wait.
- Similar functions reuse the same icon, button and layout everywhere. The owner app keeps a library of them so new screens don't invent new ones.

## Things I decided *not* to build (yet)

- Typing into or submitting application forms for the user.
- Sharing learned form rules across users (needs consent and a server).
- Automatic updates to AI-researched roles (only on request, so nothing changes under the person).
- Google sign-in and payments: planned, not built.
