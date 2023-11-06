This article refers to the lastest firmware version 1.1.2.03 (since 6-11-2023 the day this article wrote)

Z_Offset Problem and user Frustration!!!

After a lot of searching, the z_offset that your printer saves after autoleveling from the printer's touch screen is NOT saved inside printer.cfg. Hence all the frustration with z_offset to all Neptune 4 Pro users.
The printer's z_offset is saved inside a file that you cannot access without ssh. It is the file elegoo.ini inside folder: /Desktop/myfile/znp/znp_tjc_klipper from mks user. Also inside this file are saved the predefined preset heat temps for PLA etc. that you can change also.
So, if you make any changes in z_offset from fluid webpage, it is not saved properly (because this is the klipper enviroment). The same thing happens if you make changes on z_offset inside printer.cfg file.

So if you want to handle and use your printer through the touch screen AND in parallel through the fluid UI webpage, my suggestion is to set the z_offset under [probe] inside printer.cfg file to zero (z_offset: 0.0) and then make a bed leveling 
through the screen, set the offset and save it from the screen, make a restart, and the new offset will be saved as I wrote above in file: /Desktop/myfile/znp/znp_tjc_klipper/elegoo.ini

So if you want to make any change to your z_offset you either must make it from the touch screen, or through ssh directly changing the elegoo.ini file. Because otherwise if you change the z_offset inside printer.cfg file, the offsets are added with 
final result your nose hitting the bed (AS I DID TOO) which is not corrected.

Also a final tip is, to set your z_offset 0.01mm more than you thing it is the correct through the classic procedure with bed through nozzle paper grinding... I don't know why, but it helped me.

Sorry for the long text, but I wish someone wrote that for me text for me also to save me from all this suffering...

Have nice printings!!!
