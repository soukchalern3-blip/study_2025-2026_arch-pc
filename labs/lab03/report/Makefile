# Makefile for Lab 3 report (Markdown → PDF/DOCX)
# Author: Пыакео Сукчалын (НКАбд-02-25)

REPORT = report

all: $(REPORT).pdf $(REPORT).docx

$(REPORT).pdf: $(REPORT).md
	pandoc $(REPORT).md \
	--pdf-engine=xelatex \
	-V mainfont="Times New Roman" \
	-V geometry:margin=2.5cm \
	-V fontsize=12pt \
	-V documentclass=article \
	--include-in-header=titlepage.tex \
	-o $(REPORT).pdf

$(REPORT).docx: $(REPORT).md
	pandoc $(REPORT).md -o $(REPORT).docx

clean:
	rm -f $(REPORT).pdf $(REPORT).docx

.PHONY: all clean
