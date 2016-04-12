BIN_DIR=bin/
OBJ_DIR=obj/
IMG_DIR=img/

BOOTLOADER=bootloader.asm
BOOTLOADER_OBJ=${OBJ_DIR}bootloader.o

KERNEL=main.c
KERNEL_OBJ=${OBJ_DIR}kernel.o
KERNEL_BIN=${BIN_DIR}kernel

IMG=${IMG_DIR}/flippy.img

AS=nasm
AS_FLAGS=-f macho

GCC=gcc
GCC_FLAGS=-m32

LD=ld
LD_FLAGS=-static

EMU=qemu-system-x86_64
EMU_FLAGS=-fda

${IMG}:${KERNEL_BIN}
	

${EMU}:${IMG}
	${EMU} ${EMU_FLAGS} ${IMG}



clean:
  rm ${KERNEL_OBJ} ${BOOTLOADER_OBJ} ${KERNEL_BIN} 
