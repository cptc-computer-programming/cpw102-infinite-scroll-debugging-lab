# CPW 102: Infinite Scroll Code Rescue

**CS50P Week 2 · Pairs · About 50 minutes**

## Incident INC-204

Users report repeated posts, a feed that never finishes loading, and unexpected
scrolling after invalid input. Investigate the intentionally buggy [feed.py](feed.py),
repair it, and document the incident in [debugging-log.md](debugging-log.md).

Clone this shared repository and create one branch per pair from `main`:
`pair-lastname-lastname`. Both partners use that branch; alternate who drives.
You need write access. Leave `main` and other pairs' branches unchanged.

```text
python feed.py
```

Use Python 3; no packages are needed. Use Ctrl+C to stop a stuck run.

## Expected behavior

- Load the first page automatically; `y` loads the next page. Display the full
  accumulated feed and count, with each source post appearing once per display.
- An empty page prints `No more posts.` and ends without another prompt.
  Display a short final page normally; the next `y` checks for an empty page.
- `n` ends immediately. Accept either letter regardless of case or surrounding
  spaces. Other input prints `Please enter y or n.` and asks again without
  loading posts or changing the page or feed.
- Every normal exit prints `Session ended.` once.

Repair the loop logic; keep the supplied helper and original data. Test beyond
the normal case, including empty data, page boundaries, quitting, and invalid
input. Restore the eight posts and page size 3 after testing.

## Evidence and assessment

Keep a chronological log of **every debugging step as you take it**, including
unsuccessful attempts. Choose your own investigation methods and evidence.

Of 10 points: reproduction **2**, evidence-based investigation **3**, cause and
repair **2**, before/after and boundary verification **2**, individual explanation
**1**. The first nine points are shared. Each partner will briefly predict and
explain a new case. An incorrect initial hypothesis does not lose credit when
you test it and follow the evidence.

## Handoff

Push `feed.py` and `debugging-log.md` to your pair branch. Open one pull request
into `main`, name both partners, and **leave it open—do not merge**. Each partner
submits the same pull request URL in Canvas. Remove temporary diagnostic prints
before submitting.
