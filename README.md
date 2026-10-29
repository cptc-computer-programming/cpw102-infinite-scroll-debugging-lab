# CPW 102: Infinite Scroll Code Rescue

**CS50P Week 2: Loops | Pairs | About 50 minutes**

Your team maintains a social media feed. It loads three posts at a time as the
user scrolls. The previous developer left a working program with broken behavior.
Repair it using loops, conditions, and lists. No packages or internet connection
are needed to run the program.

## 1. Join your pair's branch

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

## 2. Reproduce the reports — 10 minutes

From the repository folder, run this with Python 3:

```text
python 03_execution/main.py
```

If your system uses `python3` or `py`, use that command instead of `python`.
The starter is intentionally buggy. Use `n` to end a run, or Ctrl+C if needed.

Investigate these reports:

- **#104:** “Every time I scroll, I get the same three posts again.”
- **#107:** “The feed never tells me I've reached the end.”
- **#112:** “I typed something other than y or n, and it loaded more posts.”

Record observations and a repair plan in [Product Requirements](02_planning/01_product_requirements.md)
and [Engineering Design](02_planning/02_engineering_design.md). A bug may hide
another bug; return to a report after making your first repair.

## 3. Repair the feed — 25 minutes

Edit [03_execution/main.py](03_execution/main.py). Switch driver and navigator
halfway through. The navigator traces the state and checks each change.

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

## 4. Verify — 10 minutes

Complete the [test scenarios](04_testing/01_testing_cases.md), predicting each
result before running it. Include input/output evidence and rerun failed cases.
Restore the original eight posts and `PAGE_SIZE = 3` after boundary tests.

## 5. Ship — 5 minutes

Commit and push your code, planning notes, and test evidence to your pair branch
using GitHub Desktop. Open **one pull request per pair** from your branch into
this repository's `main`. Title it `Infinite Scroll Code Rescue — Name and Name`.
Name both partners, explain one root cause and its repair, and list any remaining
issues. **Leave the pull request open; do not merge it.** Each partner submits
that same pull request URL in Canvas. Be ready to demonstrate a repair.

## Files

| Location | Purpose |
| --- | --- |
| `01_initialization/` | Learning goals and starting point |
| `02_planning/` | Pair investigation and design worksheets |
| `03_execution/main.py` | Intentionally buggy starter; edit this file |
| `04_testing/` | Manual test scenarios and evidence |
| `05_shipping/` | Submission checklist |

This is a course lab aligned with CS50P Week 2, not an official CS50 assignment.
