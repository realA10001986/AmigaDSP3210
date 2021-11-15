# Amiga and DSP 3210

### dsp3210dist: 

A package for getting the DSP 3210 on the AA3000+ going. Contains drivers, docs, GAL logic and example code to get you started. (A driver extension for ATL DSP Zorro boards is also included, albeit entirely untested and possibly incomplete.) 

For **comprehensive info** on the DSP, also see "Doc" folder here.

### GALs: 

The pld and jed files for U122, U123, U124 and U701 for the AA3000+. Some bugs of the originals in the Haynie archives have been fixed. Update 2021-06-20: U124 fixed to make bits actually stick. 

Numerous tests showed that GAL speed and type are essential. The test group settled entirely for ATFs because they are available as new parts.

The recommended combination is **ATF22V10C-5JX** for U122, U123, U124; and for U701: 
- either **ATF16V8-7JU** with the **"U701_ATF16V8-R8"** logic (works with 68030 and several accelerators; notably *not CSMK3 and CSPPC)*, 
- or **ATF16V8BQL-15JU** (or any other ATF-15ns type) with the **"U701_ATF16V8-R9"** logic (works with 68030 and several accelerators; notably *not CSMK2 and WarpEngine*).

Be aware that these timing recommendations are only valid for ATFs, not GALs. ATFs and GALs are not fully compatible timingwise.

If you are using a TL866II to program the ATFs, the 22v10s need to be burned in "UES" mode.

Here is a list of combinations of ATFs tested with results:

https://docs.google.com/spreadsheets/d/1c7zMVO1gBBRQ6kRbHjpwxwJw0_Bv94AN07wenYpk3eQ/edit?usp=sharing

Please note: Hese's AA3000+ boards from before 2021 turned out to have one DSP related tracing bug. The signals "**RW**" and "**R_W**", despite their different name, are in fact one and the same, while Hese treated them as two separate signals. In fact, they need to be connected for the DSP to work. The easiest way for already assembled boards is to run a wire from U122 pin 5 to U124 pin 27. See https://github.com/realA10001986/Amiga/blob/main/RW-R_W.jpg - the pink spots mark the pins to be connected to each other. This is accomplished easily by making a wire noose around the ATF's pin and soldering it to this pin at the very top of the package, so it's above the socket spring when the chip is in its socket.

