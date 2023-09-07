PORT = /dev/ttyUSB0

default: clean build flash

build:
	@mkdir -p obj
	@mkdir -p firmware
	avr-gcc -mmcu=atmega328p -DF_CPU=16000000UL -D__AVR_ATmega328P__ -Os -o ./obj/main.o ./src/main.c
	avr-objcopy -j .text -j .data -O ihex -R .eeprom ./obj/main.o ./firmware/firmware.hex
flash:
	avrdude -c arduino -p m328p -P $(PORT) -b 115200 -U flash:w:./firmware/firmware.hex
clean:
	@rm -rf obj firmware
