CROSS-COMPILER = arm-none-eabi-

all: simple.elf

simple.elf: simple.c startup.s
	$(CROSS-COMPILER)gcc -Wall -mcpu=cortex-m4 -mthumb -nostartfiles -Ttext=0x0 startup.s simple.c -o simple.elf
	$(CROSS-COMPILER)objdump -D simple.elf

clean:
	rm -rf *.o *.elf

