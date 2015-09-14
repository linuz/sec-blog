Title: Hijacking an Elevator Phone
Date: 2015-09-13 22:06
Tags: Red-Team, Security, Hardware, Physical

If you have ever been on an elevator, you have probably seen (or even used) the elevator phone inside the elevator. [By law](http://www.nfpa.org/~/media/Files/forms%20and%20premiums/101%20handbook/NFP101HB09_CHS2.pdf) elevators are required to have some form of two-way communication which usually entails a device connected [POTS (Plain Old Telephone Service)](https://en.wikipedia.org/wiki/Plain_old_telephone_service) or [PBX](https://en.wikipedia.org/wiki/Business_telephone_system#Private_branch_exchange) telephone line. Turns out, these devices are easy to take over and use for malicious purposes.

Many elevator phones are programmable in order to allow for different use-cases at different locations. A lot of these can be programmed simply by calling the phone number attached to the elevator phone. 

**How do we find the telephone number to the elevator phone?**

<img src="https://upload.wikimedia.org/wikipedia/commons/d/d4/Elevator_COP_-_Dover_Impulse_Elevator.JPG" width="500px">

Each phone may have a standard phone line attached to it (RJ-11). Find it and you can "borrow" that connection to find the number to the elevator phone.

[<img src="https://pbs.twimg.com/media/COpcJ5PUwAAsvvp.jpg" width="500px">](http://www.amazon.com/dp/B00F6POFL4/ref=cm_sw_su_dp)

You can use a [small corded telephone](http://www.amazon.com/dp/B00F6POFL4/ref=cm_sw_su_dp) like the one above to connect to the phone line. Once connected, dial **1-800-444-4444**. This number is a toll-free [Automatic Number Announcment Circuit](https://en.wikipedia.org/wiki/Automatic_number_announcement_circuit) that will inform you of the phone number you are calling from. Note this phone number down. Also note down the manufacturer or model number of the elevator phone if you can find it.

Look up the documentation for the specific model number of the elevator phone and you will find that you will most likely be able to program it simply by calling the number it is attached to. You will also find that it may have a default password to access programming mode, such as **123456** or **35842#**. From there, you can perform actions such as change the message it announces or even change the number it calls when the emergency button is activated. [Documentation example here](https://adamselevator.com/Specific_pdfs_HW/Programming%20Instructions/AS-3%20Series.pdf).

**How can this be used maliciously?**

1. Most elevator phones will auto answer when called. You can find the phone number to the device, call it, and now **you are listening to private conversations happening in the elevator**. This has the potential for corporate espionage.
2. You can cause a Denial-of-Service by changing who the elevator phone calls in case of an emergency.
3. You can pull a prank by changing the message it announces to people in the elevator car, or the party the phone is calling.
4. Think of some other things you can do with this. Maybe some social engineering attacks.

*PS: Sometimes, you can find the elevator phone's phone number written somewhere in the elevator by maintenance personnel*
