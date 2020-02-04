TARGETS += simple
TARGETS += unbuffered buffered
TARGETS += getpid

all: $(TARGETS)

% : %.c
	cc -Wall -O2 -o $* $^

clean:
	rm -rf $(TARGETS)
