# Laser Power and Speed Test

This folder contains the gcode test file and the resulting images.

The test was done using a 10W+ Endurance Laser. You can find it at [endurancelasers.com](https://endurancelasers.com/diode-lasers/10watt-endurance-laser-plus/).

The laser was using the long-distance lense (not the G2), and was barely focused. I don't have a good procedure to focus right now, and the laser is already giving me lots of power. 

## Disclamer

I bought this laser myself with my own money. This test was created in Autodesk Fusion360™ and exported using the post processor found in this repository. The Gcode was then duplucated and offseted using a `G92` code (by hand).
Feel free to use/test this file at your own risk. We will not feel responsible for any hurt, death or material destruction resulting of the use of this file. Do it at your own risk. Better, don't use it if you don't feel comfortable. 

## Results

### Cherry

The test was run on a Cherry wood (Merisier) about 3/4 inch thick. The last column on the right (100% laser power) was made a 200% speed... and it's still deeply carving into the wood.

![top](cherry/top.jpeg?raw=true "Top")

On cherry, which is my favorit hard wood, I would recommend using 10% at 600 mm/min or 20% at 1000 mm/min. Most of the other tests are really carving into the wood, as you can see on the other pictures : 

![side](cherry/side.jpeg?raw=true "Side")
![closeup](cherry/closeup.jpeg?raw=true "Closeup")

I will try to light sand and see. I'll comment later here.

I also note that the left and right end of each box is a little darker... My thinking is that the power-off Gcode that happen after every line is too slow and burn more before it moves to another position.

I will try to re-enable the lead-in/lead-out and stop turning the laser off. We'll see...

Also, the test file is a parallel motion from left to right. Maybe a 45 degree motion (like I usually see from people engraving pictures) would be better. Another test to do :)

### Pine

I bearly tested on pine, and anything more than 20% laser power will carve the wood. I'll re-test and add pictures soon

### Plywood

