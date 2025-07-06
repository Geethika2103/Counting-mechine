# Counting-mechine

This IR-based object counter circuit detects objects using an infrared 
transmitter (D3) and receiver (D4). The transmitter continuously emits 
infrared light, which reflects off an object when it comes close, allowing 
the receiver to pick up the reflected signal. The received signal then goes 
to an LM358 operational amplifier (U1) configured as a comparator, 
which outputs a high signal when it detects the reflected IR light. This 
high signal triggers the 555 timer (U2), configured in monostable mode, 
to generate a single pulse of fixed duration, determined by capacitor C1 
(220µF) and resistor R1. The pulse from the 555 timer acts as a clean 
signal for the counting ICs, U3 and U4, which are 4033-decade counters 
connected in cascade to form a 2-digit counter. Each time a pulse is 
received from the 555 timer, the counters increment by one, and the 
count is displayed on the connected 7-segment displays. This allows the 
display to show the number of objects detected, up to 99. The 7805-
voltage regulator (U5) provides a stable 5V supply to the circuit 
components, ensuring consistent operation. In summary, the circuit 
increments the displayed count by one each time an object passes near 
the IR sensor, making it suitable for applications such as people counters 
or object tracking systems.
