.PHONY: all clean

# (^_^) - spkirich:
# To build all lectures at once.

all: lec-01.pdf lec-02.pdf

# (^_^) - spkirich:
# To build a specific lecture.

lec-%.pdf: lec-%.md
	pandoc --standalone -V fontenc=T2A $< -o $@

# (^_^) - spkirich:
# To purge all built lectures.

clean:
	$(RM) *.pdf
