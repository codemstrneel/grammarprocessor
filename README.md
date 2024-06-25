# Grammar Processor

==========================================

This is a library for processing grammars in [GRXML] (https://www.w3.org/TR/speech-grammar) format and [JJSGF](https://support.voicegain.ai/hc/en-us/articles/360048936511-JJSGF-Grammars) format, creating railroad diagrams representing all possible outcomes of the grammar.

Diagrams
--------
Each of these files, grxmlprocessor.py and jjsgfprocessor.py, contain their own unique ways of parsing the different styles of grammar.


grxmlprocessor.py
----------
Constructing a set of diagrams for a grxml grammar contains one function call, for example

```python
grxmlToRailroad("zip_code_no_refs.grxml")  
```

,where zip_code_no_refs.grxml is found at https://support.voicegain.ai/hc/en-us/articles/360046906211-Sample-GRXML-Grammars, will creates files with name {rule name}.svg. As an example, ROOT.svg from this grammar is shown:


![ROOT (63)](https://github.com/codemstrneel/grammarprocessor/assets/41355538/b16b7b3f-c395-40f7-bcde-a20b159bb149)


__________
The following methods are used to process the grxml:

```python
extract_rules(xml_string)  
```

This method takes in a string and returns a processed dictionary with key of the rule name between < and > delimeters and the content of the rule, with tags between !! and !! delimeters as a result. As an example, the tensPlace rule from the Zip Code grammar is as follows:

'\<tensPlace\>': '(twenty  !!out.tensPlace="2";!! | thirty  !!out.tensPlace="3";!! | forty  !!out.tensPlace="4";!! | fifty  !!out.tensPlace="5";!! | sixty  !!out.tensPlace="6";!! | seventy  !!out.tensPlace="7";!! | eighty  !!out.tensPlace="8";!! | ninety  !!out.tensPlace="9";!!)'


```python
createDiagram(rules) 
```

takes a set of rules in the above format and writes to a series of svg files with file name {rule_name}.svg




jjsgfprocessor.py
----------

Constructing a set of diagrams for a grxml grammar contains one function call, for example

```python
jjsgfToRailroad("jjsgfComplex.txt")  
```

where jjsgfComplex.txt is 
[jjsgfComplex.txt](https://github.com/user-attachments/files/15980416/jjsgfComplex.txt) 

[Uploading jjsgf{
  "type": "JJSGF",
  "parameters": {
    "tag-format": "semantics/1.0-literals"
  },
  "grammar": "pizza",
  "public": {
    "root": "<card_phrase> {card} | <cash_phrase> {cash} | <pickup_phrase> {pickup} | <delivery_phrase> {delivery} | <agent_phrase> {agent} | <yes_phrase> {yes} | <no> {no} | <hello> {hello}"
  },
  "rules": { 
    "yes_phrase": "([sure|ok] ([<yes> [<yes>]] <yes> ))",
    "yes": "(yes|yeah)",
    "no": "([no] no)",
    "hello": "((hello) | (hell oh) | (hlo))",
    "card_phrase": "[uh] (([[i] [will] pay] [debit] <card> [at [the] store]) | (paying with [a] <card>) | (it will be <card>) )",
    "card": "(card|cord|car|cart)",
    "cash_phrase": "[uhm|yes] (([[(i [will]) | (i'll)] pay] <cash> [at [the] store]) | (paying <cash>) | (it will be <cash>) | (by <cash>) | (<cash> <cash>))",
    "cash": "(cash | cosh | (c a s h cash))",
    "pickup_phrase": "[uh|ah] (([i'll] <pickup> [at [the] store]) | (store <pickup>) | ([[(it's | order)] for] <pickup>) | ([<pickup>] <pickup> <pickup>))",
    "pickup": "(pickup | (pick up) | ((curbside|curside) [pickup]) | (carryout) | (takeout))",
    "delivery_phrase": "(([((it will)|(it'll)) be] [for] <delivery>) | ([[i] (want|wanna) [to]] [order] [for] <delivery>) ) [it's a robot i think]",
    "delivery": "([a | the] (delivery | delivry | dilivry | deliver | delivered))",
    "agent_phrase": "([card<yes>|no|neither|none|but] (([[([i] (need|want) to) | (could i) | (i wanna) | (can i) | (canna) | (may i)] (speak|talk) to] <agent> [dude|man]) | ( transfer [me] [to] <agent>) | (i want <agent> [to talk to]) | (give me <agent>)))",
    "agent": "( [a|aye|an|the] ((customer service) | (agent) | (representative|represenative) | (someone|somewa|somebody) | (someone else) | (human [being]) | ([live|lie] person) | (operator) | (store)))"
  }
}
Complex.txt…]()


The following methods are used to process the JJSGF::

```python
extract_rules(jjsgf_string)  
```

This method takes in a string and returns a processed dictionary with key of the rule name between < and > delimeters and the content of the rule, with tags between !! and !! delimeters as a result. As an example, the tensPlace rule from the Zip Code grammar is as follows:

'\<tensPlace\>': '(twenty  !!out.tensPlace="2";!! | thirty  !!out.tensPlace="3";!! | forty  !!out.tensPlace="4";!! | fifty  !!out.tensPlace="5";!! | sixty  !!out.tensPlace="6";!! | seventy  !!out.tensPlace="7";!! | eighty  !!out.tensPlace="8";!! | ninety  !!out.tensPlace="9";!!)'


```python
createDiagram(rules) 
```

takes a set of rules in the above format and writes to a series of svg files with file name {rule_name}.svg

