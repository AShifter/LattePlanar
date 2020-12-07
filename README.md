# LattePlanar
An open-source Planar Magnetic tweeter that you can build yourself using readily available parts &amp; a 3D printer.

**NOTE!** The current revision, 0.9, has some issues and isn't something I would consider a 'complete' product. Prepare for things not lining up, really tight tolerances, and lots of binder clips/glue. I hope to release rev. 1.0 soon to fix these issues but for now, just have fun!

## The Concept
A Planar Magnetic driver is arguably simpler than the dynamic drivers used in most loudspeakers - a small coil of wire (representing the target impedance of the driver) is adhered to a thin film, and an isodynamic magnetic field (The force which makes like poles repel) spans between each face of the membrane. This is akin to the design used by Magnepan, and potentially dates all the way back to 1911 with Edwin S. Pridham and Peter L. Jensen's 'moving-coil loudspeaker', which they called 'Magnavox' (yes, that Magnavox). *This potentially makes the Planar Magnetic concept as old as one of the (most famous handguns in American history.)[https://en.wikipedia.org/wiki/M1911_pistol]*

## Materials Needed
- 3D Printer (project was made entirely on an Ender 3, great machine and highly recommended!)
- Filament (PLA works fine)
- Drag Knife attachment (for cutting coil)
- Conductor for Coil (ideally Aluminum Foil tape, if you're feeling lucky there are a lot of sources for copper tape on Amazon - experiment!)
- Membrane material (many different options here - the thinner the better, ideally down to approximately 3 microns. I used Window Tint film, but the plastic wrap in your kitchen might work just as well if it doesn't stretch too much)
- Magnets. The ones used in this project are 3/4" x 3/16" x 1/8" N52 grade neodynium magnets sourced from eBay, I don't know about international availability though. *Be careful while handling magnets - these things can break easily and bite!)
- #10-24 machine screws and nuts (or close Metric equivalent)
- #6-32 machine screws, washers, and nuts (or close Metric equivalent)
- Cutting wasteboard/cricut board (for sticking the aluminum foil tape on to cut, cricut boards have adhesive pre-applied but I haven't tried using one)
- Medium binder clips (for LattePlanar v0.9)
- Spray Adhesive
- X-Acto knife or similar

## The Build
Print the parts at 100% infill;

2x LattePlanarMagnetPlate.stl
1x LattePlanarMembranePlate.stl
1x LattePlanarWasherPlate.stl

Cut the foil. This video outlines the process of putting the drag knife on your Ender 3; https://www.youtube.com/watch?v=4XV9aHWMRFo rather than a sheet of Vinyl we'll be cutting a piece of foil tape, and rather than making our own design, we'll be cutting the included LattePlanarCoilPath.svg file. 

LattePlanarCoilDesign is included as an editable coil with multiple paths and a reference for the frame dimensions if you want to make your own changes.

Generate Gcode from the LattePlanarCoilPath.svg file. You can do this using the Gcodetools included with Inkscape if you have it installed, or use an online tool like (JSCut)[http://jscut.org/].

If you have a Creality Ender 3 or Ender 3 Pro 3D printer, the LattePlanarCoilEnder3Sliced.gcode file is included which contains a good, working path to cut the coil. Simply put it on your SD card and run it as a print, and the machine will begin running. I recommend lightly scoring your wasteboard/cricut board with this file before you glue the tape on so you can get an idea as to where the cut will happen.

Stick the Aluminum Foil tape metal-side down on the wasteboard/cricut board and run the program. Once the cut is done (may take a few tries, don't get discouraged. I had about 20 bad cuts while I was designing the tweeter, make sure your bed is level and blade is sharp) remove the excess tape around the traces, pull up the paper backing, and stick your membrane material on the adhesive side of the aluminum foil tape.

Make sure it's stuck really well by rubbing a cloth against the membrane material, and slowly pull up the membrane from the bed. The traces should come up as well - if any part stays stuck to the bed, try lifting it up with your X-Acto knife, flatten the membrane against the bed, and try pulling up again. Once the membrane is successfully lifted off the bed, with traces intact, you can move on to final assembly.

Adhere the complete membrane and coil (foil) to the MembranePlate, making ABSOLUTELY SURE to keep the traces facing upward/toward you - none of the traces should be touching the MembranePlate. You can quickly glue these together with some spray adhesive, I used 3M Super 77.

Use an X-Acto knife to open all of the holes on the MembranePlate that have been blocked by the membrane (EXCEPT the biggest middle holes which are currently covered by traces on rev. 0.9. Opening and using these holes will destroy your foil).

Now, add magnets to both of the MagnetPlates, making sure to keep the same poles facing inward/outward so the entire plates repel eachother. This might be easier to do on a metal desk.

Finally, put all of the plates together like so;

--  MagnetPlate  --
--  WasherPlate  --
--  Planar Foil  --
-- MembranePlate --
--  MagnetPlate  --

and put screws through the four #10-24 holes that are currently open. Hold the middle closed with binder clips if it seems neccessary. Keep the entire thing together with nuts.

The two large openings on the WasherPlate are just the right size to put #6 washers in and make contact with the pads of the driver. IF YOU SEE TRACES THROUGH THIS OPENING, CLOSE THEM WITH ELECTRICIAN'S TAPE. Please don't short out your amp.

Put #6-32 screws through the smaller holes and attach your speaker wires. Your Planar Magnetic Tweeter is now finished!

**I will try to add pictures & more information to this guide as I have time. **

## Closing Notes
Just have fun! This was a really cool project and I definitely learned a lot. There are still some things to work out but it's functional and it works pretty well for the time being.

If you build one of these, feel free to open an issue on GitHub sharing your results, measurements, or any questions.

## License
Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg