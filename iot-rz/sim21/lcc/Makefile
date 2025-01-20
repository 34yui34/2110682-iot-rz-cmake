# Wedit Makefile for project sim21
SRCDIR=c:\users\prabhas\dropbox\rz-2017\iot-rz\sim21
CFLAGS=-I"c:\lcc\include"  -g2 
CC=$(LCCROOT)\bin\lcc.exe
LINKER=$(LCCROOT)\bin\lcclnk.exe
OBJS=\
	io.obj \
	load.obj \
	mon.obj \
	s21.obj \

LIBS=
EXE=c:\users\prabhas\dropbox\rz-2017\iot-rz\test\sim21.exe

$(EXE):	$(OBJS) Makefile
	$(LINKER)  -subsystem console -o c:\users\prabhas\dropbox\rz-2017\iot-rz\test\sim21.exe $(OBJS) $(LIBS)

# Build io.c
IO_C=\
	$(SRCDIR)\s21.h\

io.obj: $(IO_C) $(SRCDIR)\io.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\io.c

# Build load.c
LOAD_C=\
	$(SRCDIR)\s21.h\

load.obj: $(LOAD_C) $(SRCDIR)\load.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\load.c

# Build mon.c
MON_C=\
	$(SRCDIR)\s21.h\

mon.obj: $(MON_C) $(SRCDIR)\mon.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\mon.c

# Build s21.c
S21_C=\
	$(SRCDIR)\s21.h\

s21.obj: $(S21_C) $(SRCDIR)\s21.c
	$(CC) -c $(CFLAGS) $(SRCDIR)\s21.c

link:
	$(LINKER)  -subsystem console -o c:\users\prabhas\dropbox\rz-2017\iot-rz\test\sim21.exe $(OBJS) $(LIBS)

clean:
	del $(OBJS) sim21.exe
