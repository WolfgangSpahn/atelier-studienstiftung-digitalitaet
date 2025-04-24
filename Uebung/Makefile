
help:
	@grep -h "##" $(MAKEFILE_LIST) | grep -v fgrep | sed -e "s/\\$$//" | sed -e "s/##//"

# Define a variable for all .md files
MD_FILES := $(wildcard *.md)

PDF_FILES := $(MD_FILES:.md=.pdf)

all:    ## Default target
all: $(PDF_FILES)

# Pattern rule for converting .md to .pdf
%.pdf: %.md 
	pandoc $< -o $@ 