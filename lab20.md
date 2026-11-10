# Lab 20 — Readiness record
Linda Li · November 10, 2026

## D — Can a stranger reach the decision?
**Not yet from the inspected portfolio work alone.** The available Lab 15 app supplies a portfolio engine and controls, but the inspected files do not constitute a complete Project 2 submission. This is a preparation audit, not a partner cold run.

## R — Readiness audit

| Required item | Evidence and status |
|---|---|
| Operable Python web app | [Lab 15 app](https://github.com/llindali/lab15/blob/main/app.py) exists; select **Apex project**, since the default is Meridian training. Web runtime not verified in this preparation environment: Streamlit is absent. |
| README run instructions | [Lab 15 README](https://github.com/llindali/lab15/blob/main/README.md) lists installation and startup commands; no final Project 2 repository or single-command result route was identified. |
| Visible decision numbers | Lab 15 README has allocations, estimates, risk and window sensitivity. Baseline engine rerun independently reproduced the all-month Apex numbers below. |
| Mandate | [Lab 13 project mandate](https://github.com/llindali/lab13/blob/main/lab13.md): Apex, $50M, CPI + 4.5% net over rolling ten years, 70/30 benchmark, $1.5M buffer, long-only and 5% issuer cap. Lab 15 uses planning inflation 2.5%, fees 0.25%, and a provisional fund/Treasury exemption. Client approval and look-through interpretation remain unresolved. |
| Two baselines and constrained portfolio, each with mandate verdict in app | Not complete in inspected app: it displays as-loaded and edited optimized portfolios. Training engine baseline functions alone do not provide the required Apex baseline comparisons and rule verdicts in the app. |
| Point-in-time signal and data card | [Lab 17 DGS10 card](https://github.com/llindali/lab17/blob/main/README.md) is a separate candidate-data audit. Integration into portfolio decisions and a reproducible timestamp-aware signal rule are not shown in Lab 15. |
| Stress and stop condition | Lab 15 documents estimation-window and equity-return sensitivity and a proposed 10-point stability tolerance. Full required estimates/window/costs/constraints stress evidence is not assembled in a final project. |
| Decision memo | No final `docs/decision-memo.md` was identified in inspected Lab 15 files. A prior lab's recommendation is not silently relabeled as the final memo. |
| Validation and AI use / locked record | No final `docs/validation-and-ai-use.md` or verified AI-off prediction committed before its run was identified. Prior AI-assisted sensitivity results do not satisfy the locked record. |
| Videos 1–3 and transcripts | No final links/transcripts identified in inspected project-related files. Recording is the student's task. |
| Manifest | Final Project 2 manifest not identified. This readiness record links only verified existing evidence. |
| Week 12 must-fix list | Not located in the inspected sources; no studio feedback is invented. |
| Due date | Must be read from the Brightspace assignment header; the course GitHub page does not provide the enforced date. |

### Baseline engine rerun — AI-assisted, not the partner run
Source: [Lab 15 tree at 10f8ffdb7936a8255c368533e576ebd257de4a62](https://github.com/llindali/lab15/tree/10f8ffdb7936a8255c368533e576ebd257de4a62).

Downloaded the existing `portfolio.py` and `prices.csv` without modifying their contents. Ran the following from their directory with Python and pandas:

```python
import portfolio as p
s, c = p.estimate_prices("prices.csv")
s = [(name, estimate - 0.0025, volatility) for name, estimate, volatility in s]
print(p.search_mix(s, c, 0.07, [0], 0.03))
```

| Decision number | Reproduced value |
|---|---:|
| SGOV / BND / VT | 55% / 0% / 45% |
| Annual arithmetic net return estimate | 7.1461375% |
| Annualized volatility estimate | 6.7698422% |
| Reserve weight / initial value | 55% / $27.5M |
| Modeled net-return hurdle / minimum reserve | 7% / 3% |

Weights total 100%, are nonnegative, and meet the modeled estimated-return hurdle and reserve minimum. This does not establish the ten-year return objective, look-through issuer compliance, or client approval. The estimates use the existing September 2021–September 2026 vendor-adjusted price file, not newly fetched or independently authenticated market history.

An environment dependency check failed with `ModuleNotFoundError: No module named 'streamlit'`. Pandas engine execution succeeded. This is not a defect demonstrated in the source app and is not a partner finding. The published installation command is `python -m pip install -r requirements.txt`; app startup is `python -m streamlit run app.py`. No successful browser run is claimed.

## I — Partner cold run (in class)
Not performed. Partner opens the actual Project 2 repository in their own folder using only its README, without coaching.

Record here after the activity:
- Project 2 repository and tested commit:
- Partner:
- Exact command:
- First failure, or explicit clean-run observation:
- Elapsed time:
- Location of visible result and mandate verdict:

## V — Locked Changed-Input Record (in class, AI closed for prediction)
Not performed. No new stress run was executed for this record, and no AI-generated prediction is presented as the student's.

Before rerunning, the student records the selected load-bearing input, old/new values and units, expected direction of decision numbers, and expected decision effect. Commit and push that prediction first. Preserve the prediction commit link, baseline output, changed output, actual decision effect, and explanation after the run. Prior Lab 15 sensitivities are historical context only.

## Explain the code (in class, six minutes, no AI)
Not performed. Use the actual Project 2 block that produces the decision number; explain line by line and answer the partner's question from the code. No partner question or answer is invented here.

## E — Fix one thing (after the partner run)
Pending the actual first failure. Record the fix, pushed commit, and partner rerun; if the run is clean, record the actual clean outcome and that no fix was needed. Preparation findings above are not substituted for that activity.

## Decision line
**Reject adoption of the currently available process; reconsider a research pilot only after the missing Project 2 evidence is assembled, the complete app passes an independent cold run, and the client confirms the mandate assumptions.** No live allocation is authorized by this readiness review.

The earlier Lab 15 55% SGOV / 45% VT mix remains a reproduced research result, not a committee-approved allocation. A final allocation range cannot be established by a readiness audit of an incomplete submission.

## Reflect (in class)
Pending the actual discussion: record what the partner's cold run revealed and what the student commits not to change before the deadline.

## Checkout
Submit the individual GitHub links to [this record](https://github.com/llindali/lab20/blob/main/lab20.md) and the [README](https://github.com/llindali/lab20/blob/main/README.md) through Brightspace → Quizzes → Lab 20 after the actual activities. Check the Project 2 due date in the Brightspace assignment header. This preparation does not claim quiz submission.

Sources: [Lab 20](https://github.com/CinderZhang/FIN43900-Fall2026/blob/main/lessons/week-13/lab-20-project2-readiness.md) · [Project 2 requirements](https://github.com/CinderZhang/FIN43900-Fall2026/blob/main/projects/project-2-investment-management-application.md).
