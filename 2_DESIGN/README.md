# Circuit Diagram

![blinkTwoLED](https://user-images.githubusercontent.com/102514588/164626470-470e0694-a18d-4298-9090-b5024be32d81.jpg)

# Blinking Two LED’s Using ATmega328

![Blinking-Two-LED’s-Using-ATmega328-e1507351964566](https://user-images.githubusercontent.com/102514588/164627002-e43d83dd-92b7-4336-9c63-d10536e4d624.jpg)

* At the beginning of the program a pre-processor named “F_CPU” is defined. It is simply your way to tell some of the library code how many CPU cycles per second the processor is executing. Here we defined the F_CPU as 1 MHz. “#include <avr/io.h>” is a header files which provides you with various  i/o operations like DDRx, PINx, PORTx, etc. “#include <util/delay.h>” is a header file which provides you with inbuilt delay functions like _delay_ms(), _delay_us(), etc. “_delay_ms(1000)” provides a delay of 1000 milliseconds (i.e., equivalent to 1 second).
# DDRx  
Data Direction Register configures data direction of the port(Input/Output). The instruction “ DDRB |= (1<<DDB2)”  makes corresponding port pin as output.
# PORTx 
Port register is for assigning appropriate values for the port pins.
Writing to PORTx.n will immediately change state of the port pins according to given value. “PORTB |=(1<<PORTB2)” will generate a high signal at PB2. And “PORTB&=~(1<<PORTB3)” is for generating a low signal at PB3.
 	
