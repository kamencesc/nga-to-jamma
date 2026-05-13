# nga-to-jamma

**Neo Geo AES / AES+ to JAMMA / MVS Video & Control Adapter**

A passive/active adapter board that allows a **Neo Geo AES (original or AES+)** RGB SCART output to interface directly with a **JAMMA / MVS** edge connector, including video conditioning, audio routing, and controller passthrough.

This board is intended for arcade cabinets, superguns, test benches, and JAMMA/MVS setups where you want to use an AES console as a video and control source.

----------

## Features

-   RGB video input from Neo Geo AES SCART
-   Sync conditioning using LM1881 sync stripper
-   RGB amplification and buffering using THS7314 / THS7316
-   Direct controller passthrough via DA-15 connector
-   Stereo or mono audio routing via jumper configuration
-   Compatible with JAMMA and MVS pinouts
-   Optional through-holes for user modifications and expansions
-   Can be used with a DA-15 cable or hard-wired DA-15 lead

----------

## How It Works

### Video Path

The RGB and composite sync from the SCART connector are processed before reaching the JAMMA edge:

1.  Sync is cleaned using an LM1881 sync stripper.
2.  RGB signals are buffered and amplified through a THS7314 / THS7316 video amplifier.
3.  Conditioned video is sent to the JAMMA/MVS video pins.

This ensures stable sync and correct signal levels for arcade monitors and superguns.

### Controls

Controller signals are passed through directly from the Neo Geo DA-15 standard:

-   Use a **DA-15 male-to-male extension cable (straight-through / 1:1)**, **or**
-   Solder a DA-15 cable directly to the PCB.

⚠️ **Important:**  
The cable must be straight-through (pin 1 → pin 1, pin 2 → pin 2, …).  
Do **not** use VGA (HD15) cables or null-modem / crossover serial cables.

No logic or remapping is performed — this is a pure passthrough.

### Audio Configuration

Audio routing is configurable using onboard jumpers:

-   **Stereo passthrough** from SCART to JAMMA pins **10 / F**
-   **Mono mix** routed to JAMMA pin **11**

This allows compatibility with cabinets wired for stereo or mono audio.

----------

## Configuration Jumpers

Jumper

Function

Description

AUDIO

Stereo / Mono

Selects stereo passthrough or mono mix to JAMMA

(optional pads)

Mod points

Through-holes for custom mods or signal rerouting

----------

## Usage

1.  Connect Neo Geo AES RGB SCART to the board.
2.  Connect the JAMMA edge to your cabinet / supergun / MVS harness.
3.  Connect controller using a **DA-15 male-to-male extension cable** or soldered lead.
4.  Set the audio jumper according to your cabinet wiring.
5.  Power on.

----------

## Compatibility

-   Neo Geo AES (original model)
-   Neo Geo AES+
-   JAMMA harnesses
-   MVS pinout systems
-   Arcade CRT monitors
-   Superguns

----------

## Notes for Builders / Modders

-   The board includes extra through-holes for optional improvements or signal tapping.
-   Designed to be simple, serviceable, and mod-friendly.
-   All video conditioning components are standard and easy to source.

----------

## License

This project is licensed under the **Apache License 2.0**.
