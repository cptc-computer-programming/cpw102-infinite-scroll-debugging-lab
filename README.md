# CPW 102: Infinite Scroll Incident

## GitHub Setup

Clone this shared repository and create one branch per pair from `main`:

```text
bugfix/lastname-lastname
```

Leave `main` and other pairs' branches unchanged.

## Expected Program Behavior

Infinite scroll loads more content as you reach the bottom of a feed, keeping earlier posts visible. Try the [infinite-scroll demo](https://infinite-scroll.com/demo/full-page/) and watch new posts appear as you scroll. In this program, entering `y` simulates scrolling to load the next page.

The program should:

- Show the first three posts when the program starts, without asking the user to scroll first.
- When the user enters `y`, add the next three posts in order. If fewer than three remain, add those remaining posts.
- After loading posts, show all posts loaded so far and how many there are. Keep earlier posts visible, but do not add the same post twice.
- After displaying the last posts, the next `y` should print `No more posts.` and end the session. If there are no posts when the program starts, print that message and end without asking the user to scroll.
- When the user enters `n`, end the session without loading any more posts.
- Accept uppercase and lowercase answers, including answers with spaces before or after them. For example, `Y` and ` y ` should both work like `y`.
- For any other answer other than case-insensitive `y` or `n`, print `Please enter y or n.` and ask again. 
- Whenever the session ends through quitting or reaching the end of the feed, print `Session ended.` exactly once.

## User bug report

Users submitted the following tickets with reports of buggy behavior! 

> “Every time I scroll, I see the same three posts added again instead of new ones.”

> “I keep scrolling, but I never reach the end. The app never tells me there are no more posts.”

> “I typed ‘maybe’ instead of ‘y’ or ‘n’, and it loaded more posts anyway.”

## Your Task

Debug the program, logging your work as you go. Make code changes to fix the above bugs. 

## Debugging Log

Keep a chronological log of **every debugging step as you take it**, including unsuccessful attempts. Choose your own investigation methods and evidence. Log enough to make your instructor confident that you have thoroughly investigated and solved the users' bug(s).

## Submission

Push `feed.py` and `debugging-log.md` to your branch. Open one pull request into `main`, name both partners, and **leave it open—do not merge**. Only one partner need submit the pull request URL in Canvas.
