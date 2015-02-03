# FRC_Scout
FRC Scout is a LabView application that allows collecting team scouting data during First Robotics Competion.

The design is based on 
* entring team and match data,
* converting that data to QR Code, 
* reading QR code, saving data into JSON text file and 
* assembling all JSON files into single spreadsheet. <br>
This program has been created with the intent to help collecting such data with multiple computers and transmitting it to a single computer without using wireless data connectiong. <br>

This applicaiton needs LabView 2013 or later and Vision Module installed. It also needs JSON package which you can get from VI Package Manager. The QR generator has been taken from https://lavag.org/topic/15670-qr-code-generator/. The QR reader is a part of the NI LabView Vision Module. <br>

QR reading with a simple old USB webcam 640x480 of a text larger than 500 bytes is tricky. Initial code was written to produce XML text files, however they were 2300 bytes long and they were  not readable using a simple camera. If text is about 300 bytes long reading should be stable and fast. The QR codes contain a unique identifier. This assues that any QR code can be read but only valid scouting QR codes are accepted. <br>

Saving data will produce files named with year-day-hour-minute-second. format. Only the final assembled file asks for a file name. This code does not check for doublicate entries. <br>

This code does not run on Tablet or Phone. <br>
This code does not include analysis features. <br>
Meaning there is plenty of room for expansion. <br>

Urs Utzinger <br>
Bit Buckets, 4183, 2015

[Enter Data] (https://github.com/uutzinger/Images/blob/master/EnterData.jpg)
[Generate QR Code] (https://github.com/uutzinger/Images/blob/master/QR_Generate.jpg)
[Read QR Code] (https://github.com/uutzinger/Images/blob/master/QR_Read.jpg)
[Assemble JSON records] (https://github.com/uutzinger/Images/blob/master/Assemble.jpg)

