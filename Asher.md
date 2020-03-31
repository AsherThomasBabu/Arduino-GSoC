# **Proposal - Arduino GSoC 2020 - Write Examples for Official Libraries** 

**Name:**  *Asher Thomas Babu*

**GitHub Username:** *[@AsherThomasBabu](https://github.com/AsherThomasBabu)*

**GithubIssueTracker:** https://github.com/arduino/summer-of-code/issues/82

**Email:** ashertb2000@gmail.com

**Contact** +919847507460

**Time zone:**  India (GMT+5:30)




---

# **Abstract**

Example sketches play a very important role in helping a developer understand the functionality and functions available in a specific library. Personally, the first thing I would refer to while working with a library is the available examples.

Maintaining an updated and rich collection of easy to understand example sketches is the need of the hour.

The project that I have chosen to propose and pursue under the mentors at Arduino for Google Summer of Code 2020 is briefed in the following paragraphs

Housing about 90 Repositories, very few Libraries are well furnished with examples even though with issues. Most libraries like the `Education Shield`, `Scheduler`, `Keyboard`, `Mouse` have not been updated since their inception.

There are also inconsistencies in the availability of Examples in the Repos i.e Examples available to the IDE user may not be available to the ProIDE or Cli users because of their absence in the GitHub Repos.

Fixing these inconsistencies along with adding examples and project documentation for existing and new examples for easier understanding of these libraries shall be my main motive during the mentorship period.


# **Technical Details**

Libraries are plenty but the available examples are nowhere close to what is acceptable and understandable to beginners, from my research during the period after which Arduino was declared as an organization for GSoC, Here are the details of the projects that I would work on for the Summer.

The Examples I Propose to add are spread across a wide range, I selected these libraries after going through the current status of their examples availability and understandability of the functions.<br>
**To demonstrate my ability to contribute to Arduino during the mentorship, I have curated a simple example to be added to the core library at https://github.com/arduino/Arduino/tree/master/build/shared/examples/01.Basics/**

#### Description (to be added as ControlledFade.txt)
``` 
Reading a Potentiometer (analog input)
A potentiometer is a simple knob that provides a variable resistance, which we can read into the Arduino board 
as an analog value. In this example, that value controls the brightness of an LED.

We connect three wires to the Arduino board. The first goes to ground from one of the outer pins of the
potentiometer. 
The second goes from 5 volts to the other outer pin of the potentiometer. 
The third goes from analog input 2 to the middle pin of the potentiometer.

By turning the shaft of the potentiometer, we change the amount of resistance on either side of the wiper which
is connected to the center pin of the potentiometer. This changes the relative "closeness" of that pin to 
5 volts and ground, giving us a different analog input. When the shaft is turned all the way in one direction,
0 volts are going to the pin, and we read 0. When the shaft is turned all the way in the other direction,
5 volts are going to the pin and we read 1023. In between, analogRead() returns a number between 0 and 1023 
that is proportional to the amount of voltage being applied to the pin. 
```
#### Schematic (ControlledFade.png): <br>
_Created using [Frtizing](https://fritzing.org/)_<br>
![alt text](https://i0.wp.com/owenmundy.com/blog/wp-content/uploads/2010/05/potentiometer_to_led.png?w=600 "Schematic")

#### Code (ControlledFade.ino)
```C++
/* Analog Read to LED
 * ------------------ 
 *
 * controls a brightness of a light emitting diode(LED) connected to digital  
 * pin 13. The brightness depends on the value obtained by analogRead().
 * In the easiest case we connect
 * a potentiometer to analog pin 2.
 *
 * Created 30 March 2019
 * by AsherThomasBabu
 * 
 *
 */

int potPin = 2;    // select the input pin for the potentiometer
int ledPin = 13;   // select the pin for the LED
int val = 0;       // variable to store the value coming from the sensor

void setup() {
  pinMode(ledPin, OUTPUT);  // declare the ledPin as an OUTPUT
}

void loop() {
  val = analogRead(potPin);    // read the value from the sensor
  analogWrite(ledPin, val);    // sets the LED brigthness to the value read from the potentiometer
}
```   
To have an insight on my familiarity with GitHub, Kindly check my [Development Experiences](https://github.com/AsherThomasBabu/Arduino-GSoC/blob/master/Asher.md#development-experience) section.<br>
I have also taken care to go through the [CONTRIBUTION GUIDELINES](https://github.com/arduino/Arduino/blob/master/CONTRIBUTING.md) and followed them in my example<br>
I have also made a tutorial on this project for arduinohub.
Please find it at https://create.arduino.cc/projecthub/ashertb2000/controlledfade-using-potentiometer-b403c6

My approach to the proposal for other examples for specific libraries come from the concern for **need of examples that cover all the functions of a specific library** and not quantity. I have tabulated below the necessities that I found, and my proposed examples

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

Projects will help understand the function of a library better, HUB provides a great platform for this purpose. I intend to make and document projects that are based on these examples that I have proposed above subjective to the availability of components. All of which will aid the user to understand the usage of the libraries and their functions better.     

The main projects that I would like to work on are:
* Simple Arduino Music Player with LCD Display and Capacitive Buttons

![alt text](https://lh3.googleusercontent.com/T3gdhtJ4sJCpxy8R716tS312j8pBG7jRrVBmqXPh0OJxbO4O7_CbOeuH4fjuVjOqlrsrQqaL0-9sgf5LCR2MhNqhyfrFHLvB5PRu1_4k5yskAlqdVtoqIFM6FJ_2R08B-TAdL2bISvxSrE5AueJAgyBf_aLiSCItuJzb_NFq2lpx2-jkhdUYf7sGs2A9RjE1WqXNnjK9OOx86ibt3SnLNZb6utYVARHgjpbFEexMI3WxWJIPIq1MIEGet9VTYZTPcyBkg7uK5LWqBsP5C6Ko7dts5_jxaKqOdCKmqPxJe94K70C-LOZghEBpmojq3Svv9WuCpHHzSK7b0CIygvwOG5G04sSVy5-ecu3k45B-pC8koUiszGSMST7DObnDkiZNc4MyuLUDZqg5m4OOhX2iOKa3z3FUZZ1igT7-rj_hzS078wvdV-f3wKaPm6OYxQ0DQcq9bKATdU0rDhli2qOfF05sapSmGAHm_Ao8OGFnSe3VTfj3lA3wk3ZUtvsoCXCLOdeRYYyfQxDWum8GKpzk0KFLNkkUKEfGJT9B-UFwO_XP3TtfD1VZ3zBaynXeV3jsZZ9b0UmOBOvWOSojL48DGuYP3kudy0sxqrtbNb2V28j0KRq5qlzolrEyVMXtYoUOUlB7_aPt3BlF20GiuVumk-u17Ap9JF4Q5GonP53wTQB6ZwYoljAz3jcRJd0e700=w418-h312-no "Block Diagram")
* Accelerometer Mouse


# **Schedule of Deliverables**

### Application Review Period (March 31, 2020 - April 30, 2020)
* I have approached the Developers community to start work on an export feature for the Arduino IDE Mentioned in [#9479](https://github.com/arduino/Arduino/issues/9479). I will work on that to get familiar with the codebase and get familiar with the community.

* Go through all 90 repositories under Arduino-official libraries.

* Fix issues and create necessary pull-requests.

### **Community Bonding Period** (May 4, 2020 - May 31, 2020)

* My objective for the Community Bonding Period will be to initially get off on the right foot with my mentor and get to understand the needs of the Organization during the aforesaid period.

* Keeping my proposal in mind, I will work with the mentors to create a more refined and better plan for the coding period.

* Also, during this period I will try to work with the mentors to solve and fix issues that arise in the community to the best of my abilities to better understand the style of documentation and the structure of Examples that I have to maintain.

* And as mentioned in the Guide to the proposal, I will get hands-on experience of the Arduino and the modules that I plan to use. 


### **Phase 1** (June 1, 2020 - July 3, 2020)



*   Will work towards completing half of the Mentioned Examples at a rate of 2 - 3 per week, completing the required documentation and the required schematics of each example and regularly pushing to the public repository.

*   Code and diagrams will be regularly pushed to the public repository and will constantly communicate with the mentor to keep my work validated.

*   This phase will last about one month.


### **Phase 2** (July 4, 2020 - July 31, 2020)



*   This phase shall be more focused on the second half of the Mentioned examples at the same rate to complete the proposed examples.

*   Issues with previous examples will be rectified according to mentor advice.

*   A list of projects to be documented for the project hub will be continually discussed with mentors and finalized along the way.

*   This phase is bound to last around one month.


### **Phase 3** (August 1, 2020 - August 23, 2020)


*   This time shall be utilized for creating and documenting the projects required for the project hub.

*   This time shall also be utilized for the correction of the issues encountered in the previously curated examples.

*   This shall be the last 20 days before the final week where all the code is made public, and the mentor and I together review all the work and do the necessary corrections and also finish uploading the projects to Arduino HUB.


### **Final Week** (August 24, 2020 - August 31, 2020)


* All the above-mentioned code shall be completed along with documentation and will be pushed to the public repository. Decided upon projects shall be documented and uploaded to Arduino Project Hub. 


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
8. [arduino-libraries/Ciao#7](https://github.com/arduino-libraries/Ciao/pull/7) **(Approved)** Updated a broken Readme 
9. [arduino-libraries/SD#79](https://github.com/arduino-libraries/SD/pull/79)

Apart from that 



1. I was also the part of [@UnoPlatform](https://github.com/unoplatform) and [@Magneto](https://github.com/magento)
2. I also contributed to [@Kong](https://github.com/Kong) during the Hacktober month.

I was also the lead on the team that built IoT enabled sanitary pad vending machines based on the ESP8266.

I built a CNC Writing machine Based on the Arduino GRBL Library, it is also documented at Instructables at the following link.  

[https://www.instructables.com/id/DIY-CNC-Writing-Machine-Using-GRBL/](https://www.instructables.com/id/DIY-CNC-Writing-Machine-Using-GRBL/)

I Have been working on Arduino based projects for more than 3 years now, I Have also led and attended numerous workshops co-organized by me at my college as part of the IEEE.


# **Why this project?**

Every time I choose to work on a new module, or a library, the first thing that I often consult is the examples and the documentation. I chose to work with this organization and this project only because of the reason that I love the Arduino Community and wanted to give to the community what it had given me. I learned about Arduino being part of the Google Summer of Code and I immediately set out to understand the codebase and the needs. 

Being a part of GSoC was a big dream of mine, but tech-stacks of various organizations seemed intimidating, The reason why I decided to focus on Arduino ( only one organization and one project ) for this edition of GSoC is that I wanted to work with something that I could relate to and which is my interest rather than doing something for the sake of it.

Having the required skillset and exposure towards the necessary tools, I was sure I could attempt to cater to the needs of Arduino through this project. Also having written quite a good amount of Arduino code for various projects in school and college and also having experience in documenting projects, I decided that this project was the best fit for me and I haven’t turned on that decision ever since.


# **Do you have any other commitments during the GSoC period?**

During the GSoC Period, I do not have any other commitments. Due to the dilemmatic state of the pandemic, classes might be pushed a little into summer. I still can manage to do 30 hours of work every week.

My working hours on weekdays will be :

6:00 - 8:00 AM ; 12:00 - 1:00 PM ; 6:00 - 11:00PM (all times in IST)

Except on Sundays where it will be :

2:00 - 11:00 PM (all times in IST) 

