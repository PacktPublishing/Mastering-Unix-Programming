OS := $(shell uname)

TARGETS += buftype
TARGETS += fwide
TARGETS += reopen
TARGETS += fstatus ungetc binio
TARGETS += psprintf scanf
TARGETS += fgetc fgets
TARGETS += fmemopen open_memstream

ifeq (${OS}, Linux)
CFLAGS_getugid := -D_HAS_GETRESUID # do NOT remove the space at the end!
endif

all: $(TARGETS)

% : %.c
	cc $(CFLAGS_$*)-Wall -O2 $(CFLAGS) -o $* $^

clean:
	rm -rf $(TARGETS)
