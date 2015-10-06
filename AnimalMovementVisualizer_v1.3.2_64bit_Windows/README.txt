Animal Movement Visualizer (AMV) ver. 1.3

    "Displays animal location data in real time. This software can be used by ecologists 
    and researchers to track the migration patterns of animals, simply by uploading coordinates
    via an excel file.” - NASA World Wind Website


No-one likes README's but please read entirely thanks! =]


____________________________________________________________________________________________________________________
1.) Ensure your computer has Java, and the Java Runtime Environment installed and is properly functioning.

     a. To check: go to command prompt/terminal, type in:
  	java -version (or java -showversion)

	should come up with : Java version 1.6.X


2.)  This software is architecture dependent. Please double you have downloaded the correct .zip
     Currently compatible with: Windows x32, x64 or Mac OS.

     a. To check: Start -> Right-Click "Computer" -> Click "Properties" -> Look under "System Type"
  

3.) To run, simply execute "run.bat"

     a. Windows -- double click the "run.bat" file

     b. Mac -- type "./run.sh" in the terminal (if permissions not set

     c. If you are seeing the file chooser and no program, try using the command line. (w/o quotes)..

         i. Start -> Run -> type: "cmd.exe" -> type: "cd /path/to/this/directory/location/of/AMV.jar"
              
               ** Windows 7 simply type "cmd" in search -> Enter.

         ii. type: "java -jar AMV.jar" to start AMV 1.3. 

         iii. if program crashes, the error message will display on the command line. 

         iv. copy and paste this and send all bugs to devkavathekar23@gmail.com


____________________________________________________________________________________________________________________
FILE FORMAT:  .xls/.xlsx
 
   A       B       C       D       E       F       G
1  id	  year	  month	  day	  time	  lat	  long
2  12345   2020    10      23      2:00:00  45.234 -23.23
3  12345   2020    10      24      2:15:00  46.234 -26.23
4  82742   2020    6      09      14:45:10  46.234 -27.23
5  82742   2020    6      11      14:55:34  46.234 -28.23


*IMPORTANT* - EXACTLY use above format (keep first row blank (or use above labels) )

*IMPORTANT* - each animal's data info should be individually sorted: 
	      time relative, top down, recent to past: see example above
	      if you forget to sort, don't worry! I internally sort each animal's path :)


OPERATION:

1. Upload dialog box file prompt will appear upon execution.
   -> Only accepts ".xls" or ".xlsx" extension files.
   -> recursively prompts until an Excel file is given. Currently does not check for format correctness.

 
2. Adjust speed using the slider. Or, an arbitrary speed number can be specified in the text box.


3. Choose 1 of 3 display options:

   -> (default) Full lines: does not truncate lines after specified value. shows full path
   -> 		# trail: keeps the trail equivalent in the text field
   ->           No lines: displays only the icons 


4. Clicking "Start Animation", will begin simulation, displaying a timer.


5. Pause/Resume button will appear, use the spacebar for quick pause/play.


6. RIGHT-Clicking the animal labels on the left panel, will pop up
   a JColorChooser to update the color of animal labels/lines


7. LEFT-Clicking the animal labels on the left panel, will track the individual animal in a first person 
   perspective. Clicking again will disable and return to previous view. 
   Will keep current zoom/pan when displaying POV.


8. Clicking on an the animal's icon in the World Wind window, will display a balloon containing the current position.
   by clicking the balloon again, will remove it.


9. Speed can be adjusted mid-simulation. Line truncation value can not.


10. Upon completion of simulation, a reset button will appear. "Yes" selection will reset current data set.


____________________________________________________________________________________________________________________
Libraries Used:
JExcelApi- Java excel manipulation library (Free Open Source)
World Wind SDK v1.3 - NASA (Free Open Source)

____________________________________________________________________________________________________________________
Author: Devtulya Kavathekar
University of Maryland, College Park 
Department of Biology, Fagan Lab

Direction of: Dr. Thomas Mueller Ph.D
	      Dr. Bill Fagan Ph.D

Funding was provided by NSF grant DBI-1062411. 


--
last updated: May 10th, 2012