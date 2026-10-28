# VIII. Propositions

Seventeen propositions follow, in three tiers by testability. The first carries test designs. The second follows directly from the model's definitions. The third consists of conjectures, with the data they would require.

## 1. Testable propositions

These six each carry a test design. Each design states indicators, data sources, and falsification conditions; none presupposes that the data have been obtained.

**P2.** The greater the risk externality of a decision, the higher the density of responsibility anchors, and there is a ceiling effect that does not disappear as trust accumulates.

*Test.* Anchor density is measured as named signatories per autonomous chain, divided by the number of chains. Risk externality is graded in four classes (internal rework only; customer-visible; regulatory exposure; personal safety). Data come from action chains and gate identifiers in deployment logs, joined to a risk grading table. The ceiling effect is tested by using months without incident as the independent variable and asking whether anchor density stops falling beyond some point. If anchor density falls monotonically toward zero as trust grows, the proposition fails.

**P6.** Net loss of human judgment capital raises organizational dependence on agents, lowers resilience (measured as recovery time after AI failure), and widens tail risk. The parasitic configuration shows high performance in the short run and pays for it in fragility.

*Test.* Judgment capital is a composite of in-the-loop ratio, human participation in exception adjudication, and annual retraining hours. Resilience is the time to recover baseline output after an unplanned AI outage. Tail risk is the P99 of error severity. Identification relies on the outage as a natural experiment, comparing recovery time across groups with high and low in-the-loop quotas. If the high-quota group does not recover significantly faster, or the parasitic configuration does not show higher P99 severity than controls, the proposition fails.

**P11.** The more adequately anchoring risk is compensated, the weaker the adverse selection into anchoring roles; below a critical level of compensation, the market for anchors collapses through lemons.

*Test.* The independent variable is the level of the anchoring allowance; dependent variables are the acceptance rate (share of invitees who take an anchoring role) and one-year retention. Data come from payroll and the anchoring register; identification exploits quasi-experiments created by changes in compensation policy. If acceptance is insensitive to compensation, or high-compensation groups do not score higher on review quality, the lemons mechanism does not hold.

**P13.** Within a six-month deployment cycle, the specificity threshold for personnel adjudication exceeds that for first drafts of copy, and rises faster.

*Test.* The specificity threshold is not directly observable; the proxy is the share of that class of task still delivered under retainer. Data come from procurement and task-assignment records, with task types under a common coding. Identification is a paired comparison across task types within the same organization, measured at two points. If the retainer share for personnel tasks is not higher than for copy, or falls faster, the proposition fails.

**P14.** Spot-marketization of judgment proceeds in ascending order of specificity; the ratio of retainer humans to spot-call humans drifts systematically with the degree of agentization.

*Test.* Rate specificity independently for each task class, then measure its spot-marketization share, and test the agreement of the two orderings (Kendall's τ). Data come from a cross-section of twenty to thirty organizations in one industry; the degree of agentization is proxied by agent invocations as a share of total tasks. If the ordering of spot-marketization is uncorrelated with the ordering of specificity, the proposition fails.

**P17.** The two forms of anchoring — named at the chain level and named at the function level — differ systematically in leakage rate, false-rejection rate, and gate load.

*Test.* Leakage is the share of injected errors not intercepted; false rejection is the share of intercepted actions that should have passed; load is decisions per gate per day. Data come from controlled simulation: the same task set and the same model version, with only the anchoring form changed and randomly assigned. If none of the three differences is significant, or chain-level anchoring shows the higher leakage rate, the proposition fails.

## 2. Restatements of the model

The following hold directly from the model in Sections III and V. They are restatements rather than independent hypotheses.

**P1.** The higher the verifiability of a task, the higher the equilibrium autonomy of the executing agent.

**P5.** The verifiability of organizational memory (not its completeness) positively moderates the relationship between agent autonomy and organizational risk, as does the strictness of write-permission governance.

**P7.** The higher the turbulence of the environment, the higher the optimal frequency of structural recomputation, and the more sensitive performance is to delay in recomputation.

**P15.** The higher the specificity of an agent, the stronger the tendency for the organization to hold residual control; the lower the specificity, the stronger the tendency for the individual to hold it or for capacity to be leased.

## 3. Conjectures

The following cannot currently be tested. They are listed with the data they would require.

**P3.** The rate at which the cost of stating intent falls significantly affects the rate at which the symbiotic form diffuses. *Required:* cross-firm proxies for statement cost, and a time series of form adoption.

**P4.** There is an inverted-U relationship between the price level of attention and the quality of intent packages: price too low and attention is abused; price too high and intent shrinks and routing loses focus. *Required:* a comparable scale for price levels, which does not currently exist.

**P8.** The degree to which the institutional environment regulates agent registration, trace-keeping, and the determination of responsibility positively moderates the legitimacy and diffusion of the symbiotic form. *Required:* coding of regulatory strength across jurisdictions.

**P9.** The intensity with which receiver-side pricing power is exercised (refusal rate and renegotiation rate) correlates negatively with systematic drift in the intent complexity index. *Required:* an operational definition of intent complexity.

**P10.** Liability for AI-related harm is bifurcating. Mainstream carriers withdraw through exclusions; specialist carriers enter through certification plus insurance. The exit condition for the former is the inability to reconstruct a reasoning path; the admission condition for the latter is that governance can be documented. Insurability as a governance gate therefore depends not on whether risk can be priced but on whether governance can be verified externally. Risk that cannot be verified will not be priced; it will only be excluded.

**P12.** The survival probability of labor-protection devices within an organization rises with the equilibrium of labor politics (degree of unionization, legislative activity). *Required:* coding of protection strength across institutional settings.

**P16.** In the limiting form of an intent pool plus a capacity market, the ceiling on organizational size is set by anchoring capacity and judgment invocation bandwidth, not by the supply of agents. *Required:* empirical distributions of anchoring capacity.

Among these, P1, P2, P4, P6, P9, P11, P13, and P14 can be tested within a single organization; P3, P7, P8, P10, P12, and P15 require cross-organizational, cross-temporal, or cross-institutional comparison; P5 and P16 can be approached first through natural experiments and multi-agent simulation [52,53].
