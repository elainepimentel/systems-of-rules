DOC = abstract
AUX = # ../../../Dropbox/Writing/references/master.bib
EXTERNAL = proof-society-2024
VIEWER = okular

$(DOC).pdf: $(DOC).tex $(AUX)
	pdflatex $(DOC).tex
	bibtex $(DOC)
	aux2bib $(DOC).aux > extract.bib

force: 
	pdflatex $(DOC).tex
	bibtex $(DOC)
	aux2bib $(DOC).aux > extract.bib

show: $(DOC).pdf
	$(VIEWER) $(DOC).pdf&

dropbox: $(DOC).pdf
	cp $(DOC).pdf ~/Dropbox/Sync/Drafts/$(EXTERNAL).pdf

publish: $(DOC).pdf
	cp $(DOC).pdf ~/www/papers/$(EXTERNAL).pdf

clean:
	rm *.log *.aux *.bbl *.blg *.out *.toc
