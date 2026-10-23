# Oslo Dataset (`oslo-bids`)

## Overview

This dataset contains MRI data from a sleep manipulation study conducted at the Oslo University Hospital (Norway). It is part of the ENIGMA-Sleep Working Group collection used to study the effects of sleep loss on glymphatic MRI indices. The data are organized according to the Brain Imaging Data Structure (BIDS) and managed with DataLad (git-annex).

## Sample

| Item | Value |
|---|---|
| Site | Oslo |
| Affiliation | Oslo University Hospital |
| Country | Norway |
| Participants (N) | 36 |
| Age, mean (SD), years | 26.5 (6.9) |
| Male (%) | 38.9 |

## Sleep protocol

- **BL**: baseline (habitual) sleep
- **SD**: total sleep deprivation, 32 h
- **CL**: control, habitual sleep

Sessions T1 and T2 were collected on scanning day 1; T3 and T4 on scanning day 2.

## Imaging data

### T1-weighted (`anat/`)

| Parameter | Value |
|---|---|
| Scanner | Siemens Prisma |
| Sequence | MEMPRAGE (first echo only) |
| TR (ms) | 2530 |
| TE (ms) | 1.69 |
| TI (ms) | 1100 |
| Flip angle (°) | 7 |

### Diffusion-weighted (`dwi/`)

| Parameter | Value |
|---|---|
| Scanner | Siemens Prisma |
| Sequence | DTI EPI |
| Resolution (mm³) | 2 x 2 x 2 |
| TR (ms) | 2450 |
| TE (ms) | 85 |
| b-values (s/mm²) | 0, 500, 1000, 2000 |
| Phase-encoding direction | AP/PA |

## Data organization

- `sub-<ID>/ses-<label>/`: raw BIDS data (`anat/`, `dwi/`)
- `participants.tsv`: participant-level information
- `sub-<ID>/sub-<ID>_sessions.tsv`: session-level information (condition, visit, date, time)
- `derivatives/`: processed outputs, if present

File contents are tracked with git-annex. After cloning, retrieve data with `datalad get <path>`.

## Original publication

Voldsbekk, I., Groote, I., Zak, N., Roelfs, D., Geier, O., Due-Tønnessen, P., Løkken, L.-L., Strømstad, M., Blakstvedt, T. Y., Kuiper, Y. S., Elvsåshagen, T., Westlye, L. T., Bjørnerud, A., & Maximov, I. I. (2021). Sleep and sleep deprivation differentially alter white matter microstructure: A mixed model design utilising advanced diffusion modelling. *NeuroImage*, 226, 117540. [https://doi.org/10.1016/j.neuroimage.2020.117540](https://doi.org/10.1016/j.neuroimage.2020.117540)

## Contact

- Jorik D. Elberse: [j.elberse@fz-juelich.de](mailto:j.elberse@fz-juelich.de)
- Masoud Tahmasian: [m.tahmasian@fz-juelich.de](mailto:m.tahmasian@fz-juelich.de)
