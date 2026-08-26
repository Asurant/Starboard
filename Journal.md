# PY32 Devboard

## 8/12/2026 - Parts and Schematics

I spent some time brainstorming on what to make. Ended up deciding to make a PY32 devboard. Took me a while to decide what exact PY32 MCU to use but ended up using the PUYA PY32F002BD15S6TU. It's basically a PY32 with 14 pins. I started on the schematics and decided to use a 6 pin USB C connector. Couldn't remember why there was an EH pin so it took me a bit to figure it out, it's just for shielding so it goes to ground. Overall nothing big was done, I do however have ideas on what to do next. I probably will add a way to add a microSD since I never actually did that before. Also solves the problem with storage for it. 
<img width="631" height="404" alt="image" src="https://github.com/user-attachments/assets/47261a99-2bb9-4252-8153-25dd673789ba" />  
## Time Spent: 1 Hour

## 8/13/2026 - Added MicroSD And Schematics Progress

I added the MicroSD today. Took me a while to figure out how it worked and get it set up. I also ended up discovering that MicroSDs used way more pins than I expected (they use 6 at minimum) so I ended up having to switch a 20 pin PY32 (PUYA PY32F002BF15P6TR) since I don't see much use in a large 4 pin devboard. I ended up also discovering at PY32s don't accept USB peripherals on default so I had to go add a CH340 interface controller to allow the USB to actually be used. I also ended up spending a good amount of time understanding the datasheet for the pins and which microSD pins to connect back to the MCU. Along with this I forgot the USB C I was using was a power only USB C. So it pretty much served 0 purpose in this scenerio since it couldn't transfer data so I had to switch it out.
<img width="1226" height="738" alt="image" src="https://github.com/user-attachments/assets/506bb164-7dcf-475f-83b3-12570982a93e" />
## Time Spent: 1.2 Hours

## 8/14/2026 - Schematic Completed
I completed the schematic. Nothing much got added, I added buttons and GPIO pins. However it took me a while to figure out how to do that since in the past I never actually added buttons to my devboards, mainly focused around keeping it small. Also ended up doign some additional research and discovered that the GPIO pins could also be used for reset and boot. However it took me a while to figure out how to do that but in the end it just ended up being that I could just connect it to the setup I had for the button. No additional fancy things. I also allowed the user to use VBUS and 3.3V GPIO pins to power the pcb.  
<img width="996" height="546" alt="image" src="https://github.com/user-attachments/assets/2a64e82b-889c-4690-9c8b-299790b5ac5f" />  

## Time Spent: 1.7 Hours

## 8/15/2026 - Footprints And Schematic Changes
Not much done today mainly because I was busy. I added in the footprints for everything but had some errors pop up when I was transferring the schematic into the pcb. Turns out the design for the USB C footprint was different that the schematic symbol so I had to change the schematic and rewire it. For some reason there appears to be an extra 4 pins on the MicroSD but I'll have to check that out another time.  
<img width="1085" height="633" alt="image" src="https://github.com/user-attachments/assets/9da7cb06-e562-49ba-8ab5-df52caf5a19b" />  
<img width="670" height="696" alt="image" src="https://github.com/user-attachments/assets/9c9a6ba5-f720-4ab5-b94c-0e75c1445784" />  
<img width="565" height="430" alt="image" src="https://github.com/user-attachments/assets/299dd13b-677c-43b3-97c0-be1308709ed9" />  
## Time Spent: 0.5 Hours

## 8/16/2026 - Placed Components
I placed all the components in hopefully the most efficient manner. I realized there was nothing stopping me from keeping the space I used more efficient by putting the PY32 and the CH340 on the bottom. Thanks to that I was able to better place all of my components and keep them in an area that's about 45mm by 25mm. So pretty small which is surprising. Took me a while to actually get the buttons right because by the way they were originally, it would've caused issues for when I placed all the silkscreens. I'm going to have to add all the of gpio silkscreens and actually route the components next. Hopefully nothing is wrong.  
<img width="388" height="566" alt="image" src="https://github.com/user-attachments/assets/131ae4db-5ea6-47d9-96f0-61138854719f" />

## Time Spent: 1.5 Hours

## 8/17/2026 - Redesign and Routing
I redesigned the board from the ground up. When I started routing the parts, I realized I didn't place the components in the best way and also that there were many improvements I could make. So I went back and moved around the components and even changed the schematic so I could route it easier. I was thinking about switching to a 4 layer board but it ended up not being that difficult so I was able to just simply use 2 layers. After I placed all the parts better I ended up with a pcb that's about 40mm by 25mm. However when I did a DRC check I discovered that the silkscreens for a lot of the parts were too small so I will need to adjust them.
<img width="719" height="825" alt="image" src="https://github.com/user-attachments/assets/c1de32b2-55b3-4b31-9fb6-385913b034c7" />

## Time Spent: 2.6 Hours

## 8/19/2026 - Silkscreen Fixes
Since I had to increase the size of the silkscreen I also had to move the gpio headers further out so the text could fit. Didn't take my long but most of the time was spent rerouting those parts since the old routing needed to be extended.

<img width="494" height="563" alt="image" src="https://github.com/user-attachments/assets/f2e6a556-97eb-4fd7-a3e2-def5a8d7c061" />

## Time Spent: 0.5 Hours

## 8/19/2026 - Redesign
Under the advice of another person I did another redesign to move all the parts onto one side so I could keep the art on the other side however I now realized that the LDO is still below the USB. This means I'll have to move around the parts again. I'll probably just move the USB down in order to minimize the changes that need to be made.
<img width="572" height="815" alt="image" src="https://github.com/user-attachments/assets/c75d05d5-d03e-43e0-9870-bff34a1b3299" />

## Time Spent: 1.2 Hours

## 8/20/2026 - LDO fixes
Just some simple fixes. Got the LDO on the top and also had to move around some other parts since the LDO ended up causing more changes than I expected. I also ended up discovering I made a mistake with my +3.3V routing so I went and fixed that. All I need to do now is add some silkscreen and an actual edge cut to make it polished.  
<img width="385" height="606" alt="image" src="https://github.com/user-attachments/assets/63beba64-8102-4f0a-94a7-d4c950fe56fa" />

## Time Spent: 0.5 Hours

## 8/22/2026 - Silkscreen
I just realized I never did the devlog for the silkscreen and all. I basically experimented with a bunch of designs and tried them out. Originally put in too many stars but later I wanted to see how it would look if I connected all the vias with a silkscreen and it ended up looking a bit nice. I decided that I could probably name the devboard something like Starboard cause of all the star designs.

<img width="391" height="568" alt="image" src="https://github.com/user-attachments/assets/1af2edc3-ee95-4618-9666-5a387d477a93" />

## Time Spent: 1.5 Hours

