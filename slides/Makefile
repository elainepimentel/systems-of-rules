DOC=ps24
EXTRAS=macros.tex
EXTERNAL=ps2024talk
VIEWER=okular

$(DOC).pdf: $(DOC).tex $(EXTRAS)
	pdflatex $(DOC)

show: $(DOC).pdf
	$(VIEWER) $(DOC).pdf &

force: 
	pdflatex $(DOC)

dropbox: $(DOC).pdf
	cp $(DOC).pdf ~/Dropbox/Sync/Drafts/$(EXTERNAL).pdf

publish: $(DOC).pdf
	cp $(DOC).pdf ~/www/papers/$(EXTERNAL).pdf

usb: $(DOC).pdf
	cp $(DOC).pdf /media/dale/Lexar/$(EXTERNAL).pdf

clean:
	rm $(DOC).aux $(DOC).log $(DOC).nav $(DOC).out $(DOC).snm $(DOC).toc

backup: $(DOC).pdf
#	tar cvf     /media/dale/Kat/linearity16-backup.tar *.*
#	cp $(DOC).pdf /media/dale/Kat/linearity16.pdf
#	tar cvf "/media/USB MEMORY/linearity16-backup.tar" *.*
#	cp $(DOC).pdf "/media/USB MEMORY/linearity16.pdf"
