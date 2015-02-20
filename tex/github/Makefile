DOCUMENT = Anleitung_GitHub
OBJ_DIR = ./obj

.PHONY: all doc bib clean

all: doc clean

doc:
	pdflatex $(DOCUMENT).tex
	for i in {1..5}; do \
		pdflatex $(DOCUMENT).tex; \
	done
	mv $(DOCUMENT).pdf $(OBJ_DIR)/.

bib:
	bibtex $(DOCUMENT).aux

clean:
	rm -f *.aux
	rm -f *.bbl
	rm -f *.blg
	rm -f *.log
	rm -f *.toc
