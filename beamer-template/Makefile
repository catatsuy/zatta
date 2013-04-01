#/usr/bin/zsh

PANDOC = pandoc.my
OPTS_B = -t beamer --include-in-header header_slide.tex
OPTS_A = -V fontsize=12pt -V theme=GrayGradient -s -o

SRC = presen.md
OUTPUT = $(SRC:%.md=%.tex)
OUTPUTDVI = $(SRC:%.md=%.dvi)

all:
	$(PANDOC) $(OPTS_B) $(SRC) $(OPTS_A) $(OUTPUT)
	platex $(OUTPUT)
	dvipdfmx $(OUTPUTDVI)