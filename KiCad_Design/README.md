# RJ45 Passive Inline Coupler — KiCad Design

KiCad 10 source prepared from the supplied PCB report and Amphenol RJE601886401 datasheet.

Design basis:
- Two mirrored Amphenol RJE601886401 / RJE60-188-6X01 Cat 6A shielded 8P8C jacks.
- Direct 1:1 pass-through on pins 1–8.
- Four differential pairs: TXRX1 (1/2), TXRX2 (3/6), TXRX3 (4/5), TXRX4 (7/8).
- J1/J2 shields share /Shield and connect to GND through R1 = 1 MΩ in parallel with C1 = 1 nF, 2 kV.
- 4-layer, 1.60 mm stackup: F.Cu / In1 GND / In2 GND / B.Cu, 0.20 / 1.04 / 0.20 mm FR-4 dielectric, εr 4.5, tanδ 0.02, 35 µm copper.
- Differential routing geometry: 0.221643 mm trace width and 0.115084 mm intra-pair gap, targeting 100 Ω differential for the supplied stackup.
- TXRX1/TXRX2 on F.Cu; TXRX3/TXRX4 on B.Cu.
- Adjacent-layer signal transitions use microvias; non-adjacent GND stitching vias are classified as blind vias.

The supplied KiCad DRC report records 0 DRC violations, 0 unconnected pads and 0 footprint errors. The final local PCB source corrects the via-type classification of the non-adjacent GND stitching vias without changing signal connectivity or routing geometry.

The complete KiCad files are provided in the accompanying `RJ45_Coupler_KiCad_Final.zip` artifact from this design task.