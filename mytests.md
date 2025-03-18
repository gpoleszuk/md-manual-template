
```
$ sudo apt install pandoc
[sudo] password for username: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  pandoc-data
Suggested packages:
  texlive-xetex texlive-luatex pandoc-citeproc texlive-latex-extra context wkhtmltopdf librsvg2-bin ghc nodejs php python ruby r-base-core libjs-katex citation-style-language-styles
The following NEW packages will be installed:
  pandoc pandoc-data
0 upgraded, 2 newly installed, 0 to remove and 36 not upgraded.
Need to get 26.9 MB of archives.
After this operation, 200 MB of additional disk space will be used.
Do you want to continue? [Y/n] Y
Get:1 http://archive.ubuntu.com/ubuntu noble/universe amd64 pandoc-data all 3.1.3-1 [92.4 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble/universe amd64 pandoc amd64 3.1.3+ds-2 [26.9 MB]
Fetched 26.9 MB in 3s (9,291 kB/s) 
Selecting previously unselected package pandoc-data.
(Reading database ... 257761 files and directories currently installed.)
Preparing to unpack .../pandoc-data_3.1.3-1_all.deb ...
Unpacking pandoc-data (3.1.3-1) ...
Selecting previously unselected package pandoc.
Preparing to unpack .../pandoc_3.1.3+ds-2_amd64.deb ...
Unpacking pandoc (3.1.3+ds-2) ...
Setting up pandoc-data (3.1.3-1) ...
Setting up pandoc (3.1.3+ds-2) ...
Processing triggers for man-db (2.12.0-4build2) ...


$ make pdf
pandoc \
	metadata.yml *.md \
	--output manual.pdf \
	--template tool/template/eisvogel.tex \
	--from markdown \
	--listings \
	--number-sections \
	--table-of-contents \
	--metadata date="`date -u '+%Y-%m-%d'`"
Error producing PDF.
! LaTeX Error: File `adjustbox.sty' not found.

Type X to quit or <RETURN> to proceed,
or enter new name. (Default extension: sty)

Enter file name: 
! Emergency stop.
<read *> 
         
l.102 \usepackage

make: *** [tool/Makefile_include:14: pdf] Error 43
```
