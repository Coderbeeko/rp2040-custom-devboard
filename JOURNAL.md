Development Journal

Session 1

Date: 9 July 2026

Duration: 45

Project Setup

Today I set up the GitHub repository for the project and got Lapse and Lookout ready for time tracking. I also went through the Horizons hardware requirements to understand what needs to be included before shipping the project.

After looking over the reference RP2040 board, I decided I want to make a small modification instead of copying it exactly. I'm planning to add a WS2812B RGB LED since it only uses one GPIO and will make the board more useful for debugging and status indication.

Next session I'll start modifying the schematic and figure out where to place the LED on the PCB.

------------------------------------------------------------

Session 2

Date: 10 July 2026

Duration: 2 hours 11 minutes

Schematic Completion

Today's session was focused on finishing the schematic for my custom RP2040 development board and preparing it for PCB layout. I added an onboard SK6812MINI-E RGB status LED connected to GPIO25, along with a 330 Ω series resistor and a 100 nF decoupling capacitor.

While running ERC, I found that the downloaded SK6812MINI-E symbol incorrectly defined the DIN pin as a power input. After fixing the symbol and adding the required power flags, the schematic passed ERC with zero errors. I also imported the matching footprint and fixed a pad numbering mismatch so the PCB could be updated successfully.

By the end of the session, the schematic was complete, the PCB had been updated with the new components, and everything was ready for component placement and routing next session.
