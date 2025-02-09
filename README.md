:warning: **Still under active development**: Parts and documentation may change!
![FuseBox3](images/1.png)
## The latest in the FuseBox line of 3D printers.

FuseBox3 is a midsize CoreXY printer designed for fast printing and high output quality.

Specs:
- Safe build area (XYZ): 235x235x235mm (Absolute max travels: 238x238.75x238mm)
- Frame dimensions (XYZ): 350x372x427mm
- CoreXY movement system running on MGN9/MGN12 rail
- 2020 extrusion frame
- E3D v6 type hotend with Bowden extruder
- Dual leadscrew, belt-driven z-axis
- Dual 4010 blower print cooling + 4010 axial fan hotend cooling

## Quick Links
### [BOM](documentation/BOM.md)

# Design and changes from FuseBox2/R
While the original FuseBox and FuseBox2 were optimized for simplicity and low build cost, FuseBox3 targets a more premium price point without being overly expensive. However, accessibility and ease of construction is still a priority. Therefore, the printer needs no custom CNC'd parts, and all parts were picked to be easily sourceable online.

### Linear rails
![FuseBox3](images/7.png)

With MGN-style linear rails becoming cheaper and more easily available, the CoreXY movement has been redesigned to ride completely on rails - the y-axis now uses MGN9 rails screwed directly to the extrusions, which improves rigidity compared to the old linear rods. Like on the Fusebox2R, the gantry/x-axis uses a single MGN12 rail, although it's now 50mm longer to account for the additional build area.

### Belt path changes, tensioning improvements
The original FuseBox and FuseBox2 share a similar belt path - the motors are mounted in the corners of the frame, and the motor pulleys serve as the "ends" of the belt path on the back side. This belt path design minimizes the number of idler pulleys needed, at the cost of quite a bit of wasted space in the x direction, necessitating a wider frame.

![FuseBox3](images/4.png)

On the FuseBox3, two additional idlers have been added on the rear (motor) side to bring the belts as close to the sides of the frame as possible. This allows the FuseBox3's frame to be 42mm shorter in the x direction than the FuseBox2R's, while simultaneously having an additional 25mm of x-axis travel. The motors have been relocated to the very back of the machine, just underneath the top rear horizontal extrusion. The motor mounts now have slotted screw holes, allowing them to slide to adjust belt tension. On the FuseBox and FuseBox2, tensioning was done by manually pulling on the belts and sliding them into carriage-mounted belt clamps. The new tensioning system should significantly simplify the belt mounting and tensioning process.

Additionally, the front idler brackets have been changed so that the top and bottom idlers are stacked on top of each other rather than offset. This makes the idlers easier to assemble and saves a bolt and nut on each side.

![FuseBox3](images/5.png)

### Z-axis

The z-axis keeps the 8mm rods due to space and cost constraints, but is now reconfigured as a fully belt-driven setup. On the prototype FuseBox2, the cantilevered z-axis was slightly susceptible to vibration and was also susceptible to banding if lower quality leadscrews or bearings were used. The new design's rods have been relocated to the sides of the printer, with each end driven by its own belt loop. These are connected to a single Z motor, which drives them via a 4:1 reduction pulley. The belted design eliminates banding artifacts and greatly increases the max Z speeds achievable.

### Hotend carriage, print cooling
The general arrangement of FuseBox3's carriage is very similar to the carriage on the older FuseBox2R, with the main differences being the print cooling setup and the belt mounting method. Subjectively, it's also a lot tidier in appearance than the earlier carriage designs.

Like the carriage on the FuseBox2R, the new carriage keeps the mass vertically centered on the rail, with the belts also centered and kept as close to the rail as possible. This design minimizes any twisting of the print head during sharp directional changes.

![FuseBox3](images/3.png)

Since the FuseBox3 has sliding motor mounts, tensioning is no longer done on the carriage. The belts are now attached to the carriage by a pair of clamp pieces that screw into the main carriage body. The clamps have a small cutout on the inner side for routing excess belt, so the belts don't have to be shaved to a precise length like they do on the FuseBox2R.

![FuseBox3](images/8.png)

The print cooling setup swaps out the single 4020 blower for twin 4010 blowers flanking the hotend. The old single blower design provided relatively good cooling performance, but the one-sided airflow led to weaker cooling with certain overhang orientations. Twin blowers enable more even part cooling coverage, and the much shorter ducts provide less airflow restriction. The 40mm axial fan for the hotend has been retained, as it provides lower noise than a 30mm fan for equivalent airflow.

![FuseBox3](images/9.png)
