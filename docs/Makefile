# Minimal Sphinx Makefile

SPHINXOPTS    = "-f -silent"
SPHINXBUILD   = sphinx-build
SOURCEDIR     = source
BUILDDIR      = _build

.PHONY: help clean html pdf

all: html pdf

help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS)

clean:
	rm -rf $(BUILDDIR)

html:
	@$(SPHINXBUILD) -M html "$(SOURCEDIR)" "$(BUILDDIR)"

serve_html:
	sphinx-autobuild --watch ../generic_demo_docs source _build/html

latexpdf:
	@$(SPHINXBUILD) -M latex "$(SOURCEDIR)" "$(BUILDDIR)" 
	@cd "$(BUILDDIR)/latex" && latexmk -pdf -interaction=nonstopmode -f generic_demo_docs.tex

