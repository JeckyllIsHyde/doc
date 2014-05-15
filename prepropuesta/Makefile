TARGET=prepropuesta.article
BEAMERTARGET=prepropuesta.beamer
all: article.pdf beamer.pdf
	@echo "  ******************** Making ALL **************************************  "
article.pdf: $(TARGET).tex article.ref
	@echo "  ******************** Making PDF **************************************  "
	pdflatex $(TARGET).tex
article.ref: $(TARGET).tex article.bib
	@echo "  ******************** Making References *******************************  "
	pdflatex $(TARGET).tex
article.bib: $(TARGET).aux
	@echo "  ******************** Making BBL-file and BLG-file ********************  "
	bibtex $(TARGET).aux
$(TARGET).aux: refsprop.bib $(TARGET).tex
	@echo "  ******************** Making AUX-file *********************************  "
	pdflatex $(TARGET).tex
beamer.pdf: $(BEAMERTARGET).tex beamer.ref
	@echo "  ******************** Making PDF **************************************  "
	pdflatex $(BEAMERTARGET).tex
beamer.ref: $(BEAMERTARGET).tex beamer.bib
	@echo "  ******************** Making References *******************************  "
	pdflatex $(BEAMERTARGET).tex
beamer.bib: $(BEAMERTARGET).aux
	@echo "  ******************** Making BBL-file and BLG-file ********************  "
	bibtex $(BEAMERTARGET).aux
$(BEAMERTARGET).aux: refsprop.bib $(BEAMERTARGET).tex
	@echo "  ******************** Making AUX-file *********************************  "
	pdflatex $(BEAMERTARGET).tex
clear:
	@echo "  ******************** Removing tmp-file *******************************  "
	rm -f *.aux $(TARGET).log $(TARGET).bbl $(TARGET).blg $(TARGET).out
	rm -f *.tex.aux $(BEAMERTARGET).log $(BEAMERTARGET).bbl $(BEAMERTARGET).blg $(BEAMERTARGET).out $(BEAMERTARGET).nav $(BEAMERTARGET).snm $(BEAMERTARGET).toc
clear.bin:
	@echo "  ******************** Removing pdf-files ******************************  "
	rm -f $(TARGET).pdf $(BEAMERTARGET).pdf
