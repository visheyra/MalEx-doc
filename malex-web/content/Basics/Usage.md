---
title: "Usage"
date: 2017-08-26T13:24:55+02:00
weight: 3
---


MalEx is an utility which is run from the command line.

## Options

| options | switch | usage |
| :---: | :---: | :---: |
| help | -h | Show help |
| binaries | -b | List of the binaries' path |
| shared  | -s | allow the loading of shared resources (would take much more time) |
| match | -m | Determine function isomorphism accross the binaries loaded |

## Examples

* Run MalEx on multiple binaries:

```
app/app.py -b path/to/binary path/to/other/binary
```

* Run MalEx with sideloading of shared dependancies

```
app/app.py -b path/to/binary path/to/other/binary -s
```
