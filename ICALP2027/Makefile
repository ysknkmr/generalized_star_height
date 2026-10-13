.PHONY: all clean distclean check arxiv

all:
	latexmk -norc -pdf -interaction=nonstopmode -halt-on-error main.tex

check: all
	@test -s main.pdf
	@if grep -nE "LaTeX (Font )?Warning|Package .*Warning|pdfTeX warning|Overfull|Underfull|undefined|Undefined|Rerun|multiply defined" main.log main.blg main.diagnose | grep -vE "main\.diagnose:[0-9]+:0 undefined knowledge\(s\)\.|Package: rerunfilecheck|Font shape .*U/stmry|Some font shapes were not available|Size substitutions with differences|Underfull .vbox .badness [0-9]*. has occurred while .output is active"; then \
		echo "Build diagnostics above require attention."; \
		exit 1; \
	fi

# Source archive for arXiv (needs main.bbl from a previous build).
arxiv: all
	rm -rf arxiv arxiv.tar.gz
	mkdir -p arxiv
	cp -r main.tex main.bbl abstract.tex header kl sec fig lipics-v2021.cls cc-by.pdf lipics-logo-bw.pdf orcid.pdf arxiv/
	cd arxiv && tar czf ../arxiv.tar.gz .

clean:
	latexmk -norc -c main.tex
	$(RM) main.bbl main.kaux main.diagnose main.vtc main.synctex.gz

distclean: clean
	$(RM) main.pdf
	$(RM) -r arxiv arxiv.tar.gz
