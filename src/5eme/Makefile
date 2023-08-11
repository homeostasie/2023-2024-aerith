# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/5eme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 5x2-geometrie-quadrillage/*.ipe 5x4-symetrie/*.ipe 5x5-triangles/*.ipe 4xbb/*.ipe 5x8-aires/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

5x2-geometrie-quadrillage/%.pdf: 5x2-geometrie-quadrillage/%.ipe
	ipetoipe -pdf $<

5x4-symetrie/%.pdf: 5x4-symetrie/%.ipe
	ipetoipe -pdf $<

5x5-triangles/%.pdf: 5x5-triangles/%.ipe
	ipetoipe -pdf $<

5x8-aires/%.pdf: 5x8-aires/%.ipe
	ipetoipe -pdf $<


# Chapitre 1

1cours:
	pdflatex 5x1-calcul-numerique/5x1-cours.tex
	pdflatex 5x1-calcul-numerique/5x1-cours.tex
	mv 5x1-cours.pdf '$(PDFDIR)'/5x1-cours.pdf

1ie:
	pdflatex 5x1-calcul-numerique/5x1-ie.tex
	pdflatex 5x1-calcul-numerique/5x1-ie.tex
	mv 5x1-ie.pdf '$(PDFDIR)'/5x1-ie.pdf

2cours:
	pdflatex 5x2-probabilite/5x2-cours.tex
	pdflatex 5x2-probabilite/5x2-cours.tex
	mv 5x2-cours.pdf '$(PDFDIR)'/5x2-cours.pdf

2ie:
	pdflatex 5x2-probabilite/5x2-ie.tex
	pdflatex 5x2-probabilite/5x2-ie.tex
	mv 5x2-ie.pdf '$(PDFDIR)'/5x2-ie.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
