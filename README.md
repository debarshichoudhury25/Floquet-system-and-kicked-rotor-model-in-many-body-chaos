# Prethermalization and Synchronization in Classical Kicked Rotor Lattices

This repository contains numerical simulations exploring prethermalization, energy 
transport, and dissipation-driven synchronization in classical kicked rotor systems, 
including 1D chains, 2D lattices, coupled ladder geometries, and dissipative variants 
with stochastic driving.

## Overview

The notebooks in this repository simulate classical kicked rotor lattices under 
periodic kicking, nearest-neighbour coupling, and (in later notebooks) momentum 
dissipation and stochastic dipolar driving. Kinetic energy per rotor is tracked over 
time to identify the prethermal plateau — a long-lived quasi-stationary regime preceding 
eventual thermalization — and its dependence on coupling strength, lattice geometry, and 
dissipation. In the dissipative, stochastically-driven setting, the chain's stroboscopic 
momentum dynamics are also compared against a reference single-rotor trajectory to 
quantify synchronization behavior via a momentum variance and an order parameter.

## Contents

* `1D classical kicked rotor prethermal model script.ipynb` — Kinetic energy time 
  evolution in a 1D periodic rotor chain, swept across coupling strengths K, 
  reproducing the characteristic log-log prethermal plateau.
* `Ekin_vs_K_kicked_rotor_theory_comparison.ipynb` — Steady-state kinetic energy per 
  rotor as a function of K, compared against the analytical mean-field prediction, 
  with error bars across multiple initial-condition samples and multiple time cuts.
* `ladder_rotor_kappa_ratio_0.5.ipynb` — 2-leg ladder of kicked rotors with rung 
  coupling weaker than the along-chain coupling, probing near-decoupled-chain behavior.
* `ladder_rotor_kappa_ratio_1.ipynb` — 2-leg ladder with isotropic coupling between 
  rung and along-chain bonds.
* `ladder_rotor_kappa_ratio_2.ipynb` — 2-leg ladder with rung coupling twice the 
  along-chain coupling, probing enhanced inter-leg energy transfer.
* `ladder_rotor_kappa_ratio_5.ipynb` — 2-leg ladder with strongly rung-dominated 
  coupling, completing the kappa_ratio sweep (0.5, 1, 2, 5).
* `dissipative_prethermal_1d_chain.ipynb` — 1D chain with momentum damping added to 
  the kicked rotor dynamics, examining how dissipation truncates the prethermal 
  plateau and sets a steady-state energy level.
* `dissipative_dipolar_kicked_rotor_1d.ipynb` — Dissipative 1D chain driven by random 
  dipolar kick pairs, examining how stochastic driving combined with dissipation 
  reshapes the energy plateau across different coupling strengths.
* `trc_synchronization_1d_dissipative_chain.ipynb` — Stroboscopic synchronization 
  analysis of the dissipative, dipolar-driven chain against a reference single-rotor 
  trajectory, tracking momentum variance and a synchronization order parameter across 
  a coupling-strength sweep.

## Physical Background

The underlying model treats each rotor as a classical degree of freedom with phase 
theta_i and conjugate momentum p_i, evolving under instantaneous kicks coupling 
nearest-neighbour phases, followed by free rotation. In the conservative case, the 
system exhibits a long prethermal plateau in kinetic energy before eventual 
thermalization, with the plateau height and lifetime governed by the kick strength K 
and lattice connectivity. Introducing momentum dissipation and stochastic dipolar 
kicks shifts the question from thermalization to synchronization: whether the 
many-body chain locks onto a common momentum trajectory dictated by the external 
driving, analogous to time-crystalline ordering in dissipative periodically-driven 
systems. These simulations connect to broader work on nonequilibrium statistical 
mechanics in coupled classical and quantum many-body systems.

## Requirements

* Python 3.x
* NumPy
* Matplotlib

## Usage

Each notebook is self-contained and can be run independently. Most expose tunable 
parameters (chain length, coupling strength, dissipation rate, kick amplitude, number 
of samples) near the top of the file for quick exploration of different physical 
regimes.
