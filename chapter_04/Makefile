OS := $(shell uname)

TARGETS += stat
TARGETS += getugid
TARGETS += access
TARGETS += link unlink
TARGETS += atime
TARGETS += readdir

ifeq (${OS}, Linux)
CFLAGS_getugid := -D_HAS_GETRESUID # do NOT remove the space at the end!
endif

all: $(TARGETS)

% : %.c
	cc $(CFLAGS_$*)-Wall -O2 $(CFLAGS) -o $* $^

clean:
	rm -rf $(TARGETS)
