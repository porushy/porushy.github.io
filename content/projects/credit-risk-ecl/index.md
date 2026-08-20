---
title: Credit Risk & Expected Credit Loss (ECL)
summary: A Basel-style expected credit loss engine combining calibrated PD with LGD and EAD, implementing IFRS-9 three-stage impairment logic.
date: 2026-07-25
featured: true
links:
  - type: code
    url: https://github.com/porushy/Credit-Risk
    label: Code
    icon: brands/github
tags:
  - Quantitative Finance
  - Credit Risk
  - IFRS-9
  - Basel
---

Jul 2026

- Built a Basel-style expected credit loss engine which converts an algorithmic lending model's output into calibrated PD and combines it with LGD and EAD to produce loan-level ECL.
- Implemented IFRS-9 three-stage impairment logic and ran LGD sensitivity analysis to test how provisioning shifts under alternative recovery assumptions.
- Analysed risk-grade deciles and quantified how sharply expected loss concentrates in a small share of the book, which drives a disproportionate share of provisions.

<!--more-->
