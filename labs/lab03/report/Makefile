all: report.pdf report.docx

report.pdf: report.md template.tex
	pandoc report.md -o report.pdf --template=template.tex --pdf-engine=xelatex

report.docx: report.md
	pandoc report.md -o report.docx

clean:
	rm -f report.pdf report.docx

.PHONY: all clean
