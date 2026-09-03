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

## 8/29/2026 - New Design Planning
Turns out there were quite the few issues. I never really learned signal integrity before and only just learned my current design was causing many issues because of it's amount of vias. Also learned the fact that I'm supposed to keep a ground pour below were I have high speed signals. So I spent a good amount of time trying to figure out how to fix it. Originally I was drawing out my plan on the routing part but decided to move over the schematics since it would work out better. I also was trying to use PA5 as my MicroSD's SPI clock which isn't correct. So I decided to switch it over to PB0. I also decided to split my buttons and have the microSD in between them. It's better to have a working project than one that's meant to be space efficient.  
<img width="632" height="638" alt="image" src="https://github.com/user-attachments/assets/78ba079d-59ac-4e9a-9182-177f9cac97d1" />  
<img width="1001" height="792" alt="image" src="https://github.com/user-attachments/assets/e1af1530-3496-4d28-952c-fbd369842bb0" />  
## Time Spent: 2 Hours

## 8/29/2026 - Finished Schematic Fixes
I spent my time fixing up the issues. Realized that the CD slot is different than the CS slot so I fixed that mistake. Also moved the SPI Clock to be PB2 in order to keep better signal integrity since using PB0 would've required me to use a via for another trace. I also ended up having to switch up the header connections greatly. I ended up with a huge mismatch with the amount of IO pins on both sides so I ended up keeping all the button pins on the left side while the right side was mainly the leftover IO pins. Sadly this means that there is not BOOT or NRST headers on the right side. I also moved the GND header to be next to the VBUS since I read that was a good thing to do.  
<img width="737" height="755" alt="image" src="https://github.com/user-attachments/assets/95563d7c-4de5-4e01-bbc0-abfff2e95da5" />  
<img width="1048" height="556" alt="image" src="https://github.com/user-attachments/assets/eb824143-56fb-47ce-8946-34236966018b" />  
## Time Spent: 0.7 Hours

## 8/29/2026 - Routing and Major Design Change
I tried to do all the routing and got all the signal traces done well however when it finally came to routing the power traces, I discovered my design ended up blocking out power traces for the MicroSD. I couldn't really use a via to go under on a 2 layer pcb because it was a high speed data line. I ended up deciding to use a 4 layer pcb in order to solve all the issues I was having with signal integrity. This however does mean the PCB will now be costing a few dollars more. I remembered JLCPCB offering an additional discount for 4 layer pcbs below 50mmx50mm so I adjusted the components a bit in order to save some money. However it turns out that I misremembered and the only discount was for pcbs below 100mm by 100mm.
2 Layer:  
<img width="613" height="717" alt="image" src="https://github.com/user-attachments/assets/0a92a5ab-bf2d-4304-8d69-75c5e10f01ed" />
Redesign:  
<img width="497" height="602" alt="image" src="https://github.com/user-attachments/assets/21388030-4eb2-4cee-a837-aaf8fdf1863a" />
## Time Spent: 1.7 Hours
## 8/29/2026 - Routing Progress
So I got all the 4 layer pcb stuff working partially. I got a ground pour filling 1 of the internal layers so that solved many of my issues with signal integrity. After that everything else routed fine. Only thing I will need to do is go through everything properly and make sure nothing is broken since I do believe I have made a few mistake with my internal layers. For example, I do believe there was a different trace length necessary for internal traces which I will need to fix for my +3.3V traces.
<img width="660" height="832" alt="image" src="https://github.com/user-attachments/assets/5cf360ac-e5fd-4bee-ac9e-38e1de650f9c" />
## Time Spent: 0.7 Hours

## 8/31/2026 - Fixed Routing + Edge Cuts
A small devlog today. I fixed the issues with the routing like the 90 degree turns. Increased the trace widths of the inner layers in order for the heat the dissipate better. Was contemplating replacing it with a solid fill but decided it was best not to. I also added the edge cuts and rounded the corners. My previous design with the dog constellation shape using the vias probably won't work out anymore so I'll need to try making a new design next time.  
<img width="580" height="666" alt="image" src="https://github.com/user-attachments/assets/c141219b-a364-4759-ac18-b31bab82a3ea" />  

## Time Spent: 0.3 Hours

## 9/3/2026 - Design and More Fixes
I added all the silkscreens. Was originally planning to change the back silkscreen with the new vias, but I decided to keep the dog constellation shape. I just liked it too much to get rid of it. Along with that I added in pull up resistors for the switches. It should be ready to submit now, just gotta add all the files into github.

## Time Spent: 0.8 Hours

