---
title: "The VF2 Algorithm"
date: 2017-08-26T13:26:10+02:00
weight: 1
---

## Algorithm

The VF algorithm is an improvement of the VF algorithm. The application of this algorithm is to detect isomorphism and subgraph isomorphism. The improvement of VF2 is the requirement of a lower complexity (from O(N^2) to O(N))

## How does it works

This algorithm implements a naive detection of isomorphism. In fact, it tries to map every node in a graph *G* into another graph *G'*. This algorithm proceed node per node and

## Example

For a given graph `G` composed of 3 nodes `{n1, n2, n3}` and 2 edges `{e1, e2}`. With `e1` links together `n1` and `n2`, `e2` links together `n2` and `n3`. And for another given graph `G'` composed of 3 nodes `{n1', n2', n3'}` with 2 edges `{e1', e2'}`. `e1'` links together `n1'` and `n2'` and `e2'` links together `n1'` and `n3'`.

Below are the resolution steps to determine if `G` and `G'` are isomorphic

| Step | Explanation | Math |
| :---: | :---: | :---: |
| 1 | match empty G with empty G' |  G{} <=> G'{} |
| 2 | define which which node in G' n1 can match  | n1 <=> `n1' or n2' or n3'`
| 3 | match `n1` and `n1'` | n1 <=> n1' |
| 4 | define which which node in G' n2 can match | n2 <=> `n2` or `n3` |
| 5 | match `n2` and `n2'` | n2 <=> n2' |
| 6 | define which node n3 match in G' | n3 <=> {} |
| 7 | we can't match n3 so we fall back to step 3 | n3 <=> {} |
| 8 | `n1` match `n2'` | n1 <=> n2'
| 9 | define which remaining nodes in G' can match n2 | n2 <=> {n1', n3'} |
| 10 | match n2 with n1' | n2 <=> n1'
| 11 | define which node can be matched no n3 | n3 <=> {n3'} |
| 12 | match n3 and n3` | n3 <=> n3' |
| 13 | all nodes in G and G' are mapped | G <=> G' or {n1, n2, n3} <=> {n2', n1', n3'}
| 14 | G and G' are Isomorphic | * |
