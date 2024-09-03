all: why_free.pdf why_free.handout.pdf

why_free.pdf: why_free.tex

pacakge.handout.pdf: why_free.handout.tex

why_free.handout.tex: why_free.tex
	sed '1s/\documentclass{beamer}/\documentclass[handout]{beamer}/' $^ > $@

%.pdf: %.tex
	latexmk -pdf -shell-escape -use-make $^

clean:
	latexmk -CA
	rm -f why_free.handout.tex *.snm *.nav *.vrb *.pyg
	rm -rf _minted-*/ svg-inkscape/

.PHONY: all clean
