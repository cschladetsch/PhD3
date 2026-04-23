# PhD Research Proposal

## Simulating the Societal Impact of Political Policy Using Large Language Model-Driven Agent-Based Modelling

**Candidate:** Christian Schladetsch  
**Institution:** RMIT University  
**Programme:** Doctor of Philosophy  
**Proposed School:** Computing Technologies / Global, Urban and Social Studies (joint)  
**Date:** February 2026  

---

## 1. Abstract

Policy design is consequential and, by the standards of empirical science, poorly disciplined. This proposal investigates whether Large Language Model (LLM)-driven agent-based modelling (ABM) can change that. The core idea is straightforward: replace the fixed-rule agents of classical simulation with LLM-instantiated agents capable of reasoning, adaptation, and culturally-situated behaviour, then observe what emerges at the macro level when policy perturbations propagate through a structured societal model. The harder problem nd the central intellectual contribution of this work is developing a validation methodology rigorous enough to be credible in a domain where controlled experimentation is impossible. If that problem can be solved, the result is a tractable, scalable alternative to the trial-and-error approach that currently passes for evidence-based governance.

---

## 2. Introduction and Motivation

Governments enact policy under uncertainty and learn from consequences. This is not a criticism, it is an accurate description of how democratic governance works, and has always worked. The problem is the cost. When a housing policy produces unexpected displacement effects, or a welfare reform drives outcomes no theorist predicted, real people absorb that cost before the feedback reaches the policymakers who created it.

Computational simulation has long promised a way around this. System dynamics models, computable general equilibrium frameworks, and classical agent-based models have each had their moment. None has delivered on the promise at scale, and for a common reason: the agents are too simple. A utility-maximising automaton following fixed rules cannot model the way a person reasons about a policy change, updates their beliefs about how others will behave, and acts accordingly. The model produces predictions; the predictions miss what actually happens.

Large language models make a different kind of agent possible. An LLM-mediated agent can reason. It can hold contradictory beliefs, update them in response to new information, and act in ways that reflect something closer to actual human deliberation than anything a classical ABM can produce. Whether this is enough to close the gap between simulation and reality is the empirical question this research exists to answer.

---

## 3. Research Questions

The primary question is blunt: can this actually work? More precisely, can LLM-driven agent-based simulation produce reliable, falsifiable predictions about the macro-level societal impacts of political policy interventions; and if so, under what conditions and with what limitations?

That question cannot be answered without resolving several others. What agent architecture is required to model political and economic behaviour at policy-relevant fidelity? How do you validate outputs when there is no control group? Where does the computational cost become prohibitive, and what approximations are acceptable? How does agent heterogeneity — ideological, cultural, socioeconomic; affect emergent outcomes? And what, if anything, does this framework reveal that existing approaches cannot?

These are the questions that structure the research programme.

---

## 4. Proposed Methodology

### 4.1 Framework Architecture

The simulation comprises four layers. The agent layer is a population of LLM-instantiated individuals, each carrying a socioeconomic profile, a political identity and value system, an accumulated memory of experience, and a reasoning engine that updates beliefs and generates decisions in response to the environment. The environment layer models the societal infrastructure those agents inhabit: labour markets, housing, healthcare delivery, welfare systems, and political institutions. The policy injection layer is a formalised interface for introducing interventions as parameterised perturbations that agents can observe and respond to. The observation layer instruments the simulation to record outcomes at both the individual and aggregate level; economic indicators, wellbeing proxies, political sentiment, and emergent collective behaviour that was not programmed in.

The design reflects a deliberate choice: bottom-up emergence over top-down prediction. The model does not forecast outcomes directly. It creates conditions and watches what happens.

### 4.2 Target Policy Domains

Three domains are identified as primary targets for applied analysis, selected for the availability of historical data, the existence of cross-jurisdictional natural experiments, and direct relevance to current Australian policy debate.

The first is housing and urban planning policy. Australia's housing affordability crisis provides a live policy environment with substantial historical data, significant jurisdictional variation in regulatory approaches, and documented second-order effects (displacement, infrastructure strain, demographic sorting) that classical models have consistently failed to predict. The framework's ability to model agent-level responses to zoning changes, negative gearing reform, or vacancy taxes would be tested here.

The second is healthcare and welfare reform. The introduction and modification of universal healthcare systems across comparable countries and the variation in outcomes provides a rich backtesting environment. This domain also offers opportunities for collaboration with health policy researchers and government agencies with an interest in prospective modelling.

The third is climate and energy transition policy. Carbon pricing, subsidy structures, and energy transition mandates produce heterogeneous responses across socioeconomic groups that aggregate models smooth over. Agent-level simulation of these responses, and their political feedback effects, is an area where the framework's capabilities would be distinctively valuable.

### 4.3 Validation Methodology

This is the hard part, and treating it as such is important. The absence of a control society is not a methodological inconvenience that can be footnoted away. It is a fundamental epistemological constraint that the research must address head-on.

The proposed approach is multi-pronged because no single method is sufficient. Historical backtesting simulating known interventions and comparing emergent outcomes to observed data provides the most direct test, but is limited by data quality and the difficulty of isolating causal effects. Bias in historical data will be characterised explicitly: where training data reflects systematic social inequities, the simulation will be expected to reproduce those inequities, and the research will distinguish between model failure and accurate reflection of historical reality.

Cross-jurisdictional natural experiments, where similar policies were implemented at different times or with different parameters, offer a partial substitute for the missing counterfactual. Expert adversarial review will be conducted through structured red-teaming sessions with domain specialists, using a pre-registered protocol to prevent post-hoc rationalisation of failures. Sensitivity analysis maps how outcomes vary with agent population parameters and architectural choices. Internal consistency testing on analytically tractable toy problems establishes that the framework produces known-correct results before application to problems where the correct answer is unknown.

Success will be defined against explicit benchmarks. For historical backtesting, the framework will be required to predict the direction of documented effects (positive, negative, neutral) at greater than chance rate across a defined test set, and to place the magnitude of effects within a specified confidence interval. Benchmark comparison against existing models (CGE, classical ABM) will establish whether LLM-agent simulation adds predictive value beyond the current state of the art.

### 4.4 Computational Approach

LLM inference at agent scale is expensive, and pretending otherwise would undermine the credibility of the proposal. Initial estimates suggest that simulating a population of 10,000 agents through 100 time steps using current-generation LLMs would require substantial GPU compute in the range of hundreds of GPU-hours per run, necessitating infrastructure beyond a standard research workstation.

The research will pursue three mitigations. Hierarchical agent architectures will reserve full LLM reasoning for significant decision points, using lightweight heuristics for routine behaviour. Distillation will transform LLM-generated behavioural profiles into smaller models suitable for bulk simulation once behavioural patterns have been characterised. Partnerships with RMIT's high-performance computing facilities and potentially external cloud compute providers will be sought at the outset of the programme.

The boundaries of tractability are themselves a research output. A systematic characterisation of the relationship between agent count, time-step resolution, LLM capability, and predictive validity will inform both this framework and future work in the area.

---

## 5. Claimed Contributions

The primary contribution is a validated LLM-agent-based simulation framework for political policy impact modelling not as a prototype or proof-of-concept, but as a system tested rigorously enough to support real claims about its predictive validity.

The second contribution is the validation methodology itself, which has value independent of this particular application. The problem of validating agent-based social simulations without controlled experiments is not unique to policy research, and a systematic approach to it is genuinely lacking in the literature.

The third contribution is empirical: a characterisation of emergent societal behaviours arising from LLM agent interaction in structured policy environments, including phenomena the framework reveals that existing models do not predict.

The fourth is architectural: design patterns for tractable large-scale simulation using LLM agents, including the agent hierarchy and distillation protocols developed in the course of the research.

---

## 6. Risk Management

Three categories of risk warrant explicit treatment.

**Model limitations.** Current LLMs exhibit well-documented failure modes: hallucination, sensitivity to prompt framing, and inconsistent behaviour across runs. The research will characterise these systematically in the agent context. Where failure modes are fundamental rather than incidental, the architecture will be adjusted. For instance, constraining agent reasoning to structured outputs in domains where free-form inference is unreliable.

**Computational feasibility.** If the costs of LLM inference at simulation scale prove prohibitive even after the mitigations described above, the research will pivot to smaller agent populations with more intensive per-agent simulation, accepting reduced ecological validity in exchange for tractability. The relationship between scale and validity will be documented rather than assumed.

**Historical data availability.** Some policy domains have better longitudinal data than others. If primary target domains prove data-poor for backtesting, the research will substitute comparable domains with richer data records. A data audit will be conducted in Phase 1 before domains are finalised.

---

## 7. Collaboration and Partnerships

The research is designed to benefit from external engagement at multiple points. The Australian Treasury, the Productivity Commission, and state-level planning departments are identified as potential partners for both data access and prospective validation — organisations with an operational interest in better policy simulation tools. RMIT's existing relationships with government and industry provide a realistic pathway to these partnerships.

Within the university, collaboration with researchers in the School of Economics, Finance and Marketing and the Centre for Urban Research would strengthen both the economic modelling and the urban policy application streams. Internationally, research groups working on generative agent simulation (notably at Stanford and CMU) represent both prior work to build on and potential collaborators for cross-institutional validation studies.

---

## 8. Candidate Background

Thirty years of building systems that have to work: naval combat management, game engines, real-time distributed infrastructure produces a particular kind of engineering discipline. Problems do not stay theoretical. They have to run, at scale, under load, in conditions that were not anticipated during design. That discipline is directly relevant to a research programme whose central challenge is building and validating a complex simulation system from scratch.

The AI work is more recent but substantial. Training models for Google DeepMind and Apple, and building a series of open-source LLM inference and agent tooling projects, has produced a working understanding of where current-generation models are reliable, where they are brittle, and what that means for using them as cognitive substrates in a simulation context. This is not background knowledge. It is directly load-bearing for the research.

The intellectual foundations were laid earlier. Study under Marvin Minsky at MIT, though not completed to award, provided grounding in AI and cognitive science from one of its originating figures. The ideas from that period have been in active use for four decades.

This proposal is submitted under RMIT's Recognition of Prior Learning pathway. The candidate does not hold a formal degree. The argument for admission rests on the record above: a body of professional and research-adjacent work of sufficient depth, originality, and direct relevance to the proposed research that the Graduate Research Office is asked to consider it on its merits. The candidate welcomes any additional assessment or bridging requirements.

---

## 9. Timeline

| Phase | Duration | Key Deliverables |
|---|---|---|
| Phase 1 | Months 1-4 | Literature review; data audit; framework design; initial prototype; first supervisory panel review |
| Phase 2 | Months 5-10 | Working framework implementation; validation protocol pre-registration; confirmation of candidature |
| Phase 3 | Months 11-18 | Validation experiments; backtesting results; first journal submission |
| Phase 4 | Months 19-24 | Applied policy analyses (min. 2 domains); second journal submission; conference presentation |
| Phase 5 | Months 25-28 | Thesis writing; external examination; defence |

---

## 10. Ethical Considerations

Three issues warrant explicit attention. First, a tool that models policy impacts accurately enough to be useful is also a tool that can be used to optimise policy for narrow interests. The research will analyse misuse vectors and propose governance frameworks for responsible deployment, including transparency requirements, audit mechanisms, and stakeholder engagement protocols for any real-world application.

Second, LLM agents trained on existing data carry existing social biases into the simulation. The research will characterise these systematically and where possible mitigate their effect on outputs. Where bias cannot be mitigated, it will be disclosed.

Third, and most fundamentally, the outputs of this simulation must never be presented as anything other than what they are: decision-support tools with explicit uncertainty bounds, not predictions. The temptation to overstate what a simulation can tell us is the most persistent failure mode in computational social science. This research will resist it.

The work will be conducted in full compliance with RMIT's Human Research Ethics requirements.
