# FRC_Scout
FRC Scout is a LabView application that allows collecting team scouting data during First Robotics Competion.

The design is based on 
a) entring team and match data, 
b) converting that data to QR Code, 
c) reading QR code, saving data into JSON text file and 
d) assembling all JSON files into single spreadsheet.
This program has been created with the intent to help collecting such data with multiple computers and transmitting it to a single computer without using wireless data connectiong.

This applicaiton needs LabView 2013 or later and Vision Module installed. It also needs JSON package which you can get from VI Package Manager. The QR generator has been taken from https://lavag.org/topic/15670-qr-code-generator/.
The QR reader is a part of the Vision Module.

QR reading with a simple old USB webcam 640x480 of codes larger 500 bytes is tricky. Initial code was written to produce XML text files, however they were 2300 bytes long and were not readable using simple camera. If text is text is about 300 bytes long reading should be stable and fast.
QR codes contain unique identifier which assures that non scouting QR codes are not accepted.

Saving data will produce files named with year-day-hour-minute-second format. Only the final assembled file asks for file name.
This code does not check for doublicate entries.

This code does not run on Tablet or Phone. Meaning there is plenty of room for expansion.
Urs Utzinger
Bit Buckets, 4183, 2015
