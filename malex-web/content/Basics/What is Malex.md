---
title: "What Is Malex"
date: 2017-08-26T13:24:40+02:00
draft: true
weight: 1
---


## MalEx

MalEx is tool which aim to translate a binary to an abstract representation which will be used for further processing and perform naive isomorphism detection.

## How does it works

MalEx extracts the following information from binaries:

1. Function Calling Graph of the whole program
2. Control Flow Graph of each function defined in the binary
3. Value set of each register for each logic block in a function
4. Assembly instructions

Once these informations has been extracted, the data is structured in a yaml file which can later be analysed by other solutions.
