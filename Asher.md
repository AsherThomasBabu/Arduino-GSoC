# **Proposal - Arduino GSoC 2020 - Write Examples for Official Libraries**


# **Abstract**

Example sketches play a very important role in helping a developer understand the functionality and functions available in a specific library. Personally, the first thing I would refer to while working with a library is the available examples.

Maintaining an updated and rich collection of easy to understand example sketches is the need of the hour.

The project that I have chosen to propose and pursue under the mentors at Arduino for Google Summer of Code 2020 is briefed in the following paragraphs

Housing about 90 Repositories, very few Libraries are well furnished with examples even though with issues. Most libraries like the `Education Shield`,`Scheduler`, `Keyboard`, `Mouse` have not been updated since their inception.

There are also inconsistencies in the availability of Examples in the Repos i.e Examples available to the IDE user may not be available to the ProIDE or Cli users because of their absence in the GitHub Repos.

Fixing these inconsistencies along with adding examples and project documentation for existing and new examples for easier understanding of these libraries shall be my main motive during the mentorship period.


# **Technical Details**

Libraries are plenty but the available examples are nowhere close to what is acceptable and understandable to beginners, from my research during the period after which Arduino was declared as an organization for GSoC, Here are the details of the projects that I would work on for the Summer.


### **Library Examples**


<table>
  <tr>
   <td>
<h3><strong>Sl.No</strong></h3>


   </td>
   <td>
<h3><strong>Library</strong></h3>


   </td>
   <td>
<h3><strong>Example</strong></h3>


   </td>
   <td>
<h3><strong>Description</strong></h3>


   </td>
  </tr>
  <tr>
   <td rowspan="3" >1.
   </td>
   <td rowspan="3" >Servo
   </td>
   <td>JoyStickControl
   </td>
   <td>Using a joystick module to control the motion of 2 servos, intended to give basics of the Servo Library and also interfacing the joystick module.
   </td>
  </tr>
  <tr>
   <td>SerialControl
   </td>
   <td>Knowing and understanding the SerialInput capability of an Arduino is necessary, Along with that this program aims at letting the user know the position of the servo and also change positions by entering values into the serial monitor.
   </td>
  </tr>
  <tr>
   <td>ProgrammedMotion
   </td>
   <td>Using a potentiometer to record its motion and play it back via the servo using a button.
   </td>
  </tr>
  <tr>
   <td>2.
   </td>
   <td>MKRTHERM
   </td>
   <td>ReadSensorImperial
   </td>
   <td>The Library Lacks an Imperial Unit Read Example. Adding this example will allow for readings in Fahrenheit.
   </td>
  </tr>
  <tr>
   <td rowspan="2" >3.
   </td>
   <td rowspan="2" >Audio/AudioZero
   </td>
   <td>SimpleMusicPlayer
   </td>
   <td>Using 3 buttons as an interface to the Arduino, any music stored as .wav on an SD card can be read and played with an Arduino.
   </td>
  </tr>
  <tr>
   <td>Record Function
   </td>
   <td>Currently the library features only a playback feature. The functionality of the board can be further improved by adding a record function to the 
   </td>
  </tr>
  <tr>
   <td rowspan="3" >4.
   </td>
   <td rowspan="3" >Keyboard
   </td>
   <td>KeyboardMacro
   </td>
   <td>Perform a pre-programmed set of keyboard instructions on the press of a single Arduino button.
   </td>
  </tr>
  <tr>
   <td>HelloWorld
   </td>
   <td>Basic Program to understand the working of the keyboard library 
   </td>
  </tr>
  <tr>
   <td>KeyboardReprogram, KeyboardSerial, KeyboardLogout, KeyboardMessage,KeyboardAndMouseControl
   </td>
   <td>Add the remaining examples from Arduino.cc along with all the documentation and schematics.
   </td>
  </tr>
  <tr>
   <td rowspan="3" >5.
   </td>
   <td rowspan="3" >Mouse
   </td>
   <td>MouseMacro
   </td>
   <td>Perform a pre-programmed set of instructions at the single press of an external button.
   </td>
  </tr>
  <tr>
   <td>KeyboardAndMouseControl,
<p>
ButtonMouseControl,
<p>
JoystickMouseControl
   </td>
   <td>Add the remaining examples from Arduino.cc along with all the documentation and schematics.
   </td>
  </tr>
  <tr>
   <td>AccelerometerMouse
   </td>
   <td>Uses an accelerometer to detect tilts and converts that into mouse movements on the computer.
   </td>
  </tr>
  <tr>
   <td>6.
   </td>
   <td>ArduinoBLE
   </td>
   <td>ConnectionStatusLED
   </td>
   <td>Using the connected() function of the ArduinoBLE Library to let beginners know the basics of how to connect to a BLE device and light up an LED on establishing a proper connection.
   </td>
  </tr>
  <tr>
   <td>7.
   </td>
   <td>MKRNB
   </td>
   <td>LedControl
   </td>
   <td>MKRNB library lacks simple examples to help beginners understand the module. This Example will allow an LED to be controlled via an SMS.
   </td>
  </tr>
  <tr>
   <td>8.
   </td>
   <td>CapacitiveSensor
   </td>
   <td>CapacitiveButton
   </td>
   <td>Creating a simple Sketch along with schematics to control a simple LED using a Capacitive Button.
   </td>
  </tr>
  <tr>
   <td>9.
   </td>
   <td>CRC32
   </td>
   <td>CRCHelloWorld
   </td>
   <td>CRC is not a very easy concept for beginners, This will be a simple sketch that will allow them to learn the concept of CRC.
   </td>
  </tr>
  <tr>
   <td>10.
   </td>
   <td>Stepper
   </td>
   <td>SerialInput
   </td>
   <td>A sketch that will allow the users to control the stepper motor by using the keyboard to input step count and arrow keys to give serial input. 
   </td>
  </tr>
  <tr>
   <td>11.
   </td>
   <td>Scheduler
   </td>
   <td>MultiIO
   </td>
   <td>A Simple sketch to show the capability of this rather infamous library by integrating hardware for Simultaneous Inputs and Outputs.
   </td>
  </tr>
</table>


**Note: _All these are just my understanding of the needs of the repositories, I will be open to discussion with the mentors to curate a more fitting set of examples if needed._**


### **_Example Projects for Arduino HUB_**

Projects will help understand the function of a library better, HUB provides a really great platform for this purpose. I intend to make and document projects that are based on these examples that I have proposed above subjective to the availability of components. All of which will aid the user to understand the usage of the libraries and their functions better. 	

The main projects that I would like to work on are:
#### Simple Arduino Music Player with LCD Display and Capacitive Buttons
 **DETAILS(Schematic,Code snippets) YET TO BE ADDED**
#### Accelerometer Mouse


# **Schedule of Deliverables**


### **Community Bonding Period**

My objective for the Community Bonding Period will be to initially get off on the right foot with my mentor and get to understand the needs of the Organization during the aforesaid period of time.

Keeping my proposal in mind, I will work with the mentors to create a more refined and better plan for the coding period.

Also, during this period I will try to work with the mentors to solve and fix issues that arise in the community to the best of my abilities in order to better understand the style of documentation and the structure of Examples that I have to maintain.

And as mentioned in the Guide to the proposal, I will get hands-on experience of the Arduino and the modules that I plan to use. 


### **Phase 1**



*   Will work towards completing all of the Mentioned Examples at a minimal rate of 2 - 3 per week, completing the required documentation and the required schematics of each example.
*   Code and diagrams will be regularly pushed to the public repository and will constantly communicate with the mentor to keep my work validated.
*   This phase will last about half of the coding period. I.e. one and a half months.


### **Phase 2**



*   This phase shall be more focused on Building the Projects and documenting the process of doing so.
*   A list of projects will be continually discussed with mentors and errors corrected along the way.
*   This phase is bound to last around one month.


### **Phase 3**



*   This shall be the last few days before the final week where all the code is made public, and the mentor and I together review all the work and do the necessary corrections and also finish uploading the projects to Arduino HUB.


### **Final Week**

All the above-mentioned code shall be completed along with documentation and will be pushed to the public repository. Decided upon projects shall be documented and uploaded to Arduino Project Hub. 


# **Development Experience**

I am Asher Thomas Babu, an enthusiastic developer pursuing Electronics and Communications Engineering from India.

GitHub - [@AsherThomasBabu](https://github.com/AsherThomasBabu)

I Have been contributing to the open-source society for the past two years, I happened to be a part of the **HacktoberFest**  for the past two years.

I have also been contributing to the **Arduino community** for about a month and below mentioned are some of my contributions to the Arduino Community.



1. [arduino-libraries/SD#75](https://github.com/arduino-libraries/SD/pull/75) **(Merged)** Fixed a card corruption issue with the example in SD Library
2. [arduino-libraries/AudioZero#8](https://github.com/arduino-libraries/AudioZero/pull/8) **(Merged)** Corrected a Markdown error in a readme file.
3. [arduino-libraries/Mouse#13](https://github.com/arduino-libraries/Mouse/pull/13) **(Approved)** Added an example to the Mouse Library
4. [arduino-libraries/AudioZero#9](https://github.com/arduino-libraries/AudioZero/pull/9) Fixed an issue that caused deteriorating quality on the repeated playing of an audio file.
5. [arduino-libraries/Keyboard#31](https://github.com/arduino-libraries/Keyboard/pull/31) Added a HelloWorld Example to the Keyboard Library
6. [arduino-libraries/CapacitiveSensor#3](https://github.com/arduino-libraries/CapacitiveSensor/pull/3) **(Approved)** Fixing an inconsistency in the markdown of the readme file.
7. [arduino-libraries/Servo#41](https://github.com/arduino-libraries/Servo/pull/41) Added an example for the Servo Library.

Apart from that 



1. I was also the part of [@UnoPlatform](https://github.com/unoplatform) and [@Magneto](https://github.com/magento)
2. I also contributed to [@Kong](https://github.com/Kong) during the Hacktober month.

I was also the lead on the team that built IoT enabled sanitary pad vending machines based on the ESP8266.

I built a CNC Writing machine Based on the Arduino GRBL Library, it is also documented at Instructables at the following link.  

[https://www.instructables.com/id/DIY-CNC-Writing-Machine-Using-GRBL/](https://www.instructables.com/id/DIY-CNC-Writing-Machine-Using-GRBL/)

I Have been working on Arduino based projects for more than 3 years now, I Have also led and attended numerous workshops co-organized by me at my college as part of the IEEE.


# **Why this project?**

Every time I choose to work on a new module, or a library, the first thing that I often consult is the examples and the documentation. I chose to work with this organization and this project only because of the reason that I love the Arduino Community and wanted to give to the community what it had given me. I learned about Arduino being part of the Google Summer of Code and I immediately set out to understand the codebase and the needs. 

Having the required skill set and exposure towards the necessary tools, I was sure I could attempt to cater to the needs of Arduino through this project. Also having written quite a good amount of code for various projects in school and college and also having experience in documenting projects, I decided that this project was the best fit for me and I haven’t turned on that decision ever since.


# **Do you have any other commitments during the GSoC period?**

During the GSoC Period, I do not have any other commitments. Due to the dilemmatic state of the pandemic, classes might be pushed a little into summer. I still can manage to do 30 hours of work every week.

My working hours on weekdays will be :

6:00 - 8:00 AM ; 12:00 - 1:00 PM ; 6:00 - 11:00PM

Except on Sundays where it will be :

2:00 - 11:00 PM

