
.PHONY: update sitemap

TARGET = Semesterarbeit.pdf

FILES = \
	$(wildcard chapters/*.tex) \
	$(wildcard figures/*) \


all: $(TARGET)

%.pdf: %.tex $(FILES)
	pdflatex $<
	makeindex -s $(*F).ist -t $(*F).glg -o $(*F).gls $(*F).glo
	bibtex $(*F).aux
	pdflatex $<
	pdflatex $<
