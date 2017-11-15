# DummyCANTalon
A dummy CANTalon library for code emulation using Autodesk BXD Synthesis.
## Context
BXD Synthesis' code emulation and HAL doesn't have any support for CAN Talon (or the CAN bus as far as I'm aware). Spartronics uses CANTalons extensively in our robots, which made our existing codebase unworkable with Synthesis' current state.
## Purpose
 This is inteded to be built as a drop in replaecment JAR for the regular library, and to allow our team (and others) to utilise Synthesis' code emulation capabilities. This library is intended to be a _dummy_, simply something to get your code to run without any issues, not something to emulate any actual CANTalon functionality (although there is a little bit of code to preserve state, to avoid breaking things). It is my hope that we can use this to catch bugs in our code before deploying to the robot and spending valuable time debugging on that system-Synthesis can build and "deploy" your code much faster than on an actual robot, and allows for many instances (unlike with robots, even if you have a tester chassis).
## Roadmap
There is currently enough dummy code here to get [a version](https://github.com/pietroglyph/2017-STEAMworks/tree/controlmanager-sim) of our codebase from the 2017 game to run in the emulator without issues.

If I have the time I would like to expand this library to include all of CANTalon's functionality (it shouldn't be terribly difficult to do, there's little functional code here).
## Building the project
```bash
 $ git clone https://github.com/pietroglyph/DummyCANTalon

 $ cd ./DummyCANTalon/src/com/ctre/

 $ jar -cf DummyCANTalon.jar *.java

 $ mv ./DummyCANTalon.jar <WHEREVER YOU WANT YOUR JARFILE>
```
## Examples
![Example of a real codebase running DummyCANTalon](https://raw.githubusercontent.com/pietroglyph/pietroglyph.github.io/208998eca3a393ffce6003f737a164f025705ea7/_site/assets/example_dummycan.png)
