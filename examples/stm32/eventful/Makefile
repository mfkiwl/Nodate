# Makefile for 'Eventful' example Nodate project for STM32.
#

# Architecture must be set.
# E.g.: AVR, SAM, ESP8266.
ARCH ?= stm32

# Target programming language (Ada, C++)
NDLANGUAGE ?= cpp

# One can use the board preset.
#BOARD ?= nucleo-f042k6
BOARD ?= blue_pill
#BOARD ?= stm32f4-discovery
#BOARD ?= nucleo-f746zg

# Set the MCU and programmer types.
#
# MCU, programmer, variant
# atmega328p, arduino, standard
# atmega1280, arduino, mega 
# atmega2560, wiring, mega
#
#MCU ?= atmega2560
#PROGRAMMER ?= wiring
# Pin variant. Set 'standard' for ATmega328P, 'mega' for ATmega1280/2560.
#VARIANT ?= mega

# Set the name of the output (ELF & Hex) file.
OUTPUT := eventful


# Add files to include for compilation to these variables.
APP_CPP_FILES = $(wildcard src/*.cpp)
APP_C_FILES = $(wildcard src/*.c)


#
# --- End of user-editable variables --- #
#

# Nodate includes. Requires that the NODATE_HOME environment variable has been set.
APPFOLDER=$(CURDIR)
export

all:
	$(MAKE) -C $(NODATE_HOME)
	
flash:
	$(MAKE) -C $(NODATE_HOME) flash
	
clean:
	$(MAKE) -C $(NODATE_HOME) clean
