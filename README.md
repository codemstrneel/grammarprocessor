# Grammar Processor

==========================================

This is a library for processing grammars in [GRXML] (https://www.w3.org/TR/speech-grammar) format and [JJSGF](https://support.voicegain.ai/hc/en-us/articles/360048936511-JJSGF-Grammars) format, creating railroad diagrams representing all possible outcomes of the grammar.

Diagrams
--------
Each of these files, grxmlprocessor.py and jjsgfprocessor.py, contain their own unique ways of parsing the different styles of grammar.

grxmlprocessor.py uses parse_grxml_from_string to use xml libraries in python to get the code into a readable format. Then, extract_rules takes the root and ns values parse_grxml_from_string returns and puts it into a common dictionary format that createDiagram can process - this dictionary format is common to both proessors. createDiagram takes in a dictionary of rules in string format and parses them to generate the railroad diagram in SVG format.

jjsgfprocessor.py 
