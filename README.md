# hp-41_astro
## HP-41: A user interface for the ASTRO2010 module

The ASTRO2010 module is a collection of astronomy programs by [Jean-Marc Baillard](http://hp41programs.yolasite.com/) (such as the "Astronomical Ephemeris for the HP41"). It’s an excellent module for astronomy enthisiasts and a valuable tool when I am out scouting the sky with my telescope.

While the ASTRO2010 module is a stroke of genius, it is lacking a simple user interface. Without my ASTRO user interface program you would have to rely on the user manual or have an elephant’s memory. This ASTRO program delivers to the user a menu driven easy-to-use interface bringing the top amateur astronomy programs into one complete program.

The features list goes like this:

* Menu driven user interface
* Menu items explained
* All input variables prompted for
* All output results explained
* One consistent Date format (DD.MMYYYY or MM.DDYYYY, your choice)
* Interface for the ephimeris program
* …Find the Sun, the Moon and the planets easily
* Interface for the Rise-Transit-Set program
* …Get the rise, transit and set times for Sun/Moon/Planet/stars, etc.
* Interface for the Jupiter/Saturn/Uranus satellite program
* …Get the placement of the moons relative to those planets
* Interface for the Moon Phase program
* …Get the date for the closest moon phase quarter
* And more…

When you start ASTRO, it asks for the Longitude (LO), Latitude (LA), the Date (DT) and the Local Time (L.T) as well as the adjustment to Universal Time (UT). 
The program prompts with the suggestion of the value it has previously stored. It then displays a menu corresponding to the top row of menu keys (A-E):

**__B E:A RS M ST__**

Pressing R/S brings up the menu for the second row of menu keys (a-e):

**__D/T A:E e=MNU__**

As you may guess, the first two items correspond to labels "a" and "b" while the last is for label "e"

Pressing R/S successively gives you the explanation for the menu items (A-E,a,b and e):

B = BODY<br>
E:A = EQ->AZ<br>
RS = RISE,TR,SET<br>
M = MOON PHASE<br>
ST = SAT:JU,SA,UR<br>
D/T = NEW DT,TM<br>
A:E = AZ->EQ<br>
MNU = MENU<br>

Here is the full explanation:

Label (Menu)	|Description
----------------|-----------
ASTRO	|Starts the ASTRO program. You should assign it to a key for easy access when using the Satellites program (see below)
LBL A (B)	|Brings up a menu asking for which body you want to get the placement of. Enter a number corresponding to the body you want: 0=Sun, 1=Mercury, 2=Venus, 3=Moon, 4=Mars, 5=Jupiter, 6=Saturn, 7=Uranus, 8=Neptune, 9=Pluto. The output gives in R/S-succession: The Azimuth, the Height (altitude), the apparent Hight (adjusted for atmosphere), the elongation from the Sun (except for the Sun itself), the RA, the DEC and then it brings you back to the main menu.
LBL a (T/D)	|Set a new Date and Time but with the same LO/LA. To also set a new LO/LA, simply restart ASTRO.
LBL B (E:A)	|You get asked for Ecliptic coordinates (RA/DEC) and gets the AZ and H (Altitude) in return
LBL b (A:E)	|You get asked for the Azimuth and the Altitude and get the Ecliptic coordinates (RA and DEC) in return
LBL C (RS)	|You get asked the RA and DEC of what you want to see the Rise-Transit-Set times for. The program asks for the RA/DEC for the previous date, the actual date and the next date. This is relevant for moving bodies. For stars, these RA/DECs would simply be the same. The program suggests previously stored values.
LBL D (M)	|This function first shows the percentage of illumination of the moon, then the closest moon phase quarter, then the date of the closest moon phase quarter and the local time.
LBL E (ST)	|Brings up a menu asking for what plantes you want to see the satellites of (1=Jupiter, 2=Saturn, 3=Uranus). It then shows the various moons (names and visual magnitude) with an R/S bringing up the coordinates in relation to the planet (Nort/South is flipped to reflect what you see in the telescope). An "<" is added if the satellite is closer to earth than the planet.
LBL e (MNU)	|Back to the main menu.

The program includes two utilities, the "D-YMD" that converts a date from your normal format (DD.MMYYYY or MM.DDYYYY) to the format YYYY.MMDD that is used by most of the ASTRO2010 module. The second utility program, the "YMD-D" reverses the conversion. At the end of the program listing you will also find the program "DMD" that is called from witin the ASTRO program. It converts between a the date formats DD.MMYYYY and MM.DDYYYY.

## License
This software is released into the Public Domain.

