# UMBC_Hackathon_2016
Project Created for Hack UMBC 2016.  https://hackumbc.org/

PURPOSE:
To create an Arduino system that records a pattern of knocks on a door, and unlocks the door when that pattern is entered again later.

REQUIREMENTS:
Arduino UNO
Grove Piezo Vibration Sensor
Grove_LCD_RGB_Backlight-master Arduino Library: https://github.com/Seeed-Studio/Grove_LCD_RGB_Backlight
Grove Hardware Shield (optional)
BYJ48 Stepper motor

RESULTS:
When the arduino code is ran, it first records a sequence of (up to 11) knocks.  The project can successfullly record when the vibration sensor is on the other side of a piece of cardborad, but you must still knock hard because the sensor is not highly sensistive.  Next, a sequence of the same length as the lock pattern can be entered, and the 'unlock action' will succesfully occur if all the knocks have less than a 40% error when compared to the correct lock sequence.
The knock sequences are compared by comparing the times (in milliseconds) between successive knocks.
For this project, the 'unlock action' just changed the LCD's color, rotated a stepper motor, an turned on LEDs.

LIMITATIONS:
After recording the lock sequence, only one attempt can be made to unlock the 'door', after which the Arduino must be reset and a new lock sequence created.  This bug was due to the time constraints but didn't prevent the project from being demonstratable.  Due to the 24 hour time contstraint, the code is also somewhat inefficient/disoganized.

NOTE:
The stepper motor code was taken entirely from: http://www.instructables.com/id/BYJ48-Stepper-Motor/?ALLSTEPS

CONTRIBUTORS:
Daniel Engbert
Yash Upadhyay
Jonathan Baldauf
Mario Levi