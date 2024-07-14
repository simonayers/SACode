CPP=g++
INCDIRS=-IOSLib\: -ISALib\:
OPT=-O0
CPPFLAGS=-Wall -mlibscl $(INCDIRS) $(OPT)
LINKFLAGS=-mlibscl
LINKLIBS=-LOSLib\: -LSALib\:  -lOSLib32 -lSALib

CPPFILES=iconbar.cc logfile.cc sacode.cc
OBJECTS= iconbar.o  logfile.o  sacode.o

BINARY=../!RunImage

all: $(BINARY)

$(BINARY): $(OBJECTS)
	$(CPP) $(LINKFLAGS) -o $@ $^ $(LINKLIBS)
	SetType ^.!RunImage Absolute

%.o:%.cc
	$(CPP) -c $(CPPFLAGS) -o $@ $^

clean:
	IfThere ^.!RunImage Then X Wipe ^.!RunImage ~CFR~V
	X Wipe o.* ~CFR~V
