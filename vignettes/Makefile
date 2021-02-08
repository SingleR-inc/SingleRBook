all: compiled

compiled: 
	cd book && "${R_HOME}/bin/R" -e "bookdown::render_book('index.Rmd')"
	mv book/docs TEMPORARY
	rm -rf book/ && mkdir book/ && mv TEMPORARY book/docs
	mkdir -p ../inst/doc && cp -r book/docs ../inst/doc/book

