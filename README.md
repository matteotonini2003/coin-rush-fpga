# Coin Rush — FPGA Video Game

*A documentation-only repository for an FPGA-based arcade game developed at the University of Pisa.*

### Overview

**Coin Rush** is a 2D arcade video game implemented in **Verilog RTL** on a **Terasic DE2 FPGA development board**. The player moves vertically to avoid scrolling obstacles, collect coins and progress through three levels. A collectible star provides temporary protection against an obstacle.

The project was developed for the *Digital Systems Design* course in the Master's Degree in Electronic Engineering at the **University of Pisa** (academic year **2026/2027**). Its architecture is modular and hardware-oriented: game control, object movement, collision detection, video generation and audio processing operate as interconnected RTL blocks.

### Main features

- **FPGA platform:** Terasic DE2, Altera Cyclone II EP2C35F672C6; 50 MHz system clock.
- **Video:** VGA 640 × 480, 25 MHz pixel enable, 10-bit RGB channels.
- **Gameplay:** vertical player movement, three obstacle generators, six obstacle shapes, collectible coins and a protective star.
- **Progression:** three levels with increasing difficulty; start, play, pause, level transition, game-over and victory screens.
- **Graphics:** 32 × 32 pixel sprites stored in a synchronous ROM, with transparency and drawing priority handled by the rendering pipeline.
- **Audio:** two-voice synthesis and a WM8731 codec interfaced through I²C and I²S.
- **Verification:** RTL testbenches, Quartus II synthesis and TimeQuest analysis, VGA simulation captures, and tests on the physical DE2 board.

### Project preview

![Coin Rush gameplay screenshot captured from the VGA simulation](screenshots/gameplay.png)

[Start screen](screenshots/start.png) · [Pause screen](screenshots/pause.png)



### Technical reports

| Language | Document |
| --- | --- |
| Italian | [Coin Rush — Technical Report (IT)](docs/Coin_Rush_Report_IT.pdf) |
| English | [Coin Rush — Technical Report (EN)](docs/Coin_Rush_Report_EN.pdf) |

The reports cover specifications, FPGA architecture, the game FSM, VGA timing, collision and collection logic, sprite ROMs, the audio subsystem, verification methodology, resource utilization, timing analysis, and experimental results.

### Repository scope

This repository **contains documentation and demonstration screenshots only**. It is **not** a buildable or playable release: the complete Verilog RTL sources, project files and simulation environment are not included. The PDF appendices contain a few selected RTL excerpts for explanation.

---

## Authors

**Matteo Tonini · Antonio Tuma**  
University of Pisa — Electronic Engineering

## Copyright and reuse

This repository is publicly accessible for viewing and educational reference. **No reuse license is granted by the mere publication of these files.** The authors may add an explicit license for the written documentation after agreeing on the terms and checking the rights to any included third-party material.
