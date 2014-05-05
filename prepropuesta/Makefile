TARGET=prepropuesta
pdf: $(TARGET).tex ref
	@echo "  ******************** Making PDF **************************************  "
	pdflatex $(TARGET).tex
ref: $(TARGET).tex bib
	@echo "  ******************** Making References *******************************  "
	pdflatex $(TARGET).tex
bib: $(TARGET).aux
	@echo "  ******************** Making BBL-file and BLG-file ********************  "
	bibtex $(TARGET).aux
$(TARGET).aux: refsprop.bib $(TARGET).tex
	@echo "  ******************** Making AUX-file *********************************  "
	pdflatex $(TARGET).tex
clear:
	rm -f $(TARGET).aux $(TARGET).log $(TARGET).bbl $(TARGET).blg $(TARGET).out
