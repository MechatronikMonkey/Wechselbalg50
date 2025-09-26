# Wechselbalg 50 (WB50)
Wechselbalg 50 is a 50‑watt tube guitar amplifier built entirely on a PCB. It combines classic British crunch with a modern high‑gain voice, switchable by relay. The name “Wechselbalg” (changeling) nods to the two distinct characters living in one chassis.

> Tagline (working): “Two voices, one heart of iron.”

## Highlights
- Two switchable voicings via relay (Classic ↔ Beast)
- Cascaded 12AX7 preamp with bright peakers
- Cathode follower into a classic T/M/B tone stack
- Serial FX loop (relay‑bypassable), dual master volumes (pre/post)
- Long‑tail‑pair PI → 2× EL34 push‑pull power stage
- Classic British NFB with Presence & Resonance (Depth/Tight)
- Fixed, trimmable bias; regulated 12‑V rail (7812) for relays/loop
- Layout goals: star‑like grounding, short grid leads, disciplined heater routing, decoupled HT nodes

## Circuit overview
1) Input and V1: high‑value grid leak + grid stopper, cathode bypass options for British mid focus.  
2) Voicing section: relay switches additional gain/treble‑peaking networks for the Beast mode.  
3) Cathode follower → passive T/M/B tone stack for low‑impedance drive.  
4) FX loop: buffered send/return; loop can be bypassed by relay; pre/post masters for practical level control.  
5) Phase inverter: long‑tail‑pair (12AX7) with balanced plate loads.  
6) Power stage: 2× EL34 fixed‑bias push‑pull; screen resistors; coupling caps per side.  
7) Feedback shaping: Presence and Resonance inside the negative feedback leg from the output transformer secondary.  
8) Power supply: bridge rectifier, choke‑assisted filtering and stepped B+ distribution; regulated 12 V for control circuitry.

## Safety
This project involves lethal voltages up to ~500 V. Only qualified persons should build or service it. Always discharge filter caps, use an isolation transformer, work one‑handed where possible, and wear eye protection.

## Scope & status
This repository aims at a reproducible PCB implementation of a classic small‑box‑style topology (without using protected brand names).  
Planned artifacts: schematic capture, PCB layout, BOM, bring‑up checklist and measurement notes.

## Naming
“Wechselbalg” = changeling/shapeshifter – a subtle hint at the two switchable voices. Short code: WB50.


