# Makefile for creation of PDF, html, and Markdown
# from jupyter notebooks. Will convert all .ipynb
# files in a directory.
# Version: tis 22 sep 2020 16:49:37
# Sign: J. Nylander

nbs = $(wildcard *.ipynb)

pdfs = $(nbs:%.ipynb=%.pdf)

mds = $(nbs:%.ipynb=%.md)

htms = $(nbs:%.ipynb=%.html)

slds = $(nbs:%.ipynb=%.slides.html)

.PHONY: all pdf markdown html slides

pdf: $(pdfs)

markdown: $(mds)

html: $(htms)

slides: $(slds)

all: $(pdfs) $(mds) $(htms) $(slds)

%.pdf: %.ipynb
	jupyter-nbconvert --to pdf $<

%.md: %.ipynb
	jupyter-nbconvert --to markdown $<

%.html: %.ipynb
	jupyter-nbconvert --to html $<

%.slides.html: %.ipynb
	jupyter-nbconvert --to slides $<

