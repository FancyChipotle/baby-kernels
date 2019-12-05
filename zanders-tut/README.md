This tutorial and its requirements can be found [here](3zanders.co.uk/2017/10/13/writing-a-bootloader).

`nasm -f elf32 boot4.asm -o boot4.o`
`i686-elf-gcc -m32 kmain.cpp boot4.o -o kernel.bin -nostdlib -ffreestanding -std=c++11 
-mno-red-zone -fno-exceptions -nostdlib -fno-rtti -Wall -Wextra -Werror -T linker.ld`
`qemu-system-x86_64 -fda kernel.bin`
