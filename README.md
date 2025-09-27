# Wechselbalg 50 (WB50)
Wechselbalg 50 is a 50‑watt tube guitar amplifier built entirely on a PCB. It combines classic British crunch with a modern high‑gain voice, switchable by relay. The name “Wechselbalg” (changeling) nods to the two distinct characters living in one chassis.

> Tagline (working): “Two voices, one heart of iron.”

## Highlights
- Two switchable voicings via relay (Classic ↔ Beast)
- Cascaded 12AX7 preamp with bright peakers
- Cathode follower into a classic T/M/B tone stack
 - Serial FX loop (always active; not bypassable); dual master volumes (post‑loop, RL3 selects)
- Long‑tail‑pair PI → 2× EL34 push‑pull power stage
- Classic British NFB with Presence & Thump (Resonance/Depth)
- Fixed, trimmable bias; regulated 12‑V rail (7812) for relays/loop
- Layout goals: star‑like grounding, short grid leads, disciplined heater routing, decoupled HT nodes

## Circuit overview
1) Input and V1: high‑value grid leak + grid stopper, cathode bypass options for British mid focus.  
2) Voicing section: relay switches additional gain/treble‑peaking networks for the Beast mode.  
3) Cathode follower → passive T/M/B tone stack for low‑impedance drive.  
4) FX loop: buffered send/return; always in circuit (no bypass); two post‑loop master volumes (Rhythm/Lead) with relay selection.  
5) Phase inverter: long‑tail‑pair (12AX7) with balanced plate loads.  
6) Power stage: 2× EL34 fixed‑bias push‑pull; screen resistors; coupling caps per side.  
7) Feedback shaping: Presence and Resonance inside the negative feedback leg from the output transformer secondary.  
8) Power supply: bridge rectifier, choke‑assisted filtering and stepped B+ distribution; regulated 12 V for control circuitry.

## Channel switching and controls
- Channel toggle (front) or footswitch (“SW.” jack) drives a common control line that actuates multiple relays:
	- RL1: preamp voicing (Plexi ↔ BE)
	- RL2: gain pot routing (Gain 1 ↔ Gain 2)
	- RL3: master selection (Volume 1 ↔ Volume 2, both post‑loop)
- The “SW.” jack is a latching footswitch input (no audio). With a plug inserted, the footswitch takes over; without it, the front‑panel CHANNEL mini‑toggle controls the state.
- Result: two distinct channels with their own Gain and Master settings while keeping the FX loop operating at a stable level.
 - Rear control: Thump (Resonance/Depth) shapes low‑frequency feedback for tighter vs. bigger low‑end feel.

## Safety
This project involves lethal voltages up to ~500 V. Only qualified persons should build or service it. Always discharge filter caps, use an isolation transformer, work one‑handed where possible, and wear eye protection.

## Scope & status
This repository aims at a reproducible PCB implementation of a classic small‑box‑style topology (without using protected brand names).  
Planned artifacts: schematic capture, PCB layout, BOM, bring‑up checklist and measurement notes.

## Naming
“Wechselbalg” = changeling/shapeshifter – a subtle hint at the two switchable voices. Short code: WB50.