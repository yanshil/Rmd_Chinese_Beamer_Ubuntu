# Knit Chinese Rmd file in Ubuntu

Ubuntu上的中文 Rmarkdown 解决方案 -- 以 Slides 为例

## Install texlive in Ubuntu

The `ctex` package is needed for knitting chinese Rmd file


	sudo apt-get install texlive-full

## Set up yaml in Rmd file and create `header.tex`

	---
	title: "Ubuntu上的中文 Rmarkdown 解决方案 -- 以 Slides 为例"
	author: "Yanshi Luo"
	output:
	  beamer_presentation: 
		pandoc_args: "--latex-engine=xelatex"
		includes:
		  in_header: header.tex
		keep_tex: yes
	---

## The `header.tex`

	\usepackage{ctex}