# RS232Debug
Informations how to debug RS232 Hardware Flow Control

# Why?
I had troubles to work with my old Pen Plotter and then i tried to fix it.

# How?
I build a "Hardware Sniffer" and connect it to a Logic Analyzer.
A cheap Logic Analyzer like the cheap 10 Dollar ones with 8 Channel and 24MHz are more then enough.
The Hardware Sniffer Board is not only a connector but also a Voltage Translator. So RS232 can be up to +-9V per Channel you must limit it to the Range of the LA with 0 to 5V. So the Cheap LAs are ready to analyze 3,3V Signals it can be very solved with LEDs. If you use Red Ones you Limit the Voltage arround 3,2V - if you want more you can put a normal Diode in Series. You can also use Z-Diodes - then you are done. If you use LEDs like me then you need a second Diode for each Cannel to limit negative Voltages. Those should be Shotky types to limit it to -0.5V. So this is more complex but you can see on the LEDs whats actual happen on the Lines.
<img src=rs232sniffer.png>

Then you need to connect the Pinheader to the LA. Be careful: Pin 1 to 1 and so on - till Pin 5 on the Sniffer: This is GND (Pin9 on LA). Then continue with Pin 5 to Pin 4 and so on.
After this you can set your Logic Analyzer Software to the Line Names: DCD, RX, TX, DTR, DSR, RTS, CTS and RI

<img src=rs232LA1.png>

