## Eric Ufomadu

I work on the reliability of AI systems used in legally consequential decisions.

Law increasingly resolves the problem of algorithmic decision-making by locating
a human and imposing a duty to verify: the judge who weighs a risk score, the
attorney who checks AI-generated work, the employer who audits a hiring system.
It rarely specifies what the system must disclose for that duty to be
dischargeable. I build systems that close that gap and write about what the law
should require.

LL.B., University of Nigeria. B.S. Computer Science and B.A. Political Science,
Stetson University, 2027. Co-founder of [Glawly](https://glawly.com), a legal
research platform indexing 8M+ U.S. judicial opinions.

---

### Projects

**[ORCA](https://github.com/EricUfomadu/orca-clause-risk)** — contract clause
risk classification with disclosable reliance
`Python` `scikit-learn`

A clause risk classifier built so that an attorney can actually discharge the
duty to verify its output. The model is deliberately linear, so attribution is
exact rather than approximated: contributions plus intercept reconstruct the
decision score to 1e-9, enforced by test. Evidence spans are verified against
the source string before emission and dropped if their offsets fail. Calibration
is selected empirically on held-out log loss rather than by convention. The
system abstains when uncertain, and generates a Reliance Card disclosing error
composition, detectability separation, temporal coverage, and silent behaviours.

In evaluation the detectability separation came out negative: the model was
marginally more confident when wrong, and every error sat above the confident
threshold. A user told "96.8% accuracy" would draw exactly the wrong conclusion
about how much verification the tool saves. That property is invisible in every
disclosure format currently in use.

**[DEEP](https://github.com/EricUfomadu/deep-pay-audit)** — compensation equity
auditing
`Python` `statsmodels`

Residual pay gap estimation with HC3 robust standard errors, Oaxaca-Blinder
decomposition against a pooled reference, and individual flags under
Benjamini-Hochberg false discovery control. Individual flags come from a
group-blind model on purpose: include the group indicator and every employee is
compared against their own group's discounted baseline, so a systematically
underpaid workforce looks correctly paid person by person.

Against 25 injected underpayment cases in 1500 employees, uncorrected flagging
returns 72 names at 29% precision. Correction cuts that to 11 at 100%. The
remediation planner prices group-neutral and targeted remedies side by side and
reports explicitly when the neutral option cannot close the gap within budget.

---

### Writing

- [The Algorithmic Black Box in Criminal Sentencing: Rethinking Procedural Due Process After *State v. Loomis*](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7168198)
- [The Undischargeable Duty: Attorney Verification of Legal AI and the Case for Reliance Disclosures](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7169098)
- [RAG Systems and the Illusion of Accuracy: Rethinking Attorney Competence Standards for Legal AI](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7179919) — honors thesis, Maris Award Honorable Mention

---

### Currently

Building retrieval evaluation infrastructure at Glawly. Preparing doctoral
applications in law and technology. Occasionally playing chess at a level that
suggests I should be doing less of it.

[LinkedIn](https://www.linkedin.com/in/ericufomadu) ·
[SSRN](https://papers.ssrn.com/sol3/cf_dev/AbsByAuth.cfm?per_id=12486408) ·
eufomadu@stetson.edu
