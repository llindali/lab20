# Lab 20 — Project 2 Readiness
Linda Li · Updated November 10, 2026

ChatGPT assisted with the evidence review and documentation. Student attestations and partner reports are attributed below; AI did not witness the partner run. Education, not investment advice.

## D — Decision and repository
Actual Project 2: [llindali/project2](https://github.com/llindali/project2). This supersedes the earlier preparation audit of Lab 15, which preceded identification of the standalone project.

**Reject live adoption, with a live allocation range of 0–0%; reconsider only after policy and evidence gaps are resolved and robustness checks pass without lowering the return hurdle.** The research mix is 55% SGOV / 0% BND / 45% VT.

## R — Readiness evidence
| Item | Location / current status |
|---|---|
| App and run instructions | [README](https://github.com/llindali/project2/blob/main/README.md), [app](https://github.com/llindali/project2/blob/main/app.py), [engine](https://github.com/llindali/project2/blob/main/engine.py). Partner reports a clean run and the control checks recorded below. |
| Visible decision numbers | [visible_output.json](https://github.com/llindali/project2/blob/main/visible_output.json), also summarized in README and memo. |
| Mandate, two baselines and constrained portfolio | [Decision memo](https://github.com/llindali/project2/blob/main/docs/decision-memo.md): equal weight, 70/30 tradable proxy, constrained mix. Full issuer/risk/ten-year compliance remains unverified. |
| Point-in-time signal and data card | [Data card](https://github.com/llindali/project2/blob/main/docs/data-card.md), referenced by project README. Prospective snapshot signal; no historical-vintage performance claim. |
| Stress and stop conditions | Memo and validation: estimates, window, fees and constraints; 25-point window shift breaches proposed 10-point tolerance. |
| Validation, AI use and locked record | [Validation file](https://github.com/llindali/project2/blob/main/docs/validation-and-ai-use.md), including preserved prediction and result commits. |
| Videos and transcripts | Project README still lists three recorded YouTube videos and corrected transcripts as outstanding. |
| Manifest | [Submission manifest](https://github.com/llindali/project2/blob/main/docs/submission-manifest.md); pending video entries require actual links. |
| Week 12 must-fix list / due date | Studio list not supplied here. Enforced due date must be checked in Brightspace. |

## I — Partner cold run
**Evidence:** Linda supplied this as her partner's confirmation on November 10, 2026. The following summarizes that report, not an AI-executed or independently witnessed run.

- Repository: [llindali/project2](https://github.com/llindali/project2).
- Environment reported: Python 3.11, fresh virtual environment on macOS/Linux; exact OS not distinguished.
- Auditor label: Peer Auditor (Lab 20 Cold-Check Session); personal name not supplied.
- Exact tested commit: not supplied; the reference commit in Project 2's validation file is not asserted to be the tested checkout.
- Elapsed time: **6 minutes 15 seconds**, from clone through interactive UI validation.
- Outcome: dependencies installed without version conflicts, engine completed, app opened at localhost:8501, and unit tests passed.
- First failure: none reported.
- Result: root `visible_output.json`, terminal summary, and Streamlit app with mandate verdicts, controls, stress information and download.

### Partner-reported control checks — November 10, 2026
- **Auditor label supplied:** Peer Auditor (Lab 20 Cold-Check Session); personal name not supplied.
- **Total elapsed time:** 6 minutes 15 seconds, from clone through installation, engine run and interactive UI check.
- **Environment:** Python 3.11, fresh virtual environment, macOS/Linux as reported; exact OS not distinguished.
- **VT adjustment:** 0 to +1.5 annual percentage points. Reported mix changed 55/0/45 to 60/0/40 (SGOV/BND/VT); net estimate 7.15% to 7.34%; volatility 6.77% to 6.03%. Response time reported under one second.
- **Window check:** partner additionally reports 60 to 36 months, with 80/0/20 and a 25-point stability stop. The report does not specify whether the VT slider was reset first; this is not asserted as evidence of the combined 36-month/+1.5-point case.
- **Verdict:** reject live adoption remained active because unresolved policy and evidence conditions remain.
- **UI wording qualification:** inspected app code uses a persistent rejection message and a stress-results table. The partner's “warning banner” and “updated explanation” wording is treated as a description of the outcome, not a verbatim quote or proof of dynamically rewritten recommendation text. Stress cases are calculated separately from current sidebar inputs.
- **First failure:** none reported; no fix needed. Unit tests reported passing. Module invocation used the selected environment; prevention of hypothetical PATH errors was not separately tested.

These observations are supplied by Linda as her partner's report, not newly executed or independently witnessed by the AI assistant.

Commands reported:
```bash
git clone https://github.com/llindali/project2.git
cd project2
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python engine.py
python -m streamlit run app.py
```

Validation command reported: `python -m unittest discover -s tests -v`.
Windows activation alternative: `.venv\Scripts\activate`; no testing on multiple operating systems is inferred.

Terminology correction: the actual portfolio comparisons are equal weight, 70/30 proxy and constrained portfolio. Base 55/0/45, 36-month 80/0/20 and VT-minus-one-point 50/0/50 are optimized scenario results, not three baselines. The project's validation file already preserves this distinction.

## V — Locked Changed-Input Record
The actual Project 2 validation file now contains the student-attested AI-off prediction and subsequent AI-assisted result. These replace the earlier “not performed” preparation status.

- Input: VT additive annual return adjustment, 0 to +1.5 percentage points (+150 bps).
- [Prediction commit](https://github.com/llindali/project2/commit/339e59e2524ca17a64596ea05e2615c6b71a38e3), before the result run.
- [Preserved before/after output](https://github.com/llindali/project2/blob/c9cbbda8c57cd27f37ee927abfcde2f55460e3ec/results/locked-change-output.json).
- [Result commit](https://github.com/llindali/project2/commit/c9cbbda8c57cd27f37ee927abfcde2f55460e3ec).

| Number | Baseline | Changed |
|---|---:|---:|
| SGOV / BND / VT | 55 / 0 / 45% | 60 / 0 / 40% |
| Net annual arithmetic return estimate | 7.1461375% | 7.3371295% |
| Annualized volatility | 6.7698422% | 6.0304935% |
| Reserve value at initial $50M | $27.5M | $30M |
| Live allocation range | 0–0% | 0–0% |

The committed prediction expected unchanged weights and volatility and a 0.675-point return increase. Actual reoptimization reduced equity by five points, raised estimated return by about 0.191 points and reduced volatility by about 0.739 points. The original prediction mistook output weights for constraints: reserve floor is 3%, equity cap 70%. Higher estimated equity return lets the minimum-volatility model clear the unchanged 7% hurdle with less equity. Rejection of live adoption remains unchanged. The full prediction, diagnosis and student attestation remain in Project 2; no prediction has been rewritten after observing results.

## Explain the code
**Student-confirmed completed:** Linda confirms that the code explanation and partner Q&A were completed. Her supplied walkthrough covered monthly return estimation, annualized covariance, the five-point grid search, mandate checks, and why a higher VT return estimate permits less equity at the same hurdle. This completion is student-reported, not witnessed by the AI assistant. The supplied cheat sheet is preparation material, not proof of the conditions during the spoken activity.

**Question supplied in the report:** “Where in the code does the app enforce the 3% minimum reserve rule versus the 55% base weight?”

**Answer, with code terminology checked:** In `run(..., reserve=.03, ...)`, the grid search skips a candidate when `w[0] < reserve-1e-9`. The `measure()` function separately reports the buffer check with `w[0] + 1e-9 >= reserve`. The 55% SGOV weight is an optimized baseline output, not a constraint. The 3% floor effectively requires at least 5% on the five-point grid. This is an explicit candidate filter, not an external optimizer's bounds object.

The engine minimizes annualized volatility; minimizing its square, variance, would give the same ranking. The default 70% VT cap applies under the positive-momentum signal branch; the other branch uses 30%. The input series are adjusted-price total-return proxies, not independently authenticated total-return histories.

## E — Fix one thing
Partner reports no first failure and a clean first pass; **no fix was needed**. No fabricated fix or rerun is recorded.

## Decision line
**Reject live adoption (0–0% live allocation); reconsider only after approved issuer treatment and risk policy, authenticated fresh data, justified estimates, benchmark evidence and robust feasible stress results with no weight shift over 10 points.** Necessary conditions do not automatically grant approval. The partner's clean run supports reproducibility but does not resolve investment-policy or robustness failures.

## Reflect and checkout
**Student-confirmed completed:** Linda confirms the joint reflection was completed and supplied the following substance.

- **What the cold run revealed:** The live control response made the return-hurdle mechanism clear: adding 1.5 percentage points to VT's return estimate permitted 60% SGOV / 40% VT instead of 55% SGOV / 45% VT, while keeping the estimated-return hurdle satisfied. The reported clean run also supported README reproducibility without runtime API keys or hidden data requests. This was sensitivity to the return estimate at a fixed hurdle, not a test changing the hurdle itself.
- **What will remain unchanged before the deadline:** Preserve the saved baseline result (55% SGOV / 0% BND / 45% VT), constraint settings, and rejection of live adoption. Do not relax the reserve rule or tune estimates to force approval. Policy, ten-year evidence and issuer-treatment gaps remain disclosed. The baseline allocation is an output of frozen baseline inputs, not a hard-coded weight constraint.

The repository now contains the reported cold run, elapsed time, no-fix outcome, locked prediction/result links, decision line, and student confirmation of code explanation and reflection. The Lab 20 repository record is complete on the supplied confirmations; Project 2's outstanding submission items remain separately documented.

Submit the [Lab 20 record](https://github.com/llindali/lab20/blob/main/lab20.md) and relevant Project 2 evidence links through Brightspace → Quizzes → Lab 20. Brightspace submission and due-date confirmation are not claimed here.

Source: [Lab 20 instructions](https://github.com/CinderZhang/FIN43900-Fall2026/blob/main/lessons/week-13/lab-20-project2-readiness.md).
