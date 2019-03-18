slides.pdf: slides.md
	pandoc -t beamer -s slides.md -o slides.pdf -V classoption=t --slide-level=2

slides.html: slides.md
	pandoc -t slidy -s slides.md -o slides.html --slide-level=2

slides: slides.html slides.pdf

clean:
	rm -f slides.html slides.pdf
