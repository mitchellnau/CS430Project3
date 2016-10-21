This program was made by Mitchell Hewitt for CS430 Computer Graphics (Section 1), Project 3 - Illumination, in Fall 2016
This program reads in a height, width, json file, and output .ppm file.  
It parses the objects in the json file into a visual representation using raycasting and illumination.
The visual representation is then written out as an output p3 .ppm image file.

To use this program...

	1.  Compile it with the provided makefile (requires gcc).

	2a.  Use the command "200 200 input3.json output.ppm" to read the input json file
	     and write the objects illuminated within that json file to a p3 output.ppm 200x200 pixel image file.

	2b.  You can alternatively use input4.json to test spotlight illumination.

If you would like to verify the raycasting and illumination...

	1a.  Open the input3.json file using a text editor that can read .json files.
	    You will find:
		>a camera
                >a red sphere with radius 2 with white specularity, centered at y=1 z=5
                >a green plane with white specularity
                >a light with theta of 0, radial a# values, and a position at x=1 y=3 z=1

	2a.  Open the output file using a program that can read .ppm P3 files.
	    A correctly written output file will appear as follows:
                >a red sphere with a shiny spot toward the right on its top half
                 and its bottom-left half should be dark to black
                >a green plane that grows darker the further back it is that has an elliptical
                 shadow cast on it by the sphere

	1b.  Open the input4.json file using a text editor that can read .json files.
	    You will find:
		>a camera
                >a red sphere with radius 0.5 with white specularity, centered at y=0.5 z=5
                >a yellow sphere with radius 2 with white specularity, centered at y=12 z=5
                >a green plane with white specularity
                >a light with theta of 30, radial a# values, angular-a0 of 1, a direction of y=-20 (down)
                 and a position at x=1 y=3 z=1

	2b.  Open the output file using a program that can read .ppm P3 files.
	    A correctly written output file will appear as follows:
                >a small red sphere with a shiny spot at the top and most of its underside is black
                >a circular green plane (because of the spotlight) with an elliptical circle cast 
                 on it by the red sphere.
                >no other shadows or spheres because the yellow sphere is above the spotlight

Invalid inputs and file contents will close the program.
This program is designed to use eight bits per color channel.