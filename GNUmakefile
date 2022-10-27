#   ************    Bibliography    ***********************************
#
#   Organisation:   Chipforge
#                   Germany / European Union
#
#   Profile:        Chipforge focus on fine System-on-Chip Cores in
#                   Verilog HDL Code which are easy understandable and
#                   adjustable. For further information see
#                           www.chipforge.org
#                   there are projects from small cores up to PCBs, too.
#
#   File:           Bibliography/GNUmakefile
#
#   Purpose:        Makefile for Document Generation
#
#   ************    GNU Make 3.80 Source Code       ****************

#   project name

PROJECT =       Bibliography

#   project tools

LATEX ?= pdflatex
BIBER ?= biber

#   ----------------------------------------------------------------
#               DEFAULT TARGETS
#   ----------------------------------------------------------------

#   display help screen if no target is specified

.PHONY: help
help:
	#   ----------------------------------------------------------
	#       available targets:
	#   ----------------------------------------------------------
	#
	#   help        - print this help screen
	#   clean       - clean up all intermediate files
	#
	#   list        - generate complete list
	#

#   'clean' current directory

.PHONY: clean
clean:
	-$(RM) *.aux *.bbl *.bcf *.blg *.log *.xml

.PHONY: list
list:
	$(LATEX) $(PROJECT).tex
	$(BIBER) $(PROJECT)
	$(BIBER) $(PROJECT)
	$(LATEX) $(PROJECT).tex

