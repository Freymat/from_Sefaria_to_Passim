# Creating Ground Truth

This repository contains a pipeline for creating ground truth, which we'll be using with passim and ACDC.

Pipeline steps:

1. Retrieve texts from sefaria.org
2. Prepare texts for use with passim
   - Analyze json file structure and process each file according to its particular structure.
   - Clean up texts (html tags, unicodes, numbers...)
   - Create an index from the structured json files. The index will contain the start and end character position of each text chunk in the book.
   - Concatenate the lines of each text. Thanks to the index, it will always be possible to identify the references of a text fragment from the concatenated text.