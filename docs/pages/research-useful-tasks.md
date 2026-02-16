---
layout: default
title: Useful Tasks - Research - selfdrivenAI
subtitle: "Can inorganic intelligence do useful tasks?"
tags:
  - metamorphosis
  - societal-transition
  - transformation
  - governance
  - future
summary: >
  Can inorganic intelligence do useful work?
  GDPval measures **real-world, economically valuable professional work**, not academic puzzles.
permalink: /research/useful-tasks
---

# Can Inorganic Intelligence Do Useful Tasks?

For this research topic, GDPVal is used as a framework for useful tasks, even though GDP itself may not be the best measure of societal output.

## What is GDPval?

**GDPval measures real-world, economically valuable professional work, not academic puzzles.**

Key properties:

- Measures knowledge-work productivity, not raw correctness
- Compares AI outputs vs experienced human professionals
- Uses blind expert judging (win / tie / loss)
- Focuses on deliverables, not multiple-choice answers

**Scale:**
- 44 occupations
- 9 economic sectors
- ~1,320 total tasks (~30 per occupation)
- Authored by professionals with ~14+ years of experience

## Occupations Covered (Examples)

GDPval spans representative roles across the economy, including:

### Professional & Technical
- Software developer  
- Mechanical engineer  
- Industrial engineer  
- Project management specialist  
- Computer & information systems manager  

### Finance & Legal
- Accountant & auditor  
- Financial analyst  
- Financial manager  
- Personal financial advisor  
- Lawyer  

### Healthcare
- Registered nurse  
- Clinical nurse  
- Healthcare services manager  
- Medical secretary / admin  

### Sales, Marketing & Media
- Sales manager  
- Real estate agent / broker  
- Marketing & sales representatives  
- Journalist / editor  
- Producer / director  

### Operations & Public Services
- Compliance officer  
- Administrative services manager  
- Manufacturing operations supervisor  
- Social worker  

*(44 total roles across 9 sectors)*

---

## What GDPval Tasks Look Like

**GDPval tasks are real work outputs, not trivia.

Typical deliverables include:

- Financial models and forecasts  
- Accounting spreadsheets and variance analyses  
- Legal briefs and contract risk summaries  
- Engineering design documents  
- Sales decks and pitch presentations  
- Project plans and operational schedules  
- Customer support workflows  
- Editorial articles and media summaries  
- Healthcare care plans  

Tasks often include reference files (spreadsheets, datasets, templates) and require multi-step reasoning.

--

## The Public “Gold Subset”

**OpenAI has released a 220-task “gold subset” for public inspection and research.**

Purpose:
- Transparency
- Reproducible evaluation
- Representative sampling of the full benchmark

These tasks:
- Come from the same 44 occupations
- Include full prompts and reference materials
- Are used in OpenAI’s Evals framework

---

### Finance & Accounting Example

**Auditor Sample Testing & Variance Analysis**

**Scenario:**
You are an auditor reviewing an Anti-Financial Crime risk dataset.

**Required deliverables:**
- Select a statistically valid sample (90% confidence)
- Perform Q2 vs Q3 variance analysis
- Add flags and calculations in new spreadsheet tabs

**Skills tested:**
- Statistics
- Spreadsheet manipulation
- Professional judgment
- Clear documentation

---

### Finance Example

**Profit & Loss Report for a Music Tour**

**Scenario:**
You are Finance Lead for a touring production company.

**Required deliverables:**
- Consolidate income, costs, and tax data
- Build a multi-sheet P&L workbook
- Write an executive-level financial summary

**Skills tested:**
- Financial modeling
- Data synthesis
- Business communication

---

## How Outputs Are Judged

**GDPval does not score answers as “correct” or “incorrect”.**

**Instead:**
- Expert judges blindly compare AI output vs human output
- Judged on:
  - Accuracy
  - Completeness
  - Professional quality
  - Usefulness
- Results are reported as win / tie rates.

A reported score like **~70% GDPval** means:
- The model’s output was judged **as good as or better than** a human professional in ~70% of tasks.

## Why GDPval Matters

GDPval attempts to capture something traditional benchmarks miss:

- Real economic value
- Professional judgment
- Output quality, not token accuracy
- Productivity without direct labor input

It’s designed to answer:
> *Can this model actually do economically useful work?*

## Summary

- GDPval evaluates **real-world knowledge work**
- Covers **44 occupations, 9 sectors**
- Uses **expert-authored tasks and expert judging**
- Includes **1,320 total tasks**, with **220 publicly released**
- GPT-5.2’s ~70% score reflects **professional-level output parity**, not exam performance

---

## Appendix

Here are actual example tasks from the 220-task gold subset of OpenAI’s GDPval benchmark — the portion that’s been open-sourced so researchers can inspect real prompts and reference files.

---

## Finance & Accounting

### Auditor Sample Testing & Variance Analysis

**Scenario**  
You’re an auditor reviewing a spreadsheet of Anti-Financial Crime risk metrics.

**Deliverables include:**
- Choose a statistically justified sample at 90% confidence
- Perform a Q2 vs Q3 variance analysis
- Add sample flags and calculations in new spreadsheet tabs

Clear instructions and structured output expected.

### Profit and Loss Report for a Music Tour

**Scenario**  
You’re Finance Lead for a production company’s fall tour.

**Deliverables include:**
- Consolidate income / cost / tax data across multiple sheets
- Build a P&L Excel workbook with detailed breakdowns
- Summarise results for executive review

Requires both numerical analysis and professional report structure.

---

## Professional Services / Consulting

Many tasks require multi-step deliverables such as slide decks or written outputs based on real data and business context (not all prompts are publicly visible).

**Examples include:**
- Create market competitor landscape presentations
- Formulate strategic recommendations based on provided datasets

These combine analysis + narrative + structured formatting.

---

## Where to Explore the Full Gold Subset

OpenAI’s GDPval gold subset (220 tasks with prompts and reference files) is available via:
- [OpenAI Evals (GitHub)](https://github.com/openai/evals)
- [Hugging Face (Dataset)](https://huggingface.co/datasets/openai/gdpval)

---

GDPval is designed to answer:
*Can this system actually do economically useful work at a professional level?*