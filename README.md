# shapeokolaser
Laser Post-processor and stuffs for ShapeOKO and Autodesk Fusion360 

## Carbide 3D (ShapeOKO) Laser Post Processor

put the file from `posts/carbide3d-laser.cps` to your `Posts` folder. On OSX it is located at `Autodesk/Fusion 360 CAM/Posts`.

You can also import it to your Cloud Posts, and I recommend that.

Note that this Post Processor **DOES NOT** output Z axis movements. Put your laser to the right height and that's it.

### Warning
This post is really experimental and haven't been tested for production use. Please, test it on a scrap piece and *PUT YOUR EYEWEAR PROTECTION ON* !!

### Usage
I have two workflows for now : 

#### Laser cutting (tracing)
I use a 0.1mm Kerf width `Laser Cutter` that I created in my tool list:

![Laser Cutter Tool](pictures/laser-tool.png?raw=true "Laser Cutter Tool")

On your design, just create a sketch with all your curves, or import an SVG file.

In the CAM (Manufacrture) section of Fusion360, create a new `Setup` and define your stock size and origin. Keep the `Operation type` to the default, `Milling`
Then click on the `Fabrication` menu above the icons, then select `Cutting` -> `2D profile`.
This will add a cutting toolpath.

Select your 0.1mm laser as the tool and select the cutting mode. `Through` and `Vaporise` both use a 100% laser beam, while `Etch` is less powerfull. You can change the power output in the *Post-Process* phase.
Also select your `Cutting Feedrate` (600mm/min per default). This is the speed of the movement.

Select the curves you want to trace in the `Geometry` tab.

In the `Heights`, select a 0 (zero) offset fron `Stock top` for Clearance, Retract and Top:

![2D Profile Heights](pictures/2d-profile.png?raw=true "2D Profile Heights")

In `Passes`, select a 0.01mm tolerance, left compensation and `in computer` compensation type.

In the final tab, `Linking`, ensure nothing is checked. Lead-in and Lead-out should NOT be selected.

I had to create many `2d Profiles` on my project so everything renders nicely. This is not uncommon when using SVG. If you fell the `Generate` phase of your toolpath never ends, it may be a good option to select only few curves, then add more, or create another `2d profiles` for another section of your curves.

When calculating you will end up with a yellow warning, like 

```text
Warning: Lifting retract plane to topmost lead height.
Warning: Lifting clearance plane to retract plane.
```

This can be ignored.

Finally click on your `2d profiles` or the `Setup` you want to trace with your laser and select `Post Process`.

Select the `Laser Carbide 3D(Grbl)` post processor from you Cloud Posts or Personnal Posts.
You should not have to change any value here except the `Through Power` if you want to change the laser power:

![Post Process](pictures/post-process.png?raw=true "Post Process")

You will end up with a Gcode (nc) file that you can import in your controler software. I personnally use [CNCJS](https://cnc.js.org/).

##### Example
![Tree Of Life](pictures/treeOfLife.png?raw=true "Tree Of Life")

#### Laser burning
This workflow is used when you want to create a black and white image, logo...
TBD
