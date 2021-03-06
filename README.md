# FRC_Scout
FRC Scout is a LabView application that allows collecting team scouting data during First Robotics Competition.

The design is based on 
* Entring team and match data,
* Converting that data to string then to QR Code, 
* Reading QR code, converting to record and saving data into JSON text file and 
* Assembling all JSON files into single spreadsheet. <br>
This program has been created with the intent to help collecting data with multiple computers and transmitting it to a single computer without using wireless data connection. <br>

This applicaiton needs LabView 2013 or later and Vision Module installed. It also needs JSON package which you can get from VI Package Manager. The QR generator has been taken from https://lavag.org/topic/15670-qr-code-generator/. The QR reader is a part of the NI LabView Vision Module. <br>

QR reading with a simple old USB webcam 640x480 of a text larger than 500 bytes is tricky. Initial code was written to produce XML text files, however they were 2300 bytes long and they were not readable using a simple camera. If text is about 300 bytes long reading should be stable and fast. The QR codes contain a unique identifier. This assures that any QR code can be read but only valid scouting QR codes are accepted. <br>

Saving data will produce files named with year-day-hour-minute-second. format. Only the final assembled file asks for a file name. This code does not check for dublicate entries. <br>
This code does not run on Tablet or Phone. <br>
This code does not include analysis features. <br>
This code can be made into stand alone application not requiring LabView to run. <br>
Meaning there is plenty of room for expansion. <br>

Urs Utzinger <br>
Bit Buckets, 4183, 2015

[Enter Data] (https://github.com/uutzinger/Images/blob/master/EnterData.jpg) <br>
[Generate QR Code] (https://github.com/uutzinger/blob/master/Images/QR_Generate.jpg) <br>
[Read QR Code] (https://github.com/uutzinger/blob/master/Images/QR_Read.jpg) <br>
[Assemble JSON records] (https://github.com/uutzinger/blob/master/Images/Assemble.jpg) <br>

