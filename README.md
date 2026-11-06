# Torque Recoil Heating of Levitated Nanoparticles

This repository contains research workflows for studying torque recoil heating in levitated nanoparticles. It uses the [Optomechanical Levitation Simulator](https://github.com/barra9408/optomechanical-levitation-repo) to define incident optical fields, solve their interaction with a particle, and calculate the transfer amplitudes used in the recoil-heating analysis.

The current workflows consider focused plane-wave and Laguerre–Gauss illumination, spheroidal particles with different sizes and aspect ratios, and different torque axes.

## Installation

Python 3.11 or newer is required. From the repository root:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Iridis, load `python/3.12.6` before creating or activating the environment. `requirements.txt` specifies the simulator revision used by this project.

## Repository structure

- `cases/` defines the incident beams used in the calculations.
- `scripts/paper_parameters.py` records the parameters of the study.
- `scripts/recoil_heating/size_sweep.py` calculates recoil-heating quantities across particle sizes, beams, aspect ratios, and torque axes.
- `scripts/recoil_heating/angular_patterns.py` calculates angular patterns for selected particles and beams.

To inspect the available calculations without running them:

```bash
python -m scripts.recoil_heating.size_sweep --list-cases
python -m scripts.recoil_heating.angular_patterns --list-cases
```

## Results and paper

The CSV files currently included with the scripts come from earlier calculations. We are reviewing these results before identifying the data used in the manuscript. The paper citation, figure descriptions, and commands needed to reproduce the final results will be added when that review is complete.