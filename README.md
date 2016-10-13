This program was made by Mitchell Hewitt for CS430 Computer Graphics (Section 1), Project 3 - Illumination, in Fall 2016
This program reads in a height, width, json file, and output .ppm file.  
It parses the objects in the json file into a visual representation using raycasting and illumination.
The visual representation is then written out as an output p3 .ppm image file.

To use this program...

	1.  Compile it with the provided makefile (requires gcc).

	2.  Use the command "200 200 input.json output.ppm" to read the input json file
	    and write the objects within that json file to a p3 output.ppm 200x200 pixel image file.

If you would like to verify the raycasting...

	1.  Open the input file using a text editor that can read .json files.
	    You will find:		

	2.  Open the output file using a program that can read .ppm P3 files.
	    A correctly written output file will appear as follows:

Invalid inputs and file contents will close the program.
This program is designed to use eight bits per color channel.