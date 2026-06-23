[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000233-blue)](https://doi.org/10.82901/nemar.nm000233)

# BCI Competition 2020 Track 4 — Upper-limb grasping motor imagery

## Overview

BCIComp2020UpperLimb is a preprocessed derivative EEG dataset from BCI Competition 2020 Track 4 comprising motor imagery recordings of three grasping tasks (cylindrical, spherical, lumbrical) from 15 healthy subjects across three sessions. The dataset contains 60-channel EEG data sampled at 250 Hz with 450 trials per subject (150 trials per session). This is a processed version of the original BCI Competition 2020 data, designed to evaluate session-to-session transfer learning in brain-computer interface applications. Original 10 s trials (3 s rest, 3 s visual cue, 4 s motor imagery) have been preprocessed with 60 Hz notch filtering and cue-aligned epoching, with the 4 s motor imagery window extracted for analysis.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 15 |
| Channels | 60 |
| Classes | 3 |
| Trial length | 4 s |
| Sampling frequency | 250 Hz |
| Sessions | 3 |
| Total trials | 6750 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired using a BrainAmp system (BrainProducts GmbH) with 60 channels at 250 Hz sampling rate, referenced to FCz with Fpz as ground. Subjects performed cue-based motor imagery of three right-arm grasping tasks in three sessions separated by 7 days. Each trial consisted of a 3 s rest period, 3 s visual cue, and 4 s motor imagery window. Data were preprocessed with 60 Hz notch filtering and cue-aligned epoching. The 4 s motor imagery window (corresponding to seconds 6-10 of each original 10 s trial) was extracted by the loader for analysis.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import BCIComp2020UpperLimb
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = BCIComp2020UpperLimb()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.BCIComp2020UpperLimb.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.3389/fnhum.2022.898300](https://doi.org/10.3389/fnhum.2022.898300)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
