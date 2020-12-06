TARGET := test-generic.ihx
SOURCES := main.c stm8l10x_it.c \
	stm8l10x_clk.c \
	stm8l10x_i2c.c \
	stm8l10x_spi.c

INCDIR := . ../../lib/STM8L10x_StdPeriph_Lib/Libraries/STM8L10x_StdPeriph_Driver/inc
VPATH := . ../../lib/STM8L10x_StdPeriph_Lib/Libraries/STM8L10x_StdPeriph_Driver/src

all: $(TARGET)

-include ../../toolchain/sdcc-4.0.0-dflt.in
-include ../stm8-apps.mk
