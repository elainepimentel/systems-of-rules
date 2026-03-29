EXPORT  = systems-of-rules
ROOT    = main
MACROS  = phead.tex
SECTS   = 2-systems.tex KTbox.tex bipoles.tex ecumenical.tex hypersequents.tex intro-focusing.tex polarization.tex
VIEWER  = okular
DATE    = 19-December-2024

$(ROOT).pdf: $(ROOT).tex $(MACROS) $(SECTS)
	pdflatex $(ROOT)
	bibtex $(ROOT)

bib:
	bibtex $(ROOT)

force:
	pdflatex $(ROOT)
	bibtex $(ROOT) 


publish: $(ROOT).pdf
	cp $(ROOT).pdf ~/www/papers/$(EXPORT).pdf

dropbox: $(ROOT).pdf
	cp $(ROOT).pdf ~/Dropbox/Sync/Drafts/$(EXPORT)-draft.pdf

spawn: $(ROOT).pdf
	cp $(ROOT).pdf spawn.pdf
	$(VIEWER) spawn.pdf &

cleanaux:
	rm -f *.aux
clean:
	rm -f *.bbl *.blg *.idx *.ind *.ilg *.toc *.rel *.out *.brf *.log

show: $(ROOT).pdf
	$(VIEWER) $(ROOT).pdf &

backup:
	tar cvzf ~/Dropbox/Writing/Book/Drafts/$(EXPORT)-$(DATE).tgz *.*

select: $(ROOT).pdf
	pdftk $(ROOT).pdf cat 8-65 output select.pdf

showselect:
	$(VIEWER) select.pdf

dup: $(ROOT).pdf
	cp $(ROOT).pdf dup.pdf

showdup: 
	$(VIEWER) dup.pdf &
