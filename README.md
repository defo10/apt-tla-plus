# Advanced Programming Tools Seminar Report

This repository contains my slides and report on TLA+, a lightweight formal method capable model-checking designs. It was created during the seminar advanced programming tools at HPI, WS22/23.

## Building the Report

### Installation

 1. The bundle requires pandoc, latex, and biber
 2. Determine pandoc user-config directory via `pandoc --version`
 3. Create a directory templates in the pandoc user-config directory
 4. Copy `eisvogel.tex` to the templates folder

### Usage

 1. For building your report you can use `make full-pdf` and `make pdf` 
 2. The example report file includes several markup notations (tables, citations, images, captions)
 3. For details, see the [Pandoc documentation](https://pandoc.org/MANUAL.html#pandocs-markdown)
