The source code for my resume. I've come to prefer typesetting in LaTex to word processors, especially when bouncing between ubuntu and mac workstations. I adaped the format and style from https://github.com/sb2nov/resume. The bibliography with publications is my own. 

Git is great for making edits to a resume. As a repo, the resume's evolution and history is preserved. Further, in github, I shouldn't have to worry too much about loosing or constantly backing up my resume.


### Usage

pdflatex <name.tex>

If updating or re-biulding the bibliography with bibtex:

latex <name>

bibtex <name> Regenerates *.bib file

latex <name>  Regenerates *.aux and dependencies for bibliography 

pdflatex <name>


### Notes 

Updating Ubuntu to 2022 Jammy broke latex with a tex-common error. Uninstalling and re-installing
texlive-latex-full seems to have done the trick.

sudo dpkg --force-all --purge texlive-latex-base-doc
sudo apt-get remove --purge tex-common texlive-*
rm -rf /etc/texf/
sudo apt-get autoremove

sudo apt-get install tex-common
sudo apt-get install texlive-latex-full (took a long time, completed okay)

