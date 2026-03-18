# Datasheet for the Synthetic Dataset

## Dataset name

Simulated mitochondrial calcium, ROS, and apoptosis dataset

## Dataset type

Synthetic single-cell tabular dataset

## Motivation

This dataset was created to provide a reproducible computational test bed for studying how mitochondrial calcium overload, oxidative stress, membrane depolarization, bioenergetic decline, permeability transition, and apoptotic signaling may relate at the single-cell level.

## Generation source

The dataset is produced algorithmically by the repository notebook during execution.

## Record count

The default workflow generates 3,500 simulated cells, with 500 cells per condition.

## Composition

Each row represents one synthetic cell. The dataset includes metadata and mitochondrial stress-response variables.

### Core columns

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

The notebook may also add derived variables, such as integrated stress scores.

## Simulated conditions

The default dataset includes:

1. Control  
2. Mild Stress  
3. Ca Overload  
4. ROS Stress  
5. Combined Ca and ROS Stress  
6. Antioxidant Rescue  
7. MCU Inhibition

## Collection process

No human participants, animals, clinical records, or laboratory specimens were collected. Records are generated from stochastic rules, bounded distributions, and biologically motivated dependency structures.

## Preprocessing and transformation

The workflow:

- Draws condition-specific input variables from bounded distributions.
- Computes downstream variables sequentially.
- Clips outputs to biologically plausible normalized ranges.
- Exports both the full single-cell dataset and a condition-level summary table.

Optional downstream analyses include PCA, classification, feature-importance ranking, mediation-style decomposition, and stress-score aggregation.

## Fidelity and scale

The dataset is designed for qualitative and systems-level biological plausibility. Variables are expressed in normalized units rather than one universal experimental unit, because mitochondrial assays vary widely across platforms, cell types, and publications.

## Recommended uses

Appropriate uses include:

- Teaching and demonstration.
- Exploratory analysis.
- Workflow benchmarking.
- Visualization prototyping.
- Method development.
- Computational thought experiments in mitochondrial systems biology.

## Non-recommended uses

This dataset should not be used for:

- Training or validating clinical decision systems.
- Estimating absolute wet-lab effect sizes.
- Claiming experimentally verified pathway behavior.
- Benchmarking against real patient outcomes as though the data were measured.

## Quality considerations

Quality in this dataset means:

- Internal consistency with encoded biological assumptions.
- Reproducibility under fixed random seeds.
- Transparent generation logic.
- Clear documentation of synthetic provenance.

Quality does not imply direct equivalence to any one assay, instrument, or biological system.

## Missing data

The default workflow does not intentionally generate missing values. Any missing values after modification likely arise from downstream editing or code changes.

## Distribution and licensing

Add an explicit repository license before public release. If you distribute derived datasets, retain documentation that the data are synthetic.

## Maintenance

Revise this datasheet when the dataset schema, condition set, generation logic, or recommended use guidance changes.

## Citation

Petalcorin, M.I.R. (2026). A Synthetic Single-Cell Systems Model of Mitochondrial Calcium, Reactive Oxygen Species, and Apoptotic Commitment. https://github.com/mpetalcorin/mitochondrial-calcium-ros-apoptosis-simulation

