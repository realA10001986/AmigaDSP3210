# Amiga
A collection of Amiga stuff

dsp3210dist: A package for getting the DSP 3210 on AA3000+ boards going. Contains drivers, example code, Changelog and README to get you started.

GALs: The pld and jed files for U122, U123, U124 and U701 for the AA3000+. Some bugs of the originals in the Haynie archives have been fixed. 

Numerous tests showed that GAL speed and type are important. The test group settled for ATFs because they are available as new parts.

The recommended combination is ATF22V10C-5JX for U122, U123, U124 and for U701 
- either ATF16V8-7JU with the "NEW" PLD (works with 68030 and many accelerators; notably not CSMK3 and CSPPC), 
- or ATF16V8BQL-15JU with the non-"NEW" PLD (works with 68030 and many accelerators; notable not CSMK2 and WarpEngine).

Here is a list of combinations tested with results:

https://docs.google.com/spreadsheets/d/1c7zMVO1gBBRQ6kRbHjpwxwJw0_Bv94AN07wenYpk3eQ/edit?usp=sharing

For more information and documents on the DSP in question, see Wrangler's repo at https://github.com/Wrangler491/AA3000-DSP
