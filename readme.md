# Creating Ground Truth

This repository contains pipelines for creating ground truth, which we'll be using with passim and ACDC.

Pipeline steps:

1. Retrieve texts from sefaria.org
2. Prepare texts for use with passim
   - Analyze json file structure and process each file according to its particular structure. The code can adapt to different structures : books or corpuses of books, with simple sequences of chapters and verses, or more complex structures (nodes).
   - Clean up texts (html tags, unicodes, numbers...). Tools are provided to help you identify the elements to clean up.
   - Create an index from the structured json files. The index will contain the start and end character position of each text chunk in the book.
   - Concatenate the lines of each text. Thanks to the index, it will always be possible to identify the references of a text fragment from the concatenated text.

Note: the most elaborate pipelines are those of Talmuds, and are to be preferred if you want to evolve your code.