all: build/paris22.pdf

texoptions = \
	     --lualatex \
	     --interaction=nonstopmode \
	     --halt-on-error \
	     --output-directory=build

build/paris22.pdf: FORCE | build
	latexmk $(texoptions) paris22.tex

preview: FORCE | build
	latexmk $(texoptions) -pvc paris22.tex

FORCE:

build:
	mkdir -p build

clean:
	rm -r build
