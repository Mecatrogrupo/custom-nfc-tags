## About
Project with the goal of producing custom homemade shells and antenas for NFC tags using a streamlined workflow. Work has been done to dissolve existing cards and test their chips to retrofit them into custom enclosures.<br/>
Currently this repository contains a coil winder prototype, guide sources for analizing and working with nfc chips, a guide for tuning and making diy antenas, findings on the argentinian system (SUBE), 3d models for standarized tag disks, and keychains and wristbands that work with these.
  
## Quickstart
### About RFID, NFC and tags
RFID stands for “Radio Frequency Identification”, and defines technologies that involve (at least) a card and a reader that talk remotely. NFC stands for “near field communication”, and defines standards based on a set of RFID protocols. Broadly speaking, there exist three kinds of cards that are of interest to us:  
* 125 kHz read-only cards  
* 13.56 mHz “unencrypted” cards  
* 13.56 mHz “secure” cards  

The first kind are used in some locks and check-in and identification systems. They are usually thick keychains or cards. They are not NFC, and thus incompatible with phones, so that is a really easy way to identify them. Information is generally just an unencrypted ID, so you can easily clone them with a generic reader/writer (5YOA IDW01). Keep in mind that some of these cards use some kind of rudimentary encryption or weird non-standard frequencies, so cloning might not be possible or might require specialized equipment.  
  
13.56 mHz NFC cards are the kind that interface with a phone, which you can use to check their IDs. The unencrypted kind (often used in building doors) only contain an ID, so the easiest way to interface with these systems is by cloning the chips with a Rc522 and an arduino, and then finding an off the shelf tag that has a desired shape. They are also the cheapest and most versatile ones, so they are great for personal projects.  
  
As transit systems and secure environments can’t rely on credentials that can be easily spoofed, the last kind of tags have encrypted information and can store more data (like a card’s balance). The encryption algorithms are generally unknown, and cracking them is generally too involved for making more than a couple (and in some cases may also be illegal).  
  
This repository mainly aims at extracting the chips from these last kinds of tags for reusing them in custom enclosures, and finding ways of streamlining this process for small scale production.

### Designing an antenna
TODO

### Making an enclosure
TODO

### Testing
TODO

### Further reading/sources
TODO


<hr />
<table border="0px">
<th align="left">
Mecatrogrupo 2022.
</th>
<tr>
<td>
This source describes Open Hardware and is licensed under the 
CERN-OHL-W v2
</td>
</tr>
<tr>
<td>
You may redistribute and modify this documentation and make products
using it under the terms of the CERN-OHL-W v2 (https:/cern.ch/cern-ohl).
This documentation is distributed WITHOUT ANY EXPRESS OR IMPLIED
WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY
AND FITNESS FOR A PARTICULAR PURPOSE. Please see the CERN-OHL-W v2
for applicable conditions.<br/>
Source location: https://github.com/Mecatrogrupo/custom-nfc-tags/
</td>
</tr>
</table>
