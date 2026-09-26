# Sequential Digital Clock with Alarm

A sequential digital clock designed using digital logic principles to track hours, minutes, and seconds while providing an integrated alarm function. The project demonstrates the practical application of sequential logic, counters, registers, clock signals, and comparison logic in the design of a functional digital timekeeping system.

## Overview

The Sequential Digital Clock with Alarm is a digital logic design project that implements a real-time clock capable of tracking hours, minutes, and seconds. In addition to basic timekeeping, the system incorporates an alarm mechanism that allows a predefined alarm time to be compared with the current clock time.

The project focuses on understanding how sequential digital circuits can be combined to create a practical time-dependent digital system.

## Features

- Digital hour, minute, and second tracking
- Sequential timekeeping logic
- Counter-based time management
- Clock-driven operation
- Alarm functionality
- Alarm time comparison
- Register-based state storage
- Modular digital-system design
- Practical application of sequential logic concepts

## System Architecture

The overall operation of the digital clock can be represented as:

Clock Signal → Second Counter → Minute Counter → Hour Counter → Time Display

The current time is continuously maintained by the sequential logic. The stored alarm time is compared with the current clock value, and when the required time condition is satisfied, the alarm output is activated.

## Working Principle

### Clock Signal

The clock signal provides the timing reference for the sequential circuit. Each appropriate clock event causes the timekeeping logic to update.

### Seconds Counter

The seconds counter tracks the passage of seconds. It increments according to the clock input and rolls over after reaching its maximum value.

The basic sequence is:

00 → 01 → 02 → ... → 58 → 59 → 00

When the seconds counter completes its cycle, it generates the condition required to increment the minutes counter.

### Minutes Counter

The minutes counter increments whenever the seconds counter completes a full cycle.

The basic sequence is:

00 → 01 → 02 → ... → 58 → 59 → 00

After completing the minute cycle, the hour counter is incremented.

### Hours Counter

The hours counter maintains the current hour and rolls over when the configured clock cycle is completed.

The basic 24-hour sequence is:

00 → 01 → 02 → ... → 22 → 23 → 00

This allows the system to continuously maintain the current time.

### Alarm System

The alarm system stores a target alarm time and compares it with the current clock time.

The basic operation is:

Current Time + Alarm Time → Comparator → Time Match → Alarm Output

When the current time matches the configured alarm time, the alarm condition is activated.

## Digital Logic Concepts

### Sequential Logic

The project demonstrates sequential logic, where the current state of the system depends on previous states as well as the applied clock signal.

The clock signal controls state transitions, allowing the timekeeping system to progress in a predictable sequence.

### Counters

Counters are fundamental components of the clock. Separate counting stages are responsible for maintaining seconds, minutes, and hours.

The counters operate within their respective numerical ranges and generate rollover conditions that control the next stage.

### Registers

Registers provide storage for digital state information. They can be used to maintain the current time as well as the configured alarm values.

### Clock Signals

The clock signal provides the timing reference required for synchronized sequential operation.

All major state transitions occur according to the clock, ensuring predictable behavior throughout the system.

### Comparators

Comparison logic is used to determine whether the current time matches the configured alarm time. When the required values match, the alarm signal is activated.

## Timekeeping Flow

Clock Signal
↓
Seconds Counter
↓
Seconds Rollover
↓
Minutes Counter
↓
Minutes Rollover
↓
Hours Counter
↓
Clock Cycle Reset

This cascading counter structure allows the system to maintain a continuously progressing digital time value.

## Alarm Detection

The alarm functionality compares the current clock values against the configured alarm values.

Current Hour + Alarm Hour
Current Minute + Alarm Minute
Current Second + Alarm Second
↓
Comparison Logic
↓
Time Match?
↓
Alarm Output

If the required time values match, the alarm output is activated.

## Project Documentation

The `docs/` directory contains supporting documentation related to the project design and implementation.

The `images/` directory contains visual resources associated with the project.

## Learning Objectives

This project was developed to gain practical experience with:

- Sequential digital logic
- Digital counters
- Registers
- Clock signals
- Comparison logic
- State-based system design
- Digital timekeeping
- Alarm logic
- Hardware-oriented problem solving
- Modular digital-system design

## Design Considerations

A reliable sequential digital clock must ensure that:

- Seconds increment at the correct rate.
- Seconds correctly roll over into minutes.
- Minutes correctly roll over into hours.
- Hours correctly roll over at the end of the clock cycle.
- Time values remain synchronized with the clock signal.
- Alarm comparisons occur against the appropriate time values.
- The alarm output activates only when the configured conditions are satisfied.
- The system maintains predictable state transitions.

## Applications

The concepts demonstrated by this project can be applied to:

- Digital clocks
- Alarm clocks
- Embedded timing systems
- FPGA-based timekeeping systems
- Digital control systems
- Sequential logic circuits
- Embedded hardware projects
- Real-time digital systems

## Key Takeaways

The project demonstrates how fundamental sequential digital building blocks can be combined to create a practical digital timekeeping system.

The combination of clock signals, counters, registers, and comparison logic provides the core functionality required for maintaining digital time and detecting a configured alarm condition.

## Author

**Muhammad Sohaib Afzal**

Computer Engineer | Automation & Intelligent Systems | AI/ML/DL

- GitHub: https://github.com/msohaibafzal
- LinkedIn: https://www.linkedin.com/in/msohaibafzal/
