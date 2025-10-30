<h1 align="center">🥵🚀NDXP Alpha Peripheral Board F🚀🌡️</h1>

<p align="center">
  <img width="743" height="814" alt="Screenshot 2025-10-28 at 10 34 32 AM" src="https://github.com/user-attachments/assets/e87d1523-c357-4bfe-8ced-518662b40554" />

</p>

<h4 align="center">This is the repository for the FIRMWARE DESIGN ONLY. Hardware for the board can be found <a href="https://github.com/1112luke/ALPHA_PERIPHERAL_BOARD">here</a></h4>

## Introduction

This board was developed for NDXP's Alpha engine. Its purpose is to serve as a peripheral board to the [F.E.R.B.](https://github.com/1112luke/NDXPCOMPUTER) flight computer, and will facilitate data collection for the secifics of the Alpha mission. The board is responsible for collecting pressure and temperature data on the engine, as well as accelerometer data and load cell data during ground testing.

## Firmware Overview

The board runs an STM32F1 at 64 MHZ. the project was initialized and should be managed using STM32CubeMx anytime new peripherals or clock speeds are needed. We use VSCode to program, simply calling MAKE in the directory to build. The bin files can then be uploaded to the board via USB using STM32CubeProgrammer.

## Specifications

The board has capability in data collection, communication, actuation, and failsafe:

### Data Collection
- 12x 0-5v ADC (used for pressure sensing)
- 4x Thermocouple Channels
- 1x I2C accelerometer interface
- 1x Load Cell Interface

### Communication
- 1x RS-485 Channel (for communication with  [F.E.R.B.](https://github.com/1112luke/NDXPCOMPUTER))
- 1x Serial USB Port

### Actuation
- 4x Solenoid Valve Channels
- 1x Pyro Channel

### Failsafe
- 2x Keyed Switches (Pyro, Solenoids)
- 1x Burnwire Ignition Detection
- 1x E-STOP

## Contributors
- Luke Scholler
- Sebastian Brock
