# Spectral Memory — Hermes Agent Plugin

Frequency-encoded structured memory for Hermes Agent. 40 facts in 512 tokens, lossless under compression, 0ms cross-session retrieval.

## Install

```bash
hermes plugins install jeannemtl/spectral-memory-plugin
hermes memory setup  # select spectral_memory
```

## Get an API key

Sign up at [spectralmemory.com](https://spectralmemory.com)

## How it works

Facts are encoded as amplitude-shift keyed sinusoidal carriers superposed into a 512-token signal. Each label maps to a dedicated frequency channel — `USER.gpu` is always channel 3, `PROJ.accuracy` is always channel 34. Facts persist on our server and survive context compression.

## Supported labels

| Label | Channel |
|-------|---------|
| USER.name | 0 |
| USER.gpu | 3 |
| TASK.current | 10 |
| PROJ.accuracy | 19 |
| ... | ... |

Full label list at [spectralmemory.com/docs](https://spectralmemory.com/docs)
