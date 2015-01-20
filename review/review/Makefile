
pdf: review.tex library.bib  
	pdflatex --enable-write18 review.tex
	bibtex review
	pdflatex --enable-write18 review.tex
	pdflatex --enable-write18 review.tex

clear:
	rm -rf review.out review.log review.aux review.pdf review.toc review.bbl review.blg
