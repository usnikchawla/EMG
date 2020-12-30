# EMG
- The main purpose of the project was to design analog filters that filtered out the main muscle signal (70-200 hz ) and amplify it to
appropriate level for it to be converted into digital signal using the A to D converter of the atmega 328p (arduino). This filter block was basically
present between a INA and the microcontroller. The waveform was dispalyed using labview as it already has the drivers written for arduino. The Lab
view program was a simple analog read whose output was connected to display. The standard samplying rate of 9600 hz was used.
Generally in EMG design the frequency range of 50 to 150 hz is used but I decided to use the the range of 70 to 200 hz to avoid power line noise as
there is no proper grounding which sometimes causes problem in the data acquired. The filter section involved the usage of active filters. filter block
consisted of 1st order high pass Chebyshev filter followed by a second order low pass Chebyshev filter. A gain of about 100 was provided by the
high pass filter while the low pass filter had a unity gain. The filter block was preceded by an INA-129 providing a gain of about 5 . The electrode were
connected to the to INA through a three pin header.

- The pdf contains the  schematic for the system with LPC2142 chip and an FTDI chip. For the above discription the analog block design was used and its outpit was connected to the analog in pin of UNO through which the signal were plotted on LabView. Remember to keep the digital and analog ground seperate as in the pdf. 
