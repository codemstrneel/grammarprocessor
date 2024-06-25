# Grammar Processor

==========================================

This is a library for processing grammars in [GRXML] (https://www.w3.org/TR/speech-grammar) format and [JJSGF](https://support.voicegain.ai/hc/en-us/articles/360048936511-JJSGF-Grammars) format, creating railroad diagrams representing all possible outcomes of the grammar.

Diagrams
--------
Each of these files, grxmlprocessor.py and jjsgfprocessor.py, contain their own unique ways of parsing the different styles of grammar.

grxmlprocessor.py uses the following main methods:

parse_grxml_from_string returns root and ns, where root is the grammar in readable xml format, and ns is the set of rules for the XML.

extract_rules takes the root and ns values parse_grxml_from_string returns and puts it into a common dictionary format that createDiagram can process - the rule name is the key and maps to a string for the rule, with tags put between !! delimeters

createDiagram takes in a dictionary of rules in string format and parses them to generate the railroad diagram in SVG format


jjsgfprocessor.py

_________

extract_rules returns a dictionary with tags between two !! tags on each side and the rest of the rule in original string fore, similar to the same function in the grxmlprocessor.py library. Then, createDiagram is analogous and creates svg files.
