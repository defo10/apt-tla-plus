REPORT_FILE=report

PANDOC=pandoc

PANDOC_OPTIONS=--from markdown --template ./eisvogel.tex --listings --bibliography=bibliography.bib --biblatex

OUTPUT_FOLDER=output

PDFLATEX=pdflatex -output-directory=$(OUTPUT_FOLDER)

pdf : tex .output-folder
	$(PDFLATEX) $(REPORT_FILE).tex

.output-folder:
	mkdir -p $(OUTPUT_FOLDER) 

tex : 
	$(PANDOC) $(REPORT_FILE).md -o $(REPORT_FILE).tex $(PANDOC_OPTIONS)

full-pdf : tex .output-folder
	$(PDFLATEX) $(REPORT_FILE).tex
	biber $(OUTPUT_FOLDER)/$(REPORT_FILE)
	$(PDFLATEX) $(REPORT_FILE).tex
	$(PDFLATEX) $(REPORT_FILE).tex

all : tex pdf full_pdf .output-folder
.PHONY: all
