all: what_linux_and_install.pdf what_linux_and_install.handout.pdf

what_linux_and_install.pdf: what_linux_and_install.tex

pacakge.handout.pdf: what_linux_and_install.handout.tex

what_linux_and_install.handout.tex: what_linux_and_install.tex
	sed '1s/\documentclass{beamer}/\documentclass[handout]{beamer}/' $^ > $@

%.pdf: %.tex
	latexmk -pdf -shell-escape -use-make $^

clean:
	latexmk -CA
	rm -f what_linux_and_install.handout.tex *.snm *.nav *.vrb *.pyg
	rm -rf _minted-*/ svg-inkscape/

.PHONY: all clean
