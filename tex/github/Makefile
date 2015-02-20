DOCUMENT = Anleitung_GitHub
OBJ_DIR = ./obj

.PHONY: all doc latex bib gloss clean

all: latex gloss doc clean

doc:
	pdflatex $(DOCUMENT).tex
	for i in {1..5}; do \
		pdflatex $(DOCUMENT).tex; \
	done
	mv $(DOCUMENT).pdf $(OBJ_DIR)/.

latex:
	pdflatex $(DOCUMENT).tex

bib:
	bibtex $(DOCUMENT).aux

gloss:
	makeglossaries $(DOCUMENT)

clean:
	rm -f *.aux
	rm -f *.bbl
	rm -f *.blg
	rm -f *.log
	rm -f *.toc
	rm -f *.glg
	rm -f *.glo
	rm -f *.gls
	rm -f *.glsdefs
	rm -f *.out
	rm -f *.xdy
