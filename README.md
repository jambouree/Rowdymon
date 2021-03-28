# How to play
## Emulator
1. Download a legal Game Boy emulator (we recommend KiGB http://kigb.emuunlim.com/downloads.htm)
2. Download rom.zip from this directory (not the rom folder, that is part of the source code)
3. Load in the zip file to your emulator and enjoy!

## HTML5
* Simply navigate to rowdymon.netlify.app and enjoy!

## Soundtrack
1. Download VLC Media Player (you will need this to run .mod files)
2. Download tracks from this repository's main/soundtrack

# INFO

## Inspiration
Inspired by several retro, chiptune game series, Rowdymon seeks to emulate the classic monster-training genre with an on-theme twist! Like most children who came of age during the early 21st century, we've always has a soft spot for this archetype and wanted to create something reminiscent of some of our fondest memories. We hope you're impressed by what Rowdymon has to offer, and that you have as much fun playing as we did creating it!

## What it does
Rowdymon is a ROM built for the Nintendo Game Boy®, which can also be enjoyed using an emulator or our HTML5 port. A top-down RPG trainer, Rowdymon comes equipped with original sprites and backgrounds, as well as a full OST! This game allows you to capture, train, and battle your very own Rowdymon, complete with the ability to save and continue your file. Compete to become the absolute best, like none has been before!

## How we built it
We used GBStudio, an indie-made development software, to design, compile, and port the game as a fully functional cartridge ROM. To conform our resources fully to the Game Boy hardware, we created our assets using the following software:
Soundtrack: MilkyTracker (a chiptune audio workshop which generates compact .mod files)
Backgrounds: Tiled (an image designer built for 16-bit gaming devices)
Sprites: GNU Image Manipulation Program

## Challenges we ran into
Creating a game built for a 16-bit operating system and hardware means we had to do a bit of backwards time-traveling, which foreseeably came with a great deal of bugs and limitations! We encountered many software errors when compiling our soundtrack and had to implement several workarounds to properly format our music for the GB sound card. Despite all of this, for some unknown reason we still couldn't get the music to play within the ROM. :( We put in too much work to leave this out, though, so you can find our soundtrack in the Github repository!
GBStudio is also still in it's beta release, meaning we had to develop several algorithms to work around some functional limitations, such as the inability to define an object class. The battle system was especially tough to implement.
Finally, our biggest issue: exhaustion! We put a LOT of effort into this game to polish it the most we could, which took up a great amount of time. Nonetheless, we hope you're as proud of the finished product as we are!

## Accomplishments that we're proud of
* Learning to work with several new development software, as well as entirely new hardware!
* Overcoming technical difficulties, as always, with every program!
* Generating our artistic assets originally (with the exception of some publicly-released icons), including our own chiptune soundtrack!

## What we learned
* How to design and export pixel art with a limited color pallette
* Designing .mod files and sound generation with a 16-bit tracker
* Game-building with GBStudio and Tiled

## What's next for RowdyMon
Expanding the map, adding a leveling feature, and implementing item storage are all some great ideas we're considering for Rowdymon. We'd love to add cross-device trading and learn how to work with the Game Boy link cable (another exciting hardware hack)!


# About our development software

## JavaScript GameBoy Color Emulator

Fork of Grant Galitz's JavaScript GameBoy Color Emulator made for running a single ROM
when uploading homebrew games to services like Itch.io.

This version makes the following changes.

- Canvas fills browser window on desktop/tablet while keeping aspect ratio
- Touch controls displayed on mobile/tablet 
- Using css `image-rendering: pixelated` rather than bilinear filtering
- Touch dpad controls for mobile using touch move with a deadzone
- Keyboard fix for iPad keyboard case that doesn't report keyup event keycode
- Wait for keyboard or touch input before starting AudioContext to fix issues in Chrome and iOS not playing Audio
- No ability to switch ROM, or save/load states, this version is intended for deploying a single game

## Usage

- Clone this repository
- Add your ROM file as `rom/game.gb` (or edit romPath in js/other/mobile.js to point to your ROM file)
- Upload to a webserver and visit index.html

## Keyboard Controls

Up - Up Arrow / W  
Down - Down Arrow / S  
Left - Left Arrow / A  
Right - Right Arrow / D  
A - Alt / Z / J  
B - Ctrl / K / X  
Start - Enter  
Select - Shift  

Edit by changing `bindKeyboard` in `js/other/controls.js`.

## License

**Copyright (C) 2010 - 2016 Grant Galitz**

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
