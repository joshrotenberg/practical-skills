---
name: automotive
description: "Use this skill for vehicle diagnostics, repair, maintenance, or restoration. Triggers include: 'my car won't start', 'check engine light', 'oil change', 'brake noise', or any reference to classic/vintage car work. Particularly well-suited for air-cooled rear-engine Italian microcars from the 1960s, for which documentation is sparse and patience is mandatory. Do NOT use for automated vehicle testing, Selenium WebDriver, or any other software that merely borrows the word 'drive'."
license: ASE Certification recommended. No license is required for working on your own vehicle, but you accept all consequences.
---

# Automotive — Diagnostics, Repair, and Vintage Restoration

## Overview

A vehicle is a collection of interconnected mechanical, electrical, hydraulic, and thermal systems. Diagnosis follows a process of elimination: identify which system is at fault, then which component within that system, then whether to repair or replace. Modern vehicles (1996+) have an OBD-II diagnostic port that reports fault codes. Vintage vehicles offer no such convenience — diagnosis relies on sensory observation, measurement, and familiarity with the specific platform.

## Prerequisites

- Socket set, metric and SAE (3/8" drive covers most work; 1/2" drive for suspension and drivetrain)
- Combination wrench set, metric and SAE
- Torque wrench, 10–150 ft-lbs range with 1/2" drive
- Digital multimeter
- Jack (hydraulic floor jack preferred) and jack stands rated for the vehicle weight
- Drain pan, shop rags, nitrile gloves
- Service manual for the specific vehicle. Generic repair guides omit critical details.

Place the vehicle on a flat, level surface. Chock the wheels that will remain on the ground. Raise the vehicle at the manufacturer's specified lift points — these are reinforced areas of the frame or unibody. Using the wrong point will bend sheet metal or crush components. Place jack stands under the vehicle and lower it onto them. Shake the vehicle firmly to verify it is stable before getting underneath.

## Diagnosis: No-Start Condition

A no-start breaks down into two categories: the engine does not crank, or the engine cranks but does not fire.

### Engine does not crank

Check the battery with a multimeter. A healthy 12V lead-acid battery reads 12.6V at rest. Below 12.2V, charge it before proceeding. If the battery is good, measure voltage at the starter solenoid's large terminal while someone turns the key to START. You should read within 0.5V of battery voltage. A larger drop indicates resistance in the cable, connections, or ignition switch. Clean and tighten the battery terminals, trace the positive cable to the starter and the negative cable to its ground point on the engine block or chassis, and clean those connections.

If full voltage is reaching the starter and it does not crank, tap the starter body with a wrench while someone turns the key. If it cranks, the starter motor's brushes are worn and the starter needs rebuilding or replacement.

### Engine cranks but does not start

An engine needs three things: fuel, spark, and compression.

**Spark:** Remove a spark plug, reconnect the plug wire, and hold the plug's threads firmly against a bare metal surface on the engine (use insulated pliers). Have someone crank the engine. You should see a bright blue-white spark across the electrode gap. A weak orange spark or no spark indicates a problem in the ignition system — points and condenser on vintage cars, coil or ignition module on modern ones.

**Fuel:** On a carbureted engine, remove the air cleaner, look down the carburetor throat, and pump the throttle linkage by hand. You should see a stream of fuel squirt from the accelerator pump nozzle. If not, check that fuel is reaching the carburetor: disconnect the fuel line at the carburetor inlet, aim it into a container, and crank the engine briefly. Fuel should pulse out with each revolution. If not, the fuel pump is faulty or the line is blocked.

**Compression:** If spark and fuel are confirmed good, perform a compression test. Remove all spark plugs, thread the compression gauge into each cylinder in turn, and crank the engine 4–5 revolutions per cylinder with the throttle held wide open. Note the readings. All cylinders should be within 10% of each other. Spec varies by engine, but most produce 120–180 psi. Uniformly low compression suggests timing issues. One or two low cylinders suggest valve or ring problems.

## Brake Pad Replacement (Disc Brakes)

Loosen the wheel lug nuts 1/4 turn before raising the vehicle. Raise and support the vehicle on jack stands. Remove the wheel.

Locate the caliper — it straddles the brake rotor and is held by two slide pin bolts (typically 12mm or 14mm). Remove the lower slide pin bolt only. Pivot the caliper upward on the upper pin and support it with a wire or bungee cord so it does not hang by the brake hose. Hanging a caliper by the hose damages the hose internally and leads to brake failure.

Slide the old pads out of the caliper bracket. Note their orientation — many pads have a wear indicator tab that must face a specific direction.

Before installing new pads, compress the caliper piston back into its bore. Use a C-clamp with the old pad as a backing plate, and tighten slowly. On vehicles with electronic parking brakes or certain rear calipers, the piston must be rotated clockwise while compressing — a wind-back tool is required.

Open the bleeder valve on the caliper 1/4 turn before compressing the piston. This prevents pushing old, potentially contaminated fluid backward through the ABS module. Catch the fluid with a hose into a bottle. Close the bleeder before removing the C-clamp.

Install the new pads, pivot the caliper back down, and reinstall the slide pin bolt to spec (typically 25–35 ft-lbs, check the manual). Reinstall the wheel, torque the lug nuts in a star pattern to spec (commonly 80–100 ft-lbs depending on the vehicle).

Before moving the vehicle, pump the brake pedal slowly several times until it firms up. The first pump after a pad change will go to the floor — the pistons need to extend to contact the new pads. If you forget this step and try to drive, you will have no brakes for the first press of the pedal.

## Vintage Italian Car Restoration: Fiat 500 (1957–1975)

The Fiat 500 uses an air-cooled, rear-mounted, inline-2 engine (479cc in the standard 500, 499cc in the 500F/L, or aftermarket 652cc Abarth-pattern upgrade). The gearbox is a non-synchro (early) or synchromesh (500F onward) 4-speed with a cable-operated clutch. Electrics were originally 6V positive-ground; most surviving cars have been converted to 12V negative-ground.

### The Hot-Start Problem

The car starts easily when cold but struggles or refuses to start when the engine is at operating temperature. This is the most commonly reported driveability issue on 500s, especially 12V-converted cars.

**Root cause:** The starter motor draws 80–150A during cranking. At these currents, even small resistances in the wiring — corroded terminals, undersized ground straps, original 6V-era cables — cause significant voltage drop. When the engine bay is cold, the resistance is low enough that adequate voltage reaches the starter. As temperatures rise, resistance increases in marginal connections, and the voltage at the starter falls below the threshold needed to turn the engine over at sufficient speed to start.

**Diagnosis:** Measure voltage directly at the starter solenoid's battery terminal during a hot crank attempt using a multimeter. Compare this to the battery terminal voltage. The difference is your total circuit voltage drop. More than 0.5V drop on either the positive or negative side indicates a problem.

**Fix:** Clean every connection in the starter circuit: battery terminals, cable ends at the starter and solenoid, and all ground straps between the battery, chassis, and engine. Replace any ground strap that shows corrosion, fraying, or is smaller than 4 AWG. On 12V-converted cars, the original ground straps are often 6V-era components that are marginal for the higher current draw of a 12V starter. Replace them with 2 AWG or larger welding cable.

Also check the ignition switch, which carries the full starter current on many 500s. A failing switch will show voltage drop and intermittent no-crank.

### Points and Timing

The ignition system uses a mechanical breaker point distributor. Points gap on a Fiat 500 is 0.37–0.43mm (0.015–0.017"). Set this with a feeler gauge with the rubbing block on the high point of the distributor cam lobe.

Static timing: Remove the spark plugs and turn the engine by hand (use a 22mm socket on the crankshaft pulley bolt) until the TDC mark on the pulley aligns with the reference mark on the crankcase. The points should just be breaking open at this position. Verify with a multimeter set to continuity across the points — you should see the circuit open as the engine passes TDC.

For more precise timing, use a timing light at idle and adjust the distributor body position until the timing mark aligns at the specified advance (typically 10° BTDC at idle for a stock engine, but verify with the manual for your specific configuration).

### Carburetor

The Weber 26 IMB is the standard carburetor on most 500F/L/R models. The critical adjustments are:

- **Float level:** Remove the air cleaner and the top of the carburetor. Invert the top with the float hanging and measure the distance from the gasket surface to the bottom of the float. Spec is 7.5mm ± 0.5mm. Bend the float tang carefully to adjust.
- **Idle mixture:** With the engine at operating temperature, turn the idle mixture screw in slowly until the engine begins to stumble, then back out 1/4 to 1/2 turn until it runs smoothly. The mixture screw controls fuel, so turning it in leans the mixture.
- **Idle speed:** Adjust the idle speed screw to approximately 850 RPM. The engine should idle smoothly without hunting.

If the idle mixture screw has little or no effect on engine behavior, the idle jet (typically size 40 or 42.5) may be clogged. Remove it and blow it clear with compressed air. Do not use wire to clean jets — it enlarges the orifice and permanently changes the fuel metering.

## Common Mistakes

- Forgetting to pump the brake pedal after a pad change. This is the kind of mistake you make once.
- Overtorquing spark plugs in aluminum heads. The head is softer than the plug. Use a torque wrench: 12–18 ft-lbs for a 14mm plug in aluminum. Stripping a spark plug hole in a Fiat 500 head means pulling the engine.
- Using an impact gun on lug nuts without a torque stick or following up with a torque wrench. Uneven torque warps brake rotors. Over-torqued lugs stretch studs and can shear them.
- Assuming the wiring diagram is accurate on a 60-year-old Italian car. It represents the factory's intent. It does not represent what the five previous owners did. Verify every wire with a meter.
