# ApertureKeyboard
Instructions and resources for how to build the Aperture Keyboard

Version 0.1

## Case
Get a second hand Cherry G80-3000 or any G80-3xxx. Make sure to a non-yellowed one.

Mine cost me 40€

## Switches
You can use any MX switches. My G80-3000 came with Cherry MX Blues which are very clacks, so I got Boba U4 Silent Tactile Switches, but feel free to use whatever you like.

I got my switches for 94€, including shipping 

## Keycaps
I ordered mine on [wasdkeyboards.com](https://www.wasdkeyboards.com/). My keyboard uses the ISO layout, but you can also choose ANSI. Color the keys accordingly. The gray caps on my keyboard use the darkest gray color, not black. 
A design for a german ISO layout can be found [here](wasd-inkscape-105-04.20.2021.svg). My design is a standard layout downloadable at wasdkeyboards.com with an extra Aperture logo in place of a windows key.

The caps cost me 89€, including shipping

## Stabs
The Cherry G80-3000 already has stabalizers. I didn't get any custom ones, they were good enough.

## PCB
My standard G80-3000 PCB had a few problems, which is why I printed my own.

- The space bar switch on the G80-3000 isn't positioned in the middle, but 1u to the left. wasdkeyboards.com only ships space caps with centered stem slots
- The caps lock switch on the G80-3000 is offset to the left, but wasdkeyboards.com only ships caps lock caps with centered stem slots
- No ability to upload custom firmware
- G80-3000 PCB seems to often lag / lock if key presses are entered too quickly. Kind of a random thing but it happens often enough to become frustrating after a bit
- The stock PCB comes with a long PS2 plug. My PC actually has a PS2 slot but USB is always nicer. I also wanted to add a port right into the case instead of having a long cable constantly attached
- The stock PCB extends slightly on the top and bottom, making it significantly harder to reassemble the case

**The PCB design will be uploaded shortly after I made some adjustments to the design**

### PCB Parts and assembly
Not going to list all parts here as you can look them up on the design. The PCB uses an Atmega AT32u4 microcontroller, which is by far the most expensive component. It cost me around 40€.
JLCPCB requires you to order at least 2 fully assembled PCB, which means you will spend quite a buck. I paid 213€, including shipping, for 2 fully assembled boards and 3 empty PCBs without any components and only copper. Yes I now have 4 boards just lying around.

Once you get the PCB be prepared to soldier all 10(4|5) switches. Honestly it sounds harder than it is.

## Firmware
The PCB requires custom firmware to run. You can find my QMK firmware on my [fork here](https://github.com/StefanH-AT/qmk_firmware). (Called GA80-3000 as in G Aperture 80-3000) I might see if I can merge to upstream.

The firmware is free :) Open source software is great, thank you QMK ❤!

### Firmware flashing
The firmware is easy to flash as the microcontroller already comes with a bootloader. The QMK toolkit should do the job, if not, PCB Editor can definitely do it.

### Firmware oddities
My firmware uses QMK's RGB lighting api to control the 3 status leds. If you ever intend to add full RGB to your keyboard, you will have to significantly modify the firmware. Good luck!

Also I unbound the Menu key to act as a function key. If you like that change, consider printing a function key cap. If you rather have a menu key you can just modify the firmware and remove the macro.

## Future tasks
I am not done with this keyboard as I still need to replace the cherry logo with an Aperture logo and want to add a proper USB-C plug. Currently I have a cable hanging straight out the keyboard. It works, but mobility is more limited. 

Once I am done with these changes, I will update this readme
