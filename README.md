# Amiga
A collection of Amiga stuff

dsp3210dist: A package for getting the DSP 3210 on AA3000+ boards going. Contains drivers, example code, Changelog and README to get you started.

GALs: The pld and jed files for U122, U123, U124 and U701 for the AA3000+. Some bugs of the originals in the Haynie archives have been fixed. 

Numerous tests showed that GAL speed is important. The recommended combination is ATF22V10C-5JX for U122, U123, U124 and for U701 
- either ATF16V8-7JU with the "NEW" PLD (works with many accelerators, except CSMK3 and CSPPC), 
- or ATF16V8BQL-15JU with the non-"NEW" PLD (works with many accelerators, except WarpEngine).

For more information and documents on the DSP in question, see Wrangler's repo at https://github.com/Wrangler491/AA3000-DSP
