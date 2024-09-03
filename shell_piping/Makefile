all: shell_piping.pdf shell_piping.handout.pdf

shell_piping.pdf: shell_piping.tex

pacakge.handout.pdf: shell_piping.handout.tex

shell_piping.handout.tex: shell_piping.tex
	sed '1s/\documentclass{beamer}/\documentclass[handout]{beamer}/' $^ > $@

%.pdf: %.tex
	latexmk -pdf -shell-escape -use-make $^

clean:
	latexmk -CA
	rm -f shell_piping.handout.tex *.snm *.nav *.vrb *.pyg
	rm -rf _minted-*/ svg-inkscape/

.PHONY: all clean
