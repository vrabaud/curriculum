all:
	# clean, just in case
	rm -f *aux && rm -f *blg && rm -f *bbl && rm -f *log
	# prepare the French CV
	perl -p -i -e 's/selectlanguage{english}/selectlanguage{french}/g' ./rabaud_vincent_cv.tex
	# compile the French CV
	pdflatex rabaud_vincent_cv.tex
	mv rabaud_vincent_cv.pdf rabaud_vincent_cvFR.pdf
	# clean
	rm -f *aux && rm -f *blg && rm -f *bbl && rm -f *log
	# revert back and clean
	perl -p -i -e 's/selectlanguage{french}/selectlanguage{english}/g' ./rabaud_vincent_cv.tex
	# process the English CV
	pdflatex rabaud_vincent_cv.tex
	# clean
	rm -f *aux && rm -f *blg && rm -f *bbl && rm -f *log
