TARGETS += dup2
TARGETS += flockr flockw

all: $(TARGETS)

% : %.c
	cc -Wall -O2 -o $* $^

clean:
	rm -rf $(TARGETS)
