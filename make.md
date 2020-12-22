# Make Cheatsheet

```makefile
CC := gcc
CFLAGS := -g -Wall
EXEC := $(patsubst %.c,%,$(wildcard *.c))

all: $(EXEC)

$(EXEC): %: %.c
	$(CC) $(CFLAGS) $< -o $@
```

## Reference
* [Static Pattern Rules](https://www.gnu.org/software/make/manual/html_node/Static-Usage.html#Static-Usage)