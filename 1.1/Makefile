BOOK=taocp
CHAPTER=01
SECTION=1.1
SHOW=evince
BUILD=pdflatex
INCLUDEDIR=.
DEPS=$(INCLUDEDIR)/taocp.sty $(INCLUDEDIR)/MathematicsWorkbook.sty

BOOKCH=$(BOOK)_ch$(CHAPTER)
BOOKSEC=$(BOOK)_$(SECTION)
TEXFILE=$(BOOKSEC).tex
PDFFILE=$(BOOKSEC).pdf

all: show_$(BOOKCH)

show_$(BOOKCH): $(PDFFILE)
	$(SHOW) $(PDFFILE)

$(PDFFILE): $(TEXFILE) $(DEPS)
	$(BUILD) $(TEXFILE)

clean:
	rm -f *.bak *.aux *.log *.pdf *.sav *.ans *.inx *.ref
