# Dossiers
CODE := $(shell pwd)
PDFDIR = ../../pdf/bb
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)


bb:
	latex bb-2024.tex
	dvips bb-2024.dvi
	ps2pdf bb-2024.ps
	mv bb-2024.pdf '$(PDFDIR)'/bb-2024.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~
