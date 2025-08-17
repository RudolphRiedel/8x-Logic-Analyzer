# 8x-Logic-Analyzer

## what is this?
8 channel RP2350 logic analyzer hardware

This is a contribution project for: https://github.com/gusmanb/logicanalyzer
It might end up as a pull-request someday, however I am using version 6.5 which is still in beta.

## what the heck, why more hardware?

I was intrigued by logicanalyzer project, inexpensive, yet fast and with plenty of channels.
I have no use for 24 channels though, I did not like the daughter-board approach very much
and I had experience with 5V tolerant logic which makes switching the external reference obsolete.
Plus I had not done anything with the RP2350A before.

So I took this as an opportunity to design a RP2350A board.
Limited to 8 channels with no option to cascade, this is plenty for SPI plus four more pins.

I did two hardware revisions so far, the first is up and running, the second is functionally the same
with some details tweaked and I just ordered it.

![8x-Logic-Analyzer](/Hardware/Logic-Analyzer-01-01.png?raw=true)

![8x-Logic-Analyzer](/Hardware/Logic-Analyzer-01-02.png?raw=true)

This repository has the complete set of files for the Logic-Analyzer-01-02 design.
I just ordered five boards from JLCPCB with the gerber set Logic-Analyzer-01-02.zip, the BOM Logic-Analyzer-01-02_BOM.xlsx and the pick&place list Logic-Analyzer-01-02_CPL.xlsx.

There also is a .pdf included with the schematic: \Hardware\Logic-Analyzer-01-028x_Logic-Analyzer.PDF

## software?

This repository only has a modified version of the LogicAnaylzer_V2 firmware from the V6.5 branch.
I modified the files and added a new board: BOARD_PICO2_8X
To do that I changed CMakeLists.txt, LogicAnalyzer_Board_Settings.h, LogicAnalyzer_Build_Settings.cmake and publish.ps1
And with only 8 channels I was able to tweak the sample buffer from the original 384kiB to 469kiB.

As for the application, I am using the 6.5 beta that was made available here: https://github.com/gusmanb/logicanalyzer/discussions/277
