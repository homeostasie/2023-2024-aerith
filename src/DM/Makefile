# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/dm
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 4x3-triangles-semblables/*.ipe 4x5-pythagore/*.ipe 4x8-pythagore-2/*.ipe 4xbb/*.ipe 4x10-trigonometrie/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x3-triangles-semblables/%.pdf: 4x3-triangles-semblables/%.ipe
	ipetoipe -pdf $<

4x5-pythagore/%.pdf: 4x5-pythagore/%.ipe
	ipetoipe -pdf $<

4x8-pythagore-2/%.pdf: 4x8-pythagore-2/%.ipe
	ipetoipe -pdf $<

4x10-trigonometrie/%.pdf: 4x10-trigonometrie/%.ipe
	ipetoipe -pdf $<


1dm:
	pdflatex dm1-appolo.tex
	pdflatex dm1-appolo.tex
	mv dm1-appolo.pdf '$(PDFDIR)'/dm1-appolo.pdf

2dm:
	pdflatex dm2-murphy.tex
	pdflatex dm2-murphy.tex
	mv dm2-murphy.pdf '$(PDFDIR)'/dm2-murphy.pdf

3dm:
	pdflatex dm3-rand.tex
	pdflatex dm3-rand.tex
	mv dm3-rand.pdf '$(PDFDIR)'/dm3-rand.pdf	
# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
