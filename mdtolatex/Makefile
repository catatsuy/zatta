PANDOC = pandoc.my
OPTS_B = -f markdown -t beamer --include-in-header header_slide.tex
OPTS_A = -V fontsize=14pt -V theme=GrayGradient -s -o

SRC = presen.tex
OUTPUT = output.tex#$(SRC:%.md=%.tex)
OUTPUTDVI = output.dvi#$(SRC:%.md=%.dvi)

all:
	$(PANDOC) $(OPTS_B) $(SRC) $(OPTS_A) $(OUTPUT)
	platex $(OUTPUT)
	dvipdfmx $(OUTPUTDVI)