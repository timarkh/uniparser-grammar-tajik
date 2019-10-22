uniparser-grammar-tajik
=======================

This is a formalized description of standard Tajik morphology. The description is carried out in the UniParser format and involves a description of the inflection (paradigms.txt) and a grammatical dictionary (lexemes.txt). The dictionary contains descriptions of individual lexemes, each of which is accompanied by information about its stem, its part-of-speech tag and some other grammatical information, its inflectional type (paradigm), and Russian translation.

## How to use

This description can be used for morphological analysis of Tajik texts in the following ways:

1. The ``wordlists`` directory contains annotated frequency list of tokens based on the Tajik corpus (more than 30 million words of contemporary texts), which contains 416,000 unique tokens (case-insensitive). The simplest solution is to use this analyzed wordlist for analyzing your texts.

2. The ``analyzer`` directory contains the UniParser set of scripts together with all necessary language files. You can use it to analyze your own frequency word list. Your have to name your list "wordlist.csv" and put it to that directory. Each line should contain one token and its frequency, tab-delimited. Then you have to out your ``lexemes.txt`` and ``paradigms.txt`` files to ``analyzer``. When you run ``analyzer/UniParser/analyze.py``, the analyzer will produce two files, one with analyzed tokens, the other with unanalyzed ones. (You can also use other file names and separators with command line options, see the code of analyze.py.) This way, you will not be restricted by our word list, but the analyzer works pretty slowly (500-1000 tokens per second).

3. Finally, you are free to convert/adapt the description to whatever kind of morphological analysis you prefer to use.

