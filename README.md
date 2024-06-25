# Grammar Processor

==========================================

This is a library for processing grammars in [GRXML] (https://www.w3.org/TR/speech-grammar) format and [JJSGF](https://support.voicegain.ai/hc/en-us/articles/360048936511-JJSGF-Grammars) format, creating railroad diagrams representing all possible outcomes of the grammar.

Diagrams
--------
Each of these files, grxmlprocessor.py and jjsgfprocessor.py, contain their own unique ways of parsing the different styles of grammar.


grxmlprocessor.py
----------
Constructing a set of diagram for the rules from a grxml file contains one function call

```python
grxmlToRailroad(zip_code_no_refs.grxml)  
```

will create the folloinwg




grxmlprocessor.py uses the following main methods:

parse_grxml_from_string returns root and ns, where root is the grammar in readable xml format, and ns is the set of rules for the XML.

extract_rules takes the root and ns values parse_grxml_from_string returns and puts it into a common dictionary format that createDiagram can process - the rule name is the key and maps to a string for the rule, with tags put between !! delimeters

createDiagram takes in a dictionary of rules in string format and parses them to generate the railroad diagram in SVG format

grxmlToRailroad takes in a string for the file name and creates svg files visualizing each rule within the grammar



jjsgfprocessor.py
----------

extract_rules takes a string from a jjsgf file and puts it into a common dictionary format that createDiagram can process - the rule name is the key and maps to a string for the rule, with tags put between !! delimeters

createDiagram takes in a dictionary of rules in string format and parses them to generate the railroad diagram in SVG format

jjsgfToRailroad takes in a string for the file name and creates svg files visualizing each rule within the grammar
