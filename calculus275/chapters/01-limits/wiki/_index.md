# Wiki Index — Limits

**Last compiled:** 2026-09-01
**Sources ingested:** limits.pdf, MATH275-Week01-Lecture-Notes.pdf
**Topics covered:**
- [The Notion of a Limit](notion-of-a-limit.md)
- [One-Sided Limits](one-sided-limits.md)
- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limit Laws](limit-laws.md)
- [Infinite Limits and Vertical Asymptotes](infinite-limits.md)
- [Limits at Infinity and Horizontal Asymptotes](limits-at-infinity.md)
- [The Squeeze Theorem](squeeze-theorem.md)
- [Continuity](continuity.md)
- [The Intermediate Value Theorem](intermediate-value-theorem.md)
- [The Sequential Criterion for Limits](sequential-criterion.md)

## Source Structure

`limits.pdf` is a OneNote export titled "Week 0 Video - Limits" (Tuesday, August 8, 2023). It opens with its own section list:

1. The notion of a limit
2. Limit laws
3. Infinite limits
4. Limits at infinity
5. Squeeze theorem
6. Continuity

The nine wiki pages above split those six sections where the source's own material warranted it: §1 is split into the definition, one-sided limits, and the DNE examples; §6 is split into continuity and the Intermediate Value Theorem (stated at the end of the source but not listed in its opening section list).

`MATH275-Week01-Lecture-Notes.pdf` is a 6-page typeset handout, "Week 1: Limits, Continuity, and the IVT — Lecture summary and problem-solving clinic," attributed to instructor Zheng Zhu for Blocks 01, 02, 07, 08, MATH 275 Fall 2026. It assumes the Week 1 videos have been watched and is structured around worked examples at three marked levels: `CORE` (basic), `STUDIO` (worksheet-calibrated), `ANALYSIS` (proof/trickier). It closes with a five-item exit check.

It contributed two topics `limits.pdf` does not cover — [Computing Finite Limits](computing-finite-limits.md) (the obstruction/technique table, conjugates, absolute-value splitting) and [The Sequential Criterion for Limits](sequential-criterion.md) — plus new sections merged into seven existing pages.

## Extraction Notes

The source is handwritten ink with pasted graphs — one 194-inch-tall page carrying only 57 characters of machine-readable text. All content was transcribed visually from the rendered page.

One discrepancy is recorded in [Infinite Limits](infinite-limits.md): a pair of limits is written `x → 2` twice where the accompanying graph shows vertical asymptotes at both `x = 2` and `x = -2`. Transcribed as written and flagged in place.

`MATH275-Week01-Lecture-Notes.pdf` has a clean text layer and needed no visual transcription. Its PDF metadata records Creator "OpenAI Prism", Producer "xdvipdfmx" (a LaTeX toolchain), creation date 2026-08-31.

### Conflicts between sources

Where the two sources disagree, both statements are recorded with citations and the conflict flagged in place — neither is silently preferred.

| Topic | Conflict |
|---|---|
| [Intermediate Value Theorem](intermediate-value-theorem.md) | `limits.pdf` concludes `a < c < b` (open, endpoints excluded) and requires `f(a) ≠ f(b)` with `N` **strictly** between; Week 1 concludes `c ∈ [a,b]` (closed, endpoints allowed) and says `N` "lies between". |
| [Limit Laws](limit-laws.md) | `limits.pdf` puts two provisos on the quotient law (`M ≠ 0` **and** `g(x) ≠ 0` near `a`); Week 1 states only `M ≠ 0`. |
| [Squeeze Theorem](squeeze-theorem.md) | Notational only — the sources swap which letter names the middle function. |

## Compile History

| Date | Action | Sources Added |
|------|--------|---------------|
| 2026-09-01 | initial compile | limits.pdf |
| 2026-09-01 | recompile | MATH275-Week01-Lecture-Notes.pdf |
