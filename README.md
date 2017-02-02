# RptrIDer

Teensy3.2 Based Repeater Controller

This is a very simplistic repeater controller I built for Sherwin WB7NFX.
Included in the project is manual, schematic, eagle board files and the
Arduino sketch file for a Teensy3.2 board.

The repeater controller was designed to interface to a Westel DRB25 VHF
repeater.  This repeater did not have capability to ID per FCC Part 97 rules
and since the machine was to be used on the 2m ham band, this was a must.

Sherwin wanted the repeater to generate a Voice ID and provided me with a
small PCB that performed audio recording and playback.  I decided to build up
this board and have it controlled by a small ATtiny85 processor.  Shortly I
wanted to add CW support and have more input/outputs for buttons and LED's
so moved to an Teensy3.2 board I had purchased but had not found a project
to use it with.  A repeater controller seemed ideal.

Front panel was to have LED's to indicate status of the repeater and
controller operations.  When PTT, CW ID, Voice ID, Carrier Detect and status
for when the Voice Recording is erased or recorded.  There's also a heartbeat
and init status LED.

Interface to the repeater is via an RJ45 jack on the transceiver card.
There was an empty set of slots in the chassis for me to add a panel, speaker
microphone jack, LED's, buttons and switches and a volume control.  It also
mounts a home brew PCB that houses the Teensy and Voice ID boards.

The board is very simple 3 channel audio mixer with header for the Teensy3.2
and a voice ID board.  Uses standard header pins since that's what I had and
allowed me to debug this on the desk vs. connected to the repeater.

The Teensy3.2 is responsible for time keeping, generating a CW ID, detecting
inputs such as PTT, and front panel buttons and implements simplistic Carrier
Detect to know when the repeater is in use.  Westel did not have COS line
for me to use.  Power for the board is supplied by the transceiver card and
total current at 12v is around 150ma max.

There is a directory with photo's of the project, and if you search on
YouTube you can find a movie of the prototype in use during debug of the
project.

Special thanks goes to SV1DJG, Nick in Greece who developed the CW Beacon
sketch I leveraged into this project.

This project is available via GPL for your use.

Feel free to drop me an email if you have any questions on the project and
I'll try to answer them as best I can.  Please note, the code was quickly
developed and is probably still has a bug or two.

WB7NFX Repeater is operational in Chino Valley Az @ 144.570/145.170 Mhz with
PL of 100.0 Hz.


73,
Doug - NO1D
