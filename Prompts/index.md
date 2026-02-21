---
title: Prompts
description: Standardised prompts for use in generating Architectural Artefacts 
children :
---
#   Architectural Prompts

This directory contains a set of standardised prompts for use in generating Architectural Artefacts. 
Each section header should reflect the purpose of the prompt that can then be referenced either as a individual instruction to CoPilot or as a Process Step within in a Process definition. 

##  Generate Communication Model

##  Generate Business Entity Software Component

##  Generate Files conversion script

    Create a script to convert Microsoft Word ".doc" files into Markdown files, extracting diagrams into PNG files and keeping a record of converted documents in an index file.
    The script should
    .  not process any other kind of file found in the input directories
    .  keep a record of each converted document in the ConvertedDocs.index.md recording Input File, Output File and Date converted
    .  ignore any input file that is already registered in ConvertedDocs.index.md and successfully converted.
    .  not not copy any files that fail conversion into the ConvertedDocs directory and not record them in the ConvertedDocs.index.md file.
    .  generated markdown files should be placed in the ConvertedDocs directory with the same name as the input file but with a .md extension withg filenames in UpperCamelCase with no spaces.
    .  generated diagrams should be put into the diagram sub-directory of the ConvertedDocs directory and referenced in the generated Markdown file.
    Test the script using the jcm_articles.doc file in the DocumentsToConvert directory as a test case.

##	Process File To Convert

	Convert all Miscroft Word ".doc" files in DocumentsToConvert directory and any of its sub-directories into Markdown files and place the output in the ConvertedDocs directory. 
    Do not convert any other kind of file found in the inpur directories.
	Preserve sections and text verbatim and extract diagrams into PNG files.
	Include references to generate digrams in relevant place within the generated Markdown. 
	Keep a record of each converted document in the ConvertedDocs.index.md recording Input File, Output File and Date converted. 
	Ignore any input file that is already registered in ConvertedDocs.index.md and successfully converted.
