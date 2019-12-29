# shapeokolaser
Laser Post-processor and stuffs for ShapeOKO and Autodesk Fusion360 

## Carbide 3D (ShapeOKO) Laser Post Processor

put the file from `posts/carbide3d-laser.cps` to your `Posts` folder. On OSX it is located at `Autodesk/Fusion 360 CAM/Posts`.

You can also import it to your Cloud Posts, and I recommend that.

### Warning
This post is really experimental and haven't been tested for production use. Please, test it on a scrap piece and *PUT YOUR EYEWEAR PROTECTION ON* !!

### Usage
I have two workflows for now : 

#### Laser cutting (tracing)
in the CAM (Manufacrture) part of Fusion360, click on the `Fabrication` menue above the icons, then select `Cutting` -> `2D profile`.

This will add a cutting toolpath.
I use a 0.1mm laser that I created in my tool list.
Then select the contour you want to trace.

#### Laser burning
This workflow is used when you want to create a black and white image, logo...
TBD
