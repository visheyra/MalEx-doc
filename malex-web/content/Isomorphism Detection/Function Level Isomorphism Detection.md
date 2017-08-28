---
title: "Function Level Isomorphism Detection"
date: 2017-08-26T13:26:37+02:00
weight: 3
---

## Idea

The idea behind function level detection is simple. In MalEx it means that every functions symbol that can be extracted from a binary will be compared. In a first time, the control flow of the symbols are extracted as DiGraph's. Those DiGraph are then matched one against each using VF2 Algorithm to detect Isomorphism.

## Examples

`soon`
