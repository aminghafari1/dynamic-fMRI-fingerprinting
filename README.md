# Dynamic Functional Connectivity Fingerprinting

A Python-based framework for extracting individualized brain connectivity fingerprints from resting-state functional MRI (rs-fMRI) data using dynamic functional connectivity (dFC).

## Overview

This framework characterizes individual-specific patterns of brain connectivity by capturing temporal fluctuations in functional connectivity. It employs sliding-window analysis and hierarchical clustering to identify shared brain connectivity states and construct personalized, state-specific functional connectivity fingerprints.

The framework also extracts temporal features, including state dwell times and transition probabilities, and supports the prediction of behavioral and cognitive scores.

## Key Features

- **Dynamic Functional Connectivity:** Computes sliding-window functional connectivity matrices using Fisher-z-transformed Pearson correlations.
- **Brain State Identification:** Uses two-level hierarchical clustering to identify recurring connectivity states across subjects.
- **Individualized Brain Fingerprints:** Extracts subject-specific connectivity patterns within each identified brain state.
- **Temporal Dynamics:** Computes state occupancy fractions (dwell time) and transition probabilities.
- **Behavioral Prediction:** Supports cognitive and behavioral score prediction using bootstrap-based feature selection and leave-one-out cross-validation.

## Requirements

- Python 3.9+
- NumPy
- SciPy
- scikit-learn

## Usage

Run the framework using:

```bash
python dynamic_fingerprinting.py --data fmri_data.npz
```

Optional parameters include:

```bash
python dynamic_fingerprinting.py \
    --data fmri_data.npz \
    --window-size 15 \
    --subject-clusters 20 \
    --states 7 \
    --feature-type connectome
```

The input should contain preprocessed fMRI time series organized by subject, time point, and brain region.

## Outputs

The framework generates:

- Shared dynamic brain connectivity states
- Individualized state-specific connectivity fingerprints
- State dwell times
- State transition probability matrices
- Optional behavioral prediction results

## Development Status

🚧 **Toolbox Under Development**

This repository contains the initial implementation of the dynamic functional connectivity fingerprinting framework.

**The framework will be further developed into a comprehensive, user-friendly Python toolbox, with expanded functionality, documentation, examples, and visualization tools. The toolbox will be made publicly available soon.**

## Research Applications

The framework is designed to support investigations of individual differences in brain functional organization, cognitive variability, aging, and neurological disorders, including Alzheimer's disease.

## Citation

Citation information and related publications will be provided with future updates.

## License

License information will be added upon public release of the toolbox.
