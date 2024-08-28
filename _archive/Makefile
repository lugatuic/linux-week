TARGETS = code.pdf install_ubuntu.pdf linux_uic.pdf remote_access.pdf shell.pdf

all: $(TARGETS)

clean:
	git clean -fx

%.pdf: %.tex
	pdflatex $<

.PHONY: all clean

