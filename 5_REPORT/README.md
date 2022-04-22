
# Report
In this project, we have learnt how to blink two LEDs with AVR ATmega328 microcontroller. First, we will connect the 2 LED’s with PB2 and PB3 of PORTB of the ATmega328 microcontroller. Then, we will make the 2 LED’s to blink with an interval of 1 second. It means, initially the 1st LED alone will glow and on the next second, it will turn off and the 2nd one will glow. This process continues forever and in this way LEDs blinks continuously.
In this, we have used 
* ATmega328 Microcontroller
* 3 resistors
* 330 Ohm Resistos-2
* 10 KOhm Resistor-1
* Reset Button
* Input Button
* Ground
* 2 LED's
* DDRx
Data Direction Register configures data direction of the port(Input/Output). The instruction “ DDRB |= (1<<DDB2)” makes corresponding port pin as output.

* PORTx
Port register is for assigning appropriate values for the port pins. Writing to PORTx.n will immediately change state of the port pins according to given value. “PORTB |=(1<<PORTB2)” will generate a high signal at PB2. And “PORTB&=~(1<<PORTB3)” is for generating a low signal at PB3.
* At the beginning of the program a pre-processor named “F_CPU” is defined. It is simply your way to tell some of the library code how many CPU cycles per second the processor is executing. Here we defined the F_CPU as 1 MHz. “#include <avr/io.h>” is a header files which provides you with various i/o operations like DDRx, PINx, PORTx, etc. “#include <util/delay.h>” is a header file which provides you with inbuilt delay functions like _delay_ms(), _delay_us(), etc. “_delay_ms(1000)” provides a delay of 1000 milliseconds (i.e., equivalent to 1 second).
