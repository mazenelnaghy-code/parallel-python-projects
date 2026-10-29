# Parallel Python Projects

An interactive guide to nine project ideas for a sequential vs parallel Python task. Every idea has a
playable demo in the browser, and the main ones come with real timings measured on a laptop.

**Live demo:** [mazenelnaghy-code.github.io/parallel-python-projects/](https://mazenelnaghy-code.github.io/parallel-python-projects/)

Section project for **CCE 424 Parallel Processing**, by Mazen Elnaghy and Ahmed Tamer.

## Measured results

Python `multiprocessing` on an Intel i7-8550U laptop (4 cores / 8 threads):

| Project | Parallel speed-up | Overhead lesson |
|---|---|---|
| Mandelbrot fractal | 2.3× | One task per pixel: 9× slower than sequential |
| Photo filter (32 photos) | 2.3× | Sending whole photos means 52 MB of messages; send file names instead |
| Word count, MapReduce (6 million words) | 2.4× | 5,000 tiny tasks were almost as slow as sequential |
| Prime numbers below 1.5 million | 2.4× | Load balancing: small ranges cut 3.46 s to 3.05 s |
| Monte Carlo π | 1.7× | Tasks of 10 dots: 33× slower than sequential |

Also covered with demos: matrix multiplication, the N-Queens puzzle, downloading many files with threads,
and Conway's Game of Life.

## What's inside

- **The race:** 1 core against 4 cores, replayed from real timings (3.47 s vs 1.53 s).
- **Nine project cards,** each with how the work is split, its Flynn type, its overhead and how to fix it.
- **Overhead lab:** slide the chunk size and watch the number of messages and the time change.
- **Why processes, not threads:** how Python's GIL stops threads from speeding up heavy calculations.
- **Speed-up in numbers:** 2.27× on 4 cores is 57% efficiency, and where the rest goes.
- **Starter code:** the Mandelbrot program in all three versions (sequential, parallel, overhead).

## Run it

Open the [live demo](https://mazenelnaghy-code.github.io/parallel-python-projects/), or open `index.html` in any modern browser. It is a single file with no build step.

## Built with

HTML · CSS · JavaScript · Python `multiprocessing`

The chosen project is built out in full in [mandelbrot-parallel-lab](https://github.com/mazenelnaghy-code/mandelbrot-parallel-lab).
