# Ulbora-Fly-VTOL-V1

Because the wing area is relatively small (1 meter span with a narrow chord), this drone will
have high wing loading. It will fly like a "brick" if printed in standard PLA. To achieve the "extended
time" you want, you must optimize the material and battery choice.
The Performance Estimates
If built correctly using Lightweight PLA (LW-PLA), here is what you can expect:
Flight Performance Predictions
Cruising Capability
Estimated RangeFlight TimeCruising SpeedStall Speed
18453818

Miles (30 km)Minutes (Cruise)MPH (60 kph)MPH (29 kph)
The "Flying Brick" Risk Factor
This table compares two build materials. You must use LW-PLA (foaming filament) for this design.
ParameterStandard PLA (Avoid)LW-PLA (Recommended)
Airframe Weight~750g (Heavy)~350g (Light)
Takeoff Weight (AUW)1.5 kg+0.9 - 1.1 kg
Wing Loading125 g/dm² (Unflyable)85 g/dm² (Fast / Stable)
Flight BehaviorStalls instantly, drains battery.Glides well, efficient cruise.
Critical Hardware Fit (Battery Bay)
I analyzed your payload bay dimensions ( 130mm x 78mm x 48mm ). It is perfectly sized for a long-
range Li-Ion pack, which is 30% lighter than a standard Li-Po drone battery.
Recommended Battery: 4S2P 18650 Pack (Samsung 35E or MJ1 cells).
Configuration: 8 cells (4 series, 2 parallel).
Fit: 4 cells wide (73mm) x 2 layers high (37mm). Fits easily inside the 78x48mm bay.

Capacity: 7,000 mAh.
Weight: ~400g.
Voltage: 14.8V (Cruise at ~3-4 Amps).

Next Steps for Success
1. Slicer Settings: Do NOT print this solid. Set your slicer to 0% Infill and 2 Perimeters (Walls).
The Part.makeLoft command creates a solid block; the slicer is responsible for making it a
hollow shell.
2. Transition Speed: Because the wings are narrow, you must program your flight controller
(ArduPilot/PX4) to transition at high speed. Set Q_TRANS_SPD to at least 16 m/s. If you switch to
forward flight too slowly, the wings won't generate enough lift, and it will tumble.
3. Spar: Use a Carbon Fiber Tube (8mm OD) through the main spar hole. The printed plastic alone
will snap under flight loads.
