# Proportional Allocation Model — Code Notebook

This repository contains the Python notebook accompanying the paper:

> **Mapping Global Value Chains at the Product Level**
> Lea Karbevska & César A. Hidalgo
> *EPJ Data Science*, 14, 21 (2025)
> https://doi.org/10.1140/epjds/s13688-025-00521-5

---

## Overview

The notebook implements a **Proportional Allocation Model** to estimate product-level trade flows between world regions along global value chains. The approach combines ideas from **trade theory** and **machine learning** to infer input-output relationships between products from fine-grained international trade data — without relying on aggregate sector-level datasets.

The core intuition: regions that specialize in exporting a product tend to also specialize in importing that product's inputs. The model formalizes this relationship to quantify the trade flows that link suppliers and producers across the globe.

---

## What's Included

- **Proportional Allocation Model** — estimates region-to-region trade flows for specific input-output product pairs (HS4 and HS6 level)
- **Backward & Forward Method** — predicts which products serve as inputs to a given output by traversing value chain links in both upstream and downstream directions
- **Random Baseline** — a comparison method to benchmark model performance
- **HS4 Results (CSV)** — precomputed results listing 3 predicted inputs per product

---

## Data Requirements

> ⚠️ **Note:** The trade data used to generate the published results is **not publicly available**. Reproducing the full results requires a **Pro or Premium account** on the [Observatory of Economic Complexity (OEC)](https://oec.world). The notebook covers exports and imports across 1,200+ products and 250+ world regions (e.g., U.S. states, Japanese prefectures).

---

## Paper Abstract

Existing value chain datasets (e.g., World Input-Output Database, EXIOBASE, EORA) operate at the level of industrial sectors rather than specific products. This paper introduces a method to infer product-level value chain relationships — such as which components flow into the production of cars, telephones, or solar panels — using granular bilateral trade data and trade-theory-inspired features. The model achieves ~70% accuracy in identifying the primary input for machinery products.

---

## Citation

If you use this code or the associated results, please cite:

```
@article{karbevska2025mapping,
  title     = {Mapping global value chains at the product level},
  author    = {Karbevska, Lea and Hidalgo, C{\'e}sar A.},
  journal   = {EPJ Data Science},
  volume    = {14},
  number    = {1},
  pages     = {21},
  year      = {2025},
  publisher = {Springer},
  doi       = {10.1140/epjds/s13688-025-00521-5}
}
```
