Download Link: https://assignmentchef.com/product/solved-cs224-lab-7-programming-pic32-microcontroller
<br>
The C programming language to develop simple applications for the PIC32 microcontroller. The mikroC IDE (integrated development environment) will be used as the software environment, and the Beti PIC32 Trainer Pack will be used as the hardware environment in this lab. This lab will be implemented as a <strong>team (groups of 2).</strong>

<strong>Summary </strong>

<strong>Part 1</strong>  Preliminary Report/Preliminary Design Report: PIC32 programming with mikroC IDE for special tasks given.

<strong>Part 2</strong> Implement and test the given problem in Beti PIC32 Trainer Pack.

<strong>DUE DATE OF PART 1: SAME FOR ALL SECTIONS</strong> Dear students please bring and drop your preliminary work into the box provided in front of the lab before 10:40 AM on Wednesday.. No late submission!

<strong>LAB WORK SUBMISSION TIMING:</strong> You have to show your lab work to your TA by <strong>12:15</strong> in the morning lab and by <strong>17:15</strong> in the afternoon lab. Note that you cannot wait for the last moment to do this. If you wait for the last moment and show your work after the deadline time 20 points will be taken off.

<strong>Part 1. Preliminary Work / Preliminary Design Report (40 points)</strong>




<ol>

 <li>Cover page, with university name, department name, and course name and number at the top, “Preliminary Design Report”, Lab # (e.g. 4), Section #, and your names and ID# in the middle, and the date of your lab at the bottom <strong>(one submission per team)</strong>.</li>

 <li>Research and read about SFRs. Explain the differences between TRISx, PORTx, LATx and ODCx ports. Specify the special function registers (SFRs) for the I/O device(s) involved in Part2.a and Part2. b.</li>

 <li>Give the C code for Part2.a, with lots of comments, an explanatory header, well-chosen identifiers and good use of spacing and layout to make your program self-documenting.</li>

 <li>Give the C code for Part2.b, with lots of comments, an explanatory header, well-chosen identifiers and good use of spacing and layout to make your program self-documenting.</li>

</ol>




You can read Chapter 8.6 Embedded I/O Systems in the textbook  and learn about SFRs at <a href="http://ww1.microchip.com/downloads/en/DeviceDoc/61120D.pdf">http://ww1.microchip.com/downloads/en/DeviceDoc/61120D.pdf</a> .

<strong><u>About the Beti PIC32 Trainer Pack</u></strong>

You only need to connect USB cable to the small PIC32 daughter board for both power supply and programming. Please check schematic files of the Beti board posted on Unilica if you need more information. The part number of the microcontroller we use is PIC32MX795F512L. You can refer to its datasheet (posted in Unilica) if you need more information. Note that you borrow a Lab-board containing the development board, connectors, etc. in the beginning. You are responsible for the lab board and you have to return all of them to the lab supervisor when you are done, otherwise you will lose points.

<strong>Part 2.</strong> <strong>Implementation using C and mikroC IDE</strong>

<strong><u>Part 2.a </u></strong>

In this part, using 2 pushbutton switches for EN and DIR inputs, send an 8-bit pattern of 10001000 to the 8 LEDs, rotating its position by 1 each 1.0 seconds. When DIR=0 it rotates to the right, DIR=1 makes it rotate to the left. When EN=1, the pattern is displayed and rotates.  When EN=0, it is not displayed and its position is “frozen”, so that it continues from the last position when EN=1 again.

<strong><u>Part 2.b</u></strong>

In this part, you need to implement a function f(x)=x<sup>3</sup> given below by using the seven-segment display (SSD) on the Beti board.




<table width="0">

 <tbody>

  <tr>

   <td width="48">x=</td>

   <td width="20">1</td>

   <td width="20">2</td>

   <td width="30">3</td>

   <td width="30">4</td>

   <td width="36">5</td>

   <td width="36">6</td>

   <td width="36">7</td>

   <td width="36">8</td>

   <td width="36">9</td>

   <td width="42">10</td>

   <td width="42">11</td>

   <td width="42">12</td>

   <td rowspan="2" width="42">…….</td>

   <td width="45">18</td>

   <td width="45">19</td>

   <td width="45">20</td>

   <td width="45">21</td>

  </tr>

  <tr>

   <td width="48">f(x)=x<sup>3</sup></td>

   <td width="20">1</td>

   <td width="20">8</td>

   <td width="30">27</td>

   <td width="30">64</td>

   <td width="36">125</td>

   <td width="36">216</td>

   <td width="36">343</td>

   <td width="36">512</td>

   <td width="36">729</td>

   <td width="42">1000</td>

   <td width="42">1331</td>

   <td width="42">1728</td>

   <td width="45">5832</td>

   <td width="45">6859</td>

   <td width="45">8000</td>

   <td width="45">9261</td>

  </tr>

 </tbody>

</table>




You should display f(x) values one by one on the 7-segment display with a delay of a few seconds. Since the 7-segment display has 4 digits, you can display only the first 21 numbers of the f(x).  When the 21st number of the series is displayed (it is 9261), the sequence should continue, starting again from the first number of the series.


