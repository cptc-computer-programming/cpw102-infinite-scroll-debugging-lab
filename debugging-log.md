# Debugging Log

**Partners:**

Keep entries short and write them during the investigation. Preserve initial
hypotheses even if they turn out to be wrong. Label evidence as original starter
or describe any earlier repairs already applied.

## Report #104: Repeated posts

**Investigation lead / navigator:**

**Version and setup tested:**

**Reproduce:** Exact inputs, expected behavior, and actual behavior.

**Initial hypothesis (before editing):** Possible cause and what you predict you
will observe if it is correct.

**Investigation evidence:** A short variable trace, diagnostic output, or debugger
observation. Label the point in the loop where you observed each value.

```text

```

**Conclusion:** Did the evidence support your hypothesis? What changed your mind,
or what will you investigate next?

**Root cause and repair:** Identify the relevant code and explain why the change
fixes the behavior. If unfinished, explain what remains unresolved.

**Before/after verification:** Repeat the reproduction input. Include a short
excerpt showing the original failure and the repaired result.

```text
Before:

After:

```

**Related boundary test:** Setup and inputs, prediction before running, actual
result, and whether it passed. You may reference a final-check row below.

## Report #107: End of the feed

**Investigation lead / navigator:**

**Version and setup tested:**

**Reproduce:** Exact inputs, expected behavior, and actual behavior.

**Initial hypothesis (before editing):** Possible cause and what you predict you
will observe if it is correct.

**Investigation evidence:** A short variable trace, diagnostic output, or debugger
observation. Label the point in the loop where you observed each value.

```text

```

**Conclusion:** Did the evidence support your hypothesis? What changed your mind,
or what will you investigate next?

**Root cause and repair:** Identify the relevant code and explain why the change
fixes the behavior. If unfinished, explain what remains unresolved.

**Before/after verification:** Repeat the reproduction input. Include a short
excerpt showing the original failure and the repaired result.

```text
Before:

After:

```

**Related boundary test:** Setup and inputs, prediction before running, actual
result, and whether it passed. You may reference a final-check row below.

## Report #112: Unexpected input

**Investigation lead / navigator:**

**Version and setup tested:**

**Reproduce:** Exact inputs, expected behavior, and actual behavior.

**Initial hypothesis (before editing):** Possible cause and what you predict you
will observe if it is correct.

**Investigation evidence:** A short variable trace, diagnostic output, or debugger
observation. Label the point in the loop where you observed each value.

```text

```

**Conclusion:** Did the evidence support your hypothesis? What changed your mind,
or what will you investigate next?

**Root cause and repair:** Identify the relevant code and explain why the change
fixes the behavior. If unfinished, explain what remains unresolved.

**Before/after verification:** Repeat the reproduction input. Include a short
excerpt showing the original failure and the repaired result.

```text
Before:

After:

```

**Related boundary test:** Setup and inputs, prediction before running, actual
result, and whether it passed. You may reference a final-check row below.

## Final checks

Use the scenarios in the README. Record predictions before running. For failures,
include the observed result and any rerun. Full terminal transcripts are unnecessary.

| Scenario | Predicted result | Actual result / brief evidence | Pass or fail |
| --- | --- | --- | --- |
| Full feed | | | |
| Quit immediately | | | |
| Quit after one scroll | | | |
| Invalid and blank input | | | |
| Capitalization and spaces | | | |
| Empty feed | | | |
| One post | | | |
| Exact page boundary | | | |
| Different page size | | | |

**Remaining issues:**

**Original data restored and diagnostic prints removed:**
