# CPW 102: Infinite Scroll Code Rescue

**CS50P Week 2: Loops | Pairs | About 50 minutes**

Your team maintains a social media feed that loads three posts at a time.
Users report repeated posts, endless scrolling, and unexpected responses to input.
Your job is to investigate, explain, and repair the defects.

**Working code is only part of the submission.** Show how you reproduced each
bug, tested a hypothesis, and verified a repair in [debugging-log.md](debugging-log.md).
Write the log as you work. Short observations and small output excerpts are enough.

## Join your pair's branch
 your pair's branch

Everyone uses this shared class repository. Your instructor must give you write
access before you can publish a branch. Do not create a separate repository.

1. Open this repository with **Code > Open with GitHub Desktop**, then clone it.
2. One partner creates a branch from `main` named `pair-lastname-lastname`
   (for example, `pair-smith-jones`) and clicks **Publish branch**.
3. The other partner clones the same repository, clicks **Fetch origin**, and
   selects that pair branch under **Current branch**.
4. Open the repository in Visual Studio Code. Check your branch before editing.

Work only on your pair's branch. Keep `main` unchanged and leave other pairs'
branches alone. Use one driver at a time. If you switch computers, commit and push
before switching; the next driver fetches and pulls before editing.

## Start the investigation

Run the intentionally buggy [feed.py](feed.py) with Python 3:

```text
python feed.py
```

Use `python3` or `py` if that is your system's Python command. No packages or
network access are needed to run it. Enter `n` to quit, or use Ctrl+C if needed.

Investigate all three reports:

- **#104:** “Every time I scroll, I get the same three posts again.”
- **#107:** “The feed never tells me I've reached the end.”
- **#112:** “I typed something other than y or n, and it loaded more posts.”

For each report:

1. **Reproduce:** Record exact inputs, what happened, and what should have happened.
2. **Hypothesize:** Before editing, write a possible cause and a prediction you can test.
3. **Investigate:** Trace relevant variables, add temporary diagnostic prints, or
   inspect values with a debugger. Record what the evidence tells you.
4. **Repair:** Make a focused change and explain why it addresses the cause.
5. **Verify:** Repeat the failing input and try a related boundary case. Record
   predicted and actual results, including any failure that remains.

An incorrect first hypothesis is fine. Keep it and explain what changed your mind.
One defect may hide another; note which version you tested and return to blocked
reports after an earlier repair. Remove temporary diagnostic prints before submission.

Alternate driver and navigator during the investigation. Each partner must lead
at least one report, and both must be able to explain the repairs. Budget about
35 minutes for investigation and repair, 10 for final checks, and 5 for submission.

## Required behavior

The repaired program must:


1. Load the first page automatically. Each `y` loads the next page in order.
2. Keep earlier posts in the feed. Each source post appears once within each
   displayed feed; redrawing earlier posts on later screens is expected.
3. Display the full accumulated feed and its correct count after each load.
4. On an empty page, print `No more posts.` and end without asking again.
   A short final page is still displayed; the next `y` checks for an empty page.
5. End immediately when the user enters `n`, without loading another page.
6. Accept `y` and `n` regardless of capitalization or surrounding spaces.
   For anything else, print `Please enter y or n.` and ask again without
   fetching a page, changing the feed, or advancing the page number.
7. Print `Session ended.` once when the session ends normally.

Keep the supplied `posts`, `PAGE_SIZE`, and `fetch_page(page)` helper for the
normal run. Repair the loop logic rather than hard-coding the eight-post answer.
You may add loops and conditions. No classes, networking, or external libraries
are needed. The supplied helper uses a list slice: `posts[start:end]` returns
items from `start` up to, but not including, `end`. Page numbers begin at zero.
Treat that helper as provided infrastructure.

The feed is fixed during a session, and each source post is distinct. Handling
duplicate data from a server, network failures, or invalid page sizes is outside
this lab. Use a positive integer page size.

For the default eight posts, successive displayed counts are **3, 6, 8**.
After that, one more `y` prints `No more posts.` and `Session ended.`.

## Final checks

Run each row in a fresh session. Predict the result before running; record brief
results in the log. These checks supplement the before/after evidence for each bug.

| Scenario | Setup and inputs |
| --- | --- |
| Read the full feed | Original data; `y`, `y`, `y` |
| Quit early | Original data; `n`; also try a fresh run with `y`, `n` |
| Invalid input | Original data; `maybe`, an empty answer, `y`, `n` |
| Capitalization and spaces | Original data; ` Y `, ` N `, including spaces |
| Empty feed | Temporarily set `posts = []`; run without entering input |
| One post | Temporarily keep only the first post; enter `y` |
| Exact page boundary | Temporarily keep the first six posts; `y`, `y` |
| Different page size | All eight posts with `PAGE_SIZE = 4`; `y`, `y` |

If an unexpected prompt appears, stop with Ctrl+C and record the failure.
Restore all eight posts and `PAGE_SIZE = 3` before submitting.

## How your debugging is assessed — 10 points

| Evidence | Points |
| --- | ---: |
| Reproducible reports with expected versus actual behavior | 2 |
| Investigation evidence that tests hypotheses and supports diagnosis | 3 |
| Accurate root-cause explanations and focused repairs | 2 |
| Before/after verification and boundary testing | 2 |
| Individual explanation during a brief instructor checkout | 1 |

The first nine points are shared by the pair; the checkout point is individual.
You earn credit for sound investigation even when a repair is incomplete.
During checkout, each partner will predict and explain what a small code or input
change would do before running it. Your partner should not answer for you.

## Submit

Commit and push `feed.py` and `debugging-log.md` to your pair branch using GitHub
Desktop. Open **one pull request per pair** into this repository's `main`.
Title it `Infinite Scroll Code Rescue — Name and Name`. Name both partners,
summarize one root cause and its repair, and list any remaining issues.
**Leave the pull request open; do not merge it.** Each partner submits the same
pull request URL in Canvas. Have your code and log ready for the individual checkout.

This is a course lab aligned with CS50P Week 2, not an official CS50 assignment.
