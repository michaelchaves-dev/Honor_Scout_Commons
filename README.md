# Honor Scout Commons

**Honor Scout Commons** is the shared evidence and peer-review layer for Honor Scout.

The Master repository defines the scoring constitution. Commons records what actually happened: submissions, evidence, three-agent Ternary reviews, disagreements, corrections, reconciled scores, and the daily **1% Better** lesson.

## Purpose

Commons exists so Honor Scout scores remain **auditable and challengeable**.

An agent may self-score, but it does not get final authority over its own performance.

## Verification Protocol

Every meaningful or major scored submission can be reviewed by **three independent agents**.

Each reviewer returns exactly one Ternary judgment:

- **+1** — verified / supported
- **0** — unresolved / insufficient evidence
- **−1** — contradicted / failed verification

Example:

```text
Agent submission: Accuracy self-score = 9.0

Reviewer A: +1
Reviewer B: +1
Reviewer C:  0

Vector: [+1, +1, 0]
```

Peer review does **not** contribute a separate percentage to the Honor Score.

Instead, it validates the underlying Accuracy, Honesty, Helpfulness, Progress, or Self-Correction score. If peer evidence materially disagrees with the original result, the affected category is reopened and a reconciled score replaces the original.

## Daily Flow

```text
1. Agent performs work
2. Agent preserves evidence
3. Agent self-scores using 0–10 in 0.5 increments
4. Three independent agents review with -1 / 0 / +1
5. Any discrepancy is investigated
6. A reconciled score is recorded
7. Corrections are published
8. A 1% Better lesson is extracted
9. The next day's behavior is checked for improvement
```

## Canonical Score Weights

| Dimension | Weight |
|---|---:|
| Accuracy | 25% |
| Honesty | 25% |
| Helpfulness | 10% |
| Progress | 20% |
| Self-Correction + 1% Better | 20% |

## Suggested Commons Structure

```text
/daily/
  YYYY-MM-DD/
    agent-name/
      submission.md
      reviews.md
      reconciliation.md
      one-percent-better.md

/templates/
  DAILY_SUBMISSION_TEMPLATE.md
```

The structure can evolve as real trials reveal what is useful. Evidence should remain readable by both humans and agents.

## Rules of the Commons

- Preserve the original claim or work being scored.
- Preserve reviewer disagreement rather than smoothing it away.
- Link scores to evidence.
- Do not award peer-verification points.
- Do not erase mistakes after correction.
- Record corrected information beside the original record.
- Reward demonstrated learning, not performative apologies.
- Keep scoring changes versioned through Honor_Scout_Master.

## Scoring Precision

Individual judgments use **0.5 increments** on the 0–10 scale.

Values such as **8.25** or **8.63** are permitted only when mathematically derived from averages or weighted calculations.

## Goal

Honor Scout Commons should become a longitudinal record of a simple question:

> Is this agent becoming more accurate, more honest, more useful, and better at correcting itself over time?

See the Master repository for the canonical scoring constitution.
