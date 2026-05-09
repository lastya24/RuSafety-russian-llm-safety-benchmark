# RuSafety: Russian LLM Safety Benchmark

Authors: A. Limonova, K. Studenikina

This repository contains dataset, prompts, code, and experimental results for a study on the safety of Russian-language large language models.

The project introduces a Russian-language safety evaluation dataset derived from the Russian subset of XSafety and evaluates several LLMs on harmful or potentially unsafe prompts.

## Content Warning

This repository contains examples of unsafe, offensive, discriminatory, illegal, or otherwise harmful prompts and model responses. The materials are provided strictly for research on AI safety, evaluation, and harm mitigation.

Do not use this dataset to generate, optimize, or distribute harmful content.

## Project Overview

The project consists of three main stages:

1. Dataset construction and filtering
2. Model response generation
3. LLM-as-a-judge safety evaluation

The dataset is based on the Russian subset of XSafety. We identify and filter prompts using two complementary approaches:

- Deflection Score: a 0-100 estimate of how likely a model is to refuse answering a prompt for ethical or safety reasons.
- Binary safety classification: a 0/1 label indicating whether a prompt is potentially unsafe.

The final dataset contains 1,198 prompts.

## Evaluated Models

We evaluate the following models:

- YandexGPT Lite
- YandexGPT Pro 5.1 Release Candidate
- gpt-oss-20b
- gpt-oss-120b

All model responses were generated with temperature = 0.5.

## Repository Structure

```text
.
├── data/
│   ├── processed/          # final dataset files
│   └── results/            # model outputs and judge outputs
├── notebooks/              # original Colab notebooks
├── src/                    # reusable Python code
├── prompts/                # prompt templates
├── reports/                # figures and tables
└── docs/                   # methodology, ethics, and data documentation
