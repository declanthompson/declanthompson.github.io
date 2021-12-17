---
title: Formal Characterisations of 'Algorithm'
summary: Finding a characterisation of 'algorithm' that matches everyday usage.
tags:
- algorithms
- philosophy of computer science
- algorithmic analysis
- Turing machines
- ASM
- recursors
date: "2020-01-06T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Description of the Breadth First Search algorithm
  focal_point: Smart

links:
#- icon: twitter
#  icon_pack: fab
#  name: Follow
#  url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

The notion of *computable function* has been widely studied in theoretical computer science, and it is often assumed that any questions we have about *algorithms* can be answer by using one of the traditional models of computation (Turing machines, recursive functions, etc.). This assumption fails to square with the way *algorithm* is used in computer science practice. When discussing algorithms, we are not merely interested in input/output behaviour, since we mark a distinction between different algorithms for the same task. On the other hand, an algorithm is not a *program* or Turing machine, since multiple programs, in different programming languages, can implement the same algorithm. An adequate formal characterisation of *algorithm* has yet to be proposed.

This project focusses on analysing the notion of *algorithm*, with a view to formalising statements like "MergeSort runs in $O(n \log n)$ time", "Program $\pi$ implements Algorithm $A$" and "Kruskal's algorithm is correct for the Minimum Spanning Tree problem". Major existing work in this area can be found by authors including Yuri Gurevich, Yiannia Moschovakis and Walter Dean.
