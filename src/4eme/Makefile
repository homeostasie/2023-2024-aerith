# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/4eme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 4x3-triangles-semblables/*.ipe 4x7-pythagore-1/*.ipe 4x8-pythagore-2/*.ipe 4xbb/*.ipe 4x10-trigonometrie/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x3-triangles-semblables/%.pdf: 4x3-triangles-semblables/%.ipe
	ipetoipe -pdf $<

4x7-pythagore/%.pdf: 4x5-pythagore/%.ipe
	ipetoipe -pdf $<

4x8-pythagore-2/%.pdf: 4x8-pythagore-2/%.ipe
	ipetoipe -pdf $<

4x10-trigonometrie/%.pdf: 4x10-trigonometrie/%.ipe
	ipetoipe -pdf $<


1ie:
	pdflatex 4x1-nombres-relatifs/4x1-ie.tex
	pdflatex 4x1-nombres-relatifs/4x1-ie.tex
	mv 4x1-ie.pdf '$(PDFDIR)'/4x1-ie-relatifs.pdf


2data:
	pdflatex 4x2-graphiques/4x2-data-perso.tex
	pdflatex 4x2-graphiques/4x2-data-perso.tex
	mv 4x2-data-perso.pdf '$(PDFDIR)'/4x2-data-perso.pdf
	pdflatex 4x2-graphiques/4x2-data-temperature.tex
	pdflatex 4x2-graphiques/4x2-data-temperature.tex
	mv 4x2-data-temperature.pdf '$(PDFDIR)'/4x2-data-temperature.pdf

3ie:
	pdflatex 4x3-proportionnalite/4x3-ie.tex
	pdflatex 4x3-proportionnalite/4x3-ie.tex
	mv 4x3-ie.pdf '$(PDFDIR)'/4x3-ie-prop.pdf

6ie:
	pdflatex 4x6-notation-scientifique/4x6-ie.tex
	pdflatex 4x6-notation-scientifique/4x6-ie.tex
	mv 4x6-ie.pdf '$(PDFDIR)'/4x6-ie-sci.pdf	


7dm:
	pdflatex 4x7-pythagore-1/4x7-dm.tex
	pdflatex 4x7-pythagore-1/4x7-dm.tex
	mv 4x7-dm.pdf '$(PDFDIR)'/4x7-dm-pytha.pdf	

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
