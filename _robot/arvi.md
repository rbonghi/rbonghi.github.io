---
title: "ARVI"
excerpt: "Autonomous Rover for Video Inspection and service. Robot designed and made on my PhD thesis"
classes: wide
number: 2013
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  teaser: /assets/robot/ARVI/ARVI2-top.png
  overlay_image: /assets/robot/ARVI/arvi-tile.jpeg
---

ARVI is composed by three movable elements, two tracks fixed to the robot base by hinges and a system of springs to assure dumping and reduce vibrations during the displacements in the machine. The rover is equipped with a motorized camera, also remotely driven, for visual inspection and to provide a visual feedback signal for autonomous navigation.

The platform has been also equipped with a recovery system for tile found inside the room, such system is particularly complex because of its small size, it was necessary for the prototype use a 3D printer to realize the recovery of the crank mechanism. The latter is also provided with a camera and motors to be automated and therefore allow a recovery in the autonomy of the tile. The dimensions are: 28 cm width, 26cm depth and 7cm height.

# Robot conception

The measures of the FTU section and profile (figures 5.2(c), 5.2(d) and table 5.1) have been the base for the design a mechanical frame and type of “wheel” to sliding in the toroidal pipe.

The section compare to other Tokamak machines in FTU have a circular shape, with this configuration it is choice a tracked configuration. Inside the vacuum vessel a track can sliding over all holes and if a technicians required a particular inspection to see an hole when ARVI climbing the vacuum vessel. Compare with a wheeled mobile platform a tracked platform does not slide in a pipe and is more stable when cross an hole, but the length of track must have a dimension major than the maximum height inside the chamber.

The tracks in the mobile robot are connected to the base frame with one or more hinges. This new degree of freedom put the track surface completely in contact with circular section in the vacuum vessel. This tricky option reduce the power consumption for tracks motor and keep more stable the mobile platform when the robot sliding.

In ARVI was choose to power supply with an external cable. Without batteries and power regulators the robot is lightweight and do not have mechanical complication, only to select a point in chassis where put the power plug. In addiction with the power supply cable is added other two cables. The first one for the communication with the internal electronics components, the mini PC and the motor control board and the last cable to sustain the mechanical frame when the robot is moved inside from the gate. This cable is in nautical steel and have another functionality when the robot is in fault and the technician retrive the robot inside the chamber.