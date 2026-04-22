# Museomics Sequencing Calculator

A browser-based tool for estimating sequencing data requirements when planning whole-genome sequencing of museum specimens.

## What it does

Given parameters typical of historic/degraded DNA libraries — genome size, target coverage, duplication rate, endogenous content, read length, and filter pass rate — the calculator estimates:

- **Data needed (Gb)** per sample and in total
- **Million read clusters needed** per sample and in total
- **Platform estimates** — how many samples fit per lane/flowcell/wafer and how many units are needed

## Usage

Live at: [museomics.github.io/sequencing-calculator](https://museomics.github.io/sequencing-calculator/)

All calculations run client-side. No data is sent anywhere.

## Formulae

**Data needed (Gb) per sample:**

```
genome_size × coverage / (1 − duplication%) / endogenous_content%
```

**Million clusters per sample:**

```
data_needed_Gb × 1e9 / read_length / passing_filter% / 1e6
```


## Licence

MIT
