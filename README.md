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

Value chain data is crucial for navigating economic disruptions. Yet, despite its importance, we lack publicly available product-level value chain datasets, since resources such as the “World Input-Output Database”, “Inter-Country Input-Output Tables”, “EXIOBASE”, and “EORA”, lack information about products (e.g. Radio Receivers, Telephones, Electrical Capacitors, LCDs, etc.) and instead rely on aggregate industrial sectors (e.g. Electrical Equipment, Telecommunications). Here, we introduce a method that leverages ideas from machine learning and trade theory to infer product-level value chain relationships from fine-grained international trade data. We apply our method to data summarizing the exports and imports of 1200+ products and 250+ world regions (e.g. states in the U.S., prefectures in Japan, etc.) to infer value chain information implicit in their trade patterns. In short, we leverage the idea that due to global value chains, regions specialized in the export of a product will tend to specialize in the import of its inputs. We use this idea to develop a novel proportional allocation model to estimate product-level trade flows between regions and countries. This contributes a method to approximate value chain data at the product level that should be of interest to people working in logistics, trade, and sustainable development.

---

## Citation

If you use this code or the associated results, please cite:

```
@article{Karbevska_Hidalgo_2025,
  title    =  {Mapping global value chains at the product level},
  author   =  {Karbevska, Lea and Hidalgo, César A.}
  journal  =  {EPJ Data Science},
  volume   =  {14}, 
  number   =  {1},
  DOI      =  {10.1140/epjds/s13688-025-00521-5},
  ISSN     =  {2193-1127},,
  year     =  {2025},
  pages    =  {1–17},
  url      =  {https://epjdatascience.springeropen.com/articles/10.1140/epjds/s13688-025-00521-5}
}

```
