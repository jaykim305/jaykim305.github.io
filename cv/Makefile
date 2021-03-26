.PHONY : clean

title = Jaehong_Kim_CV
src = $(title).tex
bibs = $(title).bib
latex = pdflatex
htlatex = htlatex

all: $(addprefix $(title).,pdf html)

$(title).pdf: $(src)
	$(latex) $(src)
ifneq ($(wildcard $(bibs)), )
	bibtex $(title)
	$(latex) $(src)
	$(latex) $(src)
endif

$(title).html: $(src)
	$(htlatex) $(src)
ifneq ($(wildcard $(bibs)), )
	bibtex $(title)
	$(htlatex) $(src)
	$(htlatex) $(src)
endif

clean:
	rm -rf $(addprefix $(title).,log bbl blg dvi pdf ps aux \
								 4ct 4tc css html idv lg tmp log xref)
	rm -rf texput.log
	rm -rf *~
