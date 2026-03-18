# Model Card

## Model name

Synthetic mitochondrial stress-response simulation workflow

## Version

v1.0

## Model type

Rule-based stochastic simulator with downstream statistical and machine-learning analysis

## Primary outcome

Single-cell apoptosis probability and binary apoptotic status

## Summary

This workflow simulates how mitochondrial calcium, reactive oxygen species, ROS, mitochondrial membrane potential, ATP production, permeability transition propensity, cytochrome c release, and caspase activation interact across seven biological conditions. It produces synthetic single-cell observations and supports descriptive analysis, dimensionality reduction, classification, and feature-importance ranking.

## Intended use

The model is intended for:

- Educational demonstrations.
- Hypothesis generation.
- Exploratory computational biology.
- Systems-level reasoning about mitochondrial stress.
- Figure prototyping.
- Pipeline and code testing on synthetic biological data.

## Out-of-scope use

The model must not be used for:

- Clinical diagnosis.
- Patient stratification.
- Treatment selection.
- Regulatory decision-making.
- Claims of biological efficacy without experimental validation.

## Inputs

The simulator takes condition-specific parameters that govern:

- Cytosolic calcium baseline.
- Mitochondrial calcium shift.
- ROS burden.
- Antioxidant strength.
- MCU scaling.
- Stochastic noise.

These parameters define the simulated biological context.

## Outputs

The workflow generates synthetic single-cell values for:

- `Condition`
- `Cell_ID`
- `Cell_Size`
- `Mito_Mass`
- `Cytosolic_Ca`
- `Mito_Ca`
- `ROS`
- `DeltaPsi`
- `ATP`
- `mPTP`
- `CytC_Release`
- `Caspase3`
- `ApoptosisProb`
- `Apoptotic`

Additional downstream outputs include summary tables, plots, PCA embeddings, classification metrics, feature-importance rankings, and integrated stress scores.

## Biological assumptions

The model encodes several qualitative assumptions:

- Moderate mitochondrial calcium can support ATP production.
- Excess mitochondrial calcium can impair function.
- ROS amplifies mitochondrial stress.
- Membrane depolarization and permeability transition contribute to cytochrome c release.
- Cytochrome c release and ATP decline contribute to caspase activation and apoptosis.
- Combined calcium and oxidative stress increases the likelihood of cell death.

## Evaluation

Internal evaluation in the notebook includes:

- Descriptive condition-level summaries.
- One-way ANOVA across conditions.
- Pairwise stress-condition comparisons.
- Correlation analysis.
- PCA of mitochondrial stress state.
- Logistic regression for apoptosis prediction.
- Random forest classification.
- Model performance metrics, including ROC AUC and accuracy.
- Coefficient and feature-importance analysis.
- Resilience-versus-vulnerability comparison.

These metrics evaluate internal consistency within the synthetic dataset only.

## Performance caveat

Any performance metric reported by the notebook applies only to simulated data generated under the workflow assumptions. High predictive performance should not be interpreted as evidence of real-world clinical or experimental utility.

## Limitations

- The workflow is synthetic and literature-informed, not experimentally calibrated.
- Outputs are normalized and do not map directly to one measurement platform.
- Temporal dynamics, spatial microdomains, and detailed antioxidant systems are simplified.
- Cell-type-specific variability is not explicitly represented.
- Omitted pathways may alter behavior in real biological systems.

## Risks

Potential risks include:

- Overinterpretation of synthetic outputs as experimental truth.
- Misuse of simulated classifications as if they were validated biomarkers.
- Confusion between qualitative biological plausibility and quantitative assay fidelity.

## Ethical considerations

No human or animal data are used in the default workflow. The main ethical consideration is responsible communication of the model’s synthetic nature and limitations.

## Maintenance

Update this model card whenever the workflow changes materially, including parameter changes, new simulated conditions, modified feature definitions, or new downstream analyses.

## Contact

Mark I.R. Petalcorin
aAidea, London U.K.
