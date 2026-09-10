# CV source. Build here, then publish into the site's pdfs/ folder.
#
#   make            build cv.pdf
#   make publish    build and copy it to ../pdfs/cv.pdf (what the site serves)
#   make clean      remove LaTeX intermediates

cv.pdf: cv.tex res.cls
	pdflatex -interaction=nonstopmode -halt-on-error cv.tex
	pdflatex -interaction=nonstopmode -halt-on-error cv.tex

.PHONY: publish clean
publish: cv.pdf
	cp cv.pdf ../pdfs/cv.pdf
	@echo "Published to pdfs/cv.pdf"

clean:
	rm -f cv.aux cv.log cv.out
