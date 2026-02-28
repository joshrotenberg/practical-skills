---
name: electrical
description: "Use this skill when the user needs an outlet installed, a circuit added, a fixture wired, or a panel upgraded. Also triggers on 'my outlet doesn't work', 'the lights are flickering', 'I want to add a dedicated circuit for my workshop', or 'I'm upgrading to a 200-amp panel'. Do NOT use for low-voltage electronics, network cabling, or Arduino projects."
license: Master Electrician License required. All work must comply with NEC 2023 and local amendments.
metadata:
  author: joshrotenberg
  version: "1.0"
  references: "NFPA 70 (NEC) 2023, Ugly's Electrical References 2023 Edition, Wiring Simplified 46th Edition (Richter/Hartwell)"
---

# Electrical — Wiring, Panel Upgrades, and Circuit Installation

## Overview

A residential electrical system distributes power from the utility service through a main panel containing circuit breakers to branch circuits serving outlets, switches, and fixtures. Standard residential service in the US is 120/240V split-phase. A 120V circuit uses one hot (black), one neutral (white), and one ground (bare copper or green). A 240V circuit uses two hots (black and red), a neutral (white, if needed), and a ground.

All conductor sizes are American Wire Gauge (AWG), where lower numbers indicate thicker wire. 14 AWG is rated for 15A circuits. 12 AWG is rated for 20A circuits. Using undersized wire for the breaker amperage is a fire hazard and a code violation. See [references/WIRE-SIZING.md](references/WIRE-SIZING.md) for the complete ampacity table, cable designations, and box fill calculations.

## Prerequisites

- Non-contact voltage tester (tick tracer). Test it on a known live circuit before relying on it.
- Digital multimeter capable of AC/DC voltage, resistance, and continuity
- Wire strippers rated for 14–10 AWG
- Lineman's pliers and needle-nose pliers
- Screwdrivers: #2 Phillips, 1/4" and 3/16" flat, and an insulated set rated to 1000V
- Fish tape or fiberglass glow rods for pulling wire through walls
- Cable ripper for stripping Romex sheathing
- Headlamp and a helper, depending on the run

Turn off the circuit at the breaker before beginning any work. Verify the circuit is dead with your non-contact tester, then confirm with a multimeter set to AC volts across the hot and neutral. It should read 0V. Then test the meter on a known live circuit to confirm the meter itself is working. This three-step verification catches the scenario where your tester's battery is dead and it's showing "no voltage" on a live wire.

## Installing a New 20A Outlet on an Existing Circuit

### Step 1: Plan the location

Mark the outlet box location on the wall. Standard outlet height is 12" from finished floor to the bottom of the box. Use a stud finder to locate framing and avoid placing the box where a stud is. For an old-work (retrofit) box, you want open drywall between studs.

Trace the outline of the old-work box on the drywall and cut it out with a drywall saw. Do not cut aggressively — there may be existing wiring or plumbing behind the wall.

### Step 2: Run the cable

Determine the route from the new outlet to the existing circuit you are tapping into. For attic or basement access, drill down or up through the wall's top plate or sole plate using a 3/4" spade bit or auger. Use a fish tape to pull 12/2 NM-B (Romex) cable from the source to the new box.

Leave 8–10" of cable protruding from each box for making connections. Strip 6–8" of the outer sheathing using a cable ripper, being careful not to nick the insulation on the individual conductors.

### Step 3: Wire the outlet

Strip 3/4" of insulation from the black (hot) and white (neutral) conductors using wire strippers set to 12 AWG.

Connect to a 20A-rated duplex receptacle:
- Black wire to the brass-colored screw (hot)
- White wire to the silver-colored screw (neutral)
- Bare copper wire to the green screw (ground)

Form a hook on the stripped wire end with needle-nose pliers, wrap it clockwise around the screw terminal so tightening the screw closes the hook, and torque to the specification stamped on the receptacle (typically 12 in-lbs). Do not use the push-in (backstab) connections on the back of the receptacle. They are permitted by code but have a higher failure rate over time.

Fold the wires neatly into the box and mount the receptacle with the provided screws. Install the cover plate.

### Step 4: Connect at the source

At the existing outlet or junction box you're tapping into, join the new cable's conductors to the existing circuit using wire nuts or Wago lever connectors: black to black, white to white, ground to ground. Each connection should be mechanically secure — tug on each wire to verify. Push the connections into the box and close it.

### Step 5: Test

Turn the breaker back on. Use an outlet tester (the three-light plug-in type) to verify correct wiring: two amber lights indicate correct hot-neutral-ground. Any other pattern indicates a wiring error — kill the circuit and check your connections.

Verify voltage with a multimeter: 118–122V between hot and neutral, 118–122V between hot and ground, 0V between neutral and ground.

## Adding a GFCI Outlet

GFCI protection is required by code in kitchens, bathrooms, garages, unfinished basements, and all exterior outlets.

A GFCI receptacle has two sets of terminals: LINE and LOAD. The LINE terminals connect to the incoming power. The LOAD terminals feed downstream outlets that will also be protected by this GFCI.

Connect the incoming hot (black) and neutral (white) to the LINE terminals. If protecting downstream outlets, connect the outgoing conductors to the LOAD terminals. Do not reverse LINE and LOAD — the GFCI will not function.

After installation, press the TEST button. The RESET button should pop out and the outlet should go dead. Press RESET to restore power. If the TEST button does not trip the GFCI, the unit is either defective or wired incorrectly.

## Panel Upgrade: 100A to 200A Service

This requires a permit, coordination with the utility to disconnect power at the meter, and a final inspection. In most jurisdictions, a licensed electrician must pull the permit.

The scope includes: replacing the meter base, installing a new 200A main breaker panel, replacing the service entrance cable (typically 2/0 AWG aluminum or 4/0 for longer runs), reterminating all existing branch circuits in the new panel, bonding and grounding to current code, and scheduling the utility reconnection and inspection.

This is not a weekend project. Budget two full days of work for an experienced electrician.

## Common Mistakes

- Wiring a 15A receptacle on a 20A circuit. The receptacle itself is the weak point — use a 20A-rated receptacle (identified by the T-shaped neutral slot) on any 20A circuit.
- Mixing up neutral and ground. They are bonded together at the main panel only. In sub-panels and at devices, they must remain separate. Bonding them downstream creates a parallel return path for current on the ground conductor, which is dangerous.
- Overfilling boxes. The NEC specifies box fill calculations based on conductor count and size. A single-gang old-work box is good for about 3–4 cables (6–8 conductors plus grounds). Cramming more than that in creates a fire risk and makes it nearly impossible to make clean connections.
- Not using a torque screwdriver on panel connections. Loose connections in the panel arc, overheat, and start fires. The torque spec is printed on the breaker or bus bar — typically 20–25 in-lbs for branch breakers. This is not optional.
