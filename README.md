![ROOT (63)](https://github.com/codemstrneel/grammarprocessor/assets/41355538/b16b7b3f-c395-40f7-bcde-a20b159bb149)# Grammar Processor

==========================================

This is a library for processing grammars in [GRXML] (https://www.w3.org/TR/speech-grammar) format and [JJSGF](https://support.voicegain.ai/hc/en-us/articles/360048936511-JJSGF-Grammars) format, creating railroad diagrams representing all possible outcomes of the grammar.

Diagrams
--------
Each of these files, grxmlprocessor.py and jjsgfprocessor.py, contain their own unique ways of parsing the different styles of grammar.


grxmlprocessor.py
----------
Constructing a set of diagram for the rules from a grxml file contains one function call, for example

```python
grxmlToRailroad("zip_code_no_refs.grxml")  
```

,where zip_code_no_refs.grxml is found at https://support.voicegain.ai/hc/en-us/articles/360046906211-Sample-GRXML-Grammars, will creates files with name {rule name}.svg. As an example, ROOT.svg from this grammar is shown:


![ROOT (63)](https://github.com/codemstrneel/grammarprocessor/assets/41355538/b16b7b3f-c395-40f7-bcde-a20b159bb149)

jjsgfprocessor.py
----------

extract_rules takes a string from a jjsgf file and puts it into a common dictionary format that createDiagram can process - the rule name is the key and maps to a string for the rule, with tags put between !! delimeters

createDiagram takes in a dictionary of rules in string format and parses them to generate the railroad diagram in SVG format

jjsgfToRailroad takes in a string for the file name and creates svg files visualizing each rule within the grammar
