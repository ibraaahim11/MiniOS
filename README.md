<a id="readme-top"></a>
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/ibrahim-hesham-abdel-dayem/)

# MiniOS - Process Scheduler Simulation

## Overview

MiniOS is a simulation of an operating system process scheduler with memory management using the buddy system. It supports three scheduling algorithms:

- Non-preemptive Highest Priority First (HPF)
- Shortest Remaining Time Next (SRTN)
- Round Robin (RR)

The project demonstrates inter-process communication using message queues, process synchronization with semaphores, and shared memory for process control blocks. It also logs process and memory events for analysis.

## Features

- **Process Generator:** Reads process data and starts the simulation at the correct simulated time through `make run`.
- **Scheduler:** Receives processes, schedules them according to the selected algorithm, manages memory allocation using the buddy system, and logs events.
- **Memory Management:** Implements the buddy system for dynamic memory allocation and deallocation.
- **Logging:** Generates `scheduler.log`, `memory.log`, and `scheduler.perf` for process and memory events and performance statistics.

## Requirements

- GCC (tested with gcc on Linux)
- Make
- POSIX-compliant system (**Linux terminal is required**)
- Standard C libraries

> ⚠️ This project is meant to be compiled and run on a Linux system using a Linux terminal to access system libraries like message queues, semaphores, and shared memory.

## Installation

1. **Clone the repository:**
   ```sh
   git clone <repo-url>
   cd MiniOS-New
   ```

2. **Build the project:**
   ```sh
   make
   ```
   This will compile all binaries into the `bin` directory.

## Usage

1. **Run the simulation:**
   ```sh
   make run
   ```
   - The process generator will start automatically and prompt you to:
     - Choose the scheduling algorithm (HPF, SRTN, RR).
     - If RR is selected, enter the quantum value.

2. **View Output:**
   - `scheduler.log`: Logs process state changes (start, stop, resume, finish).
   - `memory.log`: Logs memory allocation and deallocation events.
   - `scheduler.perf`: Contains performance statistics (CPU utilization, average WTA, waiting time, standard deviation).

## File Structure

- `src`: Source code files
- `include`: Header files
- `models`: Data structure definitions
- `bin`: Compiled binaries
- `processes.txt`: Input file for processes (generated)
- `scheduler.log`, `memory.log`, `scheduler.perf`: Output logs

## Cleaning Up

To remove binaries and output files:
```sh
make clean
```

For more details, see the comments in each source file.

