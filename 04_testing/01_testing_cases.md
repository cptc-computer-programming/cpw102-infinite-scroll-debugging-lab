# Test Scenarios

Run each case in a fresh session with `python 03_execution/main.py` from the
repository root. Before running, predict displayed posts/counts, prompts, and
termination. Check against the [README](../README.md).

For boundary cases, edit only the stated data or page size. Restore the original
eight posts and page size 3 before submitting. If a broken version asks for
unexpected input, stop with Ctrl+C and record the failure.

## 1. Full feed

**Setup:** Original eight posts, page size 3.

**Input:** `y`, `y`, `y`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 2. Quit immediately

**Setup:** Original data.

**Input:** `n`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 3. Quit after one scroll

**Setup:** Original data.

**Input:** `y`, `n`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 4. Invalid input

**Setup:** Original data.

**Input:** `maybe`, an empty answer (Enter), `y`, `n`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 5. Capitalization and spaces

**Setup:** Original data.

**Input:** ` Y `, ` N ` (include the spaces)

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 6. Empty feed

**Setup:** Temporarily replace the posts list with `posts = []`.

**Input:** No input should be needed.

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 7. One post

**Setup:** Temporarily keep only the first post; page size 3.

**Input:** `y`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 8. Exact page boundary

**Setup:** Temporarily keep the first six posts; page size 3.

**Input:** `y`, `y`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**

## 9. Different page size

**Setup:** Restore all eight posts; temporarily set `PAGE_SIZE = 4`.

**Input:** `y`, `y`

**Expected results (before running):**

**Actual input/output evidence:**

```text

```

**Pass / Fail and why:**

**Rerun evidence, if needed:**
