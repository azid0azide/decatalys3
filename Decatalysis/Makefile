TeXSRC := ./main.tex
AuxSRC := $(TeXSRC:.tex=.aux)

.PHONY: all clean

all: target

target: $(TeXSRC) $(AuxSRC)
	biblatex $(AuxSRC) && pdflatex $(TeXSRC) && pdflatex $(TeXSRC)

$(AuxSRC): ./main.tex
	pdflatex $(TeXSRC)

clean:
	rm -f target
