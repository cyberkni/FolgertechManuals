**Table of Contents**

- [Introduction](#introduction)
- [Resources](#resources)
- [Bill of Materials](#bill-of-materials)
- [Overview](#overview)
	- [Axes](#axes)
	- [Origin](#origin)
- [Build Guide](#build-guide)
	- [0. Prep](#0-prep)
	- [1. Assemble Bottom Half of Main Frame](#1-assemble-bottom-half-of-main-frame)
	- [2. Attach Y Carriage Rails and Bearings](#2-attach-y-carriage-rails-and-bearings)
	- [3. Attach and Assemble the Upper Frame](#3-attach-and-assemble-the-upper-frame)
	- [4. Assemble the Aluminum Heat Bed Plate](#4-assemble-the-aluminum-heat-bed-plate)
	- [5. Solder the MK2B Heated Bed and Attach Thermistor](#5-solder-the-mk2b-heated-bed-and-attach-thermistor)
	- [6. Attach Motors and Motor Mounts](#6-attach-motors-and-motor-mounts)
	- [7. Assemble Z Carriage](#7-assemble-z-carriage)
	- [8. Attach the Extruder to the X Carriage](#8-attach-the-extruder-to-the-x-carriage)
	- [9. Attach Chrome and Threaded Rod to the Assembled X Carriage](#9-attach-chrome-and-threaded-rod-to-the-assembled-x-carriage)
	- [10. Assemble the Front Pulley Assembly](#10-assemble-the-front-pulley-assembly)
	- [11. Attach the Pulley and Belt to the Y Carriage](#11-attach-the-pulley-and-belt-to-the-y-carriage)
	- [12. Attach the Couplings and SHF8UU Clamps in Preparation for the X Carriage to Be Attached in the Next Step](#12-attach-the-couplings-and-shf8uu-clamps-in-preparation-for-the-x-carriage-to-be-attached-in-the-next-step)
	- [13. Attach X and Z Assembly to the Printer](#13-attach-x-and-z-assembly-to-the-printer)
	- [14. Attach the Power Supply](#14-attach-the-power-supply)
	- [15. Attach the Acrylic Electronics Mount](#15-attach-the-acrylic-electronics-mount)
	- [16. Assemble and Mount the Electronics](#16-assemble-and-mount-the-electronics)
	- [17. Attach the Motor Wires](#17-attach-the-motor-wires)
	- [18. Wire the Heated Bed and the Extruder Heater to the RAMPS Board](#18-wire-the-heated-bed-and-the-extruder-heater-to-the-ramps-board)
	- [19. Attach Heated Bed and Extruder Thermistors](#19-attach-heated-bed-and-extruder-thermistors)
	- [20. Mount and Wire the End Stops](#20-mount-and-wire-the-end-stops)
	- [21. Wire Power Cable to the Power Supply](#21-wire-power-cable-to-the-power-supply)
	- [22. Wire the RAMPS to the Power Supply](#22-wire-the-ramps-to-the-power-supply)
	- [23. Attach Wire Extension to Extruder Fan and Wire it to the Power Supply](#23-attach-wire-extension-to-extruder-fan-and-wire-it-to-the-power-supply)
	- [24. Verify Your Wiring Using the Below Pictures as a Reference](#24-verify-your-wiring-using-the-below-pictures-as-a-reference)
	- [25. Mount Filament Feed Assist](#25-mount-filament-feed-assist)
	- [26. Attach the Spool Holder](#26-attach-the-spool-holder)
	- [27. Wire Cleanup and Cosmetics](#27-wire-cleanup-and-cosmetics)
- [Conclusion](#conclusion)


# FOLGER TECHNOLOGIES, LLC 2020 i3 – 3D Printer Kit Build Guide

![](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-001-000.png)

## Introduction
This document is an adaptation of the original documentation written by Folger Technologies. It exists to enable the community to continue to revise the document without needing to burden the company with managing this document.

The original introduction was:

> Thank you for your purchase!
>
> We are happy to announce this as our 3rd complete 3D printer kit. The Folger Tech 2020 i3 kit combines the simplicity of an erector set with the power of a much more expensive desktop printer. This kit includes everything you need to assemble the 8 cubic inch print area machine (with the exception of an 8x8” glass surface and the tools required for assembly).
>
> Note From the Author:
> This guide was made from the perspective of someone that has never built a 3D printer. I built the printer with only the prototype as a visual reference. Taking pictures each step of the way and making small notations I was able to put together the following guide over the next couple weeks. Once the first draft was completed we had one of our warehouse girls take a kit and try to assemble it. She had zero technical experience and made notes (lots of them) on each page as she went along. She completed her first printer and I took the notes back to my desk to complete this guide. This is the finished product. I look forward to your feedback and hope you enjoy building this extremely fun i3 kit!
>
>
> Thanks, Dan
> Folger Technologies


## Resources
Offical RepRap Forum Thread: http://forums.reprap.org/read.php?4,512329,512329#msg-512329

IRC: irc.freenode.net #folgertech

## Optional tools that you'll probably want to have

* **NOTE: There is an allen wrench in the bag with the motor belt, but it is not the only one you will need.**
* A set of both US and metric allen keys (or allen wrenches, or hex keys, or hex wrenches, you get the point)
* A pair of needle-nose pliers
* A pair of wire-strippers - Very optional, you may just use a knife
* A pair of wire-cutters - Usually combined with the tool above, but if not, get a separate pair
* A 7/32 socket and a socket driver - This is for the nylock nuts and will make your life much easier
* A pair of scissors - Again, very optional, but everyone has scissors
* A utility knife/blade
* A clean workspace
* Small cups for sorting hardware - Some have suggested egg cartons, but there are a LOT of different screws and nuts, etc.
* Time... Between 1-3 days depending on your skills, endurance and patience

## Bill of Materials

TODO: Write this!

## Overview
Understanding the end goals of the printer will help with the build process.

### Axes
The extruder is connected to the X axis. The moving platform axis is Y. The Z axis is the one powered by the two steppers connected to the threaded rods. See the image below:

![Axes](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/axis-diagram.png)

### Origin
In this build and related firmware the origin (0,0,0) is the following:
* X is all the way to the right
* Y is all the way to the back of the printer
* Z is at the bottom

This means that the origin should be the front right corner of the print bed, at the lowest vertical point. When you home the printer the extruder should end up here.

## Build guide
### 0. Prep

*NOTE: It has been noticed that some screws in this build guide, particularly in the pictures, don't match the screws which you're given. Make sure to use common sense over instruction, as in: Don't force parts together and don't strip mounts and motors because the screw isn't fitting, or is too long. If there is an over abundance of one type of screw in your kit, don't be afraid to use some of them, they are usually extras.*

1\. Un-box everything and separate like parts into areas you can grab from.

2\. Get out your calipers or ruler and separate screws into different piles based on size: Believe us, it makes things much easier.

3\. Find your 16 Gauge red and black wire, and cut two 240mm lengths from each, so you have 2x black 240mm sections, 2x red 240mm sections and one each of the long remaining section of red and black (about a meter long). 

TODO: INSERT IMAGE

### 1. Assemble Bottom Half of Main Frame

Parts Needed:
* (2) 365mm 2020 Beam
* (2) 375mm 2020 Beam
* (4) SK8 Linear Axis Bracket
* (1) Motor Mount
* (2) 2020 Corner Bracket

Hardware Needed:
* (8) 2020 L Mounts with set screw
* (8) 5mm T-nut
* (4) 4mm T-nut
* (4) M4x8mm Pan Head Bolt
* (8) M5x8mm Bolt

*NOTE* Recent kits have included M5x8mm bolts which are just a bit too short to complete step 4. A quick trip to the hardware store for M5x10mm screws is recommended - 12mm length will work too.

1\. Take the 375mm 2020 Beam and place it in front of you, we are going to attach the Corner Brackets and and SK8s before continuing with the frame assembly.

[Insert Picture Here]

2\. Using (2) 4mm T-nuts and (2) M4x8mm Pan Head Bolts attach the 2020 Corner Brackets to the center of the 375mm 2020 Beam spacing them about an inch apart. Note: This will be adjusted later.

![Corner Brackets mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-003-001.png)

3\. Slide (2) 5mm T-nuts to the left of the Corner Brackets, and (2) 5mm T-nuts to the right of the Corner Brackets.

![Large TNuts Added](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-003-002.png)
![Large TNuts Added](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-003-003.png)

4\. Attach the (2) SK8s to the M5 T-nuts using the (4) M5x8mm Bolts. Note: The tension screws for the SK8s should be facing outwards to make it easier to tighten them later.

![SK8s mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-004-004.png)

5\. Take the other 375mm 2020 Beam and place it in front of you: We are going to attach the motor mount and the remaining 2 SK8s.

6\. Repeat the process from step 3 to attach the remaining 2 SK8s by sliding (4) M5 T-nuts onto the top of the 2020 Beam and attach the remaining (2) SK8s using (4) M5x8mm Bolts.
TODO: TAKE A PHOTO OF THIS STEP

7\. Take the metal Motor Mount and attach it to the front face of the 375mm 2020 Beam in between the SK8s using (2) M4 T-nuts and (2) M4x8mm Pan Head Bolts. Note: This will need to be moved left and right to adjust screws later so you can leave it loose for now.

![Motor mount](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-004-005.png)

![Motor mount](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-004-006.png)

8\. Now take (4) 2020 L mounts and the remaining (2) 365mm 2020 Beams. Slide (2) 2020 L Mounts back to back on the top of each of the 365mm 2020 Beams. Each one should look like the picture below. Do not secure these in place as they will be moved later. Note: Ignore the L Bracket in the left of the picture it shouldn't be there yet.

![Side base](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-004-007.png)

9\. You can now use the remaining (4) 2020 L Mounts to secure the bottom frame together. Tighten the set screws to lock them in place. Use the below pictures as reference. Note: The Motor Mount is not pictured, but should be attached to the rear 2020 Beam.

![Bracket detail](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-005-008.png)
![Joint detail](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-005-009.png)
![Finished base frame](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-005-010.png)

### 2. Attach Y Carriage Rails and Bearings

Parts Needed:
* (2) 395mm Chrome Rod
* (3) LM8UU Bearing
* Bottom Frame Assembly

Hardware Needed: None

1\. Place the bottom frame in front of you so the motor mount is at the back of the printer. Note: This is the front position of the printer. The motor mount is missing from this picture but should be attached to the rear 2020 Beam.

![Finished base frame](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-005-010.png)

2\. Slide (1) 395mm Chrome Rod through the front right SK8 about half way through.

![Chrome rod halfway](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-005-012.png)

3\. Carefully slide (2) LM8UU Bearings onto the Chrome Rod and finish pushing the Chrome Rod through to the other SK8. Be careful not to hit the corner of the rod on the inside of the LM8UU which can cause bearings to fall out.

![Add 2 bearings](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-013.png)

![Completely installed rod](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-014.png)

4\. Similar to step 3, slide the remaining (1) 395mm Chrome Rod into the left side SK8 and slide (1) LM8UU Bearing onto the rod.

![Second installed rod](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-015.png)

5\. Be sure to tighten the tension screws on the (4) SK8s to secure the Chrome Rods in place.

### 3. Attach and Assemble the Upper Frame

Parts Needed:
* (2) 295mm 2020 Beam
* (1) 375mm 2020 Beam
* Bottom Frame Assembly

Hardware Needed:
* (3) 2020 L Mounts with set screws

1\. Take the (2) 295mm 2020 Beams and attach them vertically to the left and right side of the Bottom Frame Assembly using the (2) 2020 L Mounts on each side that we placed in step 1:8. Before securing them make sure the back side of the Beam is 90mm from the back of the printer.

![Beam alignment](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-016.png)
![Beam installed](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-017.png)
![Beams installed](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-006-018.png)

2\. Before attaching the top we are going to attach (1) 2020 L Mount to the outside of the left most vertical 295mm 2020 Beam for the Spool Holder which we will attach later.

![Spool holder L mount](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-007-019.png)

3\. Now attach the remaining (1) 375mm 2020 Beam to the top of the (2) vertical 295mm 2020 Beams using (2) 2020 L Mounts with set screws to secure them in place.

![Top Beam](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-007-020.png)
![Overview](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-007-021.png)

### 4. Assemble the Aluminum Heat Bed Plate

Parts Needed:
* (1) Aluminum Bed Plate
* (3) Printed Bearing Mount
* (1) Printed Belt Carriage

Hardware Needed:
* (6) Small Zip Tie
* (6) M3x20mm Bolt
* (2) M3x12mm Bolt
* (8) M3 Nylock Nut

1\. Remove the blue protective layer off both sides of the Aluminum Bed Mount.

![Remove plastic](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-007-022.png)

2\. Take the (3) Printed Bearing Mounts and attach (2) Small Zip Ties to each by sliding the Zip Tie through the guide holes, as pictured.

![Install zip ties](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-008-025.png)

3\. Using the (6) M3x20mm Bolts and (6) M3 Nylock Nuts, attach the Printed Bearing Holders to the Aluminum Bed Plate. Use the (2) M3x12mm Bolts and (2) M3 Nylock Nuts to attach the Printed Belt Carriage to the Aluminum Bed Mount using the pre drilled holes. Note: The opening on the Printed Belt Carriage is facing the side with 2 bearing holders. Also, the bolts sometimes fit rather snug within the holes: They sometimes take a little persuasion.

![Mount bearing holders](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-008-026.png)
![All parts mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-008-028.png)

4\. Now we are going to attach the Aluminum Bed Mount to the bearings on the Bottom Frame Assembly of the printer by pushing them down into the LM8UU Bearings. Line up the Printed Bearing Holders over the LM8UUs attached to the Chrome Rod and apply enough pressure to snap the bearings into the Printed Bearing Mounts. Note: Hold the rods up with your hand while you do this as good practice so that you don't bend anything. You probably couldn't put enough force to do that anyway, but safety first. You should feel a small pop as it sets into the grooves.

![Bed attached](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-008-029.png)

5\. Tip the frame backward and close the Small Zip Ties that you previously attached to the Printed Bearing Holders over the LM8UU Bearings securing them in place. Note: You may tighten these by grabbing the excess end of the zip tie at the base with a needle-nose pliers and twist in the direction opposite the grooves in the zip tie. Once tightened you can clip the excess material from the Small Zip Ties.

![Secure zipties](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-009-031.png)

### 5. Solder The MK2B Heated Bed and Attach Thermistor

Parts Needed:
* (1) MK2B Heated Bed
* (1) Thermistor
* (1) ~1M Black 16 Gauge Wire
* (1) ~1M Red 16 Gauge Wire

Special Tools Needed:
* Soldering Iron
* Solder
* Kapton Tape

1\. Prepare your MK2B Heated Bed to be soldered.

![Prep](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-009-034.png)

2\. Apply solder to contacts #1, #2, & #3. Note: It is advised that you apply flux to the contacts and the wires at this point to make soldering easier.

![Prep pads](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-009-037.png)

3\. Strip the ends off one side of the long Red and Black 16 Gauge Wires and apply solder to the twisted bare strands.

![Tin leads](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-010-038.png)

4\. Lay the Heated Bed down in front of you where you will solder it so the pad with the number 3 is on your left and the pad numbered 1 is on your right. This makes the Bed lay upside down from the orientation you will attach it to the printer. Solder the stripped and soldered end of the Black 16 Gauge Wire to both contacts #3 & #2. Note: This is critical, if you do not make contact with both #3 & #2 you will only be running at 12V and will not be able to reach maximum bed temperature.

![Attach Black to 3 and 2](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-010-039.png)

5\. Solder the stripped and soldered end of the Red 16 Gauge Wire to contact #1.

![Attach Red to 1](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-010-039.png)

6\. Place the glass of (1) Thermistor into the small hole in the center of the Heated Bed.

![Position thermistor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-010-042.png)

7\. Using the provided Kapton Tape, secure both the Thermistor and the Red & Black 16 Gauge wire to the bottom of the Heated Bed. Note: Use these pictures as a guideline but you can use more or less tape and position the wires as you see fit.

![Tape it up](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-011-043.png)

Step 8: Attach the Heated Bed to the Aluminum Bed Plate, so the wires are all underneath the bed.

Parts Needed:
* (1) MK2B Heated Bed Pre Wired from Step 7

Hardware Needed:
* (4) Springs
* (4) Thumb Screw
* (4) M3x16mm Bolt

1\. Feed (1) M3x16mm Bolt through each corner hole on the MK2B Heated Bed > Spring > Aluminum Bed Plate > Secure with (1) Thumb Screw. Note: Wires should be coming out the back of the printer. Thumb screws just need to be hand tight for now and can be adjusted later.

![Screw detail for bed mount](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-011-045.png)

### 6. Attach Motors and Motor Mounts

Parts Needed:
* (2) Metal Motor Mount
* (2) Acrylic Rod Keeper
* (1) NEMA 17 4.8kg/cm Bed Stepper Motor
* (2) NEMA 17 2.6kg/cm Stepper Motor

Hardware Needed:
* (6) M4 T-nut
* (6) M4x8mm Pan Head Bolt
* (4) M3x8mm Bolt
* (8) M3x12mm Bolt
* (12) Lock Washer

1\. Take the (2) Metal Motor Mounts and (2) Acrylic Rod Keepers and attach them to the (2) 2.6kg/cm Stepper Motors using (8) M3x12mm Bolts & (8) Lock Washers. Note: One acrylic rod keeper should have the small hole facing right, and one should have hole facing left, as pictured. The wire harness should be facing the corner of the bracket.

![Motor mounts installed](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-012-050.png)

2\. Mount the (1) 4.8kg/cm Bed Motor to the Metal Motor Mount that we attached to the Bottom Frame Assembly earlier in the build guide using (4) M3x8mm Bolts & (4) M3 Lock Washers.

![Motor mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-012-052.png)

3\. Attach the (2) Metal Motor Mounts with the attached motors and acrylic rod keepers to the top right and left corners on the front of the 2020 Frame using (3) M4x8mm Pan Head Bolts and (3) M4-T-nuts per side. Note: The small holes in the acrylic rod keepers should be facing the outside of the printer. These don't need to be secured to tightly as we will be raising them later.

![Motor mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-013-054.png)
![Overview](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-013-055.png)

### 7. Assemble Z Carriage

Parts Needed:
* (7) LM8UU Bearing
* (1) NEMA 17 2.6kg/cm Stepper Motor
* (1) 3D Printed: Extruder Carriage
* (1) 3D Printed: Left Side
* (1) 3D Printed: Right Side
* (1) Folger Tech Direct Drive Extruder: Pre Assembled
* (2) F623Z Bearing
* (1) 20T Pulley
* (1) 1M GT2 Belt
* (2) 365mm Chromed Rod

Hardware Needed:
* (3) M3x20mm Bolt
* (1) M3x16mm Bolt
* (4) M3 Nylock Nut
* (2) M5 Nut
* (8) Zip Tie

1\. Insert (2) LM8UU Bearings into the (1) 3D Printed: Right Side by pressing them firmly. Note: You can use the table to push them into place if more force is required.

![Insert bearings](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-013-056.png)

2\. Insert (1) M5 Nut into the pre cut slot provided.

![Insert nut](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-013-057.png)

3\. Attach the (1) 2.6kg/cm Stepper Motor to the (1) 3D Printed: Right Side using (3) M3x20mm Bolts. Note: *Some have experienced the motor being loose in the 3D printed frame with the M3x20mm Bolts: Consider using shorter screws if this happens, but most importantly don't strip the motor.* Also, you want the motor wire connectors to be facing up so using the picture as a reference it would be facing the upper left.

![Attach motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-014-058.png)

4\. Attach the (1) 20T Pulley onto the shaft of the (1) 2.6kg/cm Stepper Motor and secure with the set screws. Set this aside for now. Note: Tooth side down on the pulley.

![Install pulley](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-014-059.png)

5\. Take the (1) 3D Printed: Left Side and place the 2 Bearings into the spot provided, just like you did with the Right Side.

![Install bearings](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-014-060.png)

6\. Place the remaining (1) M5 Nut into the spot provided on the (1) 3D Printed: Left Side.

![Install nut](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-014-061.png)

7\. Take the (2) F623ZZ Bearings and using (1) M3x16mm Bolt and (1) M3 Nylock Nut to secure the bearings into the (1) 3D Printed: Left Side as pictured. Set aside for now.

![Install bearings](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-015-063.png)

8\. Take the (1) 3D Printed: Extruder Carriage and place (6) Zip Ties into the slots provided to later secure the bearings.

![Install zipties](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-015-064.png)

9\. Press (3) LM8UU Bearings into the (1) 3D Printed: Extruder Carriage. Secure into place using the Zip Ties and clip the ends off the Zip Ties. Note: Use the table to press the bearings into place if you are having trouble getting them to lock in. Also, you may tighten these by grabbing the excess end of the tie wrap at the base with a needle-nose pliers and twist in the direction opposite the grooves in the tie wrap, same as before.

![Install bearings](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-015-065.png)
![Fasten zipties](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-015-066.png)

10\. Very carefully slide the (2) 365mm Chromed Rod through the bearings in the (1) 3D Printed: Extruder Carriage. Note: Be very careful when pushing the rod through the bearings not to push out the ball bearings. Also, make sure that the rods run through the bearings smoothly. If the single bearing alone runs smoother than the two together, it's likely that you have to readjust the two bearings to put less pressure on the rod. Just wiggle them around a little until it sounds right.

![Install rods](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-016-068.png)

11\. Take the 3D Printed Part: Extruder Carriage (with the rods and bearings attached, the 3D Printed Part: Left Side (assembled) and the 3D Printed Part: Right Side (assembled) and set them in front of you. You should have the parts laid out in front of you as pictured. Note: These are mirrored to how they will be when attached to the printer so don't get confused with how we define left and right in the next step. See above image.

12\. Push the 2 ends of the Chrome Rods on the left into the 2 holes in the 3D Printed: Right Side. Push them in so they are snug, we will have to adjust this later.

![Rods in right side](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-016-069.png)

13\. Push the 2 ends of the Chrome Rods on the right into the 2 holes in the 3D Printed: Left Side.

![Rods in left side](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-017-070.png)

14\. Push the outside 3D Printed Left and Right together to snug up the assembly. The inner diameter, inside the Right Plastic to inside the Left Plastic, should be 300mm. This is important to ensure it fits on the printer later.

![Assembled](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-017-071.png)

15\. We are now going to take 1m of GT2 belt and attach it to the back of the 3D Printed: Extruder Carriage by looping it around the right side upper belt block as pictured below. Note: Allow a little extra slack we will secure this later with zip ties.

![Around the pulley](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-017-073.png)

16\. Now take the rest of the belt, feed it over the top of the FZ623ZZ Pulleys on the right side and back to feed under and above the 20T Pulley on the motor on the left side. Bring the belt back and attach to to the left side belt block the same way you did above, but on the opposite side. Trim the extra belt. Note: You want the belt to be tight but not to tight, we can always add a belt spring later to adjust tension.

![Around pulley](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-018-074.png)
![GT2 Secured](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-017-072.png)

17\. Now take (2) Zip Ties and secure the overhanging GT2 Belt to the upper belt on each side as picture below.

![Around pulley](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-018-077.png)

### 8. Attach the Extruder to the X Carriage

Parts Needed:
* (1) Extruder Assembly
* (1) X Carriage - Assembled in step 10

Hardware Needed: None

1\. Remove the 2 screws from the top of the motor that is part of the Extruder Assembly.

![Remove screws](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-018-078.png)

2\. Using the 2 screws removed in step 1, attach the motor to the X Carriage by screwing it to the 3D Printed Part: Extruder Carriage as pictured. Note: *Some have experienced that the 2 extruder mount screws do not fit well through the 3D printed X Carriage holes. Make sure that you don't strip the motor screw holes because it's hard to feel whether you are going through plastic, or stripping through the aluminum thread.*

![Attach motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-019-079.png)

### 9. Attach Chrome Rod and Threaded Rod to the Assembled X Carriage.

Parts Needed:
* (2) 235mm 5mm Threaded Rod
* (2) 320mm 8mm Chrome Rod
* (1) Assembled X Carriage

Hardware Needed: None

1\. Take the Assembled X Carriage, the (2) xxmm 5mm Threaded Rod and the (2) xxmm 8mm Chromed Rod and lay them out in front of you like so:

![Carriage Layout](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-019-082.png)

2\. Thread the 235mm 5mm Threaded Rod through the 5mm nut that was previously inserted into the Left and Right 3D Printed Parts. Thread it about half way through so the same amount of thread is showing on the top and bottom of the part. Feed the 320mm 8mm Chrome Rod through the bearings on the Left and Right 3D Printed Parts as pictured below. Note: Be careful when putting the chrome rod in not to push out the ball bearings. Set this aside for later.

![Thread Carriage](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-019-083.png)

### 10. Assemble the Front Pulley Assembly

Parts Needed:
* (2) F623Z Bearing
* (1) 623ZZ Bearing

Hardware Needed:
* (1) M3x30mm Bolt
* (4) M4 Large Washer
* (2) M3 Washers
* (1) M3 Nylock Nut
* (2) M4x8mm Pan Head Bolt

1\. Assemble the hardware in the following order going through the 2020 Corner Brackets you previously attached to the front of the frame, during step 3 of assembly. Note: Some have found that the M3x30mm Bolt is too long for this usage, since the end of the bolt often covers the screws holding in the Corner Brackets (These usually have to be adjusted during this step, and cannot be reached with the bolt covering them).

![Pulley assembly](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-020-084.png)

M3x30mm Bolt > M4 Large Washer > 2020 Corner Bracket > M4 Large Washer > M3 Washer > F623ZZ Bearing (Flange out) > 623ZZ Bearing > F623ZZ Bearing (Flange out) > M3 Washer > M4 Large Washer > 2020 Corner Bracket > M4 Large Washer > Nylock Nut

### 11. Attach the Pulley and Belt to the Y Carriage.

Parts Needed:
* (1) 20T Pulley
* (1) ~1M Meters GT2 Belt

Hardware Needed:
* (2) Zip Tie

1\. Attach the (1) 20T Pulley to the Large Motor attached to the bottom frame using the set screws in the pulley to secure it in place. Note: Teeth on motor side.

![Pulley on motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-020-087.png)

2\. Tip the printer back and using the same method used for the X Carriage belt installation we are going to attach the (1) xM GT2 Belt to the Y carriage.

![GT2 Setup](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-021-091.png)

3\. Attach the belt to the back end of the 3D Printed: Belt Carriage on the bottom of the Aluminum Mount plate, leaving enough slack to zip tie it later. Feed the belt around the 20T Pulley on the motor and then bring it to the front of the printer then go under and above the F23ZZ bearing mount you assembled in Step 12. You can then feed it back and attach it to the front part of the 3D Printed: Belt Carriage again leaving enough slack for zip ties.

![GT2 Secured](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-021-090.png)

### 12. Attach the Couplings and SHF8UU Clamps in Preparation for the X Carriage to Be Attached in the Next Step

Parts Needed:
* (2) 5x5 Coupling
* (2) SHF8UU Clamp

Hardware Needed:
* (4) M4x14mm Black Bolt
* (2) M4 T-nut

1\. Before we can attach the SHF8UU Clamp we need to remove 2 set screws from (2) 2020 L Brackets that are attached to the frame. With the printer in front of you, remove the 2 set screws from the 2020 L Brackets that are securing the top frame to the bottom frame on the front of the printer. Note: These are the set screws directly below the small motors on the bottom frame.

![Remove these set screws](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-021-092.png)

2\. Now take (1) M4x14mm Bolt and put it through the right hole in the SHF8U (as pictured) and attach (1) M4 T-nut to the other end of the bolt loosely: We are going to place this on the bottom frame and use the hole from the removed set screw to attach the other M4x14mm Bolt securing both the frame and the SCH8UU in place. Tighten both screws. Note: The tension bolt on the SCH8UU Clamp is facing forward to allow access to tighten it later.

![Install SCH8UU](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-022-093.png)

3\. Repeat this process for the opposite side.

4\. Attach the (2) 5x5 Couplings to each of the 2.6kg/m Stepper Motors mounted to the top of the frame using the 2 set screws provided in the coupling. Leave enough overhang so that the second set of set screws in the coupling can be later used to secure the threaded rod that we will be inserting.

![Attach coupling](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-022-095.png)

### 13. Attach X and Z Assembly to the Printer.

Parts Needed:
* X and Z Assembly
* Assembled Frame

Hardware Needed: None

1\. First loosen both of the motor mounts on the top of the printer that are for the Z Axis and pull them up as far as they will go. Secure them in place by tightening one of the M4 bolts. This is just to give you clearance when attaching the X and Z Assembly.

![Move motors out of the way](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-023-096.png)

2\. Take your X and Z Assembly you previously assembled and set the chrome rods into the SCH8UUs on the bottom of the frame, directly below the Z Axis Motors that we just raised. Note: Make sure they are pushed in all the way so they touch the 2020 Beam below them.

![Install assembly on sch8uu](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-023-097.png)

3\. Now we are going to lower each of the motor brackets that we raised in step 1 so that they drop down allowing the top of the chrome rod for the X & Z Assembly to sit in the hole in the Acrylic Rod Keeper. Note: Try to keep the bracket squared but make sure the chrome rod is fully seated in the hole.

![Drop motors down](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-023-099.png)

4\. Now screw the 5mm Threaded rod until it feeds up into the 5x5mm Coupling attached to the motor. You want the threaded rod to be snug against the tip of the motor shaft inside the coupler. If you go to far it will try to push the 5mm Nut out of the 3D Printed part below so pay close attention. Once you are confident the rod is touching the motor shaft you can tighten the 2 set screws on the 5x5mm Coupling to secure it in place. Repeat this for both sides.

![Threaded rod up to coupling](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-024-101.png)

### 14. Attach the Power Supply

Parts Needed:
* (1) Power Supply
* (2) 2020 Corner Brackets

Hardware Needed:
* (4) M4x8mm Pan Head Bolt
* (2) M4 T-nut

1\. Using (2) M4x8mm Pan Head Bolts attach (2) 2020 Corner Brackets to the left side of the power supply. Note: Direction based on the wire connectors facing the top front of the power supply.

![Corner Brackets on PSU](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-024-103.png)

2\. Using (2) M4x8mm Pan Head Bolts and (2) M4 T-nuts attach the power supply to the inner side of the right vertical 2020 Beam. Note: The power supply can rest on the bottom frame.

![PSU Mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-024-104.png)

### 15. Attach the Acrylic Electronics Mount

Parts Needed:
* (1) Acrylic Hardware Mount

Hardware Needed:
* (2) M4x10mm Pan Head Bolt
* (1) M4 T-nut

1\. Similar to attaching the SCH8UU in previous steps, we will be removing a set screw from the 2020 L Bracket that is directly above the power supply 2020 Bracket on the vertical 2020 Beam.

2\. Attach the (1) Acrylic Hardware Mount to the 2020 frame directly above the power supply by using the (2) M4x10mm Pan Head Bolts and using the 2020 L Bracket already in place for the top screw and (1) M4 T-nut for the lower screw hole. Note: The holes on the acrylic are differently spaced; if they don't line up try the other side.

![Acrylic Mounted](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-025-106.png)

### 16. Assemble and Mount the Electronics

Parts Needed:
* (1) Mega Board
* (1) RAMPS Board with jumpers and power connector
* (4) A4988 Stepper Drivers with heatsinks

![Electronic Parts](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-025-108.png)

Hardware Needed:
* (3) M3x30mm Bolt
* (3) Nylock Nut

1\. Attach the jumpers (included in RAMPS bag) to the (1) RAMPS Board. Each stepper driver requires 3 jumpers. Note: We are also placing jumpers on the 5th slot in case you decide to upgrade to a dual extruder sometime in the future.

![Jumpers](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-026-110.png)

2\. Attach the (1) RAMPS Board to the (1) Mega Board. This can only be installed one way, line up the pins on the underside of the RAMPS Board to the connectors on the Mega Board and firmly press them into place. Note: Some users have reported that this step was completed by Folgertech already.

![Connected](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-026-114.png)

3\. Attach the heat sinks that came with the (4) A4988 Stepper Drivers to the Stepper Drivers by removing the sticky back protector from the bottom of the heat sink and sticking it to the chip on the top of the Stepper Drivers.

![Peel](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-026-116.png)
![Stick](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-026-117.png)

4\. Attach the (4) A4988 Stepper Drivers to the RAMPS Board. Make note of the orientation of the steppers when attaching them. The tuning screws on all of them should be facing to the left of the power connections on the RAMPS Board. Note: Line up the pins with the connectors starting from the right as there are only just enough holes for the pins as necessary so if you are off by 1 you will come short at the end.

![Insert Steppers](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-027-120.png)

5\. Attach the now finished Electronics Assembly to the Acrylic Electronics Mount that we previously mounted to the printer using the (3) M3x30mm Bolts and (3) Nylock Nuts. There is a 4th screw mount hole on the Arduino, but the pin output connectors prevent any of our bolts from being inserted correctly. You can ignore this hole. Note: The power connections and USB port should be facing the outside of the printer.

![Attach boards](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-027-122.png)

### 17. Attach the Motor Wires

Parts Needed:
* (5) Motor Cables with Pre Wired End

Hardware Needed: None

1\. Take the white end from all of your Motor Cables and plug one of them into each of the motors so that each motor has a wire attached to it.

![Connect motor wire](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-027-125.png)

2\. Now take (2) wires from the Z axis (top) motors and plug them into the RAMPS board under the left most top stepper driver. Note: These motors mirror each other so it doesn't matter which is on top and which is on the bottom.

![Connect Z motors](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-028-127.png)

3\. Take the wire from the Y Carriage Motor and plug it in under the 2nd (middle) stepper driver.

![Connect Y motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-028-130.png)

4\. Take the wire from the Z Carriage Assembly (the motor with the 20T Pulley) and plug it in under the 3rd (right most) stepper driver.

![Connect X motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-028-132.png)

5\. Take the wire from the Extruder Assembly and plug it it under the bottom right most stepper driver.

![Connect Extruder motor](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-028-134.png)

### 18. Wire the Heated Bed and the Extruder Heater to the RAMPS Board

Parts Needed:
* Heated Bed Wires
* Extruder Heater Wires

Special Tools Needed: Wire Strippers

1\. Take your Black & Red 16 Gauge wires from your heated bed and strip the ends off exposing the wiring underneath as pictured.

![Strip Wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-029-135.png)

2\. Use a flat screwdriver to open up the +/- ports of the D8 connector on the Ramp Board's blue power strip. Plug the Black (-) 16 Gauge wire into the first hole (-) and plug the Red (+) 16 Gauge wire into the second hole (+). Tighten down the flat screws to secure the wire in place.

![Insert Wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-029-136.png)

3\. Take the red wires from the extruder and strip the ends off to expose a small amount of wire, as pictured.

![Strip Wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-029-138.png)

4\. Use a flat screwdriver to open up the +/- ports of the D10 connector on the Ramp Board's blue power strip. Plug the 2 wires into the +/- ports of the D10 connector and secure the wire in place by tightening down the flat screws. Note: These have no polarity so it doesn't matter which wire goes into which port.

![Insert Wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-030-139.png)

### 19. Attach Heated Bed and Extruder Thermistors

Parts Needed:
* Heated Bed Thermistor Wires
* Extruder Thermistor Wires
* (4) Small Crimp
* (2) 2 Pin Molex Connector

Special Tools Needed:
* Crimp Tool or Pliers
* Wire Strippers

1\. First take both pairs of thermistor wires (Heated Bed & Extruder) and strip the ends off as pictured below. Attach the crimp ends to each wire using either pliers or a crimp tool if you have one available. Plug the now crimped ends into the black 2 Pin Molex Connector (polarity does not matter here) as pictured below.

![molex bits](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-030-140.png)
![molex built](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-030-143.png)

2\. Take the Extruder Thermistor and attach it to the RAMPS board. This thermistor plugs into the pins directly below the left most top Stepper Driver on the far right side of the pin set.

![Connect probe](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-030-144.png)

3\. Take the Heated Bed Thermistor and attach it to the RAMPS board directly to the left and right next too the Extruder Thermistor wire.

![Connect other probe](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-031-146.png)

### 20. Mount and Wire the End Stops

Parts Needed:
* (3) End Stops with Wires
* (3) 3D Printed End Stop Mount

Hardware Needed:
* (3) M3x8mm Bolt
* (3) M3x18mm Bolt
* (6) M3 Nylock Nut

1\. Plug the white end of the wires into each of the End Stops.

![Connect end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-031-147.png)

2\. We are going to attach the Z Axis End Stop. Take (1) End Stop and mount it to (1) 3D Printed End stop using (1) M3x8mm Bolt and (1) M3 Nylock Nut as pictured. Note: This only requires 1 bolt, to the right of the limit switch.

![Mount endstop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-031-148.png)

3\. Mount the now assembled End Stop to the vertical chrome rod on the right side of the printer using (1) M3x18mm Bolts and (1) M3 Nylock Nut.

![Install end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-032-150.png)

4\. Position the End Stop so that the limit switch makes contact with the 3D Printed: Right Side plastic part. Note: When homing the printer you want the Z axis to come down and click the limit switch at a point where the Hot End Nozzle is only a paper width from the heated bed. You can eyeball it for now and move it up and down when you calibrate it later so that it is in the correct vertical position.

![Position end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-032-151.png)

5\. Attach another End Stop to one of the 3D Printed End Stop Mounts using (2) M3x8mm Bolts and (2) M3 Nylock Nuts.

![Position end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-032-152.png)

6\. Attach the now assembled End Stop just to the left of the 3D Printed: Right Side on the lower Chrome Rod using (1) M3x18mm Bolt. Note: The limit switch should be hitting the motor on the extruder when it moves over. Position the End Stop on the Chrome Rod so that when the motor makes contact with the switch the Extruder Nozzle is just to the right edge of the heated bed print area.

![Position end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-033-154.png)

7\. We are going to mount the Y carriage End Stop. This one is a bit trickier to mount. The End Stop mounts to the 3D Printed End Stop Mount using the same (1) M3x18mm Bolt and (1) M3 Nylock Nut that is used to mount the 3D Printed End Stop Mount to the Chrome Rod. Clip the 3D Printed End Stop Mount to the rear of the printer on the right most Chrome Rod about an inch from the SK8. Note: This limit switch should hit the 3D Printed Bearing holder under the Aluminum Mount Plate and you want the switch to make contact when the Extruder Nozzle is at the front most of the heated bed print area.

![Position end stop](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-033-156.png)

8\. Take the end of the wire from the Z Axis End Stop. The End Stops plug into the pin set that is on the lower left corner of the RAMPS board. There are 6 rows of pins. Plug the End Stop into the 3rd row over. Use the picture as a reference. The red wire should be facing up, if plugged in backwards it will short the RAMPS causing permanent damage.

![Z Endstop wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-033-157.png)
![Z Endstop connected](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-033-158.png)

9\. Take the end of the wire from the Y Carriage End Stop. Skip a row and plug this End Stop into the 5th row, one over from the previous End Stop. Use the picture as a reference. The red wire should be facing up, if plugged in backwards it will short the RAMPS causing permanent damage.

![Y Endstop wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-034-159.png)
![Y Endstop connected](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-034-160.png)

10\. Take the end of the wire from the X Carriage End Stop. Again you are going to skip a row from the previous plugged in end Stop and plug this End Stop into the 7th row. Use the picture as a reference. The red wire should be facing up, if plugged in backwards it will short the RAMPS causing permanent damage.

![X Endstop wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-034-161.png)
![X Endstop connected](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-034-162.png)


### 21. Wire Power Cable to the Power Supply

Parts Needed:
* (1) Black Power Cable

Special Tools Needed:
* Multimeter

1\. Take the Black Power cable and cut off the female end of the cable. Strip off a bit of the black outer protector and strip the wires inside as pictured.

![Cut power cable](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-034-164.png)

2\. Because the wire colors can differ from kit to kit, use a multimeter to determine which wires are live and which wire is the ground. We are going to attach the stripped ends of the power supply to contacts #7, #8, and #9 on the power supply. Unscrew the screw for each contact and place the stripped end of the wire under the screw before tightening it back down. If you have the same cable pictured, the 2 black wires can be wired into #8 and #9 which are the Line and Neutral contacts: Polarity doesn't matter with these two. The blue wire can be wired into #7 which is the Earth Ground.

![Wire up power](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-035-167.png)

### 22. Wire the RAMPS to the Power Supply

Parts Needed:
* (2) 240mm 16 Gauge Red Wire
* (2) 240mm 16 Gauge Black Wire
* (1) Green RAMPS Connector

Hardware Needed: None

1\. Take all both the (2) 240mm 16 Gauge Red Wire and the (2) 240mm 16 Gauge Black Wire and strip the ends off both sides slightly, as pictured.

![Strip wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-035-169.png)

2\. Insert one end of each of the 16 gauge wires into the (1) Green RAMPS Connector using a small flat head screwdriver to open up the port and feeding the wire ends into it. You can then tighten down the screw to secure the wire in place. It should be Red, Black, Red, Black as pictured below. You can then take it and plug it into the RAMPS board.

![Insert wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-036-170.png)
![Insert wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-036-171.png)

3\. We are now going to wire the opposite ends of these wires to the Power Supply. Take the ends of the (2) 16 Gauge Red Wire and attach them to contacts #2 and #3 on the power supply. These are the positive wires.

![Insert wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-036-173.png)

4\. Take the ends of the (2) 16 Gauge Black Wire and attach them to contacts #4 and #5 on the power supply. These are the negative wires.

![Insert wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-036-174.png)

### 23. Attach Wire Extension to Extruder Fan and Wire it to the Power Supply

Parts Needed:
* (1) 1m 22 Gauge Black Wire
* (1) 1m 22 Gauge Red Wire

Special Tools Needed:
* Soldering Iron
* Kapton Tape

1\. Cut the end off of the Extruder Fan and Strip the ends of the wires slightly.

![Cut connector](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-037-177.png)

2\. Take 1m of 22 Gauge Black & Red wire and strip a small amount off of each end of the wires. Using a soldering iron attach the wires to the Extruder Fan wires.

![Connect wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-037-180.png)

3\. Use either Kapton Tape (included) or another non conductive material to cover the exposed wires and stop them from pulling apart easily.

![Wrap wires](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-037-182.png)

4\. Plug the other end of the now extended fan wires to the Power Supply. You can plug the Red Wire to contact #1, and the Black Wire to contact #6. This will allow your fan to run all the time and limit jamming or clogging in your extruder. Note: This is our preferred method for wiring the fan.

![Connect Red](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-184.png)
![Connect Black](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-185.png)

### 24. Verify Your Wiring Using the Below Pictures as a Reference

![PSU Wiring](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-186.png)
![RAMPS Wiring](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-187.png)
![RAMPS Wiring](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-188.png)
![RAMPS Wiring](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-038-189.png)


### 25. Mount Filament Feed Assist

Parts Needed:
* (1) Wire Keeper

Hardware Needed:
* (1) M3x30mm Bolt
* (1) M4 Washer

1\. Remove the bolt from the front left corner of the upper left Z Axis Motor and replace it with (1) Wire Keeper holding it in place by using (1) M3x30mm Bolt and (1) M4 Washer in the empty socket from the removed screw.

![Wire keeper](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-039-190.png)

### 26. Attach the Spool Holder

Parts Needed:
* (1) 140mm 2020 Beam

Hardware Needed:
* (1) 2020 L Bracket w/ Set Screw

1\. Using the (1) 2020 L Bracket we left in place on the left side of the printers vertical 2020 Beam, attach the (1) 140mm 2020 Beam to it. Then place your last (1) 2020 L Bracket on the top of the 140mm 2020 Beam to stop your spool of filament from sliding off.

![Spool holder](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-039-191.png)

### 27. Wire Cleanup and Cosmetics

Parts Needed:
* (1) Wire Keeper
* (1) 1m Wire Wrap
* (1) 2m Black 2020 Wire Conceal

Hardware Needed:
* (2) M4 T-nut
* (2) M4 Pan Head Bolt


1\. This step is honestly purely user preference. If you prefer to copy our printer we use the wire wrap for both the extruder wires and the X axis motor wires. We use the (1) Wire Keeper on the top most 2020 on the printer to attach the extruder cables for a nice clean look and to keep them from floating around. You can use these pictures as reference. Use zip ties to clean up the wiring and tuck it in next to the RAMPS Board. Note: Ignore the black cable with the extruder wires these pictures were taken after we installed a proximity sensor to test out our upgrade kit.

![Wire wrap](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-040-192.png)

2\. You can use the 2m of Black 2020 Wire Conceal you were provided to hide wires inside the 2020 Beam slots, or just for purely cosmetic purposes on the face of the printer. Some people even prefer to cut all their wires short and put new crimps on the end, we didn't on this build to make it a bit easier.

![Wire conceal](https://raw.githubusercontent.com/cyberkni/FolgertechManuals/master/2020i3/images/-040-193.png)

## Conclusion

Done! Wow, take a break!

When you're ready, get started with the configuration guide on [FolgerTech's Google Drive](https://drive.google.com/open?id=0B9b1NbuMK524fldIWWVCa0xfSXAtZmttcDhrbjBMeFNWcENBdVUzWnhtWDZ2YWdHVXpoUXM&authuser=0) - If that link is broken, you should be able to find it [here](http://folgertech.com/products/folger-tech-reprap-2020-prusa-i3-full-aluminum-3d-printer-kit).

If you have any suggestions or changes you wish to address on this manual, notify us with an [issue](https://github.com/cyberkni/FolgertechManuals/issues) or just edit the manual yourself.

Thanks!

The original conclusion was:

> Congratulations, you have officially finished building the Folger Tech 2020 i3 3D Printer Kit!! You are now ready to follow up with the configuration guide and get started with your first print! If you have any suggestions for changes to this guide, spots you thought need improvement or steps that might have been missing all together please email orders@folgertech.com. We value your feedback and we want to make sure this guide is as easy to follow as possible!

> Thank you for your continued business and support!

> - The Folger Tech Team
