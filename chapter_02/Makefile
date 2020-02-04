OS := $(shell uname)

TARGETS += open
TARGETS += read
TARGETS += lseek
TARGETS += iospeed
TARGETS += async sync
ifneq (${OS}, FreeBSD)
TARGETS += dsync
endif

OBJECTS += wrappers.o

all: $(TARGETS)

% : %.c
	cc -Wall -O2 -o $* $^

clean:
	rm -rf $(TARGETS) $(OBJECTS)

read: wrappers.o
async dsync sync: wrappers.o
