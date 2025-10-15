Assembly Instructions – VoxAble Assistive Communication Device
Overview

This document explains how to assemble and customize the VoxAble assistive communication device.
The device uses an Arduino Nano, a DFPlayer Mini MP3 module, a 16-key keypad, and a 3-watt speaker, powered by 18650 lithium-ion batteries and enclosed in a 3D-printed casing.
The instructions cover breadboard testing, wiring, enclosure preparation, final assembly, and customization of audio files.

Components and Tools
Components

Arduino Nano V3.0

DFPlayer Mini MP3 player module

16-key membrane keypad

3-watt 8-ohm speaker

Two 18650 lithium-ion batteries

Dual 18650 battery holder

Power switch

Breadboard and jumper wires

3D-printed enclosure (enclosure design.stl)

Tools

Breadboard for initial prototyping

Wire stripper and cutter

Screwdriver set

Digital caliper or ruler

3D printer with PLA filament

Hot-glue gun or adhesive

Laptop with Arduino IDE and microSD card reader

Step 1. Breadboard Setup and Initial Wiring

Place the Arduino Nano on a breadboard.

Connect the DFPlayer Mini to the Arduino Nano as follows:

DFPlayer Pin	Arduino Pin	Description
VCC	5V	Power input
GND	GND	Ground
TX	D10	Serial transmit
RX	D11	Serial receive
SPK1	Speaker +	Audio output
SPK2	Speaker –	Audio output

Connect the 16-key keypad to the Arduino Nano:

Rows (R1–R4) → D9, D8, D7, D6

Columns (C1–C4) → D5, D4, D3, D2

Connect the power switch inline with the battery’s positive terminal.

Power the circuit via USB or battery pack.

Upload test firmware using the Arduino IDE and confirm that keypad presses trigger sound playback.

Step 2. Measuring Components for the Enclosure

Measure the approximate dimensions of each component to confirm enclosure fit.

You do not need precision measurements; approximate sizes are sufficient if you are using standard modules.

Check the following general dimensions:

Arduino Nano: 45 × 18 × 8 mm

DFPlayer Mini: 22 × 18 × 3 mm

Speaker: 40–45 mm diameter

Keypad: 70 × 77 mm

Battery holder: 76 × 40 × 22 mm

Power switch: 12 mm mounting hole diameter

Allow a few millimeters of clearance when designing or printing your enclosure.

Step 3. Printing the Enclosure

Open enclosure design.stl or enclosure design.step in your slicer.

Recommended print settings:

Layer height: 0.2 mm

Infill: 20%

Wall thickness: 1.2 mm

Material: PLA or PETG

Print both the base and top shell.

Test-fit all components before proceeding to final assembly.

Step 4. Mounting Components

Mount the battery holder inside the base and secure it with screws or hot glue.

Position the Arduino Nano and DFPlayer Mini so that their USB and SD card ports are accessible.

Mount the speaker behind the circular grill in the enclosure.

Pass the keypad cable through the front slot.

Mount the power switch through the side opening.

Verify that each component fits comfortably.

Step 5. Internal Wiring and Final Connection

Reconnect all components as per the breadboard wiring diagram.

Keep wiring short and tidy; group wires by signal type.

Connect all ground lines to a common GND point.

Double-check all connections before applying power:

Red wire to VIN or 5V (depending on power input)

Black wire to GND

DFPlayer Mini connected to Arduino pins D10 and D11

If soldering, keep wire insulation close to terminals and avoid exposed leads.

Step 6. Testing the Circuit

Insert batteries and turn on the power switch.

Confirm that the Arduino Nano’s power LED lights up.

Press each keypad button and verify that the corresponding audio plays.

Check that the speaker output is clear and volume is sufficient.

If using rechargeable cells, ensure total voltage is about 7.4 volts.

Turn off the device after testing.

Step 7. Customizing Audio Files

Prepare a microSD card (formatted as FAT32).

Create a folder named mp3 or 01 depending on your code setup.

Place your audio files on the card using the correct numbered file names.

DFPlayer Mini recognizes files by numeric names only.

Example file naming format:

0001.mp3
0002.mp3
0003.mp3
...


Each number corresponds to a keypad button in your Arduino code.
For example:

Button 1 → 0001.mp3

Button 2 → 0002.mp3

Button A → 0010.mp3 (if mapped in your firmware)

Store your audio files in MP3 or WAV format. Keep file sizes small for faster playback.

Insert the microSD card into the DFPlayer Mini.

Turn on the device and test each button to confirm the correct audio file plays.

To change or add new audios:

Replace the files on the SD card with new audio clips using the same numeric names.

Update your Arduino code only if you want to change the button-to-audio mapping.

Tips for audio customization:

Record voice messages at 44.1 kHz mono for clear output.

Keep file names consistent (four-digit numbering).

Do not include spaces or letters in file names.

Always eject the SD card safely from your computer before reinserting it into the DFPlayer.

Step 8. Closing the Enclosure

Place all modules and wires securely inside the enclosure.

Attach the top cover and align all sides properly.

Secure the top cover using screws or clips.

Check that the keypad, speaker, and switch remain accessible.

Turn on the device again and perform a full functionality test.

Step 9. Maintenance and Notes

Recharge the batteries externally using an 18650 charger.

Update firmware by connecting the Arduino Nano’s USB port to a computer.

Replace or add new audio files on the SD card as needed.

Keep the speaker vent and keypad clean and dry.

Store the device at room temperature and avoid excessive heat or moisture.
