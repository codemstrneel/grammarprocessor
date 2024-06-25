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

![Uplo<svg class="railroad-diagram" height="5702" viewBox="0 0 5038.0 5702" width="5038.0" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
<g transform="translate(.5 .5)">
<g>
<path d="M20 21v20m10 -20v20m-10 -10h20" /></g><path d="M40 31h10" /><g>
<path d="M50 31h0.0" /><path d="M4988.0 31h0.0" /><g>
<path d="M50.0 31h0.0" /><path d="M4988.0 31h0.0" /><path d="M50.0 31h20" /><g>
<path d="M70.0 31h0.0" /><path d="M4968.0 31h0.0" /><g>
<path d="M70.0 31h0.0" /><path d="M4784.0 31h0.0" /><g>
<path d="M70.0 31h0.0" /><path d="M332.0 31h0.0" /><g class="terminal ">
<path d="M70.0 31h0.0" /><path d="M115.5 31h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="70" y="20"></rect><text x="92.75" y="35">the</text></g><path d="M115.5 31h10" /><g>
<path d="M125.5 31h0.0" /><path d="M285.0 31h0.0" /><path d="M125.5 31h20" /><g>
<path d="M145.5 31h37.0" /><path d="M228.0 31h37.0" /><g class="terminal ">
<path d="M182.5 31h0.0" /><path d="M228.0 31h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="182.5" y="20"></rect><text x="205.25" y="35">zip</text></g></g><path d="M265.0 31h20" /><path d="M125.5 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M145.5 61h0.0" /><path d="M265.0 61h0.0" /><g class="terminal ">
<path d="M145.5 61h0.0" /><path d="M191.0 61h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="145.5" y="50"></rect><text x="168.25" y="65">zip</text></g><path d="M191.0 61h10" /><path d="M201.0 61h10" /><g class="terminal ">
<path d="M211.0 61h0.0" /><path d="M265.0 61h0.0" /><rect height="22" rx="10" ry="10" width="54" x="211" y="50"></rect><text x="238" y="65">code</text></g></g><path d="M265.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M285.0 31h10" /><g class="terminal ">
<path d="M295.0 31h0.0" /><path d="M332.0 31h0.0" /><rect height="22" rx="10" ry="10" width="37" x="295" y="20"></rect><text x="313.5" y="35">is</text></g></g><path d="M332.0 31h10" /><g>
<path d="M342.0 31h0.0" /><path d="M4463.0 31h0.0" /><path d="M342.0 31h20" /><g>
<path d="M362.0 31h893.0" /><path d="M3550.0 31h893.0" /><g>
<path d="M1255.0 31h0.0" /><path d="M1479.0 31h0.0" /><g>
<path d="M1255.0 31h0.0" /><path d="M1479.0 31h0.0" /><path d="M1255.0 31h20" /><g>
<path d="M1275.0 31h0.0" /><path d="M1459.0 31h0.0" /><g>
<path d="M1275.0 31h0.0" /><path d="M1369.0 31h0.0" /><path d="M1275.0 31h20" /><g>
<path d="M1295.0 31h0.0" /><path d="M1349.0 31h0.0" /><g class="terminal ">
<path d="M1295.0 31h0.0" /><path d="M1349.0 31h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1295" y="20"></rect><text x="1322" y="35">zero</text></g></g><path d="M1349.0 31h20" /><path d="M1275.0 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1295.0 61h8.5" /><path d="M1340.5 61h8.5" /><g class="terminal ">
<path d="M1303.5 61h0.0" /><path d="M1340.5 61h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1303.5" y="50"></rect><text x="1322" y="65">oh</text></g></g><path d="M1349.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1369.0 31h10" /><g class="non-terminal ">
<path d="M1379.0 31h0.0" /><path d="M1459.0 31h0.0" /><text class="comment" x="1419" y="36">out.d=&quot;0&quot;;</text></g></g><path d="M1459.0 31h20" /><path d="M1255.0 31a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 91h19.25" /><path d="M1439.75 91h19.25" /><g class="terminal ">
<path d="M1294.25 91h0.0" /><path d="M1339.75 91h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1294.25" y="80"></rect><text x="1317" y="95">one</text></g><path d="M1339.75 91h10" /><path d="M1349.75 91h10" /><g class="non-terminal ">
<path d="M1359.75 91h0.0" /><path d="M1439.75 91h0.0" /><text class="comment" x="1399.75" y="96">out.d=&quot;1&quot;;</text></g></g><path d="M1459.0 91a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 121h19.25" /><path d="M1439.75 121h19.25" /><g class="terminal ">
<path d="M1294.25 121h0.0" /><path d="M1339.75 121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1294.25" y="110"></rect><text x="1317" y="125">two</text></g><path d="M1339.75 121h10" /><path d="M1349.75 121h10" /><g class="non-terminal ">
<path d="M1359.75 121h0.0" /><path d="M1439.75 121h0.0" /><text class="comment" x="1399.75" y="126">out.d=&quot;2&quot;;</text></g></g><path d="M1459.0 121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 151h10.75" /><path d="M1448.25 151h10.75" /><g class="terminal ">
<path d="M1285.75 151h0.0" /><path d="M1348.25 151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1285.75" y="140"></rect><text x="1317" y="155">three</text></g><path d="M1348.25 151h10" /><path d="M1358.25 151h10" /><g class="non-terminal ">
<path d="M1368.25 151h0.0" /><path d="M1448.25 151h0.0" /><text class="comment" x="1408.25" y="156">out.d=&quot;3&quot;;</text></g></g><path d="M1459.0 151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 181h15.0" /><path d="M1444.0 181h15.0" /><g class="terminal ">
<path d="M1290.0 181h0.0" /><path d="M1344.0 181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1290" y="170"></rect><text x="1317" y="185">four</text></g><path d="M1344.0 181h10" /><path d="M1354.0 181h10" /><g class="non-terminal ">
<path d="M1364.0 181h0.0" /><path d="M1444.0 181h0.0" /><text class="comment" x="1404" y="186">out.d=&quot;4&quot;;</text></g></g><path d="M1459.0 181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 211h15.0" /><path d="M1444.0 211h15.0" /><g class="terminal ">
<path d="M1290.0 211h0.0" /><path d="M1344.0 211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1290" y="200"></rect><text x="1317" y="215">five</text></g><path d="M1344.0 211h10" /><path d="M1354.0 211h10" /><g class="non-terminal ">
<path d="M1364.0 211h0.0" /><path d="M1444.0 211h0.0" /><text class="comment" x="1404" y="216">out.d=&quot;5&quot;;</text></g></g><path d="M1459.0 211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 241h19.25" /><path d="M1439.75 241h19.25" /><g class="terminal ">
<path d="M1294.25 241h0.0" /><path d="M1339.75 241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1294.25" y="230"></rect><text x="1317" y="245">six</text></g><path d="M1339.75 241h10" /><path d="M1349.75 241h10" /><g class="non-terminal ">
<path d="M1359.75 241h0.0" /><path d="M1439.75 241h0.0" /><text class="comment" x="1399.75" y="246">out.d=&quot;6&quot;;</text></g></g><path d="M1459.0 241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 271h10.75" /><path d="M1448.25 271h10.75" /><g class="terminal ">
<path d="M1285.75 271h0.0" /><path d="M1348.25 271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1285.75" y="260"></rect><text x="1317" y="275">seven</text></g><path d="M1348.25 271h10" /><path d="M1358.25 271h10" /><g class="non-terminal ">
<path d="M1368.25 271h0.0" /><path d="M1448.25 271h0.0" /><text class="comment" x="1408.25" y="276">out.d=&quot;7&quot;;</text></g></g><path d="M1459.0 271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 301h10.75" /><path d="M1448.25 301h10.75" /><g class="terminal ">
<path d="M1285.75 301h0.0" /><path d="M1348.25 301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1285.75" y="290"></rect><text x="1317" y="305">eight</text></g><path d="M1348.25 301h10" /><path d="M1358.25 301h10" /><g class="non-terminal ">
<path d="M1368.25 301h0.0" /><path d="M1448.25 301h0.0" /><text class="comment" x="1408.25" y="306">out.d=&quot;8&quot;;</text></g></g><path d="M1459.0 301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1255.0 31a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1275.0 331h15.0" /><path d="M1444.0 331h15.0" /><g class="terminal ">
<path d="M1290.0 331h0.0" /><path d="M1344.0 331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1290" y="320"></rect><text x="1317" y="335">nine</text></g><path d="M1344.0 331h10" /><path d="M1354.0 331h10" /><g class="non-terminal ">
<path d="M1364.0 331h0.0" /><path d="M1444.0 331h0.0" /><text class="comment" x="1404" y="336">out.d=&quot;9&quot;;</text></g></g><path d="M1459.0 331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1479.0 31h10" /><path d="M1489.0 31h10" /><g class="non-terminal ">
<path d="M1499.0 31h0.0" /><path d="M1698.0 31h0.0" /><text class="comment" x="1598.5" y="36">out.d1=rules.singleDigit.d;</text></g><path d="M1698.0 31h10" /><path d="M1708.0 31h10" /><g>
<path d="M1718.0 31h0.0" /><path d="M1942.0 31h0.0" /><g>
<path d="M1718.0 31h0.0" /><path d="M1942.0 31h0.0" /><path d="M1718.0 31h20" /><g>
<path d="M1738.0 31h0.0" /><path d="M1922.0 31h0.0" /><g>
<path d="M1738.0 31h0.0" /><path d="M1832.0 31h0.0" /><path d="M1738.0 31h20" /><g>
<path d="M1758.0 31h0.0" /><path d="M1812.0 31h0.0" /><g class="terminal ">
<path d="M1758.0 31h0.0" /><path d="M1812.0 31h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1758" y="20"></rect><text x="1785" y="35">zero</text></g></g><path d="M1812.0 31h20" /><path d="M1738.0 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1758.0 61h8.5" /><path d="M1803.5 61h8.5" /><g class="terminal ">
<path d="M1766.5 61h0.0" /><path d="M1803.5 61h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1766.5" y="50"></rect><text x="1785" y="65">oh</text></g></g><path d="M1812.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1832.0 31h10" /><g class="non-terminal ">
<path d="M1842.0 31h0.0" /><path d="M1922.0 31h0.0" /><text class="comment" x="1882" y="36">out.d=&quot;0&quot;;</text></g></g><path d="M1922.0 31h20" /><path d="M1718.0 31a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 91h19.25" /><path d="M1902.75 91h19.25" /><g class="terminal ">
<path d="M1757.25 91h0.0" /><path d="M1802.75 91h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1757.25" y="80"></rect><text x="1780" y="95">one</text></g><path d="M1802.75 91h10" /><path d="M1812.75 91h10" /><g class="non-terminal ">
<path d="M1822.75 91h0.0" /><path d="M1902.75 91h0.0" /><text class="comment" x="1862.75" y="96">out.d=&quot;1&quot;;</text></g></g><path d="M1922.0 91a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 121h19.25" /><path d="M1902.75 121h19.25" /><g class="terminal ">
<path d="M1757.25 121h0.0" /><path d="M1802.75 121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1757.25" y="110"></rect><text x="1780" y="125">two</text></g><path d="M1802.75 121h10" /><path d="M1812.75 121h10" /><g class="non-terminal ">
<path d="M1822.75 121h0.0" /><path d="M1902.75 121h0.0" /><text class="comment" x="1862.75" y="126">out.d=&quot;2&quot;;</text></g></g><path d="M1922.0 121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 151h10.75" /><path d="M1911.25 151h10.75" /><g class="terminal ">
<path d="M1748.75 151h0.0" /><path d="M1811.25 151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1748.75" y="140"></rect><text x="1780" y="155">three</text></g><path d="M1811.25 151h10" /><path d="M1821.25 151h10" /><g class="non-terminal ">
<path d="M1831.25 151h0.0" /><path d="M1911.25 151h0.0" /><text class="comment" x="1871.25" y="156">out.d=&quot;3&quot;;</text></g></g><path d="M1922.0 151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 181h15.0" /><path d="M1907.0 181h15.0" /><g class="terminal ">
<path d="M1753.0 181h0.0" /><path d="M1807.0 181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1753" y="170"></rect><text x="1780" y="185">four</text></g><path d="M1807.0 181h10" /><path d="M1817.0 181h10" /><g class="non-terminal ">
<path d="M1827.0 181h0.0" /><path d="M1907.0 181h0.0" /><text class="comment" x="1867" y="186">out.d=&quot;4&quot;;</text></g></g><path d="M1922.0 181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 211h15.0" /><path d="M1907.0 211h15.0" /><g class="terminal ">
<path d="M1753.0 211h0.0" /><path d="M1807.0 211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1753" y="200"></rect><text x="1780" y="215">five</text></g><path d="M1807.0 211h10" /><path d="M1817.0 211h10" /><g class="non-terminal ">
<path d="M1827.0 211h0.0" /><path d="M1907.0 211h0.0" /><text class="comment" x="1867" y="216">out.d=&quot;5&quot;;</text></g></g><path d="M1922.0 211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 241h19.25" /><path d="M1902.75 241h19.25" /><g class="terminal ">
<path d="M1757.25 241h0.0" /><path d="M1802.75 241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1757.25" y="230"></rect><text x="1780" y="245">six</text></g><path d="M1802.75 241h10" /><path d="M1812.75 241h10" /><g class="non-terminal ">
<path d="M1822.75 241h0.0" /><path d="M1902.75 241h0.0" /><text class="comment" x="1862.75" y="246">out.d=&quot;6&quot;;</text></g></g><path d="M1922.0 241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 271h10.75" /><path d="M1911.25 271h10.75" /><g class="terminal ">
<path d="M1748.75 271h0.0" /><path d="M1811.25 271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1748.75" y="260"></rect><text x="1780" y="275">seven</text></g><path d="M1811.25 271h10" /><path d="M1821.25 271h10" /><g class="non-terminal ">
<path d="M1831.25 271h0.0" /><path d="M1911.25 271h0.0" /><text class="comment" x="1871.25" y="276">out.d=&quot;7&quot;;</text></g></g><path d="M1922.0 271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 301h10.75" /><path d="M1911.25 301h10.75" /><g class="terminal ">
<path d="M1748.75 301h0.0" /><path d="M1811.25 301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1748.75" y="290"></rect><text x="1780" y="305">eight</text></g><path d="M1811.25 301h10" /><path d="M1821.25 301h10" /><g class="non-terminal ">
<path d="M1831.25 301h0.0" /><path d="M1911.25 301h0.0" /><text class="comment" x="1871.25" y="306">out.d=&quot;8&quot;;</text></g></g><path d="M1922.0 301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1718.0 31a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1738.0 331h15.0" /><path d="M1907.0 331h15.0" /><g class="terminal ">
<path d="M1753.0 331h0.0" /><path d="M1807.0 331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1753" y="320"></rect><text x="1780" y="335">nine</text></g><path d="M1807.0 331h10" /><path d="M1817.0 331h10" /><g class="non-terminal ">
<path d="M1827.0 331h0.0" /><path d="M1907.0 331h0.0" /><text class="comment" x="1867" y="336">out.d=&quot;9&quot;;</text></g></g><path d="M1922.0 331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1942.0 31h10" /><path d="M1952.0 31h10" /><g class="non-terminal ">
<path d="M1962.0 31h0.0" /><path d="M2161.0 31h0.0" /><text class="comment" x="2061.5" y="36">out.d2=rules.singleDigit.d;</text></g><path d="M2161.0 31h10" /><path d="M2171.0 31h10" /><g>
<path d="M2181.0 31h0.0" /><path d="M2405.0 31h0.0" /><g>
<path d="M2181.0 31h0.0" /><path d="M2405.0 31h0.0" /><path d="M2181.0 31h20" /><g>
<path d="M2201.0 31h0.0" /><path d="M2385.0 31h0.0" /><g>
<path d="M2201.0 31h0.0" /><path d="M2295.0 31h0.0" /><path d="M2201.0 31h20" /><g>
<path d="M2221.0 31h0.0" /><path d="M2275.0 31h0.0" /><g class="terminal ">
<path d="M2221.0 31h0.0" /><path d="M2275.0 31h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2221" y="20"></rect><text x="2248" y="35">zero</text></g></g><path d="M2275.0 31h20" /><path d="M2201.0 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 61h8.5" /><path d="M2266.5 61h8.5" /><g class="terminal ">
<path d="M2229.5 61h0.0" /><path d="M2266.5 61h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2229.5" y="50"></rect><text x="2248" y="65">oh</text></g></g><path d="M2275.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2295.0 31h10" /><g class="non-terminal ">
<path d="M2305.0 31h0.0" /><path d="M2385.0 31h0.0" /><text class="comment" x="2345" y="36">out.d=&quot;0&quot;;</text></g></g><path d="M2385.0 31h20" /><path d="M2181.0 31a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 91h19.25" /><path d="M2365.75 91h19.25" /><g class="terminal ">
<path d="M2220.25 91h0.0" /><path d="M2265.75 91h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="80"></rect><text x="2243" y="95">one</text></g><path d="M2265.75 91h10" /><path d="M2275.75 91h10" /><g class="non-terminal ">
<path d="M2285.75 91h0.0" /><path d="M2365.75 91h0.0" /><text class="comment" x="2325.75" y="96">out.d=&quot;1&quot;;</text></g></g><path d="M2385.0 91a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 121h19.25" /><path d="M2365.75 121h19.25" /><g class="terminal ">
<path d="M2220.25 121h0.0" /><path d="M2265.75 121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="110"></rect><text x="2243" y="125">two</text></g><path d="M2265.75 121h10" /><path d="M2275.75 121h10" /><g class="non-terminal ">
<path d="M2285.75 121h0.0" /><path d="M2365.75 121h0.0" /><text class="comment" x="2325.75" y="126">out.d=&quot;2&quot;;</text></g></g><path d="M2385.0 121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 151h10.75" /><path d="M2374.25 151h10.75" /><g class="terminal ">
<path d="M2211.75 151h0.0" /><path d="M2274.25 151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="140"></rect><text x="2243" y="155">three</text></g><path d="M2274.25 151h10" /><path d="M2284.25 151h10" /><g class="non-terminal ">
<path d="M2294.25 151h0.0" /><path d="M2374.25 151h0.0" /><text class="comment" x="2334.25" y="156">out.d=&quot;3&quot;;</text></g></g><path d="M2385.0 151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 181h15.0" /><path d="M2370.0 181h15.0" /><g class="terminal ">
<path d="M2216.0 181h0.0" /><path d="M2270.0 181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="170"></rect><text x="2243" y="185">four</text></g><path d="M2270.0 181h10" /><path d="M2280.0 181h10" /><g class="non-terminal ">
<path d="M2290.0 181h0.0" /><path d="M2370.0 181h0.0" /><text class="comment" x="2330" y="186">out.d=&quot;4&quot;;</text></g></g><path d="M2385.0 181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 211h15.0" /><path d="M2370.0 211h15.0" /><g class="terminal ">
<path d="M2216.0 211h0.0" /><path d="M2270.0 211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="200"></rect><text x="2243" y="215">five</text></g><path d="M2270.0 211h10" /><path d="M2280.0 211h10" /><g class="non-terminal ">
<path d="M2290.0 211h0.0" /><path d="M2370.0 211h0.0" /><text class="comment" x="2330" y="216">out.d=&quot;5&quot;;</text></g></g><path d="M2385.0 211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 241h19.25" /><path d="M2365.75 241h19.25" /><g class="terminal ">
<path d="M2220.25 241h0.0" /><path d="M2265.75 241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="230"></rect><text x="2243" y="245">six</text></g><path d="M2265.75 241h10" /><path d="M2275.75 241h10" /><g class="non-terminal ">
<path d="M2285.75 241h0.0" /><path d="M2365.75 241h0.0" /><text class="comment" x="2325.75" y="246">out.d=&quot;6&quot;;</text></g></g><path d="M2385.0 241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 271h10.75" /><path d="M2374.25 271h10.75" /><g class="terminal ">
<path d="M2211.75 271h0.0" /><path d="M2274.25 271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="260"></rect><text x="2243" y="275">seven</text></g><path d="M2274.25 271h10" /><path d="M2284.25 271h10" /><g class="non-terminal ">
<path d="M2294.25 271h0.0" /><path d="M2374.25 271h0.0" /><text class="comment" x="2334.25" y="276">out.d=&quot;7&quot;;</text></g></g><path d="M2385.0 271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 301h10.75" /><path d="M2374.25 301h10.75" /><g class="terminal ">
<path d="M2211.75 301h0.0" /><path d="M2274.25 301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="290"></rect><text x="2243" y="305">eight</text></g><path d="M2274.25 301h10" /><path d="M2284.25 301h10" /><g class="non-terminal ">
<path d="M2294.25 301h0.0" /><path d="M2374.25 301h0.0" /><text class="comment" x="2334.25" y="306">out.d=&quot;8&quot;;</text></g></g><path d="M2385.0 301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2181.0 31a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 331h15.0" /><path d="M2370.0 331h15.0" /><g class="terminal ">
<path d="M2216.0 331h0.0" /><path d="M2270.0 331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="320"></rect><text x="2243" y="335">nine</text></g><path d="M2270.0 331h10" /><path d="M2280.0 331h10" /><g class="non-terminal ">
<path d="M2290.0 331h0.0" /><path d="M2370.0 331h0.0" /><text class="comment" x="2330" y="336">out.d=&quot;9&quot;;</text></g></g><path d="M2385.0 331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2405.0 31h10" /><path d="M2415.0 31h10" /><g class="non-terminal ">
<path d="M2425.0 31h0.0" /><path d="M2624.0 31h0.0" /><text class="comment" x="2524.5" y="36">out.d3=rules.singleDigit.d;</text></g><path d="M2624.0 31h10" /><path d="M2634.0 31h10" /><g>
<path d="M2644.0 31h0.0" /><path d="M2868.0 31h0.0" /><g>
<path d="M2644.0 31h0.0" /><path d="M2868.0 31h0.0" /><path d="M2644.0 31h20" /><g>
<path d="M2664.0 31h0.0" /><path d="M2848.0 31h0.0" /><g>
<path d="M2664.0 31h0.0" /><path d="M2758.0 31h0.0" /><path d="M2664.0 31h20" /><g>
<path d="M2684.0 31h0.0" /><path d="M2738.0 31h0.0" /><g class="terminal ">
<path d="M2684.0 31h0.0" /><path d="M2738.0 31h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2684" y="20"></rect><text x="2711" y="35">zero</text></g></g><path d="M2738.0 31h20" /><path d="M2664.0 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 61h8.5" /><path d="M2729.5 61h8.5" /><g class="terminal ">
<path d="M2692.5 61h0.0" /><path d="M2729.5 61h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2692.5" y="50"></rect><text x="2711" y="65">oh</text></g></g><path d="M2738.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2758.0 31h10" /><g class="non-terminal ">
<path d="M2768.0 31h0.0" /><path d="M2848.0 31h0.0" /><text class="comment" x="2808" y="36">out.d=&quot;0&quot;;</text></g></g><path d="M2848.0 31h20" /><path d="M2644.0 31a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 91h19.25" /><path d="M2828.75 91h19.25" /><g class="terminal ">
<path d="M2683.25 91h0.0" /><path d="M2728.75 91h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2683.25" y="80"></rect><text x="2706" y="95">one</text></g><path d="M2728.75 91h10" /><path d="M2738.75 91h10" /><g class="non-terminal ">
<path d="M2748.75 91h0.0" /><path d="M2828.75 91h0.0" /><text class="comment" x="2788.75" y="96">out.d=&quot;1&quot;;</text></g></g><path d="M2848.0 91a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 121h19.25" /><path d="M2828.75 121h19.25" /><g class="terminal ">
<path d="M2683.25 121h0.0" /><path d="M2728.75 121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2683.25" y="110"></rect><text x="2706" y="125">two</text></g><path d="M2728.75 121h10" /><path d="M2738.75 121h10" /><g class="non-terminal ">
<path d="M2748.75 121h0.0" /><path d="M2828.75 121h0.0" /><text class="comment" x="2788.75" y="126">out.d=&quot;2&quot;;</text></g></g><path d="M2848.0 121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 151h10.75" /><path d="M2837.25 151h10.75" /><g class="terminal ">
<path d="M2674.75 151h0.0" /><path d="M2737.25 151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2674.75" y="140"></rect><text x="2706" y="155">three</text></g><path d="M2737.25 151h10" /><path d="M2747.25 151h10" /><g class="non-terminal ">
<path d="M2757.25 151h0.0" /><path d="M2837.25 151h0.0" /><text class="comment" x="2797.25" y="156">out.d=&quot;3&quot;;</text></g></g><path d="M2848.0 151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 181h15.0" /><path d="M2833.0 181h15.0" /><g class="terminal ">
<path d="M2679.0 181h0.0" /><path d="M2733.0 181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2679" y="170"></rect><text x="2706" y="185">four</text></g><path d="M2733.0 181h10" /><path d="M2743.0 181h10" /><g class="non-terminal ">
<path d="M2753.0 181h0.0" /><path d="M2833.0 181h0.0" /><text class="comment" x="2793" y="186">out.d=&quot;4&quot;;</text></g></g><path d="M2848.0 181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 211h15.0" /><path d="M2833.0 211h15.0" /><g class="terminal ">
<path d="M2679.0 211h0.0" /><path d="M2733.0 211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2679" y="200"></rect><text x="2706" y="215">five</text></g><path d="M2733.0 211h10" /><path d="M2743.0 211h10" /><g class="non-terminal ">
<path d="M2753.0 211h0.0" /><path d="M2833.0 211h0.0" /><text class="comment" x="2793" y="216">out.d=&quot;5&quot;;</text></g></g><path d="M2848.0 211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 241h19.25" /><path d="M2828.75 241h19.25" /><g class="terminal ">
<path d="M2683.25 241h0.0" /><path d="M2728.75 241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2683.25" y="230"></rect><text x="2706" y="245">six</text></g><path d="M2728.75 241h10" /><path d="M2738.75 241h10" /><g class="non-terminal ">
<path d="M2748.75 241h0.0" /><path d="M2828.75 241h0.0" /><text class="comment" x="2788.75" y="246">out.d=&quot;6&quot;;</text></g></g><path d="M2848.0 241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 271h10.75" /><path d="M2837.25 271h10.75" /><g class="terminal ">
<path d="M2674.75 271h0.0" /><path d="M2737.25 271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2674.75" y="260"></rect><text x="2706" y="275">seven</text></g><path d="M2737.25 271h10" /><path d="M2747.25 271h10" /><g class="non-terminal ">
<path d="M2757.25 271h0.0" /><path d="M2837.25 271h0.0" /><text class="comment" x="2797.25" y="276">out.d=&quot;7&quot;;</text></g></g><path d="M2848.0 271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 301h10.75" /><path d="M2837.25 301h10.75" /><g class="terminal ">
<path d="M2674.75 301h0.0" /><path d="M2737.25 301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2674.75" y="290"></rect><text x="2706" y="305">eight</text></g><path d="M2737.25 301h10" /><path d="M2747.25 301h10" /><g class="non-terminal ">
<path d="M2757.25 301h0.0" /><path d="M2837.25 301h0.0" /><text class="comment" x="2797.25" y="306">out.d=&quot;8&quot;;</text></g></g><path d="M2848.0 301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2644.0 31a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 331h15.0" /><path d="M2833.0 331h15.0" /><g class="terminal ">
<path d="M2679.0 331h0.0" /><path d="M2733.0 331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2679" y="320"></rect><text x="2706" y="335">nine</text></g><path d="M2733.0 331h10" /><path d="M2743.0 331h10" /><g class="non-terminal ">
<path d="M2753.0 331h0.0" /><path d="M2833.0 331h0.0" /><text class="comment" x="2793" y="336">out.d=&quot;9&quot;;</text></g></g><path d="M2848.0 331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2868.0 31h10" /><path d="M2878.0 31h10" /><g class="non-terminal ">
<path d="M2888.0 31h0.0" /><path d="M3087.0 31h0.0" /><text class="comment" x="2987.5" y="36">out.d4=rules.singleDigit.d;</text></g><path d="M3087.0 31h10" /><path d="M3097.0 31h10" /><g>
<path d="M3107.0 31h0.0" /><path d="M3331.0 31h0.0" /><g>
<path d="M3107.0 31h0.0" /><path d="M3331.0 31h0.0" /><path d="M3107.0 31h20" /><g>
<path d="M3127.0 31h0.0" /><path d="M3311.0 31h0.0" /><g>
<path d="M3127.0 31h0.0" /><path d="M3221.0 31h0.0" /><path d="M3127.0 31h20" /><g>
<path d="M3147.0 31h0.0" /><path d="M3201.0 31h0.0" /><g class="terminal ">
<path d="M3147.0 31h0.0" /><path d="M3201.0 31h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3147" y="20"></rect><text x="3174" y="35">zero</text></g></g><path d="M3201.0 31h20" /><path d="M3127.0 31a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3147.0 61h8.5" /><path d="M3192.5 61h8.5" /><g class="terminal ">
<path d="M3155.5 61h0.0" /><path d="M3192.5 61h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3155.5" y="50"></rect><text x="3174" y="65">oh</text></g></g><path d="M3201.0 61a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3221.0 31h10" /><g class="non-terminal ">
<path d="M3231.0 31h0.0" /><path d="M3311.0 31h0.0" /><text class="comment" x="3271" y="36">out.d=&quot;0&quot;;</text></g></g><path d="M3311.0 31h20" /><path d="M3107.0 31a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 91h19.25" /><path d="M3291.75 91h19.25" /><g class="terminal ">
<path d="M3146.25 91h0.0" /><path d="M3191.75 91h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3146.25" y="80"></rect><text x="3169" y="95">one</text></g><path d="M3191.75 91h10" /><path d="M3201.75 91h10" /><g class="non-terminal ">
<path d="M3211.75 91h0.0" /><path d="M3291.75 91h0.0" /><text class="comment" x="3251.75" y="96">out.d=&quot;1&quot;;</text></g></g><path d="M3311.0 91a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 121h19.25" /><path d="M3291.75 121h19.25" /><g class="terminal ">
<path d="M3146.25 121h0.0" /><path d="M3191.75 121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3146.25" y="110"></rect><text x="3169" y="125">two</text></g><path d="M3191.75 121h10" /><path d="M3201.75 121h10" /><g class="non-terminal ">
<path d="M3211.75 121h0.0" /><path d="M3291.75 121h0.0" /><text class="comment" x="3251.75" y="126">out.d=&quot;2&quot;;</text></g></g><path d="M3311.0 121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 151h10.75" /><path d="M3300.25 151h10.75" /><g class="terminal ">
<path d="M3137.75 151h0.0" /><path d="M3200.25 151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3137.75" y="140"></rect><text x="3169" y="155">three</text></g><path d="M3200.25 151h10" /><path d="M3210.25 151h10" /><g class="non-terminal ">
<path d="M3220.25 151h0.0" /><path d="M3300.25 151h0.0" /><text class="comment" x="3260.25" y="156">out.d=&quot;3&quot;;</text></g></g><path d="M3311.0 151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 181h15.0" /><path d="M3296.0 181h15.0" /><g class="terminal ">
<path d="M3142.0 181h0.0" /><path d="M3196.0 181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3142" y="170"></rect><text x="3169" y="185">four</text></g><path d="M3196.0 181h10" /><path d="M3206.0 181h10" /><g class="non-terminal ">
<path d="M3216.0 181h0.0" /><path d="M3296.0 181h0.0" /><text class="comment" x="3256" y="186">out.d=&quot;4&quot;;</text></g></g><path d="M3311.0 181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 211h15.0" /><path d="M3296.0 211h15.0" /><g class="terminal ">
<path d="M3142.0 211h0.0" /><path d="M3196.0 211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3142" y="200"></rect><text x="3169" y="215">five</text></g><path d="M3196.0 211h10" /><path d="M3206.0 211h10" /><g class="non-terminal ">
<path d="M3216.0 211h0.0" /><path d="M3296.0 211h0.0" /><text class="comment" x="3256" y="216">out.d=&quot;5&quot;;</text></g></g><path d="M3311.0 211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 241h19.25" /><path d="M3291.75 241h19.25" /><g class="terminal ">
<path d="M3146.25 241h0.0" /><path d="M3191.75 241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3146.25" y="230"></rect><text x="3169" y="245">six</text></g><path d="M3191.75 241h10" /><path d="M3201.75 241h10" /><g class="non-terminal ">
<path d="M3211.75 241h0.0" /><path d="M3291.75 241h0.0" /><text class="comment" x="3251.75" y="246">out.d=&quot;6&quot;;</text></g></g><path d="M3311.0 241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 271h10.75" /><path d="M3300.25 271h10.75" /><g class="terminal ">
<path d="M3137.75 271h0.0" /><path d="M3200.25 271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3137.75" y="260"></rect><text x="3169" y="275">seven</text></g><path d="M3200.25 271h10" /><path d="M3210.25 271h10" /><g class="non-terminal ">
<path d="M3220.25 271h0.0" /><path d="M3300.25 271h0.0" /><text class="comment" x="3260.25" y="276">out.d=&quot;7&quot;;</text></g></g><path d="M3311.0 271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 301h10.75" /><path d="M3300.25 301h10.75" /><g class="terminal ">
<path d="M3137.75 301h0.0" /><path d="M3200.25 301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3137.75" y="290"></rect><text x="3169" y="305">eight</text></g><path d="M3200.25 301h10" /><path d="M3210.25 301h10" /><g class="non-terminal ">
<path d="M3220.25 301h0.0" /><path d="M3300.25 301h0.0" /><text class="comment" x="3260.25" y="306">out.d=&quot;8&quot;;</text></g></g><path d="M3311.0 301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3107.0 31a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3127.0 331h15.0" /><path d="M3296.0 331h15.0" /><g class="terminal ">
<path d="M3142.0 331h0.0" /><path d="M3196.0 331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3142" y="320"></rect><text x="3169" y="335">nine</text></g><path d="M3196.0 331h10" /><path d="M3206.0 331h10" /><g class="non-terminal ">
<path d="M3216.0 331h0.0" /><path d="M3296.0 331h0.0" /><text class="comment" x="3256" y="336">out.d=&quot;9&quot;;</text></g></g><path d="M3311.0 331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3331.0 31h10" /><path d="M3341.0 31h10" /><g class="non-terminal ">
<path d="M3351.0 31h0.0" /><path d="M3550.0 31h0.0" /><text class="comment" x="3450.5" y="36">out.d5=rules.singleDigit.d;</text></g></g><path d="M4443.0 31h20" /><path d="M342.0 31a10 10 0 0 1 10 10v310a10 10 0 0 0 10 10" /><g>
<path d="M362.0 361h446.5" /><path d="M3996.5 361h446.5" /><g>
<path d="M808.5 361h0.0" /><path d="M1032.5 361h0.0" /><g>
<path d="M808.5 361h0.0" /><path d="M1032.5 361h0.0" /><path d="M808.5 361h20" /><g>
<path d="M828.5 361h0.0" /><path d="M1012.5 361h0.0" /><g>
<path d="M828.5 361h0.0" /><path d="M922.5 361h0.0" /><path d="M828.5 361h20" /><g>
<path d="M848.5 361h0.0" /><path d="M902.5 361h0.0" /><g class="terminal ">
<path d="M848.5 361h0.0" /><path d="M902.5 361h0.0" /><rect height="22" rx="10" ry="10" width="54" x="848.5" y="350"></rect><text x="875.5" y="365">zero</text></g></g><path d="M902.5 361h20" /><path d="M828.5 361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M848.5 391h8.5" /><path d="M894.0 391h8.5" /><g class="terminal ">
<path d="M857.0 391h0.0" /><path d="M894.0 391h0.0" /><rect height="22" rx="10" ry="10" width="37" x="857" y="380"></rect><text x="875.5" y="395">oh</text></g></g><path d="M902.5 391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M922.5 361h10" /><g class="non-terminal ">
<path d="M932.5 361h0.0" /><path d="M1012.5 361h0.0" /><text class="comment" x="972.5" y="366">out.d=&quot;0&quot;;</text></g></g><path d="M1012.5 361h20" /><path d="M808.5 361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M828.5 421h19.25" /><path d="M993.25 421h19.25" /><g class="terminal ">
<path d="M847.75 421h0.0" /><path d="M893.25 421h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="410"></rect><text x="870.5" y="425">one</text></g><path d="M893.25 421h10" /><path d="M903.25 421h10" /><g class="non-terminal ">
<path d="M913.25 421h0.0" /><path d="M993.25 421h0.0" /><text class="comment" x="953.25" y="426">out.d=&quot;1&quot;;</text></g></g><path d="M1012.5 421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M828.5 451h19.25" /><path d="M993.25 451h19.25" /><g class="terminal ">
<path d="M847.75 451h0.0" /><path d="M893.25 451h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="440"></rect><text x="870.5" y="455">two</text></g><path d="M893.25 451h10" /><path d="M903.25 451h10" /><g class="non-terminal ">
<path d="M913.25 451h0.0" /><path d="M993.25 451h0.0" /><text class="comment" x="953.25" y="456">out.d=&quot;2&quot;;</text></g></g><path d="M1012.5 451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M828.5 481h10.75" /><path d="M1001.75 481h10.75" /><g class="terminal ">
<path d="M839.25 481h0.0" /><path d="M901.75 481h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="470"></rect><text x="870.5" y="485">three</text></g><path d="M901.75 481h10" /><path d="M911.75 481h10" /><g class="non-terminal ">
<path d="M921.75 481h0.0" /><path d="M1001.75 481h0.0" /><text class="comment" x="961.75" y="486">out.d=&quot;3&quot;;</text></g></g><path d="M1012.5 481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M828.5 511h15.0" /><path d="M997.5 511h15.0" /><g class="terminal ">
<path d="M843.5 511h0.0" /><path d="M897.5 511h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="500"></rect><text x="870.5" y="515">four</text></g><path d="M897.5 511h10" /><path d="M907.5 511h10" /><g class="non-terminal ">
<path d="M917.5 511h0.0" /><path d="M997.5 511h0.0" /><text class="comment" x="957.5" y="516">out.d=&quot;4&quot;;</text></g></g><path d="M1012.5 511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M828.5 541h15.0" /><path d="M997.5 541h15.0" /><g class="terminal ">
<path d="M843.5 541h0.0" /><path d="M897.5 541h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="530"></rect><text x="870.5" y="545">five</text></g><path d="M897.5 541h10" /><path d="M907.5 541h10" /><g class="non-terminal ">
<path d="M917.5 541h0.0" /><path d="M997.5 541h0.0" /><text class="comment" x="957.5" y="546">out.d=&quot;5&quot;;</text></g></g><path d="M1012.5 541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M828.5 571h19.25" /><path d="M993.25 571h19.25" /><g class="terminal ">
<path d="M847.75 571h0.0" /><path d="M893.25 571h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="560"></rect><text x="870.5" y="575">six</text></g><path d="M893.25 571h10" /><path d="M903.25 571h10" /><g class="non-terminal ">
<path d="M913.25 571h0.0" /><path d="M993.25 571h0.0" /><text class="comment" x="953.25" y="576">out.d=&quot;6&quot;;</text></g></g><path d="M1012.5 571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M828.5 601h10.75" /><path d="M1001.75 601h10.75" /><g class="terminal ">
<path d="M839.25 601h0.0" /><path d="M901.75 601h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="590"></rect><text x="870.5" y="605">seven</text></g><path d="M901.75 601h10" /><path d="M911.75 601h10" /><g class="non-terminal ">
<path d="M921.75 601h0.0" /><path d="M1001.75 601h0.0" /><text class="comment" x="961.75" y="606">out.d=&quot;7&quot;;</text></g></g><path d="M1012.5 601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M828.5 631h10.75" /><path d="M1001.75 631h10.75" /><g class="terminal ">
<path d="M839.25 631h0.0" /><path d="M901.75 631h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="620"></rect><text x="870.5" y="635">eight</text></g><path d="M901.75 631h10" /><path d="M911.75 631h10" /><g class="non-terminal ">
<path d="M921.75 631h0.0" /><path d="M1001.75 631h0.0" /><text class="comment" x="961.75" y="636">out.d=&quot;8&quot;;</text></g></g><path d="M1012.5 631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M808.5 361a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M828.5 661h15.0" /><path d="M997.5 661h15.0" /><g class="terminal ">
<path d="M843.5 661h0.0" /><path d="M897.5 661h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="650"></rect><text x="870.5" y="665">nine</text></g><path d="M897.5 661h10" /><path d="M907.5 661h10" /><g class="non-terminal ">
<path d="M917.5 661h0.0" /><path d="M997.5 661h0.0" /><text class="comment" x="957.5" y="666">out.d=&quot;9&quot;;</text></g></g><path d="M1012.5 661a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1032.5 361h10" /><path d="M1042.5 361h10" /><g class="non-terminal ">
<path d="M1052.5 361h0.0" /><path d="M1251.5 361h0.0" /><text class="comment" x="1152" y="366">out.d1=rules.singleDigit.d;</text></g><path d="M1251.5 361h10" /><path d="M1261.5 361h10" /><g>
<path d="M1271.5 361h0.0" /><path d="M1495.5 361h0.0" /><g>
<path d="M1271.5 361h0.0" /><path d="M1495.5 361h0.0" /><path d="M1271.5 361h20" /><g>
<path d="M1291.5 361h0.0" /><path d="M1475.5 361h0.0" /><g>
<path d="M1291.5 361h0.0" /><path d="M1385.5 361h0.0" /><path d="M1291.5 361h20" /><g>
<path d="M1311.5 361h0.0" /><path d="M1365.5 361h0.0" /><g class="terminal ">
<path d="M1311.5 361h0.0" /><path d="M1365.5 361h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1311.5" y="350"></rect><text x="1338.5" y="365">zero</text></g></g><path d="M1365.5 361h20" /><path d="M1291.5 361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 391h8.5" /><path d="M1357.0 391h8.5" /><g class="terminal ">
<path d="M1320.0 391h0.0" /><path d="M1357.0 391h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1320" y="380"></rect><text x="1338.5" y="395">oh</text></g></g><path d="M1365.5 391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1385.5 361h10" /><g class="non-terminal ">
<path d="M1395.5 361h0.0" /><path d="M1475.5 361h0.0" /><text class="comment" x="1435.5" y="366">out.d=&quot;0&quot;;</text></g></g><path d="M1475.5 361h20" /><path d="M1271.5 361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 421h19.25" /><path d="M1456.25 421h19.25" /><g class="terminal ">
<path d="M1310.75 421h0.0" /><path d="M1356.25 421h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="410"></rect><text x="1333.5" y="425">one</text></g><path d="M1356.25 421h10" /><path d="M1366.25 421h10" /><g class="non-terminal ">
<path d="M1376.25 421h0.0" /><path d="M1456.25 421h0.0" /><text class="comment" x="1416.25" y="426">out.d=&quot;1&quot;;</text></g></g><path d="M1475.5 421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 451h19.25" /><path d="M1456.25 451h19.25" /><g class="terminal ">
<path d="M1310.75 451h0.0" /><path d="M1356.25 451h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="440"></rect><text x="1333.5" y="455">two</text></g><path d="M1356.25 451h10" /><path d="M1366.25 451h10" /><g class="non-terminal ">
<path d="M1376.25 451h0.0" /><path d="M1456.25 451h0.0" /><text class="comment" x="1416.25" y="456">out.d=&quot;2&quot;;</text></g></g><path d="M1475.5 451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 481h10.75" /><path d="M1464.75 481h10.75" /><g class="terminal ">
<path d="M1302.25 481h0.0" /><path d="M1364.75 481h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="470"></rect><text x="1333.5" y="485">three</text></g><path d="M1364.75 481h10" /><path d="M1374.75 481h10" /><g class="non-terminal ">
<path d="M1384.75 481h0.0" /><path d="M1464.75 481h0.0" /><text class="comment" x="1424.75" y="486">out.d=&quot;3&quot;;</text></g></g><path d="M1475.5 481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 511h15.0" /><path d="M1460.5 511h15.0" /><g class="terminal ">
<path d="M1306.5 511h0.0" /><path d="M1360.5 511h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="500"></rect><text x="1333.5" y="515">four</text></g><path d="M1360.5 511h10" /><path d="M1370.5 511h10" /><g class="non-terminal ">
<path d="M1380.5 511h0.0" /><path d="M1460.5 511h0.0" /><text class="comment" x="1420.5" y="516">out.d=&quot;4&quot;;</text></g></g><path d="M1475.5 511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 541h15.0" /><path d="M1460.5 541h15.0" /><g class="terminal ">
<path d="M1306.5 541h0.0" /><path d="M1360.5 541h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="530"></rect><text x="1333.5" y="545">five</text></g><path d="M1360.5 541h10" /><path d="M1370.5 541h10" /><g class="non-terminal ">
<path d="M1380.5 541h0.0" /><path d="M1460.5 541h0.0" /><text class="comment" x="1420.5" y="546">out.d=&quot;5&quot;;</text></g></g><path d="M1475.5 541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 571h19.25" /><path d="M1456.25 571h19.25" /><g class="terminal ">
<path d="M1310.75 571h0.0" /><path d="M1356.25 571h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="560"></rect><text x="1333.5" y="575">six</text></g><path d="M1356.25 571h10" /><path d="M1366.25 571h10" /><g class="non-terminal ">
<path d="M1376.25 571h0.0" /><path d="M1456.25 571h0.0" /><text class="comment" x="1416.25" y="576">out.d=&quot;6&quot;;</text></g></g><path d="M1475.5 571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 601h10.75" /><path d="M1464.75 601h10.75" /><g class="terminal ">
<path d="M1302.25 601h0.0" /><path d="M1364.75 601h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="590"></rect><text x="1333.5" y="605">seven</text></g><path d="M1364.75 601h10" /><path d="M1374.75 601h10" /><g class="non-terminal ">
<path d="M1384.75 601h0.0" /><path d="M1464.75 601h0.0" /><text class="comment" x="1424.75" y="606">out.d=&quot;7&quot;;</text></g></g><path d="M1475.5 601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 631h10.75" /><path d="M1464.75 631h10.75" /><g class="terminal ">
<path d="M1302.25 631h0.0" /><path d="M1364.75 631h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="620"></rect><text x="1333.5" y="635">eight</text></g><path d="M1364.75 631h10" /><path d="M1374.75 631h10" /><g class="non-terminal ">
<path d="M1384.75 631h0.0" /><path d="M1464.75 631h0.0" /><text class="comment" x="1424.75" y="636">out.d=&quot;8&quot;;</text></g></g><path d="M1475.5 631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1271.5 361a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 661h15.0" /><path d="M1460.5 661h15.0" /><g class="terminal ">
<path d="M1306.5 661h0.0" /><path d="M1360.5 661h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="650"></rect><text x="1333.5" y="665">nine</text></g><path d="M1360.5 661h10" /><path d="M1370.5 661h10" /><g class="non-terminal ">
<path d="M1380.5 661h0.0" /><path d="M1460.5 661h0.0" /><text class="comment" x="1420.5" y="666">out.d=&quot;9&quot;;</text></g></g><path d="M1475.5 661a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1495.5 361h10" /><path d="M1505.5 361h10" /><g class="non-terminal ">
<path d="M1515.5 361h0.0" /><path d="M1714.5 361h0.0" /><text class="comment" x="1615" y="366">out.d2=rules.singleDigit.d;</text></g><path d="M1714.5 361h10" /><path d="M1724.5 361h10" /><g>
<path d="M1734.5 361h0.0" /><path d="M1958.5 361h0.0" /><g>
<path d="M1734.5 361h0.0" /><path d="M1958.5 361h0.0" /><path d="M1734.5 361h20" /><g>
<path d="M1754.5 361h0.0" /><path d="M1938.5 361h0.0" /><g>
<path d="M1754.5 361h0.0" /><path d="M1848.5 361h0.0" /><path d="M1754.5 361h20" /><g>
<path d="M1774.5 361h0.0" /><path d="M1828.5 361h0.0" /><g class="terminal ">
<path d="M1774.5 361h0.0" /><path d="M1828.5 361h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1774.5" y="350"></rect><text x="1801.5" y="365">zero</text></g></g><path d="M1828.5 361h20" /><path d="M1754.5 361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 391h8.5" /><path d="M1820.0 391h8.5" /><g class="terminal ">
<path d="M1783.0 391h0.0" /><path d="M1820.0 391h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1783" y="380"></rect><text x="1801.5" y="395">oh</text></g></g><path d="M1828.5 391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1848.5 361h10" /><g class="non-terminal ">
<path d="M1858.5 361h0.0" /><path d="M1938.5 361h0.0" /><text class="comment" x="1898.5" y="366">out.d=&quot;0&quot;;</text></g></g><path d="M1938.5 361h20" /><path d="M1734.5 361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 421h19.25" /><path d="M1919.25 421h19.25" /><g class="terminal ">
<path d="M1773.75 421h0.0" /><path d="M1819.25 421h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1773.75" y="410"></rect><text x="1796.5" y="425">one</text></g><path d="M1819.25 421h10" /><path d="M1829.25 421h10" /><g class="non-terminal ">
<path d="M1839.25 421h0.0" /><path d="M1919.25 421h0.0" /><text class="comment" x="1879.25" y="426">out.d=&quot;1&quot;;</text></g></g><path d="M1938.5 421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 451h19.25" /><path d="M1919.25 451h19.25" /><g class="terminal ">
<path d="M1773.75 451h0.0" /><path d="M1819.25 451h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1773.75" y="440"></rect><text x="1796.5" y="455">two</text></g><path d="M1819.25 451h10" /><path d="M1829.25 451h10" /><g class="non-terminal ">
<path d="M1839.25 451h0.0" /><path d="M1919.25 451h0.0" /><text class="comment" x="1879.25" y="456">out.d=&quot;2&quot;;</text></g></g><path d="M1938.5 451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 481h10.75" /><path d="M1927.75 481h10.75" /><g class="terminal ">
<path d="M1765.25 481h0.0" /><path d="M1827.75 481h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1765.25" y="470"></rect><text x="1796.5" y="485">three</text></g><path d="M1827.75 481h10" /><path d="M1837.75 481h10" /><g class="non-terminal ">
<path d="M1847.75 481h0.0" /><path d="M1927.75 481h0.0" /><text class="comment" x="1887.75" y="486">out.d=&quot;3&quot;;</text></g></g><path d="M1938.5 481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 511h15.0" /><path d="M1923.5 511h15.0" /><g class="terminal ">
<path d="M1769.5 511h0.0" /><path d="M1823.5 511h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1769.5" y="500"></rect><text x="1796.5" y="515">four</text></g><path d="M1823.5 511h10" /><path d="M1833.5 511h10" /><g class="non-terminal ">
<path d="M1843.5 511h0.0" /><path d="M1923.5 511h0.0" /><text class="comment" x="1883.5" y="516">out.d=&quot;4&quot;;</text></g></g><path d="M1938.5 511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 541h15.0" /><path d="M1923.5 541h15.0" /><g class="terminal ">
<path d="M1769.5 541h0.0" /><path d="M1823.5 541h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1769.5" y="530"></rect><text x="1796.5" y="545">five</text></g><path d="M1823.5 541h10" /><path d="M1833.5 541h10" /><g class="non-terminal ">
<path d="M1843.5 541h0.0" /><path d="M1923.5 541h0.0" /><text class="comment" x="1883.5" y="546">out.d=&quot;5&quot;;</text></g></g><path d="M1938.5 541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 571h19.25" /><path d="M1919.25 571h19.25" /><g class="terminal ">
<path d="M1773.75 571h0.0" /><path d="M1819.25 571h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1773.75" y="560"></rect><text x="1796.5" y="575">six</text></g><path d="M1819.25 571h10" /><path d="M1829.25 571h10" /><g class="non-terminal ">
<path d="M1839.25 571h0.0" /><path d="M1919.25 571h0.0" /><text class="comment" x="1879.25" y="576">out.d=&quot;6&quot;;</text></g></g><path d="M1938.5 571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 601h10.75" /><path d="M1927.75 601h10.75" /><g class="terminal ">
<path d="M1765.25 601h0.0" /><path d="M1827.75 601h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1765.25" y="590"></rect><text x="1796.5" y="605">seven</text></g><path d="M1827.75 601h10" /><path d="M1837.75 601h10" /><g class="non-terminal ">
<path d="M1847.75 601h0.0" /><path d="M1927.75 601h0.0" /><text class="comment" x="1887.75" y="606">out.d=&quot;7&quot;;</text></g></g><path d="M1938.5 601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 631h10.75" /><path d="M1927.75 631h10.75" /><g class="terminal ">
<path d="M1765.25 631h0.0" /><path d="M1827.75 631h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1765.25" y="620"></rect><text x="1796.5" y="635">eight</text></g><path d="M1827.75 631h10" /><path d="M1837.75 631h10" /><g class="non-terminal ">
<path d="M1847.75 631h0.0" /><path d="M1927.75 631h0.0" /><text class="comment" x="1887.75" y="636">out.d=&quot;8&quot;;</text></g></g><path d="M1938.5 631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1734.5 361a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 661h15.0" /><path d="M1923.5 661h15.0" /><g class="terminal ">
<path d="M1769.5 661h0.0" /><path d="M1823.5 661h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1769.5" y="650"></rect><text x="1796.5" y="665">nine</text></g><path d="M1823.5 661h10" /><path d="M1833.5 661h10" /><g class="non-terminal ">
<path d="M1843.5 661h0.0" /><path d="M1923.5 661h0.0" /><text class="comment" x="1883.5" y="666">out.d=&quot;9&quot;;</text></g></g><path d="M1938.5 661a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1958.5 361h10" /><path d="M1968.5 361h10" /><g class="non-terminal ">
<path d="M1978.5 361h0.0" /><path d="M2177.5 361h0.0" /><text class="comment" x="2078" y="366">out.d3=rules.singleDigit.d;</text></g><path d="M2177.5 361h10" /><path d="M2187.5 361h10" /><g>
<path d="M2197.5 361h0.0" /><path d="M3389.5 361h0.0" /><g>
<path d="M2197.5 361h0.0" /><path d="M3389.5 361h0.0" /><path d="M2197.5 361h20" /><g>
<path d="M2217.5 361h87.75" /><path d="M3281.75 361h87.75" /><g>
<path d="M2305.25 361h0.0" /><path d="M2759.75 361h0.0" /><g>
<path d="M2305.25 361h0.0" /><path d="M2759.75 361h0.0" /><path d="M2305.25 361h20" /><g>
<path d="M2325.25 361h12.75" /><path d="M2727.0 361h12.75" /><g class="terminal ">
<path d="M2338.0 361h0.0" /><path d="M2409.0 361h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2338" y="350"></rect><text x="2373.5" y="365">eleven</text></g><path d="M2409.0 361h10" /><path d="M2419.0 361h10" /><g class="terminal ">
<path d="M2429.0 361h0.0" /><path d="M2568.0 361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2429" y="350"></rect><text x="2498.5" y="365">!!out.dd1=&quot;1&quot;;</text></g><path d="M2568.0 361h10" /><path d="M2578.0 361h10" /><g class="terminal ">
<path d="M2588.0 361h0.0" /><path d="M2727.0 361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2588" y="350"></rect><text x="2657.5" y="365">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M2739.75 361h20" /><path d="M2305.25 361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 391h12.75" /><path d="M2727.0 391h12.75" /><g class="terminal ">
<path d="M2338.0 391h0.0" /><path d="M2409.0 391h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2338" y="380"></rect><text x="2373.5" y="395">twelve</text></g><path d="M2409.0 391h10" /><path d="M2419.0 391h10" /><g class="terminal ">
<path d="M2429.0 391h0.0" /><path d="M2568.0 391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2429" y="380"></rect><text x="2498.5" y="395">!!out.dd1=&quot;1&quot;;</text></g><path d="M2568.0 391h10" /><path d="M2578.0 391h10" /><g class="terminal ">
<path d="M2588.0 391h0.0" /><path d="M2727.0 391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2588" y="380"></rect><text x="2657.5" y="395">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M2739.75 391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 421h4.25" /><path d="M2735.5 421h4.25" /><g class="terminal ">
<path d="M2329.5 421h0.0" /><path d="M2417.5 421h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2329.5" y="410"></rect><text x="2373.5" y="425">thirteen</text></g><path d="M2417.5 421h10" /><path d="M2427.5 421h10" /><g class="terminal ">
<path d="M2437.5 421h0.0" /><path d="M2576.5 421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2437.5" y="410"></rect><text x="2507" y="425">!!out.dd1=&quot;1&quot;;</text></g><path d="M2576.5 421h10" /><path d="M2586.5 421h10" /><g class="terminal ">
<path d="M2596.5 421h0.0" /><path d="M2735.5 421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2596.5" y="410"></rect><text x="2666" y="425">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M2739.75 421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 451h4.25" /><path d="M2735.5 451h4.25" /><g class="terminal ">
<path d="M2329.5 451h0.0" /><path d="M2417.5 451h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2329.5" y="440"></rect><text x="2373.5" y="455">fourteen</text></g><path d="M2417.5 451h10" /><path d="M2427.5 451h10" /><g class="terminal ">
<path d="M2437.5 451h0.0" /><path d="M2576.5 451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2437.5" y="440"></rect><text x="2507" y="455">!!out.dd1=&quot;1&quot;;</text></g><path d="M2576.5 451h10" /><path d="M2586.5 451h10" /><g class="terminal ">
<path d="M2596.5 451h0.0" /><path d="M2735.5 451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2596.5" y="440"></rect><text x="2666" y="455">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M2739.75 451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 481h8.5" /><path d="M2731.25 481h8.5" /><g class="terminal ">
<path d="M2333.75 481h0.0" /><path d="M2413.25 481h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2333.75" y="470"></rect><text x="2373.5" y="485">fifteen</text></g><path d="M2413.25 481h10" /><path d="M2423.25 481h10" /><g class="terminal ">
<path d="M2433.25 481h0.0" /><path d="M2572.25 481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2433.25" y="470"></rect><text x="2502.75" y="485">!!out.dd1=&quot;1&quot;;</text></g><path d="M2572.25 481h10" /><path d="M2582.25 481h10" /><g class="terminal ">
<path d="M2592.25 481h0.0" /><path d="M2731.25 481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2592.25" y="470"></rect><text x="2661.75" y="485">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M2739.75 481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 511h8.5" /><path d="M2731.25 511h8.5" /><g class="terminal ">
<path d="M2333.75 511h0.0" /><path d="M2413.25 511h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2333.75" y="500"></rect><text x="2373.5" y="515">sixteen</text></g><path d="M2413.25 511h10" /><path d="M2423.25 511h10" /><g class="terminal ">
<path d="M2433.25 511h0.0" /><path d="M2572.25 511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2433.25" y="500"></rect><text x="2502.75" y="515">!!out.dd1=&quot;1&quot;;</text></g><path d="M2572.25 511h10" /><path d="M2582.25 511h10" /><g class="terminal ">
<path d="M2592.25 511h0.0" /><path d="M2731.25 511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2592.25" y="500"></rect><text x="2661.75" y="515">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M2739.75 511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 541h0.0" /><path d="M2739.75 541h0.0" /><g class="terminal ">
<path d="M2325.25 541h0.0" /><path d="M2421.75 541h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="2325.25" y="530"></rect><text x="2373.5" y="545">seventeen</text></g><path d="M2421.75 541h10" /><path d="M2431.75 541h10" /><g class="terminal ">
<path d="M2441.75 541h0.0" /><path d="M2580.75 541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2441.75" y="530"></rect><text x="2511.25" y="545">!!out.dd1=&quot;1&quot;;</text></g><path d="M2580.75 541h10" /><path d="M2590.75 541h10" /><g class="terminal ">
<path d="M2600.75 541h0.0" /><path d="M2739.75 541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2600.75" y="530"></rect><text x="2670.25" y="545">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M2739.75 541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 571h4.25" /><path d="M2735.5 571h4.25" /><g class="terminal ">
<path d="M2329.5 571h0.0" /><path d="M2417.5 571h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2329.5" y="560"></rect><text x="2373.5" y="575">eighteen</text></g><path d="M2417.5 571h10" /><path d="M2427.5 571h10" /><g class="terminal ">
<path d="M2437.5 571h0.0" /><path d="M2576.5 571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2437.5" y="560"></rect><text x="2507" y="575">!!out.dd1=&quot;1&quot;;</text></g><path d="M2576.5 571h10" /><path d="M2586.5 571h10" /><g class="terminal ">
<path d="M2596.5 571h0.0" /><path d="M2735.5 571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2596.5" y="560"></rect><text x="2666" y="575">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M2739.75 571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2305.25 361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2325.25 601h4.25" /><path d="M2735.5 601h4.25" /><g class="terminal ">
<path d="M2329.5 601h0.0" /><path d="M2417.5 601h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2329.5" y="590"></rect><text x="2373.5" y="605">nineteen</text></g><path d="M2417.5 601h10" /><path d="M2427.5 601h10" /><g class="terminal ">
<path d="M2437.5 601h0.0" /><path d="M2576.5 601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2437.5" y="590"></rect><text x="2507" y="605">!!out.dd1=&quot;1&quot;;</text></g><path d="M2576.5 601h10" /><path d="M2586.5 601h10" /><g class="terminal ">
<path d="M2596.5 601h0.0" /><path d="M2735.5 601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2596.5" y="590"></rect><text x="2666" y="605">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M2739.75 601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M2759.75 361h10" /><path d="M2769.75 361h10" /><g class="terminal ">
<path d="M2779.75 361h0.0" /><path d="M3020.75 361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="2779.75" y="350"></rect><text x="2900.25" y="365">!!out.dd1=rules.teens.dd1;</text></g><path d="M3020.75 361h10" /><path d="M3030.75 361h10" /><g class="terminal ">
<path d="M3040.75 361h0.0" /><path d="M3281.75 361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3040.75" y="350"></rect><text x="3161.25" y="365">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M3369.5 361h20" /><path d="M2197.5 361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2217.5 631h0.0" /><path d="M3369.5 631h0.0" /><g>
<path d="M2217.5 631h0.0" /><path d="M2493.0 631h0.0" /><g>
<path d="M2217.5 631h0.0" /><path d="M2493.0 631h0.0" /><path d="M2217.5 631h20" /><g>
<path d="M2237.5 631h4.25" /><path d="M2468.75 631h4.25" /><g class="terminal ">
<path d="M2241.75 631h0.0" /><path d="M2312.75 631h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2241.75" y="620"></rect><text x="2277.25" y="635">twenty</text></g><path d="M2312.75 631h10" /><path d="M2322.75 631h10" /><g class="non-terminal ">
<path d="M2332.75 631h0.0" /><path d="M2468.75 631h0.0" /><text class="comment" x="2400.75" y="636">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M2473.0 631h20" /><path d="M2217.5 631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 661h4.25" /><path d="M2468.75 661h4.25" /><g class="terminal ">
<path d="M2241.75 661h0.0" /><path d="M2312.75 661h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2241.75" y="650"></rect><text x="2277.25" y="665">thirty</text></g><path d="M2312.75 661h10" /><path d="M2322.75 661h10" /><g class="non-terminal ">
<path d="M2332.75 661h0.0" /><path d="M2468.75 661h0.0" /><text class="comment" x="2400.75" y="666">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M2473.0 661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 691h8.5" /><path d="M2464.5 691h8.5" /><g class="terminal ">
<path d="M2246.0 691h0.0" /><path d="M2308.5 691h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2246" y="680"></rect><text x="2277.25" y="695">forty</text></g><path d="M2308.5 691h10" /><path d="M2318.5 691h10" /><g class="non-terminal ">
<path d="M2328.5 691h0.0" /><path d="M2464.5 691h0.0" /><text class="comment" x="2396.5" y="696">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M2473.0 691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 721h8.5" /><path d="M2464.5 721h8.5" /><g class="terminal ">
<path d="M2246.0 721h0.0" /><path d="M2308.5 721h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2246" y="710"></rect><text x="2277.25" y="725">fifty</text></g><path d="M2308.5 721h10" /><path d="M2318.5 721h10" /><g class="non-terminal ">
<path d="M2328.5 721h0.0" /><path d="M2464.5 721h0.0" /><text class="comment" x="2396.5" y="726">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M2473.0 721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 751h8.5" /><path d="M2464.5 751h8.5" /><g class="terminal ">
<path d="M2246.0 751h0.0" /><path d="M2308.5 751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2246" y="740"></rect><text x="2277.25" y="755">sixty</text></g><path d="M2308.5 751h10" /><path d="M2318.5 751h10" /><g class="non-terminal ">
<path d="M2328.5 751h0.0" /><path d="M2464.5 751h0.0" /><text class="comment" x="2396.5" y="756">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M2473.0 751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 781h0.0" /><path d="M2473.0 781h0.0" /><g class="terminal ">
<path d="M2237.5 781h0.0" /><path d="M2317.0 781h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2237.5" y="770"></rect><text x="2277.25" y="785">seventy</text></g><path d="M2317.0 781h10" /><path d="M2327.0 781h10" /><g class="non-terminal ">
<path d="M2337.0 781h0.0" /><path d="M2473.0 781h0.0" /><text class="comment" x="2405" y="786">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M2473.0 781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 811h4.25" /><path d="M2468.75 811h4.25" /><g class="terminal ">
<path d="M2241.75 811h0.0" /><path d="M2312.75 811h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2241.75" y="800"></rect><text x="2277.25" y="815">eighty</text></g><path d="M2312.75 811h10" /><path d="M2322.75 811h10" /><g class="non-terminal ">
<path d="M2332.75 811h0.0" /><path d="M2468.75 811h0.0" /><text class="comment" x="2400.75" y="816">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M2473.0 811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2217.5 631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2237.5 841h4.25" /><path d="M2468.75 841h4.25" /><g class="terminal ">
<path d="M2241.75 841h0.0" /><path d="M2312.75 841h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2241.75" y="830"></rect><text x="2277.25" y="845">ninety</text></g><path d="M2312.75 841h10" /><path d="M2322.75 841h10" /><g class="non-terminal ">
<path d="M2332.75 841h0.0" /><path d="M2468.75 841h0.0" /><text class="comment" x="2400.75" y="846">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M2473.0 841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M2493.0 631h10" /><path d="M2503.0 631h10" /><g>
<path d="M2513.0 631h0.0" /><path d="M2737.0 631h0.0" /><g>
<path d="M2513.0 631h0.0" /><path d="M2737.0 631h0.0" /><path d="M2513.0 631h20" /><g>
<path d="M2533.0 631h0.0" /><path d="M2717.0 631h0.0" /><g>
<path d="M2533.0 631h0.0" /><path d="M2627.0 631h0.0" /><path d="M2533.0 631h20" /><g>
<path d="M2553.0 631h0.0" /><path d="M2607.0 631h0.0" /><g class="terminal ">
<path d="M2553.0 631h0.0" /><path d="M2607.0 631h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2553" y="620"></rect><text x="2580" y="635">zero</text></g></g><path d="M2607.0 631h20" /><path d="M2533.0 631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2553.0 661h8.5" /><path d="M2598.5 661h8.5" /><g class="terminal ">
<path d="M2561.5 661h0.0" /><path d="M2598.5 661h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2561.5" y="650"></rect><text x="2580" y="665">oh</text></g></g><path d="M2607.0 661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2627.0 631h10" /><g class="non-terminal ">
<path d="M2637.0 631h0.0" /><path d="M2717.0 631h0.0" /><text class="comment" x="2677" y="636">out.d=&quot;0&quot;;</text></g></g><path d="M2717.0 631h20" /><path d="M2513.0 631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 691h19.25" /><path d="M2697.75 691h19.25" /><g class="terminal ">
<path d="M2552.25 691h0.0" /><path d="M2597.75 691h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2552.25" y="680"></rect><text x="2575" y="695">one</text></g><path d="M2597.75 691h10" /><path d="M2607.75 691h10" /><g class="non-terminal ">
<path d="M2617.75 691h0.0" /><path d="M2697.75 691h0.0" /><text class="comment" x="2657.75" y="696">out.d=&quot;1&quot;;</text></g></g><path d="M2717.0 691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 721h19.25" /><path d="M2697.75 721h19.25" /><g class="terminal ">
<path d="M2552.25 721h0.0" /><path d="M2597.75 721h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2552.25" y="710"></rect><text x="2575" y="725">two</text></g><path d="M2597.75 721h10" /><path d="M2607.75 721h10" /><g class="non-terminal ">
<path d="M2617.75 721h0.0" /><path d="M2697.75 721h0.0" /><text class="comment" x="2657.75" y="726">out.d=&quot;2&quot;;</text></g></g><path d="M2717.0 721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 751h10.75" /><path d="M2706.25 751h10.75" /><g class="terminal ">
<path d="M2543.75 751h0.0" /><path d="M2606.25 751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2543.75" y="740"></rect><text x="2575" y="755">three</text></g><path d="M2606.25 751h10" /><path d="M2616.25 751h10" /><g class="non-terminal ">
<path d="M2626.25 751h0.0" /><path d="M2706.25 751h0.0" /><text class="comment" x="2666.25" y="756">out.d=&quot;3&quot;;</text></g></g><path d="M2717.0 751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 781h15.0" /><path d="M2702.0 781h15.0" /><g class="terminal ">
<path d="M2548.0 781h0.0" /><path d="M2602.0 781h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2548" y="770"></rect><text x="2575" y="785">four</text></g><path d="M2602.0 781h10" /><path d="M2612.0 781h10" /><g class="non-terminal ">
<path d="M2622.0 781h0.0" /><path d="M2702.0 781h0.0" /><text class="comment" x="2662" y="786">out.d=&quot;4&quot;;</text></g></g><path d="M2717.0 781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 811h15.0" /><path d="M2702.0 811h15.0" /><g class="terminal ">
<path d="M2548.0 811h0.0" /><path d="M2602.0 811h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2548" y="800"></rect><text x="2575" y="815">five</text></g><path d="M2602.0 811h10" /><path d="M2612.0 811h10" /><g class="non-terminal ">
<path d="M2622.0 811h0.0" /><path d="M2702.0 811h0.0" /><text class="comment" x="2662" y="816">out.d=&quot;5&quot;;</text></g></g><path d="M2717.0 811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 841h19.25" /><path d="M2697.75 841h19.25" /><g class="terminal ">
<path d="M2552.25 841h0.0" /><path d="M2597.75 841h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2552.25" y="830"></rect><text x="2575" y="845">six</text></g><path d="M2597.75 841h10" /><path d="M2607.75 841h10" /><g class="non-terminal ">
<path d="M2617.75 841h0.0" /><path d="M2697.75 841h0.0" /><text class="comment" x="2657.75" y="846">out.d=&quot;6&quot;;</text></g></g><path d="M2717.0 841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 871h10.75" /><path d="M2706.25 871h10.75" /><g class="terminal ">
<path d="M2543.75 871h0.0" /><path d="M2606.25 871h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2543.75" y="860"></rect><text x="2575" y="875">seven</text></g><path d="M2606.25 871h10" /><path d="M2616.25 871h10" /><g class="non-terminal ">
<path d="M2626.25 871h0.0" /><path d="M2706.25 871h0.0" /><text class="comment" x="2666.25" y="876">out.d=&quot;7&quot;;</text></g></g><path d="M2717.0 871a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 901h10.75" /><path d="M2706.25 901h10.75" /><g class="terminal ">
<path d="M2543.75 901h0.0" /><path d="M2606.25 901h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2543.75" y="890"></rect><text x="2575" y="905">eight</text></g><path d="M2606.25 901h10" /><path d="M2616.25 901h10" /><g class="non-terminal ">
<path d="M2626.25 901h0.0" /><path d="M2706.25 901h0.0" /><text class="comment" x="2666.25" y="906">out.d=&quot;8&quot;;</text></g></g><path d="M2717.0 901a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2513.0 631a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2533.0 931h15.0" /><path d="M2702.0 931h15.0" /><g class="terminal ">
<path d="M2548.0 931h0.0" /><path d="M2602.0 931h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2548" y="920"></rect><text x="2575" y="935">nine</text></g><path d="M2602.0 931h10" /><path d="M2612.0 931h10" /><g class="non-terminal ">
<path d="M2622.0 931h0.0" /><path d="M2702.0 931h0.0" /><text class="comment" x="2662" y="936">out.d=&quot;9&quot;;</text></g></g><path d="M2717.0 931a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2737.0 631h10" /><path d="M2747.0 631h10" /><g class="terminal ">
<path d="M2757.0 631h0.0" /><path d="M3083.0 631h0.0" /><rect height="22" rx="10" ry="10" width="326" x="2757" y="620"></rect><text x="2920" y="635">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M3083.0 631h10" /><path d="M3093.0 631h10" /><g class="terminal ">
<path d="M3103.0 631h0.0" /><path d="M3369.5 631h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="3103" y="620"></rect><text x="3236.25" y="635">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M3369.5 631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M3389.5 361h10" /><path d="M3399.5 361h10" /><g class="terminal ">
<path d="M3409.5 361h0.0" /><path d="M3693.0 361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3409.5" y="350"></rect><text x="3551.25" y="365">!!out.d4=rules.doubleDigit.dd1;</text></g><path d="M3693.0 361h10" /><path d="M3703.0 361h10" /><g class="terminal ">
<path d="M3713.0 361h0.0" /><path d="M3996.5 361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3713" y="350"></rect><text x="3854.75" y="365">out.d5=rules.doubleDigit.dd2;!!</text></g></g><path d="M4443.0 361a10 10 0 0 0 10 -10v-310a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v910a10 10 0 0 0 10 10" /><g>
<path d="M362.0 961h446.5" /><path d="M3996.5 961h446.5" /><g>
<path d="M808.5 961h0.0" /><path d="M1032.5 961h0.0" /><g>
<path d="M808.5 961h0.0" /><path d="M1032.5 961h0.0" /><path d="M808.5 961h20" /><g>
<path d="M828.5 961h0.0" /><path d="M1012.5 961h0.0" /><g>
<path d="M828.5 961h0.0" /><path d="M922.5 961h0.0" /><path d="M828.5 961h20" /><g>
<path d="M848.5 961h0.0" /><path d="M902.5 961h0.0" /><g class="terminal ">
<path d="M848.5 961h0.0" /><path d="M902.5 961h0.0" /><rect height="22" rx="10" ry="10" width="54" x="848.5" y="950"></rect><text x="875.5" y="965">zero</text></g></g><path d="M902.5 961h20" /><path d="M828.5 961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M848.5 991h8.5" /><path d="M894.0 991h8.5" /><g class="terminal ">
<path d="M857.0 991h0.0" /><path d="M894.0 991h0.0" /><rect height="22" rx="10" ry="10" width="37" x="857" y="980"></rect><text x="875.5" y="995">oh</text></g></g><path d="M902.5 991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M922.5 961h10" /><g class="non-terminal ">
<path d="M932.5 961h0.0" /><path d="M1012.5 961h0.0" /><text class="comment" x="972.5" y="966">out.d=&quot;0&quot;;</text></g></g><path d="M1012.5 961h20" /><path d="M808.5 961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1021h19.25" /><path d="M993.25 1021h19.25" /><g class="terminal ">
<path d="M847.75 1021h0.0" /><path d="M893.25 1021h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1010"></rect><text x="870.5" y="1025">one</text></g><path d="M893.25 1021h10" /><path d="M903.25 1021h10" /><g class="non-terminal ">
<path d="M913.25 1021h0.0" /><path d="M993.25 1021h0.0" /><text class="comment" x="953.25" y="1026">out.d=&quot;1&quot;;</text></g></g><path d="M1012.5 1021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1051h19.25" /><path d="M993.25 1051h19.25" /><g class="terminal ">
<path d="M847.75 1051h0.0" /><path d="M893.25 1051h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1040"></rect><text x="870.5" y="1055">two</text></g><path d="M893.25 1051h10" /><path d="M903.25 1051h10" /><g class="non-terminal ">
<path d="M913.25 1051h0.0" /><path d="M993.25 1051h0.0" /><text class="comment" x="953.25" y="1056">out.d=&quot;2&quot;;</text></g></g><path d="M1012.5 1051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1081h10.75" /><path d="M1001.75 1081h10.75" /><g class="terminal ">
<path d="M839.25 1081h0.0" /><path d="M901.75 1081h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1070"></rect><text x="870.5" y="1085">three</text></g><path d="M901.75 1081h10" /><path d="M911.75 1081h10" /><g class="non-terminal ">
<path d="M921.75 1081h0.0" /><path d="M1001.75 1081h0.0" /><text class="comment" x="961.75" y="1086">out.d=&quot;3&quot;;</text></g></g><path d="M1012.5 1081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1111h15.0" /><path d="M997.5 1111h15.0" /><g class="terminal ">
<path d="M843.5 1111h0.0" /><path d="M897.5 1111h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1100"></rect><text x="870.5" y="1115">four</text></g><path d="M897.5 1111h10" /><path d="M907.5 1111h10" /><g class="non-terminal ">
<path d="M917.5 1111h0.0" /><path d="M997.5 1111h0.0" /><text class="comment" x="957.5" y="1116">out.d=&quot;4&quot;;</text></g></g><path d="M1012.5 1111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1141h15.0" /><path d="M997.5 1141h15.0" /><g class="terminal ">
<path d="M843.5 1141h0.0" /><path d="M897.5 1141h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1130"></rect><text x="870.5" y="1145">five</text></g><path d="M897.5 1141h10" /><path d="M907.5 1141h10" /><g class="non-terminal ">
<path d="M917.5 1141h0.0" /><path d="M997.5 1141h0.0" /><text class="comment" x="957.5" y="1146">out.d=&quot;5&quot;;</text></g></g><path d="M1012.5 1141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1171h19.25" /><path d="M993.25 1171h19.25" /><g class="terminal ">
<path d="M847.75 1171h0.0" /><path d="M893.25 1171h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1160"></rect><text x="870.5" y="1175">six</text></g><path d="M893.25 1171h10" /><path d="M903.25 1171h10" /><g class="non-terminal ">
<path d="M913.25 1171h0.0" /><path d="M993.25 1171h0.0" /><text class="comment" x="953.25" y="1176">out.d=&quot;6&quot;;</text></g></g><path d="M1012.5 1171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1201h10.75" /><path d="M1001.75 1201h10.75" /><g class="terminal ">
<path d="M839.25 1201h0.0" /><path d="M901.75 1201h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1190"></rect><text x="870.5" y="1205">seven</text></g><path d="M901.75 1201h10" /><path d="M911.75 1201h10" /><g class="non-terminal ">
<path d="M921.75 1201h0.0" /><path d="M1001.75 1201h0.0" /><text class="comment" x="961.75" y="1206">out.d=&quot;7&quot;;</text></g></g><path d="M1012.5 1201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1231h10.75" /><path d="M1001.75 1231h10.75" /><g class="terminal ">
<path d="M839.25 1231h0.0" /><path d="M901.75 1231h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1220"></rect><text x="870.5" y="1235">eight</text></g><path d="M901.75 1231h10" /><path d="M911.75 1231h10" /><g class="non-terminal ">
<path d="M921.75 1231h0.0" /><path d="M1001.75 1231h0.0" /><text class="comment" x="961.75" y="1236">out.d=&quot;8&quot;;</text></g></g><path d="M1012.5 1231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M808.5 961a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1261h15.0" /><path d="M997.5 1261h15.0" /><g class="terminal ">
<path d="M843.5 1261h0.0" /><path d="M897.5 1261h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1250"></rect><text x="870.5" y="1265">nine</text></g><path d="M897.5 1261h10" /><path d="M907.5 1261h10" /><g class="non-terminal ">
<path d="M917.5 1261h0.0" /><path d="M997.5 1261h0.0" /><text class="comment" x="957.5" y="1266">out.d=&quot;9&quot;;</text></g></g><path d="M1012.5 1261a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1032.5 961h10" /><path d="M1042.5 961h10" /><g class="non-terminal ">
<path d="M1052.5 961h0.0" /><path d="M1251.5 961h0.0" /><text class="comment" x="1152" y="966">out.d1=rules.singleDigit.d;</text></g><path d="M1251.5 961h10" /><path d="M1261.5 961h10" /><g>
<path d="M1271.5 961h0.0" /><path d="M1495.5 961h0.0" /><g>
<path d="M1271.5 961h0.0" /><path d="M1495.5 961h0.0" /><path d="M1271.5 961h20" /><g>
<path d="M1291.5 961h0.0" /><path d="M1475.5 961h0.0" /><g>
<path d="M1291.5 961h0.0" /><path d="M1385.5 961h0.0" /><path d="M1291.5 961h20" /><g>
<path d="M1311.5 961h0.0" /><path d="M1365.5 961h0.0" /><g class="terminal ">
<path d="M1311.5 961h0.0" /><path d="M1365.5 961h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1311.5" y="950"></rect><text x="1338.5" y="965">zero</text></g></g><path d="M1365.5 961h20" /><path d="M1291.5 961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 991h8.5" /><path d="M1357.0 991h8.5" /><g class="terminal ">
<path d="M1320.0 991h0.0" /><path d="M1357.0 991h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1320" y="980"></rect><text x="1338.5" y="995">oh</text></g></g><path d="M1365.5 991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1385.5 961h10" /><g class="non-terminal ">
<path d="M1395.5 961h0.0" /><path d="M1475.5 961h0.0" /><text class="comment" x="1435.5" y="966">out.d=&quot;0&quot;;</text></g></g><path d="M1475.5 961h20" /><path d="M1271.5 961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1021h19.25" /><path d="M1456.25 1021h19.25" /><g class="terminal ">
<path d="M1310.75 1021h0.0" /><path d="M1356.25 1021h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="1010"></rect><text x="1333.5" y="1025">one</text></g><path d="M1356.25 1021h10" /><path d="M1366.25 1021h10" /><g class="non-terminal ">
<path d="M1376.25 1021h0.0" /><path d="M1456.25 1021h0.0" /><text class="comment" x="1416.25" y="1026">out.d=&quot;1&quot;;</text></g></g><path d="M1475.5 1021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1051h19.25" /><path d="M1456.25 1051h19.25" /><g class="terminal ">
<path d="M1310.75 1051h0.0" /><path d="M1356.25 1051h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="1040"></rect><text x="1333.5" y="1055">two</text></g><path d="M1356.25 1051h10" /><path d="M1366.25 1051h10" /><g class="non-terminal ">
<path d="M1376.25 1051h0.0" /><path d="M1456.25 1051h0.0" /><text class="comment" x="1416.25" y="1056">out.d=&quot;2&quot;;</text></g></g><path d="M1475.5 1051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1081h10.75" /><path d="M1464.75 1081h10.75" /><g class="terminal ">
<path d="M1302.25 1081h0.0" /><path d="M1364.75 1081h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="1070"></rect><text x="1333.5" y="1085">three</text></g><path d="M1364.75 1081h10" /><path d="M1374.75 1081h10" /><g class="non-terminal ">
<path d="M1384.75 1081h0.0" /><path d="M1464.75 1081h0.0" /><text class="comment" x="1424.75" y="1086">out.d=&quot;3&quot;;</text></g></g><path d="M1475.5 1081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1111h15.0" /><path d="M1460.5 1111h15.0" /><g class="terminal ">
<path d="M1306.5 1111h0.0" /><path d="M1360.5 1111h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="1100"></rect><text x="1333.5" y="1115">four</text></g><path d="M1360.5 1111h10" /><path d="M1370.5 1111h10" /><g class="non-terminal ">
<path d="M1380.5 1111h0.0" /><path d="M1460.5 1111h0.0" /><text class="comment" x="1420.5" y="1116">out.d=&quot;4&quot;;</text></g></g><path d="M1475.5 1111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1141h15.0" /><path d="M1460.5 1141h15.0" /><g class="terminal ">
<path d="M1306.5 1141h0.0" /><path d="M1360.5 1141h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="1130"></rect><text x="1333.5" y="1145">five</text></g><path d="M1360.5 1141h10" /><path d="M1370.5 1141h10" /><g class="non-terminal ">
<path d="M1380.5 1141h0.0" /><path d="M1460.5 1141h0.0" /><text class="comment" x="1420.5" y="1146">out.d=&quot;5&quot;;</text></g></g><path d="M1475.5 1141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1171h19.25" /><path d="M1456.25 1171h19.25" /><g class="terminal ">
<path d="M1310.75 1171h0.0" /><path d="M1356.25 1171h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1310.75" y="1160"></rect><text x="1333.5" y="1175">six</text></g><path d="M1356.25 1171h10" /><path d="M1366.25 1171h10" /><g class="non-terminal ">
<path d="M1376.25 1171h0.0" /><path d="M1456.25 1171h0.0" /><text class="comment" x="1416.25" y="1176">out.d=&quot;6&quot;;</text></g></g><path d="M1475.5 1171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1201h10.75" /><path d="M1464.75 1201h10.75" /><g class="terminal ">
<path d="M1302.25 1201h0.0" /><path d="M1364.75 1201h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="1190"></rect><text x="1333.5" y="1205">seven</text></g><path d="M1364.75 1201h10" /><path d="M1374.75 1201h10" /><g class="non-terminal ">
<path d="M1384.75 1201h0.0" /><path d="M1464.75 1201h0.0" /><text class="comment" x="1424.75" y="1206">out.d=&quot;7&quot;;</text></g></g><path d="M1475.5 1201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1231h10.75" /><path d="M1464.75 1231h10.75" /><g class="terminal ">
<path d="M1302.25 1231h0.0" /><path d="M1364.75 1231h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1302.25" y="1220"></rect><text x="1333.5" y="1235">eight</text></g><path d="M1364.75 1231h10" /><path d="M1374.75 1231h10" /><g class="non-terminal ">
<path d="M1384.75 1231h0.0" /><path d="M1464.75 1231h0.0" /><text class="comment" x="1424.75" y="1236">out.d=&quot;8&quot;;</text></g></g><path d="M1475.5 1231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1271.5 961a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1261h15.0" /><path d="M1460.5 1261h15.0" /><g class="terminal ">
<path d="M1306.5 1261h0.0" /><path d="M1360.5 1261h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1306.5" y="1250"></rect><text x="1333.5" y="1265">nine</text></g><path d="M1360.5 1261h10" /><path d="M1370.5 1261h10" /><g class="non-terminal ">
<path d="M1380.5 1261h0.0" /><path d="M1460.5 1261h0.0" /><text class="comment" x="1420.5" y="1266">out.d=&quot;9&quot;;</text></g></g><path d="M1475.5 1261a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1495.5 961h10" /><path d="M1505.5 961h10" /><g class="non-terminal ">
<path d="M1515.5 961h0.0" /><path d="M1714.5 961h0.0" /><text class="comment" x="1615" y="966">out.d2=rules.singleDigit.d;</text></g><path d="M1714.5 961h10" /><path d="M1724.5 961h10" /><g>
<path d="M1734.5 961h0.0" /><path d="M2926.5 961h0.0" /><g>
<path d="M1734.5 961h0.0" /><path d="M2926.5 961h0.0" /><path d="M1734.5 961h20" /><g>
<path d="M1754.5 961h87.75" /><path d="M2818.75 961h87.75" /><g>
<path d="M1842.25 961h0.0" /><path d="M2296.75 961h0.0" /><g>
<path d="M1842.25 961h0.0" /><path d="M2296.75 961h0.0" /><path d="M1842.25 961h20" /><g>
<path d="M1862.25 961h12.75" /><path d="M2264.0 961h12.75" /><g class="terminal ">
<path d="M1875.0 961h0.0" /><path d="M1946.0 961h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1875" y="950"></rect><text x="1910.5" y="965">eleven</text></g><path d="M1946.0 961h10" /><path d="M1956.0 961h10" /><g class="terminal ">
<path d="M1966.0 961h0.0" /><path d="M2105.0 961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1966" y="950"></rect><text x="2035.5" y="965">!!out.dd1=&quot;1&quot;;</text></g><path d="M2105.0 961h10" /><path d="M2115.0 961h10" /><g class="terminal ">
<path d="M2125.0 961h0.0" /><path d="M2264.0 961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2125" y="950"></rect><text x="2194.5" y="965">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M2276.75 961h20" /><path d="M1842.25 961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 991h12.75" /><path d="M2264.0 991h12.75" /><g class="terminal ">
<path d="M1875.0 991h0.0" /><path d="M1946.0 991h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1875" y="980"></rect><text x="1910.5" y="995">twelve</text></g><path d="M1946.0 991h10" /><path d="M1956.0 991h10" /><g class="terminal ">
<path d="M1966.0 991h0.0" /><path d="M2105.0 991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1966" y="980"></rect><text x="2035.5" y="995">!!out.dd1=&quot;1&quot;;</text></g><path d="M2105.0 991h10" /><path d="M2115.0 991h10" /><g class="terminal ">
<path d="M2125.0 991h0.0" /><path d="M2264.0 991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2125" y="980"></rect><text x="2194.5" y="995">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M2276.75 991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1021h4.25" /><path d="M2272.5 1021h4.25" /><g class="terminal ">
<path d="M1866.5 1021h0.0" /><path d="M1954.5 1021h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1866.5" y="1010"></rect><text x="1910.5" y="1025">thirteen</text></g><path d="M1954.5 1021h10" /><path d="M1964.5 1021h10" /><g class="terminal ">
<path d="M1974.5 1021h0.0" /><path d="M2113.5 1021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1974.5" y="1010"></rect><text x="2044" y="1025">!!out.dd1=&quot;1&quot;;</text></g><path d="M2113.5 1021h10" /><path d="M2123.5 1021h10" /><g class="terminal ">
<path d="M2133.5 1021h0.0" /><path d="M2272.5 1021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2133.5" y="1010"></rect><text x="2203" y="1025">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M2276.75 1021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1051h4.25" /><path d="M2272.5 1051h4.25" /><g class="terminal ">
<path d="M1866.5 1051h0.0" /><path d="M1954.5 1051h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1866.5" y="1040"></rect><text x="1910.5" y="1055">fourteen</text></g><path d="M1954.5 1051h10" /><path d="M1964.5 1051h10" /><g class="terminal ">
<path d="M1974.5 1051h0.0" /><path d="M2113.5 1051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1974.5" y="1040"></rect><text x="2044" y="1055">!!out.dd1=&quot;1&quot;;</text></g><path d="M2113.5 1051h10" /><path d="M2123.5 1051h10" /><g class="terminal ">
<path d="M2133.5 1051h0.0" /><path d="M2272.5 1051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2133.5" y="1040"></rect><text x="2203" y="1055">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M2276.75 1051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1081h8.5" /><path d="M2268.25 1081h8.5" /><g class="terminal ">
<path d="M1870.75 1081h0.0" /><path d="M1950.25 1081h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1870.75" y="1070"></rect><text x="1910.5" y="1085">fifteen</text></g><path d="M1950.25 1081h10" /><path d="M1960.25 1081h10" /><g class="terminal ">
<path d="M1970.25 1081h0.0" /><path d="M2109.25 1081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1970.25" y="1070"></rect><text x="2039.75" y="1085">!!out.dd1=&quot;1&quot;;</text></g><path d="M2109.25 1081h10" /><path d="M2119.25 1081h10" /><g class="terminal ">
<path d="M2129.25 1081h0.0" /><path d="M2268.25 1081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2129.25" y="1070"></rect><text x="2198.75" y="1085">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M2276.75 1081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1111h8.5" /><path d="M2268.25 1111h8.5" /><g class="terminal ">
<path d="M1870.75 1111h0.0" /><path d="M1950.25 1111h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1870.75" y="1100"></rect><text x="1910.5" y="1115">sixteen</text></g><path d="M1950.25 1111h10" /><path d="M1960.25 1111h10" /><g class="terminal ">
<path d="M1970.25 1111h0.0" /><path d="M2109.25 1111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1970.25" y="1100"></rect><text x="2039.75" y="1115">!!out.dd1=&quot;1&quot;;</text></g><path d="M2109.25 1111h10" /><path d="M2119.25 1111h10" /><g class="terminal ">
<path d="M2129.25 1111h0.0" /><path d="M2268.25 1111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2129.25" y="1100"></rect><text x="2198.75" y="1115">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M2276.75 1111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1141h0.0" /><path d="M2276.75 1141h0.0" /><g class="terminal ">
<path d="M1862.25 1141h0.0" /><path d="M1958.75 1141h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="1862.25" y="1130"></rect><text x="1910.5" y="1145">seventeen</text></g><path d="M1958.75 1141h10" /><path d="M1968.75 1141h10" /><g class="terminal ">
<path d="M1978.75 1141h0.0" /><path d="M2117.75 1141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1978.75" y="1130"></rect><text x="2048.25" y="1145">!!out.dd1=&quot;1&quot;;</text></g><path d="M2117.75 1141h10" /><path d="M2127.75 1141h10" /><g class="terminal ">
<path d="M2137.75 1141h0.0" /><path d="M2276.75 1141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2137.75" y="1130"></rect><text x="2207.25" y="1145">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M2276.75 1141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1171h4.25" /><path d="M2272.5 1171h4.25" /><g class="terminal ">
<path d="M1866.5 1171h0.0" /><path d="M1954.5 1171h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1866.5" y="1160"></rect><text x="1910.5" y="1175">eighteen</text></g><path d="M1954.5 1171h10" /><path d="M1964.5 1171h10" /><g class="terminal ">
<path d="M1974.5 1171h0.0" /><path d="M2113.5 1171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1974.5" y="1160"></rect><text x="2044" y="1175">!!out.dd1=&quot;1&quot;;</text></g><path d="M2113.5 1171h10" /><path d="M2123.5 1171h10" /><g class="terminal ">
<path d="M2133.5 1171h0.0" /><path d="M2272.5 1171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2133.5" y="1160"></rect><text x="2203" y="1175">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M2276.75 1171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1842.25 961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1862.25 1201h4.25" /><path d="M2272.5 1201h4.25" /><g class="terminal ">
<path d="M1866.5 1201h0.0" /><path d="M1954.5 1201h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1866.5" y="1190"></rect><text x="1910.5" y="1205">nineteen</text></g><path d="M1954.5 1201h10" /><path d="M1964.5 1201h10" /><g class="terminal ">
<path d="M1974.5 1201h0.0" /><path d="M2113.5 1201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1974.5" y="1190"></rect><text x="2044" y="1205">!!out.dd1=&quot;1&quot;;</text></g><path d="M2113.5 1201h10" /><path d="M2123.5 1201h10" /><g class="terminal ">
<path d="M2133.5 1201h0.0" /><path d="M2272.5 1201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2133.5" y="1190"></rect><text x="2203" y="1205">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M2276.75 1201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M2296.75 961h10" /><path d="M2306.75 961h10" /><g class="terminal ">
<path d="M2316.75 961h0.0" /><path d="M2557.75 961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="2316.75" y="950"></rect><text x="2437.25" y="965">!!out.dd1=rules.teens.dd1;</text></g><path d="M2557.75 961h10" /><path d="M2567.75 961h10" /><g class="terminal ">
<path d="M2577.75 961h0.0" /><path d="M2818.75 961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="2577.75" y="950"></rect><text x="2698.25" y="965">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M2906.5 961h20" /><path d="M1734.5 961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1754.5 1231h0.0" /><path d="M2906.5 1231h0.0" /><g>
<path d="M1754.5 1231h0.0" /><path d="M2030.0 1231h0.0" /><g>
<path d="M1754.5 1231h0.0" /><path d="M2030.0 1231h0.0" /><path d="M1754.5 1231h20" /><g>
<path d="M1774.5 1231h4.25" /><path d="M2005.75 1231h4.25" /><g class="terminal ">
<path d="M1778.75 1231h0.0" /><path d="M1849.75 1231h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1778.75" y="1220"></rect><text x="1814.25" y="1235">twenty</text></g><path d="M1849.75 1231h10" /><path d="M1859.75 1231h10" /><g class="non-terminal ">
<path d="M1869.75 1231h0.0" /><path d="M2005.75 1231h0.0" /><text class="comment" x="1937.75" y="1236">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M2010.0 1231h20" /><path d="M1754.5 1231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1261h4.25" /><path d="M2005.75 1261h4.25" /><g class="terminal ">
<path d="M1778.75 1261h0.0" /><path d="M1849.75 1261h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1778.75" y="1250"></rect><text x="1814.25" y="1265">thirty</text></g><path d="M1849.75 1261h10" /><path d="M1859.75 1261h10" /><g class="non-terminal ">
<path d="M1869.75 1261h0.0" /><path d="M2005.75 1261h0.0" /><text class="comment" x="1937.75" y="1266">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M2010.0 1261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1291h8.5" /><path d="M2001.5 1291h8.5" /><g class="terminal ">
<path d="M1783.0 1291h0.0" /><path d="M1845.5 1291h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1783" y="1280"></rect><text x="1814.25" y="1295">forty</text></g><path d="M1845.5 1291h10" /><path d="M1855.5 1291h10" /><g class="non-terminal ">
<path d="M1865.5 1291h0.0" /><path d="M2001.5 1291h0.0" /><text class="comment" x="1933.5" y="1296">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M2010.0 1291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1321h8.5" /><path d="M2001.5 1321h8.5" /><g class="terminal ">
<path d="M1783.0 1321h0.0" /><path d="M1845.5 1321h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1783" y="1310"></rect><text x="1814.25" y="1325">fifty</text></g><path d="M1845.5 1321h10" /><path d="M1855.5 1321h10" /><g class="non-terminal ">
<path d="M1865.5 1321h0.0" /><path d="M2001.5 1321h0.0" /><text class="comment" x="1933.5" y="1326">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M2010.0 1321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1351h8.5" /><path d="M2001.5 1351h8.5" /><g class="terminal ">
<path d="M1783.0 1351h0.0" /><path d="M1845.5 1351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1783" y="1340"></rect><text x="1814.25" y="1355">sixty</text></g><path d="M1845.5 1351h10" /><path d="M1855.5 1351h10" /><g class="non-terminal ">
<path d="M1865.5 1351h0.0" /><path d="M2001.5 1351h0.0" /><text class="comment" x="1933.5" y="1356">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M2010.0 1351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1381h0.0" /><path d="M2010.0 1381h0.0" /><g class="terminal ">
<path d="M1774.5 1381h0.0" /><path d="M1854.0 1381h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1774.5" y="1370"></rect><text x="1814.25" y="1385">seventy</text></g><path d="M1854.0 1381h10" /><path d="M1864.0 1381h10" /><g class="non-terminal ">
<path d="M1874.0 1381h0.0" /><path d="M2010.0 1381h0.0" /><text class="comment" x="1942" y="1386">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M2010.0 1381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1411h4.25" /><path d="M2005.75 1411h4.25" /><g class="terminal ">
<path d="M1778.75 1411h0.0" /><path d="M1849.75 1411h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1778.75" y="1400"></rect><text x="1814.25" y="1415">eighty</text></g><path d="M1849.75 1411h10" /><path d="M1859.75 1411h10" /><g class="non-terminal ">
<path d="M1869.75 1411h0.0" /><path d="M2005.75 1411h0.0" /><text class="comment" x="1937.75" y="1416">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M2010.0 1411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1754.5 1231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1774.5 1441h4.25" /><path d="M2005.75 1441h4.25" /><g class="terminal ">
<path d="M1778.75 1441h0.0" /><path d="M1849.75 1441h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1778.75" y="1430"></rect><text x="1814.25" y="1445">ninety</text></g><path d="M1849.75 1441h10" /><path d="M1859.75 1441h10" /><g class="non-terminal ">
<path d="M1869.75 1441h0.0" /><path d="M2005.75 1441h0.0" /><text class="comment" x="1937.75" y="1446">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M2010.0 1441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M2030.0 1231h10" /><path d="M2040.0 1231h10" /><g>
<path d="M2050.0 1231h0.0" /><path d="M2274.0 1231h0.0" /><g>
<path d="M2050.0 1231h0.0" /><path d="M2274.0 1231h0.0" /><path d="M2050.0 1231h20" /><g>
<path d="M2070.0 1231h0.0" /><path d="M2254.0 1231h0.0" /><g>
<path d="M2070.0 1231h0.0" /><path d="M2164.0 1231h0.0" /><path d="M2070.0 1231h20" /><g>
<path d="M2090.0 1231h0.0" /><path d="M2144.0 1231h0.0" /><g class="terminal ">
<path d="M2090.0 1231h0.0" /><path d="M2144.0 1231h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2090" y="1220"></rect><text x="2117" y="1235">zero</text></g></g><path d="M2144.0 1231h20" /><path d="M2070.0 1231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2090.0 1261h8.5" /><path d="M2135.5 1261h8.5" /><g class="terminal ">
<path d="M2098.5 1261h0.0" /><path d="M2135.5 1261h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2098.5" y="1250"></rect><text x="2117" y="1265">oh</text></g></g><path d="M2144.0 1261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2164.0 1231h10" /><g class="non-terminal ">
<path d="M2174.0 1231h0.0" /><path d="M2254.0 1231h0.0" /><text class="comment" x="2214" y="1236">out.d=&quot;0&quot;;</text></g></g><path d="M2254.0 1231h20" /><path d="M2050.0 1231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1291h19.25" /><path d="M2234.75 1291h19.25" /><g class="terminal ">
<path d="M2089.25 1291h0.0" /><path d="M2134.75 1291h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2089.25" y="1280"></rect><text x="2112" y="1295">one</text></g><path d="M2134.75 1291h10" /><path d="M2144.75 1291h10" /><g class="non-terminal ">
<path d="M2154.75 1291h0.0" /><path d="M2234.75 1291h0.0" /><text class="comment" x="2194.75" y="1296">out.d=&quot;1&quot;;</text></g></g><path d="M2254.0 1291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1321h19.25" /><path d="M2234.75 1321h19.25" /><g class="terminal ">
<path d="M2089.25 1321h0.0" /><path d="M2134.75 1321h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2089.25" y="1310"></rect><text x="2112" y="1325">two</text></g><path d="M2134.75 1321h10" /><path d="M2144.75 1321h10" /><g class="non-terminal ">
<path d="M2154.75 1321h0.0" /><path d="M2234.75 1321h0.0" /><text class="comment" x="2194.75" y="1326">out.d=&quot;2&quot;;</text></g></g><path d="M2254.0 1321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1351h10.75" /><path d="M2243.25 1351h10.75" /><g class="terminal ">
<path d="M2080.75 1351h0.0" /><path d="M2143.25 1351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2080.75" y="1340"></rect><text x="2112" y="1355">three</text></g><path d="M2143.25 1351h10" /><path d="M2153.25 1351h10" /><g class="non-terminal ">
<path d="M2163.25 1351h0.0" /><path d="M2243.25 1351h0.0" /><text class="comment" x="2203.25" y="1356">out.d=&quot;3&quot;;</text></g></g><path d="M2254.0 1351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1381h15.0" /><path d="M2239.0 1381h15.0" /><g class="terminal ">
<path d="M2085.0 1381h0.0" /><path d="M2139.0 1381h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2085" y="1370"></rect><text x="2112" y="1385">four</text></g><path d="M2139.0 1381h10" /><path d="M2149.0 1381h10" /><g class="non-terminal ">
<path d="M2159.0 1381h0.0" /><path d="M2239.0 1381h0.0" /><text class="comment" x="2199" y="1386">out.d=&quot;4&quot;;</text></g></g><path d="M2254.0 1381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1411h15.0" /><path d="M2239.0 1411h15.0" /><g class="terminal ">
<path d="M2085.0 1411h0.0" /><path d="M2139.0 1411h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2085" y="1400"></rect><text x="2112" y="1415">five</text></g><path d="M2139.0 1411h10" /><path d="M2149.0 1411h10" /><g class="non-terminal ">
<path d="M2159.0 1411h0.0" /><path d="M2239.0 1411h0.0" /><text class="comment" x="2199" y="1416">out.d=&quot;5&quot;;</text></g></g><path d="M2254.0 1411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1441h19.25" /><path d="M2234.75 1441h19.25" /><g class="terminal ">
<path d="M2089.25 1441h0.0" /><path d="M2134.75 1441h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2089.25" y="1430"></rect><text x="2112" y="1445">six</text></g><path d="M2134.75 1441h10" /><path d="M2144.75 1441h10" /><g class="non-terminal ">
<path d="M2154.75 1441h0.0" /><path d="M2234.75 1441h0.0" /><text class="comment" x="2194.75" y="1446">out.d=&quot;6&quot;;</text></g></g><path d="M2254.0 1441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1471h10.75" /><path d="M2243.25 1471h10.75" /><g class="terminal ">
<path d="M2080.75 1471h0.0" /><path d="M2143.25 1471h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2080.75" y="1460"></rect><text x="2112" y="1475">seven</text></g><path d="M2143.25 1471h10" /><path d="M2153.25 1471h10" /><g class="non-terminal ">
<path d="M2163.25 1471h0.0" /><path d="M2243.25 1471h0.0" /><text class="comment" x="2203.25" y="1476">out.d=&quot;7&quot;;</text></g></g><path d="M2254.0 1471a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1501h10.75" /><path d="M2243.25 1501h10.75" /><g class="terminal ">
<path d="M2080.75 1501h0.0" /><path d="M2143.25 1501h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2080.75" y="1490"></rect><text x="2112" y="1505">eight</text></g><path d="M2143.25 1501h10" /><path d="M2153.25 1501h10" /><g class="non-terminal ">
<path d="M2163.25 1501h0.0" /><path d="M2243.25 1501h0.0" /><text class="comment" x="2203.25" y="1506">out.d=&quot;8&quot;;</text></g></g><path d="M2254.0 1501a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2050.0 1231a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2070.0 1531h15.0" /><path d="M2239.0 1531h15.0" /><g class="terminal ">
<path d="M2085.0 1531h0.0" /><path d="M2139.0 1531h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2085" y="1520"></rect><text x="2112" y="1535">nine</text></g><path d="M2139.0 1531h10" /><path d="M2149.0 1531h10" /><g class="non-terminal ">
<path d="M2159.0 1531h0.0" /><path d="M2239.0 1531h0.0" /><text class="comment" x="2199" y="1536">out.d=&quot;9&quot;;</text></g></g><path d="M2254.0 1531a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2274.0 1231h10" /><path d="M2284.0 1231h10" /><g class="terminal ">
<path d="M2294.0 1231h0.0" /><path d="M2620.0 1231h0.0" /><rect height="22" rx="10" ry="10" width="326" x="2294" y="1220"></rect><text x="2457" y="1235">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M2620.0 1231h10" /><path d="M2630.0 1231h10" /><g class="terminal ">
<path d="M2640.0 1231h0.0" /><path d="M2906.5 1231h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="2640" y="1220"></rect><text x="2773.25" y="1235">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M2906.5 1231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M2926.5 961h10" /><path d="M2936.5 961h10" /><g class="terminal ">
<path d="M2946.5 961h0.0" /><path d="M3230.0 961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2946.5" y="950"></rect><text x="3088.25" y="965">!!out.d3=rules.doubleDigit.dd1;</text></g><path d="M3230.0 961h10" /><path d="M3240.0 961h10" /><g class="terminal ">
<path d="M3250.0 961h0.0" /><path d="M3533.5 961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3250" y="950"></rect><text x="3391.75" y="965">out.d4=rules.doubleDigit.dd2;!!</text></g><path d="M3533.5 961h10" /><path d="M3543.5 961h10" /><g>
<path d="M3553.5 961h0.0" /><path d="M3777.5 961h0.0" /><g>
<path d="M3553.5 961h0.0" /><path d="M3777.5 961h0.0" /><path d="M3553.5 961h20" /><g>
<path d="M3573.5 961h0.0" /><path d="M3757.5 961h0.0" /><g>
<path d="M3573.5 961h0.0" /><path d="M3667.5 961h0.0" /><path d="M3573.5 961h20" /><g>
<path d="M3593.5 961h0.0" /><path d="M3647.5 961h0.0" /><g class="terminal ">
<path d="M3593.5 961h0.0" /><path d="M3647.5 961h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3593.5" y="950"></rect><text x="3620.5" y="965">zero</text></g></g><path d="M3647.5 961h20" /><path d="M3573.5 961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3593.5 991h8.5" /><path d="M3639.0 991h8.5" /><g class="terminal ">
<path d="M3602.0 991h0.0" /><path d="M3639.0 991h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3602" y="980"></rect><text x="3620.5" y="995">oh</text></g></g><path d="M3647.5 991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3667.5 961h10" /><g class="non-terminal ">
<path d="M3677.5 961h0.0" /><path d="M3757.5 961h0.0" /><text class="comment" x="3717.5" y="966">out.d=&quot;0&quot;;</text></g></g><path d="M3757.5 961h20" /><path d="M3553.5 961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1021h19.25" /><path d="M3738.25 1021h19.25" /><g class="terminal ">
<path d="M3592.75 1021h0.0" /><path d="M3638.25 1021h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1010"></rect><text x="3615.5" y="1025">one</text></g><path d="M3638.25 1021h10" /><path d="M3648.25 1021h10" /><g class="non-terminal ">
<path d="M3658.25 1021h0.0" /><path d="M3738.25 1021h0.0" /><text class="comment" x="3698.25" y="1026">out.d=&quot;1&quot;;</text></g></g><path d="M3757.5 1021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1051h19.25" /><path d="M3738.25 1051h19.25" /><g class="terminal ">
<path d="M3592.75 1051h0.0" /><path d="M3638.25 1051h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1040"></rect><text x="3615.5" y="1055">two</text></g><path d="M3638.25 1051h10" /><path d="M3648.25 1051h10" /><g class="non-terminal ">
<path d="M3658.25 1051h0.0" /><path d="M3738.25 1051h0.0" /><text class="comment" x="3698.25" y="1056">out.d=&quot;2&quot;;</text></g></g><path d="M3757.5 1051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1081h10.75" /><path d="M3746.75 1081h10.75" /><g class="terminal ">
<path d="M3584.25 1081h0.0" /><path d="M3646.75 1081h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1070"></rect><text x="3615.5" y="1085">three</text></g><path d="M3646.75 1081h10" /><path d="M3656.75 1081h10" /><g class="non-terminal ">
<path d="M3666.75 1081h0.0" /><path d="M3746.75 1081h0.0" /><text class="comment" x="3706.75" y="1086">out.d=&quot;3&quot;;</text></g></g><path d="M3757.5 1081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1111h15.0" /><path d="M3742.5 1111h15.0" /><g class="terminal ">
<path d="M3588.5 1111h0.0" /><path d="M3642.5 1111h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1100"></rect><text x="3615.5" y="1115">four</text></g><path d="M3642.5 1111h10" /><path d="M3652.5 1111h10" /><g class="non-terminal ">
<path d="M3662.5 1111h0.0" /><path d="M3742.5 1111h0.0" /><text class="comment" x="3702.5" y="1116">out.d=&quot;4&quot;;</text></g></g><path d="M3757.5 1111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1141h15.0" /><path d="M3742.5 1141h15.0" /><g class="terminal ">
<path d="M3588.5 1141h0.0" /><path d="M3642.5 1141h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1130"></rect><text x="3615.5" y="1145">five</text></g><path d="M3642.5 1141h10" /><path d="M3652.5 1141h10" /><g class="non-terminal ">
<path d="M3662.5 1141h0.0" /><path d="M3742.5 1141h0.0" /><text class="comment" x="3702.5" y="1146">out.d=&quot;5&quot;;</text></g></g><path d="M3757.5 1141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1171h19.25" /><path d="M3738.25 1171h19.25" /><g class="terminal ">
<path d="M3592.75 1171h0.0" /><path d="M3638.25 1171h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1160"></rect><text x="3615.5" y="1175">six</text></g><path d="M3638.25 1171h10" /><path d="M3648.25 1171h10" /><g class="non-terminal ">
<path d="M3658.25 1171h0.0" /><path d="M3738.25 1171h0.0" /><text class="comment" x="3698.25" y="1176">out.d=&quot;6&quot;;</text></g></g><path d="M3757.5 1171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1201h10.75" /><path d="M3746.75 1201h10.75" /><g class="terminal ">
<path d="M3584.25 1201h0.0" /><path d="M3646.75 1201h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1190"></rect><text x="3615.5" y="1205">seven</text></g><path d="M3646.75 1201h10" /><path d="M3656.75 1201h10" /><g class="non-terminal ">
<path d="M3666.75 1201h0.0" /><path d="M3746.75 1201h0.0" /><text class="comment" x="3706.75" y="1206">out.d=&quot;7&quot;;</text></g></g><path d="M3757.5 1201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1231h10.75" /><path d="M3746.75 1231h10.75" /><g class="terminal ">
<path d="M3584.25 1231h0.0" /><path d="M3646.75 1231h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1220"></rect><text x="3615.5" y="1235">eight</text></g><path d="M3646.75 1231h10" /><path d="M3656.75 1231h10" /><g class="non-terminal ">
<path d="M3666.75 1231h0.0" /><path d="M3746.75 1231h0.0" /><text class="comment" x="3706.75" y="1236">out.d=&quot;8&quot;;</text></g></g><path d="M3757.5 1231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3553.5 961a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1261h15.0" /><path d="M3742.5 1261h15.0" /><g class="terminal ">
<path d="M3588.5 1261h0.0" /><path d="M3642.5 1261h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1250"></rect><text x="3615.5" y="1265">nine</text></g><path d="M3642.5 1261h10" /><path d="M3652.5 1261h10" /><g class="non-terminal ">
<path d="M3662.5 1261h0.0" /><path d="M3742.5 1261h0.0" /><text class="comment" x="3702.5" y="1266">out.d=&quot;9&quot;;</text></g></g><path d="M3757.5 1261a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3777.5 961h10" /><path d="M3787.5 961h10" /><g class="non-terminal ">
<path d="M3797.5 961h0.0" /><path d="M3996.5 961h0.0" /><text class="comment" x="3897" y="966">out.d5=rules.singleDigit.d;</text></g></g><path d="M4443.0 961a10 10 0 0 0 10 -10v-910a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v1510a10 10 0 0 0 10 10" /><g>
<path d="M362.0 1561h446.5" /><path d="M3996.5 1561h446.5" /><g>
<path d="M808.5 1561h0.0" /><path d="M1032.5 1561h0.0" /><g>
<path d="M808.5 1561h0.0" /><path d="M1032.5 1561h0.0" /><path d="M808.5 1561h20" /><g>
<path d="M828.5 1561h0.0" /><path d="M1012.5 1561h0.0" /><g>
<path d="M828.5 1561h0.0" /><path d="M922.5 1561h0.0" /><path d="M828.5 1561h20" /><g>
<path d="M848.5 1561h0.0" /><path d="M902.5 1561h0.0" /><g class="terminal ">
<path d="M848.5 1561h0.0" /><path d="M902.5 1561h0.0" /><rect height="22" rx="10" ry="10" width="54" x="848.5" y="1550"></rect><text x="875.5" y="1565">zero</text></g></g><path d="M902.5 1561h20" /><path d="M828.5 1561a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M848.5 1591h8.5" /><path d="M894.0 1591h8.5" /><g class="terminal ">
<path d="M857.0 1591h0.0" /><path d="M894.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="37" x="857" y="1580"></rect><text x="875.5" y="1595">oh</text></g></g><path d="M902.5 1591a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M922.5 1561h10" /><g class="non-terminal ">
<path d="M932.5 1561h0.0" /><path d="M1012.5 1561h0.0" /><text class="comment" x="972.5" y="1566">out.d=&quot;0&quot;;</text></g></g><path d="M1012.5 1561h20" /><path d="M808.5 1561a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1621h19.25" /><path d="M993.25 1621h19.25" /><g class="terminal ">
<path d="M847.75 1621h0.0" /><path d="M893.25 1621h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1610"></rect><text x="870.5" y="1625">one</text></g><path d="M893.25 1621h10" /><path d="M903.25 1621h10" /><g class="non-terminal ">
<path d="M913.25 1621h0.0" /><path d="M993.25 1621h0.0" /><text class="comment" x="953.25" y="1626">out.d=&quot;1&quot;;</text></g></g><path d="M1012.5 1621a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1651h19.25" /><path d="M993.25 1651h19.25" /><g class="terminal ">
<path d="M847.75 1651h0.0" /><path d="M893.25 1651h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1640"></rect><text x="870.5" y="1655">two</text></g><path d="M893.25 1651h10" /><path d="M903.25 1651h10" /><g class="non-terminal ">
<path d="M913.25 1651h0.0" /><path d="M993.25 1651h0.0" /><text class="comment" x="953.25" y="1656">out.d=&quot;2&quot;;</text></g></g><path d="M1012.5 1651a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1681h10.75" /><path d="M1001.75 1681h10.75" /><g class="terminal ">
<path d="M839.25 1681h0.0" /><path d="M901.75 1681h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1670"></rect><text x="870.5" y="1685">three</text></g><path d="M901.75 1681h10" /><path d="M911.75 1681h10" /><g class="non-terminal ">
<path d="M921.75 1681h0.0" /><path d="M1001.75 1681h0.0" /><text class="comment" x="961.75" y="1686">out.d=&quot;3&quot;;</text></g></g><path d="M1012.5 1681a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1711h15.0" /><path d="M997.5 1711h15.0" /><g class="terminal ">
<path d="M843.5 1711h0.0" /><path d="M897.5 1711h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1700"></rect><text x="870.5" y="1715">four</text></g><path d="M897.5 1711h10" /><path d="M907.5 1711h10" /><g class="non-terminal ">
<path d="M917.5 1711h0.0" /><path d="M997.5 1711h0.0" /><text class="comment" x="957.5" y="1716">out.d=&quot;4&quot;;</text></g></g><path d="M1012.5 1711a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1741h15.0" /><path d="M997.5 1741h15.0" /><g class="terminal ">
<path d="M843.5 1741h0.0" /><path d="M897.5 1741h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1730"></rect><text x="870.5" y="1745">five</text></g><path d="M897.5 1741h10" /><path d="M907.5 1741h10" /><g class="non-terminal ">
<path d="M917.5 1741h0.0" /><path d="M997.5 1741h0.0" /><text class="comment" x="957.5" y="1746">out.d=&quot;5&quot;;</text></g></g><path d="M1012.5 1741a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1771h19.25" /><path d="M993.25 1771h19.25" /><g class="terminal ">
<path d="M847.75 1771h0.0" /><path d="M893.25 1771h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="847.75" y="1760"></rect><text x="870.5" y="1775">six</text></g><path d="M893.25 1771h10" /><path d="M903.25 1771h10" /><g class="non-terminal ">
<path d="M913.25 1771h0.0" /><path d="M993.25 1771h0.0" /><text class="comment" x="953.25" y="1776">out.d=&quot;6&quot;;</text></g></g><path d="M1012.5 1771a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1801h10.75" /><path d="M1001.75 1801h10.75" /><g class="terminal ">
<path d="M839.25 1801h0.0" /><path d="M901.75 1801h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1790"></rect><text x="870.5" y="1805">seven</text></g><path d="M901.75 1801h10" /><path d="M911.75 1801h10" /><g class="non-terminal ">
<path d="M921.75 1801h0.0" /><path d="M1001.75 1801h0.0" /><text class="comment" x="961.75" y="1806">out.d=&quot;7&quot;;</text></g></g><path d="M1012.5 1801a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1831h10.75" /><path d="M1001.75 1831h10.75" /><g class="terminal ">
<path d="M839.25 1831h0.0" /><path d="M901.75 1831h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="839.25" y="1820"></rect><text x="870.5" y="1835">eight</text></g><path d="M901.75 1831h10" /><path d="M911.75 1831h10" /><g class="non-terminal ">
<path d="M921.75 1831h0.0" /><path d="M1001.75 1831h0.0" /><text class="comment" x="961.75" y="1836">out.d=&quot;8&quot;;</text></g></g><path d="M1012.5 1831a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M808.5 1561a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M828.5 1861h15.0" /><path d="M997.5 1861h15.0" /><g class="terminal ">
<path d="M843.5 1861h0.0" /><path d="M897.5 1861h0.0" /><rect height="22" rx="10" ry="10" width="54" x="843.5" y="1850"></rect><text x="870.5" y="1865">nine</text></g><path d="M897.5 1861h10" /><path d="M907.5 1861h10" /><g class="non-terminal ">
<path d="M917.5 1861h0.0" /><path d="M997.5 1861h0.0" /><text class="comment" x="957.5" y="1866">out.d=&quot;9&quot;;</text></g></g><path d="M1012.5 1861a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1032.5 1561h10" /><path d="M1042.5 1561h10" /><g class="non-terminal ">
<path d="M1052.5 1561h0.0" /><path d="M1251.5 1561h0.0" /><text class="comment" x="1152" y="1566">out.d1=rules.singleDigit.d;</text></g><path d="M1251.5 1561h10" /><path d="M1261.5 1561h10" /><g>
<path d="M1271.5 1561h0.0" /><path d="M2463.5 1561h0.0" /><g>
<path d="M1271.5 1561h0.0" /><path d="M2463.5 1561h0.0" /><path d="M1271.5 1561h20" /><g>
<path d="M1291.5 1561h87.75" /><path d="M2355.75 1561h87.75" /><g>
<path d="M1379.25 1561h0.0" /><path d="M1833.75 1561h0.0" /><g>
<path d="M1379.25 1561h0.0" /><path d="M1833.75 1561h0.0" /><path d="M1379.25 1561h20" /><g>
<path d="M1399.25 1561h12.75" /><path d="M1801.0 1561h12.75" /><g class="terminal ">
<path d="M1412.0 1561h0.0" /><path d="M1483.0 1561h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1412" y="1550"></rect><text x="1447.5" y="1565">eleven</text></g><path d="M1483.0 1561h10" /><path d="M1493.0 1561h10" /><g class="terminal ">
<path d="M1503.0 1561h0.0" /><path d="M1642.0 1561h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1503" y="1550"></rect><text x="1572.5" y="1565">!!out.dd1=&quot;1&quot;;</text></g><path d="M1642.0 1561h10" /><path d="M1652.0 1561h10" /><g class="terminal ">
<path d="M1662.0 1561h0.0" /><path d="M1801.0 1561h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1662" y="1550"></rect><text x="1731.5" y="1565">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M1813.75 1561h20" /><path d="M1379.25 1561a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1591h12.75" /><path d="M1801.0 1591h12.75" /><g class="terminal ">
<path d="M1412.0 1591h0.0" /><path d="M1483.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1412" y="1580"></rect><text x="1447.5" y="1595">twelve</text></g><path d="M1483.0 1591h10" /><path d="M1493.0 1591h10" /><g class="terminal ">
<path d="M1503.0 1591h0.0" /><path d="M1642.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1503" y="1580"></rect><text x="1572.5" y="1595">!!out.dd1=&quot;1&quot;;</text></g><path d="M1642.0 1591h10" /><path d="M1652.0 1591h10" /><g class="terminal ">
<path d="M1662.0 1591h0.0" /><path d="M1801.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1662" y="1580"></rect><text x="1731.5" y="1595">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M1813.75 1591a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1621h4.25" /><path d="M1809.5 1621h4.25" /><g class="terminal ">
<path d="M1403.5 1621h0.0" /><path d="M1491.5 1621h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1403.5" y="1610"></rect><text x="1447.5" y="1625">thirteen</text></g><path d="M1491.5 1621h10" /><path d="M1501.5 1621h10" /><g class="terminal ">
<path d="M1511.5 1621h0.0" /><path d="M1650.5 1621h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1511.5" y="1610"></rect><text x="1581" y="1625">!!out.dd1=&quot;1&quot;;</text></g><path d="M1650.5 1621h10" /><path d="M1660.5 1621h10" /><g class="terminal ">
<path d="M1670.5 1621h0.0" /><path d="M1809.5 1621h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1670.5" y="1610"></rect><text x="1740" y="1625">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M1813.75 1621a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1651h4.25" /><path d="M1809.5 1651h4.25" /><g class="terminal ">
<path d="M1403.5 1651h0.0" /><path d="M1491.5 1651h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1403.5" y="1640"></rect><text x="1447.5" y="1655">fourteen</text></g><path d="M1491.5 1651h10" /><path d="M1501.5 1651h10" /><g class="terminal ">
<path d="M1511.5 1651h0.0" /><path d="M1650.5 1651h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1511.5" y="1640"></rect><text x="1581" y="1655">!!out.dd1=&quot;1&quot;;</text></g><path d="M1650.5 1651h10" /><path d="M1660.5 1651h10" /><g class="terminal ">
<path d="M1670.5 1651h0.0" /><path d="M1809.5 1651h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1670.5" y="1640"></rect><text x="1740" y="1655">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M1813.75 1651a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1681h8.5" /><path d="M1805.25 1681h8.5" /><g class="terminal ">
<path d="M1407.75 1681h0.0" /><path d="M1487.25 1681h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1407.75" y="1670"></rect><text x="1447.5" y="1685">fifteen</text></g><path d="M1487.25 1681h10" /><path d="M1497.25 1681h10" /><g class="terminal ">
<path d="M1507.25 1681h0.0" /><path d="M1646.25 1681h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1507.25" y="1670"></rect><text x="1576.75" y="1685">!!out.dd1=&quot;1&quot;;</text></g><path d="M1646.25 1681h10" /><path d="M1656.25 1681h10" /><g class="terminal ">
<path d="M1666.25 1681h0.0" /><path d="M1805.25 1681h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1666.25" y="1670"></rect><text x="1735.75" y="1685">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M1813.75 1681a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1711h8.5" /><path d="M1805.25 1711h8.5" /><g class="terminal ">
<path d="M1407.75 1711h0.0" /><path d="M1487.25 1711h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1407.75" y="1700"></rect><text x="1447.5" y="1715">sixteen</text></g><path d="M1487.25 1711h10" /><path d="M1497.25 1711h10" /><g class="terminal ">
<path d="M1507.25 1711h0.0" /><path d="M1646.25 1711h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1507.25" y="1700"></rect><text x="1576.75" y="1715">!!out.dd1=&quot;1&quot;;</text></g><path d="M1646.25 1711h10" /><path d="M1656.25 1711h10" /><g class="terminal ">
<path d="M1666.25 1711h0.0" /><path d="M1805.25 1711h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1666.25" y="1700"></rect><text x="1735.75" y="1715">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M1813.75 1711a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1741h0.0" /><path d="M1813.75 1741h0.0" /><g class="terminal ">
<path d="M1399.25 1741h0.0" /><path d="M1495.75 1741h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="1399.25" y="1730"></rect><text x="1447.5" y="1745">seventeen</text></g><path d="M1495.75 1741h10" /><path d="M1505.75 1741h10" /><g class="terminal ">
<path d="M1515.75 1741h0.0" /><path d="M1654.75 1741h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1515.75" y="1730"></rect><text x="1585.25" y="1745">!!out.dd1=&quot;1&quot;;</text></g><path d="M1654.75 1741h10" /><path d="M1664.75 1741h10" /><g class="terminal ">
<path d="M1674.75 1741h0.0" /><path d="M1813.75 1741h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1674.75" y="1730"></rect><text x="1744.25" y="1745">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M1813.75 1741a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1771h4.25" /><path d="M1809.5 1771h4.25" /><g class="terminal ">
<path d="M1403.5 1771h0.0" /><path d="M1491.5 1771h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1403.5" y="1760"></rect><text x="1447.5" y="1775">eighteen</text></g><path d="M1491.5 1771h10" /><path d="M1501.5 1771h10" /><g class="terminal ">
<path d="M1511.5 1771h0.0" /><path d="M1650.5 1771h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1511.5" y="1760"></rect><text x="1581" y="1775">!!out.dd1=&quot;1&quot;;</text></g><path d="M1650.5 1771h10" /><path d="M1660.5 1771h10" /><g class="terminal ">
<path d="M1670.5 1771h0.0" /><path d="M1809.5 1771h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1670.5" y="1760"></rect><text x="1740" y="1775">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M1813.75 1771a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1379.25 1561a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1399.25 1801h4.25" /><path d="M1809.5 1801h4.25" /><g class="terminal ">
<path d="M1403.5 1801h0.0" /><path d="M1491.5 1801h0.0" /><rect height="22" rx="10" ry="10" width="88" x="1403.5" y="1790"></rect><text x="1447.5" y="1805">nineteen</text></g><path d="M1491.5 1801h10" /><path d="M1501.5 1801h10" /><g class="terminal ">
<path d="M1511.5 1801h0.0" /><path d="M1650.5 1801h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1511.5" y="1790"></rect><text x="1581" y="1805">!!out.dd1=&quot;1&quot;;</text></g><path d="M1650.5 1801h10" /><path d="M1660.5 1801h10" /><g class="terminal ">
<path d="M1670.5 1801h0.0" /><path d="M1809.5 1801h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1670.5" y="1790"></rect><text x="1740" y="1805">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M1813.75 1801a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M1833.75 1561h10" /><path d="M1843.75 1561h10" /><g class="terminal ">
<path d="M1853.75 1561h0.0" /><path d="M2094.75 1561h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1853.75" y="1550"></rect><text x="1974.25" y="1565">!!out.dd1=rules.teens.dd1;</text></g><path d="M2094.75 1561h10" /><path d="M2104.75 1561h10" /><g class="terminal ">
<path d="M2114.75 1561h0.0" /><path d="M2355.75 1561h0.0" /><rect height="22" rx="10" ry="10" width="241" x="2114.75" y="1550"></rect><text x="2235.25" y="1565">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M2443.5 1561h20" /><path d="M1271.5 1561a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1291.5 1831h0.0" /><path d="M2443.5 1831h0.0" /><g>
<path d="M1291.5 1831h0.0" /><path d="M1567.0 1831h0.0" /><g>
<path d="M1291.5 1831h0.0" /><path d="M1567.0 1831h0.0" /><path d="M1291.5 1831h20" /><g>
<path d="M1311.5 1831h4.25" /><path d="M1542.75 1831h4.25" /><g class="terminal ">
<path d="M1315.75 1831h0.0" /><path d="M1386.75 1831h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1315.75" y="1820"></rect><text x="1351.25" y="1835">twenty</text></g><path d="M1386.75 1831h10" /><path d="M1396.75 1831h10" /><g class="non-terminal ">
<path d="M1406.75 1831h0.0" /><path d="M1542.75 1831h0.0" /><text class="comment" x="1474.75" y="1836">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M1547.0 1831h20" /><path d="M1291.5 1831a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 1861h4.25" /><path d="M1542.75 1861h4.25" /><g class="terminal ">
<path d="M1315.75 1861h0.0" /><path d="M1386.75 1861h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1315.75" y="1850"></rect><text x="1351.25" y="1865">thirty</text></g><path d="M1386.75 1861h10" /><path d="M1396.75 1861h10" /><g class="non-terminal ">
<path d="M1406.75 1861h0.0" /><path d="M1542.75 1861h0.0" /><text class="comment" x="1474.75" y="1866">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M1547.0 1861a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 1891h8.5" /><path d="M1538.5 1891h8.5" /><g class="terminal ">
<path d="M1320.0 1891h0.0" /><path d="M1382.5 1891h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1320" y="1880"></rect><text x="1351.25" y="1895">forty</text></g><path d="M1382.5 1891h10" /><path d="M1392.5 1891h10" /><g class="non-terminal ">
<path d="M1402.5 1891h0.0" /><path d="M1538.5 1891h0.0" /><text class="comment" x="1470.5" y="1896">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M1547.0 1891a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 1921h8.5" /><path d="M1538.5 1921h8.5" /><g class="terminal ">
<path d="M1320.0 1921h0.0" /><path d="M1382.5 1921h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1320" y="1910"></rect><text x="1351.25" y="1925">fifty</text></g><path d="M1382.5 1921h10" /><path d="M1392.5 1921h10" /><g class="non-terminal ">
<path d="M1402.5 1921h0.0" /><path d="M1538.5 1921h0.0" /><text class="comment" x="1470.5" y="1926">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M1547.0 1921a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 1951h8.5" /><path d="M1538.5 1951h8.5" /><g class="terminal ">
<path d="M1320.0 1951h0.0" /><path d="M1382.5 1951h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1320" y="1940"></rect><text x="1351.25" y="1955">sixty</text></g><path d="M1382.5 1951h10" /><path d="M1392.5 1951h10" /><g class="non-terminal ">
<path d="M1402.5 1951h0.0" /><path d="M1538.5 1951h0.0" /><text class="comment" x="1470.5" y="1956">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M1547.0 1951a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 1981h0.0" /><path d="M1547.0 1981h0.0" /><g class="terminal ">
<path d="M1311.5 1981h0.0" /><path d="M1391.0 1981h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="1311.5" y="1970"></rect><text x="1351.25" y="1985">seventy</text></g><path d="M1391.0 1981h10" /><path d="M1401.0 1981h10" /><g class="non-terminal ">
<path d="M1411.0 1981h0.0" /><path d="M1547.0 1981h0.0" /><text class="comment" x="1479" y="1986">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M1547.0 1981a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 2011h4.25" /><path d="M1542.75 2011h4.25" /><g class="terminal ">
<path d="M1315.75 2011h0.0" /><path d="M1386.75 2011h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1315.75" y="2000"></rect><text x="1351.25" y="2015">eighty</text></g><path d="M1386.75 2011h10" /><path d="M1396.75 2011h10" /><g class="non-terminal ">
<path d="M1406.75 2011h0.0" /><path d="M1542.75 2011h0.0" /><text class="comment" x="1474.75" y="2016">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M1547.0 2011a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1291.5 1831a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1311.5 2041h4.25" /><path d="M1542.75 2041h4.25" /><g class="terminal ">
<path d="M1315.75 2041h0.0" /><path d="M1386.75 2041h0.0" /><rect height="22" rx="10" ry="10" width="71" x="1315.75" y="2030"></rect><text x="1351.25" y="2045">ninety</text></g><path d="M1386.75 2041h10" /><path d="M1396.75 2041h10" /><g class="non-terminal ">
<path d="M1406.75 2041h0.0" /><path d="M1542.75 2041h0.0" /><text class="comment" x="1474.75" y="2046">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M1547.0 2041a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M1567.0 1831h10" /><path d="M1577.0 1831h10" /><g>
<path d="M1587.0 1831h0.0" /><path d="M1811.0 1831h0.0" /><g>
<path d="M1587.0 1831h0.0" /><path d="M1811.0 1831h0.0" /><path d="M1587.0 1831h20" /><g>
<path d="M1607.0 1831h0.0" /><path d="M1791.0 1831h0.0" /><g>
<path d="M1607.0 1831h0.0" /><path d="M1701.0 1831h0.0" /><path d="M1607.0 1831h20" /><g>
<path d="M1627.0 1831h0.0" /><path d="M1681.0 1831h0.0" /><g class="terminal ">
<path d="M1627.0 1831h0.0" /><path d="M1681.0 1831h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1627" y="1820"></rect><text x="1654" y="1835">zero</text></g></g><path d="M1681.0 1831h20" /><path d="M1607.0 1831a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1627.0 1861h8.5" /><path d="M1672.5 1861h8.5" /><g class="terminal ">
<path d="M1635.5 1861h0.0" /><path d="M1672.5 1861h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1635.5" y="1850"></rect><text x="1654" y="1865">oh</text></g></g><path d="M1681.0 1861a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1701.0 1831h10" /><g class="non-terminal ">
<path d="M1711.0 1831h0.0" /><path d="M1791.0 1831h0.0" /><text class="comment" x="1751" y="1836">out.d=&quot;0&quot;;</text></g></g><path d="M1791.0 1831h20" /><path d="M1587.0 1831a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 1891h19.25" /><path d="M1771.75 1891h19.25" /><g class="terminal ">
<path d="M1626.25 1891h0.0" /><path d="M1671.75 1891h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1626.25" y="1880"></rect><text x="1649" y="1895">one</text></g><path d="M1671.75 1891h10" /><path d="M1681.75 1891h10" /><g class="non-terminal ">
<path d="M1691.75 1891h0.0" /><path d="M1771.75 1891h0.0" /><text class="comment" x="1731.75" y="1896">out.d=&quot;1&quot;;</text></g></g><path d="M1791.0 1891a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 1921h19.25" /><path d="M1771.75 1921h19.25" /><g class="terminal ">
<path d="M1626.25 1921h0.0" /><path d="M1671.75 1921h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1626.25" y="1910"></rect><text x="1649" y="1925">two</text></g><path d="M1671.75 1921h10" /><path d="M1681.75 1921h10" /><g class="non-terminal ">
<path d="M1691.75 1921h0.0" /><path d="M1771.75 1921h0.0" /><text class="comment" x="1731.75" y="1926">out.d=&quot;2&quot;;</text></g></g><path d="M1791.0 1921a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 1951h10.75" /><path d="M1780.25 1951h10.75" /><g class="terminal ">
<path d="M1617.75 1951h0.0" /><path d="M1680.25 1951h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1617.75" y="1940"></rect><text x="1649" y="1955">three</text></g><path d="M1680.25 1951h10" /><path d="M1690.25 1951h10" /><g class="non-terminal ">
<path d="M1700.25 1951h0.0" /><path d="M1780.25 1951h0.0" /><text class="comment" x="1740.25" y="1956">out.d=&quot;3&quot;;</text></g></g><path d="M1791.0 1951a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 1981h15.0" /><path d="M1776.0 1981h15.0" /><g class="terminal ">
<path d="M1622.0 1981h0.0" /><path d="M1676.0 1981h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1622" y="1970"></rect><text x="1649" y="1985">four</text></g><path d="M1676.0 1981h10" /><path d="M1686.0 1981h10" /><g class="non-terminal ">
<path d="M1696.0 1981h0.0" /><path d="M1776.0 1981h0.0" /><text class="comment" x="1736" y="1986">out.d=&quot;4&quot;;</text></g></g><path d="M1791.0 1981a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 2011h15.0" /><path d="M1776.0 2011h15.0" /><g class="terminal ">
<path d="M1622.0 2011h0.0" /><path d="M1676.0 2011h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1622" y="2000"></rect><text x="1649" y="2015">five</text></g><path d="M1676.0 2011h10" /><path d="M1686.0 2011h10" /><g class="non-terminal ">
<path d="M1696.0 2011h0.0" /><path d="M1776.0 2011h0.0" /><text class="comment" x="1736" y="2016">out.d=&quot;5&quot;;</text></g></g><path d="M1791.0 2011a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 2041h19.25" /><path d="M1771.75 2041h19.25" /><g class="terminal ">
<path d="M1626.25 2041h0.0" /><path d="M1671.75 2041h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1626.25" y="2030"></rect><text x="1649" y="2045">six</text></g><path d="M1671.75 2041h10" /><path d="M1681.75 2041h10" /><g class="non-terminal ">
<path d="M1691.75 2041h0.0" /><path d="M1771.75 2041h0.0" /><text class="comment" x="1731.75" y="2046">out.d=&quot;6&quot;;</text></g></g><path d="M1791.0 2041a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 2071h10.75" /><path d="M1780.25 2071h10.75" /><g class="terminal ">
<path d="M1617.75 2071h0.0" /><path d="M1680.25 2071h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1617.75" y="2060"></rect><text x="1649" y="2075">seven</text></g><path d="M1680.25 2071h10" /><path d="M1690.25 2071h10" /><g class="non-terminal ">
<path d="M1700.25 2071h0.0" /><path d="M1780.25 2071h0.0" /><text class="comment" x="1740.25" y="2076">out.d=&quot;7&quot;;</text></g></g><path d="M1791.0 2071a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 2101h10.75" /><path d="M1780.25 2101h10.75" /><g class="terminal ">
<path d="M1617.75 2101h0.0" /><path d="M1680.25 2101h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1617.75" y="2090"></rect><text x="1649" y="2105">eight</text></g><path d="M1680.25 2101h10" /><path d="M1690.25 2101h10" /><g class="non-terminal ">
<path d="M1700.25 2101h0.0" /><path d="M1780.25 2101h0.0" /><text class="comment" x="1740.25" y="2106">out.d=&quot;8&quot;;</text></g></g><path d="M1791.0 2101a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1587.0 1831a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1607.0 2131h15.0" /><path d="M1776.0 2131h15.0" /><g class="terminal ">
<path d="M1622.0 2131h0.0" /><path d="M1676.0 2131h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1622" y="2120"></rect><text x="1649" y="2135">nine</text></g><path d="M1676.0 2131h10" /><path d="M1686.0 2131h10" /><g class="non-terminal ">
<path d="M1696.0 2131h0.0" /><path d="M1776.0 2131h0.0" /><text class="comment" x="1736" y="2136">out.d=&quot;9&quot;;</text></g></g><path d="M1791.0 2131a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1811.0 1831h10" /><path d="M1821.0 1831h10" /><g class="terminal ">
<path d="M1831.0 1831h0.0" /><path d="M2157.0 1831h0.0" /><rect height="22" rx="10" ry="10" width="326" x="1831" y="1820"></rect><text x="1994" y="1835">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M2157.0 1831h10" /><path d="M2167.0 1831h10" /><g class="terminal ">
<path d="M2177.0 1831h0.0" /><path d="M2443.5 1831h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="2177" y="1820"></rect><text x="2310.25" y="1835">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M2443.5 1831a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M2463.5 1561h10" /><path d="M2473.5 1561h10" /><g class="terminal ">
<path d="M2483.5 1561h0.0" /><path d="M2767.0 1561h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2483.5" y="1550"></rect><text x="2625.25" y="1565">!!out.d2=rules.doubleDigit.dd1;</text></g><path d="M2767.0 1561h10" /><path d="M2777.0 1561h10" /><g class="terminal ">
<path d="M2787.0 1561h0.0" /><path d="M3070.5 1561h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2787" y="1550"></rect><text x="2928.75" y="1565">out.d3=rules.doubleDigit.dd2;!!</text></g><path d="M3070.5 1561h10" /><path d="M3080.5 1561h10" /><g>
<path d="M3090.5 1561h0.0" /><path d="M3314.5 1561h0.0" /><g>
<path d="M3090.5 1561h0.0" /><path d="M3314.5 1561h0.0" /><path d="M3090.5 1561h20" /><g>
<path d="M3110.5 1561h0.0" /><path d="M3294.5 1561h0.0" /><g>
<path d="M3110.5 1561h0.0" /><path d="M3204.5 1561h0.0" /><path d="M3110.5 1561h20" /><g>
<path d="M3130.5 1561h0.0" /><path d="M3184.5 1561h0.0" /><g class="terminal ">
<path d="M3130.5 1561h0.0" /><path d="M3184.5 1561h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3130.5" y="1550"></rect><text x="3157.5" y="1565">zero</text></g></g><path d="M3184.5 1561h20" /><path d="M3110.5 1561a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3130.5 1591h8.5" /><path d="M3176.0 1591h8.5" /><g class="terminal ">
<path d="M3139.0 1591h0.0" /><path d="M3176.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3139" y="1580"></rect><text x="3157.5" y="1595">oh</text></g></g><path d="M3184.5 1591a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3204.5 1561h10" /><g class="non-terminal ">
<path d="M3214.5 1561h0.0" /><path d="M3294.5 1561h0.0" /><text class="comment" x="3254.5" y="1566">out.d=&quot;0&quot;;</text></g></g><path d="M3294.5 1561h20" /><path d="M3090.5 1561a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1621h19.25" /><path d="M3275.25 1621h19.25" /><g class="terminal ">
<path d="M3129.75 1621h0.0" /><path d="M3175.25 1621h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="1610"></rect><text x="3152.5" y="1625">one</text></g><path d="M3175.25 1621h10" /><path d="M3185.25 1621h10" /><g class="non-terminal ">
<path d="M3195.25 1621h0.0" /><path d="M3275.25 1621h0.0" /><text class="comment" x="3235.25" y="1626">out.d=&quot;1&quot;;</text></g></g><path d="M3294.5 1621a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1651h19.25" /><path d="M3275.25 1651h19.25" /><g class="terminal ">
<path d="M3129.75 1651h0.0" /><path d="M3175.25 1651h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="1640"></rect><text x="3152.5" y="1655">two</text></g><path d="M3175.25 1651h10" /><path d="M3185.25 1651h10" /><g class="non-terminal ">
<path d="M3195.25 1651h0.0" /><path d="M3275.25 1651h0.0" /><text class="comment" x="3235.25" y="1656">out.d=&quot;2&quot;;</text></g></g><path d="M3294.5 1651a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1681h10.75" /><path d="M3283.75 1681h10.75" /><g class="terminal ">
<path d="M3121.25 1681h0.0" /><path d="M3183.75 1681h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="1670"></rect><text x="3152.5" y="1685">three</text></g><path d="M3183.75 1681h10" /><path d="M3193.75 1681h10" /><g class="non-terminal ">
<path d="M3203.75 1681h0.0" /><path d="M3283.75 1681h0.0" /><text class="comment" x="3243.75" y="1686">out.d=&quot;3&quot;;</text></g></g><path d="M3294.5 1681a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1711h15.0" /><path d="M3279.5 1711h15.0" /><g class="terminal ">
<path d="M3125.5 1711h0.0" /><path d="M3179.5 1711h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="1700"></rect><text x="3152.5" y="1715">four</text></g><path d="M3179.5 1711h10" /><path d="M3189.5 1711h10" /><g class="non-terminal ">
<path d="M3199.5 1711h0.0" /><path d="M3279.5 1711h0.0" /><text class="comment" x="3239.5" y="1716">out.d=&quot;4&quot;;</text></g></g><path d="M3294.5 1711a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1741h15.0" /><path d="M3279.5 1741h15.0" /><g class="terminal ">
<path d="M3125.5 1741h0.0" /><path d="M3179.5 1741h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="1730"></rect><text x="3152.5" y="1745">five</text></g><path d="M3179.5 1741h10" /><path d="M3189.5 1741h10" /><g class="non-terminal ">
<path d="M3199.5 1741h0.0" /><path d="M3279.5 1741h0.0" /><text class="comment" x="3239.5" y="1746">out.d=&quot;5&quot;;</text></g></g><path d="M3294.5 1741a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1771h19.25" /><path d="M3275.25 1771h19.25" /><g class="terminal ">
<path d="M3129.75 1771h0.0" /><path d="M3175.25 1771h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="1760"></rect><text x="3152.5" y="1775">six</text></g><path d="M3175.25 1771h10" /><path d="M3185.25 1771h10" /><g class="non-terminal ">
<path d="M3195.25 1771h0.0" /><path d="M3275.25 1771h0.0" /><text class="comment" x="3235.25" y="1776">out.d=&quot;6&quot;;</text></g></g><path d="M3294.5 1771a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1801h10.75" /><path d="M3283.75 1801h10.75" /><g class="terminal ">
<path d="M3121.25 1801h0.0" /><path d="M3183.75 1801h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="1790"></rect><text x="3152.5" y="1805">seven</text></g><path d="M3183.75 1801h10" /><path d="M3193.75 1801h10" /><g class="non-terminal ">
<path d="M3203.75 1801h0.0" /><path d="M3283.75 1801h0.0" /><text class="comment" x="3243.75" y="1806">out.d=&quot;7&quot;;</text></g></g><path d="M3294.5 1801a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1831h10.75" /><path d="M3283.75 1831h10.75" /><g class="terminal ">
<path d="M3121.25 1831h0.0" /><path d="M3183.75 1831h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="1820"></rect><text x="3152.5" y="1835">eight</text></g><path d="M3183.75 1831h10" /><path d="M3193.75 1831h10" /><g class="non-terminal ">
<path d="M3203.75 1831h0.0" /><path d="M3283.75 1831h0.0" /><text class="comment" x="3243.75" y="1836">out.d=&quot;8&quot;;</text></g></g><path d="M3294.5 1831a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3090.5 1561a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 1861h15.0" /><path d="M3279.5 1861h15.0" /><g class="terminal ">
<path d="M3125.5 1861h0.0" /><path d="M3179.5 1861h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="1850"></rect><text x="3152.5" y="1865">nine</text></g><path d="M3179.5 1861h10" /><path d="M3189.5 1861h10" /><g class="non-terminal ">
<path d="M3199.5 1861h0.0" /><path d="M3279.5 1861h0.0" /><text class="comment" x="3239.5" y="1866">out.d=&quot;9&quot;;</text></g></g><path d="M3294.5 1861a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3314.5 1561h10" /><path d="M3324.5 1561h10" /><g class="non-terminal ">
<path d="M3334.5 1561h0.0" /><path d="M3533.5 1561h0.0" /><text class="comment" x="3434" y="1566">out.d4=rules.singleDigit.d;</text></g><path d="M3533.5 1561h10" /><path d="M3543.5 1561h10" /><g>
<path d="M3553.5 1561h0.0" /><path d="M3777.5 1561h0.0" /><g>
<path d="M3553.5 1561h0.0" /><path d="M3777.5 1561h0.0" /><path d="M3553.5 1561h20" /><g>
<path d="M3573.5 1561h0.0" /><path d="M3757.5 1561h0.0" /><g>
<path d="M3573.5 1561h0.0" /><path d="M3667.5 1561h0.0" /><path d="M3573.5 1561h20" /><g>
<path d="M3593.5 1561h0.0" /><path d="M3647.5 1561h0.0" /><g class="terminal ">
<path d="M3593.5 1561h0.0" /><path d="M3647.5 1561h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3593.5" y="1550"></rect><text x="3620.5" y="1565">zero</text></g></g><path d="M3647.5 1561h20" /><path d="M3573.5 1561a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3593.5 1591h8.5" /><path d="M3639.0 1591h8.5" /><g class="terminal ">
<path d="M3602.0 1591h0.0" /><path d="M3639.0 1591h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3602" y="1580"></rect><text x="3620.5" y="1595">oh</text></g></g><path d="M3647.5 1591a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3667.5 1561h10" /><g class="non-terminal ">
<path d="M3677.5 1561h0.0" /><path d="M3757.5 1561h0.0" /><text class="comment" x="3717.5" y="1566">out.d=&quot;0&quot;;</text></g></g><path d="M3757.5 1561h20" /><path d="M3553.5 1561a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1621h19.25" /><path d="M3738.25 1621h19.25" /><g class="terminal ">
<path d="M3592.75 1621h0.0" /><path d="M3638.25 1621h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1610"></rect><text x="3615.5" y="1625">one</text></g><path d="M3638.25 1621h10" /><path d="M3648.25 1621h10" /><g class="non-terminal ">
<path d="M3658.25 1621h0.0" /><path d="M3738.25 1621h0.0" /><text class="comment" x="3698.25" y="1626">out.d=&quot;1&quot;;</text></g></g><path d="M3757.5 1621a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1651h19.25" /><path d="M3738.25 1651h19.25" /><g class="terminal ">
<path d="M3592.75 1651h0.0" /><path d="M3638.25 1651h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1640"></rect><text x="3615.5" y="1655">two</text></g><path d="M3638.25 1651h10" /><path d="M3648.25 1651h10" /><g class="non-terminal ">
<path d="M3658.25 1651h0.0" /><path d="M3738.25 1651h0.0" /><text class="comment" x="3698.25" y="1656">out.d=&quot;2&quot;;</text></g></g><path d="M3757.5 1651a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1681h10.75" /><path d="M3746.75 1681h10.75" /><g class="terminal ">
<path d="M3584.25 1681h0.0" /><path d="M3646.75 1681h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1670"></rect><text x="3615.5" y="1685">three</text></g><path d="M3646.75 1681h10" /><path d="M3656.75 1681h10" /><g class="non-terminal ">
<path d="M3666.75 1681h0.0" /><path d="M3746.75 1681h0.0" /><text class="comment" x="3706.75" y="1686">out.d=&quot;3&quot;;</text></g></g><path d="M3757.5 1681a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1711h15.0" /><path d="M3742.5 1711h15.0" /><g class="terminal ">
<path d="M3588.5 1711h0.0" /><path d="M3642.5 1711h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1700"></rect><text x="3615.5" y="1715">four</text></g><path d="M3642.5 1711h10" /><path d="M3652.5 1711h10" /><g class="non-terminal ">
<path d="M3662.5 1711h0.0" /><path d="M3742.5 1711h0.0" /><text class="comment" x="3702.5" y="1716">out.d=&quot;4&quot;;</text></g></g><path d="M3757.5 1711a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1741h15.0" /><path d="M3742.5 1741h15.0" /><g class="terminal ">
<path d="M3588.5 1741h0.0" /><path d="M3642.5 1741h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1730"></rect><text x="3615.5" y="1745">five</text></g><path d="M3642.5 1741h10" /><path d="M3652.5 1741h10" /><g class="non-terminal ">
<path d="M3662.5 1741h0.0" /><path d="M3742.5 1741h0.0" /><text class="comment" x="3702.5" y="1746">out.d=&quot;5&quot;;</text></g></g><path d="M3757.5 1741a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1771h19.25" /><path d="M3738.25 1771h19.25" /><g class="terminal ">
<path d="M3592.75 1771h0.0" /><path d="M3638.25 1771h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="1760"></rect><text x="3615.5" y="1775">six</text></g><path d="M3638.25 1771h10" /><path d="M3648.25 1771h10" /><g class="non-terminal ">
<path d="M3658.25 1771h0.0" /><path d="M3738.25 1771h0.0" /><text class="comment" x="3698.25" y="1776">out.d=&quot;6&quot;;</text></g></g><path d="M3757.5 1771a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1801h10.75" /><path d="M3746.75 1801h10.75" /><g class="terminal ">
<path d="M3584.25 1801h0.0" /><path d="M3646.75 1801h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1790"></rect><text x="3615.5" y="1805">seven</text></g><path d="M3646.75 1801h10" /><path d="M3656.75 1801h10" /><g class="non-terminal ">
<path d="M3666.75 1801h0.0" /><path d="M3746.75 1801h0.0" /><text class="comment" x="3706.75" y="1806">out.d=&quot;7&quot;;</text></g></g><path d="M3757.5 1801a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1831h10.75" /><path d="M3746.75 1831h10.75" /><g class="terminal ">
<path d="M3584.25 1831h0.0" /><path d="M3646.75 1831h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="1820"></rect><text x="3615.5" y="1835">eight</text></g><path d="M3646.75 1831h10" /><path d="M3656.75 1831h10" /><g class="non-terminal ">
<path d="M3666.75 1831h0.0" /><path d="M3746.75 1831h0.0" /><text class="comment" x="3706.75" y="1836">out.d=&quot;8&quot;;</text></g></g><path d="M3757.5 1831a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3553.5 1561a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 1861h15.0" /><path d="M3742.5 1861h15.0" /><g class="terminal ">
<path d="M3588.5 1861h0.0" /><path d="M3642.5 1861h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="1850"></rect><text x="3615.5" y="1865">nine</text></g><path d="M3642.5 1861h10" /><path d="M3652.5 1861h10" /><g class="non-terminal ">
<path d="M3662.5 1861h0.0" /><path d="M3742.5 1861h0.0" /><text class="comment" x="3702.5" y="1866">out.d=&quot;9&quot;;</text></g></g><path d="M3757.5 1861a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3777.5 1561h10" /><path d="M3787.5 1561h10" /><g class="non-terminal ">
<path d="M3797.5 1561h0.0" /><path d="M3996.5 1561h0.0" /><text class="comment" x="3897" y="1566">out.d5=rules.singleDigit.d;</text></g></g><path d="M4443.0 1561a10 10 0 0 0 10 -10v-1510a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v2110a10 10 0 0 0 10 10" /><g>
<path d="M362.0 2161h446.5" /><path d="M3996.5 2161h446.5" /><g>
<path d="M808.5 2161h0.0" /><path d="M2000.5 2161h0.0" /><g>
<path d="M808.5 2161h0.0" /><path d="M2000.5 2161h0.0" /><path d="M808.5 2161h20" /><g>
<path d="M828.5 2161h87.75" /><path d="M1892.75 2161h87.75" /><g>
<path d="M916.25 2161h0.0" /><path d="M1370.75 2161h0.0" /><g>
<path d="M916.25 2161h0.0" /><path d="M1370.75 2161h0.0" /><path d="M916.25 2161h20" /><g>
<path d="M936.25 2161h12.75" /><path d="M1338.0 2161h12.75" /><g class="terminal ">
<path d="M949.0 2161h0.0" /><path d="M1020.0 2161h0.0" /><rect height="22" rx="10" ry="10" width="71" x="949" y="2150"></rect><text x="984.5" y="2165">eleven</text></g><path d="M1020.0 2161h10" /><path d="M1030.0 2161h10" /><g class="terminal ">
<path d="M1040.0 2161h0.0" /><path d="M1179.0 2161h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1040" y="2150"></rect><text x="1109.5" y="2165">!!out.dd1=&quot;1&quot;;</text></g><path d="M1179.0 2161h10" /><path d="M1189.0 2161h10" /><g class="terminal ">
<path d="M1199.0 2161h0.0" /><path d="M1338.0 2161h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1199" y="2150"></rect><text x="1268.5" y="2165">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M1350.75 2161h20" /><path d="M916.25 2161a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2191h12.75" /><path d="M1338.0 2191h12.75" /><g class="terminal ">
<path d="M949.0 2191h0.0" /><path d="M1020.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="71" x="949" y="2180"></rect><text x="984.5" y="2195">twelve</text></g><path d="M1020.0 2191h10" /><path d="M1030.0 2191h10" /><g class="terminal ">
<path d="M1040.0 2191h0.0" /><path d="M1179.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1040" y="2180"></rect><text x="1109.5" y="2195">!!out.dd1=&quot;1&quot;;</text></g><path d="M1179.0 2191h10" /><path d="M1189.0 2191h10" /><g class="terminal ">
<path d="M1199.0 2191h0.0" /><path d="M1338.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1199" y="2180"></rect><text x="1268.5" y="2195">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M1350.75 2191a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2221h4.25" /><path d="M1346.5 2221h4.25" /><g class="terminal ">
<path d="M940.5 2221h0.0" /><path d="M1028.5 2221h0.0" /><rect height="22" rx="10" ry="10" width="88" x="940.5" y="2210"></rect><text x="984.5" y="2225">thirteen</text></g><path d="M1028.5 2221h10" /><path d="M1038.5 2221h10" /><g class="terminal ">
<path d="M1048.5 2221h0.0" /><path d="M1187.5 2221h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1048.5" y="2210"></rect><text x="1118" y="2225">!!out.dd1=&quot;1&quot;;</text></g><path d="M1187.5 2221h10" /><path d="M1197.5 2221h10" /><g class="terminal ">
<path d="M1207.5 2221h0.0" /><path d="M1346.5 2221h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1207.5" y="2210"></rect><text x="1277" y="2225">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M1350.75 2221a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2251h4.25" /><path d="M1346.5 2251h4.25" /><g class="terminal ">
<path d="M940.5 2251h0.0" /><path d="M1028.5 2251h0.0" /><rect height="22" rx="10" ry="10" width="88" x="940.5" y="2240"></rect><text x="984.5" y="2255">fourteen</text></g><path d="M1028.5 2251h10" /><path d="M1038.5 2251h10" /><g class="terminal ">
<path d="M1048.5 2251h0.0" /><path d="M1187.5 2251h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1048.5" y="2240"></rect><text x="1118" y="2255">!!out.dd1=&quot;1&quot;;</text></g><path d="M1187.5 2251h10" /><path d="M1197.5 2251h10" /><g class="terminal ">
<path d="M1207.5 2251h0.0" /><path d="M1346.5 2251h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1207.5" y="2240"></rect><text x="1277" y="2255">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M1350.75 2251a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2281h8.5" /><path d="M1342.25 2281h8.5" /><g class="terminal ">
<path d="M944.75 2281h0.0" /><path d="M1024.25 2281h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="944.75" y="2270"></rect><text x="984.5" y="2285">fifteen</text></g><path d="M1024.25 2281h10" /><path d="M1034.25 2281h10" /><g class="terminal ">
<path d="M1044.25 2281h0.0" /><path d="M1183.25 2281h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1044.25" y="2270"></rect><text x="1113.75" y="2285">!!out.dd1=&quot;1&quot;;</text></g><path d="M1183.25 2281h10" /><path d="M1193.25 2281h10" /><g class="terminal ">
<path d="M1203.25 2281h0.0" /><path d="M1342.25 2281h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1203.25" y="2270"></rect><text x="1272.75" y="2285">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M1350.75 2281a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2311h8.5" /><path d="M1342.25 2311h8.5" /><g class="terminal ">
<path d="M944.75 2311h0.0" /><path d="M1024.25 2311h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="944.75" y="2300"></rect><text x="984.5" y="2315">sixteen</text></g><path d="M1024.25 2311h10" /><path d="M1034.25 2311h10" /><g class="terminal ">
<path d="M1044.25 2311h0.0" /><path d="M1183.25 2311h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1044.25" y="2300"></rect><text x="1113.75" y="2315">!!out.dd1=&quot;1&quot;;</text></g><path d="M1183.25 2311h10" /><path d="M1193.25 2311h10" /><g class="terminal ">
<path d="M1203.25 2311h0.0" /><path d="M1342.25 2311h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1203.25" y="2300"></rect><text x="1272.75" y="2315">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M1350.75 2311a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2341h0.0" /><path d="M1350.75 2341h0.0" /><g class="terminal ">
<path d="M936.25 2341h0.0" /><path d="M1032.75 2341h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="936.25" y="2330"></rect><text x="984.5" y="2345">seventeen</text></g><path d="M1032.75 2341h10" /><path d="M1042.75 2341h10" /><g class="terminal ">
<path d="M1052.75 2341h0.0" /><path d="M1191.75 2341h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1052.75" y="2330"></rect><text x="1122.25" y="2345">!!out.dd1=&quot;1&quot;;</text></g><path d="M1191.75 2341h10" /><path d="M1201.75 2341h10" /><g class="terminal ">
<path d="M1211.75 2341h0.0" /><path d="M1350.75 2341h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1211.75" y="2330"></rect><text x="1281.25" y="2345">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M1350.75 2341a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2371h4.25" /><path d="M1346.5 2371h4.25" /><g class="terminal ">
<path d="M940.5 2371h0.0" /><path d="M1028.5 2371h0.0" /><rect height="22" rx="10" ry="10" width="88" x="940.5" y="2360"></rect><text x="984.5" y="2375">eighteen</text></g><path d="M1028.5 2371h10" /><path d="M1038.5 2371h10" /><g class="terminal ">
<path d="M1048.5 2371h0.0" /><path d="M1187.5 2371h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1048.5" y="2360"></rect><text x="1118" y="2375">!!out.dd1=&quot;1&quot;;</text></g><path d="M1187.5 2371h10" /><path d="M1197.5 2371h10" /><g class="terminal ">
<path d="M1207.5 2371h0.0" /><path d="M1346.5 2371h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1207.5" y="2360"></rect><text x="1277" y="2375">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M1350.75 2371a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M916.25 2161a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M936.25 2401h4.25" /><path d="M1346.5 2401h4.25" /><g class="terminal ">
<path d="M940.5 2401h0.0" /><path d="M1028.5 2401h0.0" /><rect height="22" rx="10" ry="10" width="88" x="940.5" y="2390"></rect><text x="984.5" y="2405">nineteen</text></g><path d="M1028.5 2401h10" /><path d="M1038.5 2401h10" /><g class="terminal ">
<path d="M1048.5 2401h0.0" /><path d="M1187.5 2401h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1048.5" y="2390"></rect><text x="1118" y="2405">!!out.dd1=&quot;1&quot;;</text></g><path d="M1187.5 2401h10" /><path d="M1197.5 2401h10" /><g class="terminal ">
<path d="M1207.5 2401h0.0" /><path d="M1346.5 2401h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1207.5" y="2390"></rect><text x="1277" y="2405">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M1350.75 2401a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M1370.75 2161h10" /><path d="M1380.75 2161h10" /><g class="terminal ">
<path d="M1390.75 2161h0.0" /><path d="M1631.75 2161h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1390.75" y="2150"></rect><text x="1511.25" y="2165">!!out.dd1=rules.teens.dd1;</text></g><path d="M1631.75 2161h10" /><path d="M1641.75 2161h10" /><g class="terminal ">
<path d="M1651.75 2161h0.0" /><path d="M1892.75 2161h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1651.75" y="2150"></rect><text x="1772.25" y="2165">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M1980.5 2161h20" /><path d="M808.5 2161a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M828.5 2431h0.0" /><path d="M1980.5 2431h0.0" /><g>
<path d="M828.5 2431h0.0" /><path d="M1104.0 2431h0.0" /><g>
<path d="M828.5 2431h0.0" /><path d="M1104.0 2431h0.0" /><path d="M828.5 2431h20" /><g>
<path d="M848.5 2431h4.25" /><path d="M1079.75 2431h4.25" /><g class="terminal ">
<path d="M852.75 2431h0.0" /><path d="M923.75 2431h0.0" /><rect height="22" rx="10" ry="10" width="71" x="852.75" y="2420"></rect><text x="888.25" y="2435">twenty</text></g><path d="M923.75 2431h10" /><path d="M933.75 2431h10" /><g class="non-terminal ">
<path d="M943.75 2431h0.0" /><path d="M1079.75 2431h0.0" /><text class="comment" x="1011.75" y="2436">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M1084.0 2431h20" /><path d="M828.5 2431a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2461h4.25" /><path d="M1079.75 2461h4.25" /><g class="terminal ">
<path d="M852.75 2461h0.0" /><path d="M923.75 2461h0.0" /><rect height="22" rx="10" ry="10" width="71" x="852.75" y="2450"></rect><text x="888.25" y="2465">thirty</text></g><path d="M923.75 2461h10" /><path d="M933.75 2461h10" /><g class="non-terminal ">
<path d="M943.75 2461h0.0" /><path d="M1079.75 2461h0.0" /><text class="comment" x="1011.75" y="2466">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M1084.0 2461a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2491h8.5" /><path d="M1075.5 2491h8.5" /><g class="terminal ">
<path d="M857.0 2491h0.0" /><path d="M919.5 2491h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="857" y="2480"></rect><text x="888.25" y="2495">forty</text></g><path d="M919.5 2491h10" /><path d="M929.5 2491h10" /><g class="non-terminal ">
<path d="M939.5 2491h0.0" /><path d="M1075.5 2491h0.0" /><text class="comment" x="1007.5" y="2496">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M1084.0 2491a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2521h8.5" /><path d="M1075.5 2521h8.5" /><g class="terminal ">
<path d="M857.0 2521h0.0" /><path d="M919.5 2521h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="857" y="2510"></rect><text x="888.25" y="2525">fifty</text></g><path d="M919.5 2521h10" /><path d="M929.5 2521h10" /><g class="non-terminal ">
<path d="M939.5 2521h0.0" /><path d="M1075.5 2521h0.0" /><text class="comment" x="1007.5" y="2526">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M1084.0 2521a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2551h8.5" /><path d="M1075.5 2551h8.5" /><g class="terminal ">
<path d="M857.0 2551h0.0" /><path d="M919.5 2551h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="857" y="2540"></rect><text x="888.25" y="2555">sixty</text></g><path d="M919.5 2551h10" /><path d="M929.5 2551h10" /><g class="non-terminal ">
<path d="M939.5 2551h0.0" /><path d="M1075.5 2551h0.0" /><text class="comment" x="1007.5" y="2556">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M1084.0 2551a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2581h0.0" /><path d="M1084.0 2581h0.0" /><g class="terminal ">
<path d="M848.5 2581h0.0" /><path d="M928.0 2581h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="848.5" y="2570"></rect><text x="888.25" y="2585">seventy</text></g><path d="M928.0 2581h10" /><path d="M938.0 2581h10" /><g class="non-terminal ">
<path d="M948.0 2581h0.0" /><path d="M1084.0 2581h0.0" /><text class="comment" x="1016" y="2586">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M1084.0 2581a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2611h4.25" /><path d="M1079.75 2611h4.25" /><g class="terminal ">
<path d="M852.75 2611h0.0" /><path d="M923.75 2611h0.0" /><rect height="22" rx="10" ry="10" width="71" x="852.75" y="2600"></rect><text x="888.25" y="2615">eighty</text></g><path d="M923.75 2611h10" /><path d="M933.75 2611h10" /><g class="non-terminal ">
<path d="M943.75 2611h0.0" /><path d="M1079.75 2611h0.0" /><text class="comment" x="1011.75" y="2616">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M1084.0 2611a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M828.5 2431a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M848.5 2641h4.25" /><path d="M1079.75 2641h4.25" /><g class="terminal ">
<path d="M852.75 2641h0.0" /><path d="M923.75 2641h0.0" /><rect height="22" rx="10" ry="10" width="71" x="852.75" y="2630"></rect><text x="888.25" y="2645">ninety</text></g><path d="M923.75 2641h10" /><path d="M933.75 2641h10" /><g class="non-terminal ">
<path d="M943.75 2641h0.0" /><path d="M1079.75 2641h0.0" /><text class="comment" x="1011.75" y="2646">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M1084.0 2641a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M1104.0 2431h10" /><path d="M1114.0 2431h10" /><g>
<path d="M1124.0 2431h0.0" /><path d="M1348.0 2431h0.0" /><g>
<path d="M1124.0 2431h0.0" /><path d="M1348.0 2431h0.0" /><path d="M1124.0 2431h20" /><g>
<path d="M1144.0 2431h0.0" /><path d="M1328.0 2431h0.0" /><g>
<path d="M1144.0 2431h0.0" /><path d="M1238.0 2431h0.0" /><path d="M1144.0 2431h20" /><g>
<path d="M1164.0 2431h0.0" /><path d="M1218.0 2431h0.0" /><g class="terminal ">
<path d="M1164.0 2431h0.0" /><path d="M1218.0 2431h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1164" y="2420"></rect><text x="1191" y="2435">zero</text></g></g><path d="M1218.0 2431h20" /><path d="M1144.0 2431a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1164.0 2461h8.5" /><path d="M1209.5 2461h8.5" /><g class="terminal ">
<path d="M1172.5 2461h0.0" /><path d="M1209.5 2461h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1172.5" y="2450"></rect><text x="1191" y="2465">oh</text></g></g><path d="M1218.0 2461a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1238.0 2431h10" /><g class="non-terminal ">
<path d="M1248.0 2431h0.0" /><path d="M1328.0 2431h0.0" /><text class="comment" x="1288" y="2436">out.d=&quot;0&quot;;</text></g></g><path d="M1328.0 2431h20" /><path d="M1124.0 2431a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2491h19.25" /><path d="M1308.75 2491h19.25" /><g class="terminal ">
<path d="M1163.25 2491h0.0" /><path d="M1208.75 2491h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1163.25" y="2480"></rect><text x="1186" y="2495">one</text></g><path d="M1208.75 2491h10" /><path d="M1218.75 2491h10" /><g class="non-terminal ">
<path d="M1228.75 2491h0.0" /><path d="M1308.75 2491h0.0" /><text class="comment" x="1268.75" y="2496">out.d=&quot;1&quot;;</text></g></g><path d="M1328.0 2491a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2521h19.25" /><path d="M1308.75 2521h19.25" /><g class="terminal ">
<path d="M1163.25 2521h0.0" /><path d="M1208.75 2521h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1163.25" y="2510"></rect><text x="1186" y="2525">two</text></g><path d="M1208.75 2521h10" /><path d="M1218.75 2521h10" /><g class="non-terminal ">
<path d="M1228.75 2521h0.0" /><path d="M1308.75 2521h0.0" /><text class="comment" x="1268.75" y="2526">out.d=&quot;2&quot;;</text></g></g><path d="M1328.0 2521a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2551h10.75" /><path d="M1317.25 2551h10.75" /><g class="terminal ">
<path d="M1154.75 2551h0.0" /><path d="M1217.25 2551h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1154.75" y="2540"></rect><text x="1186" y="2555">three</text></g><path d="M1217.25 2551h10" /><path d="M1227.25 2551h10" /><g class="non-terminal ">
<path d="M1237.25 2551h0.0" /><path d="M1317.25 2551h0.0" /><text class="comment" x="1277.25" y="2556">out.d=&quot;3&quot;;</text></g></g><path d="M1328.0 2551a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2581h15.0" /><path d="M1313.0 2581h15.0" /><g class="terminal ">
<path d="M1159.0 2581h0.0" /><path d="M1213.0 2581h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1159" y="2570"></rect><text x="1186" y="2585">four</text></g><path d="M1213.0 2581h10" /><path d="M1223.0 2581h10" /><g class="non-terminal ">
<path d="M1233.0 2581h0.0" /><path d="M1313.0 2581h0.0" /><text class="comment" x="1273" y="2586">out.d=&quot;4&quot;;</text></g></g><path d="M1328.0 2581a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2611h15.0" /><path d="M1313.0 2611h15.0" /><g class="terminal ">
<path d="M1159.0 2611h0.0" /><path d="M1213.0 2611h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1159" y="2600"></rect><text x="1186" y="2615">five</text></g><path d="M1213.0 2611h10" /><path d="M1223.0 2611h10" /><g class="non-terminal ">
<path d="M1233.0 2611h0.0" /><path d="M1313.0 2611h0.0" /><text class="comment" x="1273" y="2616">out.d=&quot;5&quot;;</text></g></g><path d="M1328.0 2611a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2641h19.25" /><path d="M1308.75 2641h19.25" /><g class="terminal ">
<path d="M1163.25 2641h0.0" /><path d="M1208.75 2641h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1163.25" y="2630"></rect><text x="1186" y="2645">six</text></g><path d="M1208.75 2641h10" /><path d="M1218.75 2641h10" /><g class="non-terminal ">
<path d="M1228.75 2641h0.0" /><path d="M1308.75 2641h0.0" /><text class="comment" x="1268.75" y="2646">out.d=&quot;6&quot;;</text></g></g><path d="M1328.0 2641a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2671h10.75" /><path d="M1317.25 2671h10.75" /><g class="terminal ">
<path d="M1154.75 2671h0.0" /><path d="M1217.25 2671h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1154.75" y="2660"></rect><text x="1186" y="2675">seven</text></g><path d="M1217.25 2671h10" /><path d="M1227.25 2671h10" /><g class="non-terminal ">
<path d="M1237.25 2671h0.0" /><path d="M1317.25 2671h0.0" /><text class="comment" x="1277.25" y="2676">out.d=&quot;7&quot;;</text></g></g><path d="M1328.0 2671a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2701h10.75" /><path d="M1317.25 2701h10.75" /><g class="terminal ">
<path d="M1154.75 2701h0.0" /><path d="M1217.25 2701h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1154.75" y="2690"></rect><text x="1186" y="2705">eight</text></g><path d="M1217.25 2701h10" /><path d="M1227.25 2701h10" /><g class="non-terminal ">
<path d="M1237.25 2701h0.0" /><path d="M1317.25 2701h0.0" /><text class="comment" x="1277.25" y="2706">out.d=&quot;8&quot;;</text></g></g><path d="M1328.0 2701a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1124.0 2431a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1144.0 2731h15.0" /><path d="M1313.0 2731h15.0" /><g class="terminal ">
<path d="M1159.0 2731h0.0" /><path d="M1213.0 2731h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1159" y="2720"></rect><text x="1186" y="2735">nine</text></g><path d="M1213.0 2731h10" /><path d="M1223.0 2731h10" /><g class="non-terminal ">
<path d="M1233.0 2731h0.0" /><path d="M1313.0 2731h0.0" /><text class="comment" x="1273" y="2736">out.d=&quot;9&quot;;</text></g></g><path d="M1328.0 2731a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1348.0 2431h10" /><path d="M1358.0 2431h10" /><g class="terminal ">
<path d="M1368.0 2431h0.0" /><path d="M1694.0 2431h0.0" /><rect height="22" rx="10" ry="10" width="326" x="1368" y="2420"></rect><text x="1531" y="2435">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M1694.0 2431h10" /><path d="M1704.0 2431h10" /><g class="terminal ">
<path d="M1714.0 2431h0.0" /><path d="M1980.5 2431h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="1714" y="2420"></rect><text x="1847.25" y="2435">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M1980.5 2431a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M2000.5 2161h10" /><path d="M2010.5 2161h10" /><g class="terminal ">
<path d="M2020.5 2161h0.0" /><path d="M2304.0 2161h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2020.5" y="2150"></rect><text x="2162.25" y="2165">!!out.d1=rules.doubleDigit.dd1;</text></g><path d="M2304.0 2161h10" /><path d="M2314.0 2161h10" /><g class="terminal ">
<path d="M2324.0 2161h0.0" /><path d="M2607.5 2161h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2324" y="2150"></rect><text x="2465.75" y="2165">out.d2=rules.doubleDigit.dd2;!!</text></g><path d="M2607.5 2161h10" /><path d="M2617.5 2161h10" /><g>
<path d="M2627.5 2161h0.0" /><path d="M2851.5 2161h0.0" /><g>
<path d="M2627.5 2161h0.0" /><path d="M2851.5 2161h0.0" /><path d="M2627.5 2161h20" /><g>
<path d="M2647.5 2161h0.0" /><path d="M2831.5 2161h0.0" /><g>
<path d="M2647.5 2161h0.0" /><path d="M2741.5 2161h0.0" /><path d="M2647.5 2161h20" /><g>
<path d="M2667.5 2161h0.0" /><path d="M2721.5 2161h0.0" /><g class="terminal ">
<path d="M2667.5 2161h0.0" /><path d="M2721.5 2161h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2667.5" y="2150"></rect><text x="2694.5" y="2165">zero</text></g></g><path d="M2721.5 2161h20" /><path d="M2647.5 2161a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2667.5 2191h8.5" /><path d="M2713.0 2191h8.5" /><g class="terminal ">
<path d="M2676.0 2191h0.0" /><path d="M2713.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2676" y="2180"></rect><text x="2694.5" y="2195">oh</text></g></g><path d="M2721.5 2191a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2741.5 2161h10" /><g class="non-terminal ">
<path d="M2751.5 2161h0.0" /><path d="M2831.5 2161h0.0" /><text class="comment" x="2791.5" y="2166">out.d=&quot;0&quot;;</text></g></g><path d="M2831.5 2161h20" /><path d="M2627.5 2161a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2221h19.25" /><path d="M2812.25 2221h19.25" /><g class="terminal ">
<path d="M2666.75 2221h0.0" /><path d="M2712.25 2221h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2666.75" y="2210"></rect><text x="2689.5" y="2225">one</text></g><path d="M2712.25 2221h10" /><path d="M2722.25 2221h10" /><g class="non-terminal ">
<path d="M2732.25 2221h0.0" /><path d="M2812.25 2221h0.0" /><text class="comment" x="2772.25" y="2226">out.d=&quot;1&quot;;</text></g></g><path d="M2831.5 2221a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2251h19.25" /><path d="M2812.25 2251h19.25" /><g class="terminal ">
<path d="M2666.75 2251h0.0" /><path d="M2712.25 2251h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2666.75" y="2240"></rect><text x="2689.5" y="2255">two</text></g><path d="M2712.25 2251h10" /><path d="M2722.25 2251h10" /><g class="non-terminal ">
<path d="M2732.25 2251h0.0" /><path d="M2812.25 2251h0.0" /><text class="comment" x="2772.25" y="2256">out.d=&quot;2&quot;;</text></g></g><path d="M2831.5 2251a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2281h10.75" /><path d="M2820.75 2281h10.75" /><g class="terminal ">
<path d="M2658.25 2281h0.0" /><path d="M2720.75 2281h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2658.25" y="2270"></rect><text x="2689.5" y="2285">three</text></g><path d="M2720.75 2281h10" /><path d="M2730.75 2281h10" /><g class="non-terminal ">
<path d="M2740.75 2281h0.0" /><path d="M2820.75 2281h0.0" /><text class="comment" x="2780.75" y="2286">out.d=&quot;3&quot;;</text></g></g><path d="M2831.5 2281a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2311h15.0" /><path d="M2816.5 2311h15.0" /><g class="terminal ">
<path d="M2662.5 2311h0.0" /><path d="M2716.5 2311h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2662.5" y="2300"></rect><text x="2689.5" y="2315">four</text></g><path d="M2716.5 2311h10" /><path d="M2726.5 2311h10" /><g class="non-terminal ">
<path d="M2736.5 2311h0.0" /><path d="M2816.5 2311h0.0" /><text class="comment" x="2776.5" y="2316">out.d=&quot;4&quot;;</text></g></g><path d="M2831.5 2311a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2341h15.0" /><path d="M2816.5 2341h15.0" /><g class="terminal ">
<path d="M2662.5 2341h0.0" /><path d="M2716.5 2341h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2662.5" y="2330"></rect><text x="2689.5" y="2345">five</text></g><path d="M2716.5 2341h10" /><path d="M2726.5 2341h10" /><g class="non-terminal ">
<path d="M2736.5 2341h0.0" /><path d="M2816.5 2341h0.0" /><text class="comment" x="2776.5" y="2346">out.d=&quot;5&quot;;</text></g></g><path d="M2831.5 2341a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2371h19.25" /><path d="M2812.25 2371h19.25" /><g class="terminal ">
<path d="M2666.75 2371h0.0" /><path d="M2712.25 2371h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2666.75" y="2360"></rect><text x="2689.5" y="2375">six</text></g><path d="M2712.25 2371h10" /><path d="M2722.25 2371h10" /><g class="non-terminal ">
<path d="M2732.25 2371h0.0" /><path d="M2812.25 2371h0.0" /><text class="comment" x="2772.25" y="2376">out.d=&quot;6&quot;;</text></g></g><path d="M2831.5 2371a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2401h10.75" /><path d="M2820.75 2401h10.75" /><g class="terminal ">
<path d="M2658.25 2401h0.0" /><path d="M2720.75 2401h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2658.25" y="2390"></rect><text x="2689.5" y="2405">seven</text></g><path d="M2720.75 2401h10" /><path d="M2730.75 2401h10" /><g class="non-terminal ">
<path d="M2740.75 2401h0.0" /><path d="M2820.75 2401h0.0" /><text class="comment" x="2780.75" y="2406">out.d=&quot;7&quot;;</text></g></g><path d="M2831.5 2401a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2431h10.75" /><path d="M2820.75 2431h10.75" /><g class="terminal ">
<path d="M2658.25 2431h0.0" /><path d="M2720.75 2431h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2658.25" y="2420"></rect><text x="2689.5" y="2435">eight</text></g><path d="M2720.75 2431h10" /><path d="M2730.75 2431h10" /><g class="non-terminal ">
<path d="M2740.75 2431h0.0" /><path d="M2820.75 2431h0.0" /><text class="comment" x="2780.75" y="2436">out.d=&quot;8&quot;;</text></g></g><path d="M2831.5 2431a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2627.5 2161a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2647.5 2461h15.0" /><path d="M2816.5 2461h15.0" /><g class="terminal ">
<path d="M2662.5 2461h0.0" /><path d="M2716.5 2461h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2662.5" y="2450"></rect><text x="2689.5" y="2465">nine</text></g><path d="M2716.5 2461h10" /><path d="M2726.5 2461h10" /><g class="non-terminal ">
<path d="M2736.5 2461h0.0" /><path d="M2816.5 2461h0.0" /><text class="comment" x="2776.5" y="2466">out.d=&quot;9&quot;;</text></g></g><path d="M2831.5 2461a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2851.5 2161h10" /><path d="M2861.5 2161h10" /><g class="non-terminal ">
<path d="M2871.5 2161h0.0" /><path d="M3070.5 2161h0.0" /><text class="comment" x="2971" y="2166">out.d3=rules.singleDigit.d;</text></g><path d="M3070.5 2161h10" /><path d="M3080.5 2161h10" /><g>
<path d="M3090.5 2161h0.0" /><path d="M3314.5 2161h0.0" /><g>
<path d="M3090.5 2161h0.0" /><path d="M3314.5 2161h0.0" /><path d="M3090.5 2161h20" /><g>
<path d="M3110.5 2161h0.0" /><path d="M3294.5 2161h0.0" /><g>
<path d="M3110.5 2161h0.0" /><path d="M3204.5 2161h0.0" /><path d="M3110.5 2161h20" /><g>
<path d="M3130.5 2161h0.0" /><path d="M3184.5 2161h0.0" /><g class="terminal ">
<path d="M3130.5 2161h0.0" /><path d="M3184.5 2161h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3130.5" y="2150"></rect><text x="3157.5" y="2165">zero</text></g></g><path d="M3184.5 2161h20" /><path d="M3110.5 2161a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3130.5 2191h8.5" /><path d="M3176.0 2191h8.5" /><g class="terminal ">
<path d="M3139.0 2191h0.0" /><path d="M3176.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3139" y="2180"></rect><text x="3157.5" y="2195">oh</text></g></g><path d="M3184.5 2191a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3204.5 2161h10" /><g class="non-terminal ">
<path d="M3214.5 2161h0.0" /><path d="M3294.5 2161h0.0" /><text class="comment" x="3254.5" y="2166">out.d=&quot;0&quot;;</text></g></g><path d="M3294.5 2161h20" /><path d="M3090.5 2161a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2221h19.25" /><path d="M3275.25 2221h19.25" /><g class="terminal ">
<path d="M3129.75 2221h0.0" /><path d="M3175.25 2221h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="2210"></rect><text x="3152.5" y="2225">one</text></g><path d="M3175.25 2221h10" /><path d="M3185.25 2221h10" /><g class="non-terminal ">
<path d="M3195.25 2221h0.0" /><path d="M3275.25 2221h0.0" /><text class="comment" x="3235.25" y="2226">out.d=&quot;1&quot;;</text></g></g><path d="M3294.5 2221a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2251h19.25" /><path d="M3275.25 2251h19.25" /><g class="terminal ">
<path d="M3129.75 2251h0.0" /><path d="M3175.25 2251h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="2240"></rect><text x="3152.5" y="2255">two</text></g><path d="M3175.25 2251h10" /><path d="M3185.25 2251h10" /><g class="non-terminal ">
<path d="M3195.25 2251h0.0" /><path d="M3275.25 2251h0.0" /><text class="comment" x="3235.25" y="2256">out.d=&quot;2&quot;;</text></g></g><path d="M3294.5 2251a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2281h10.75" /><path d="M3283.75 2281h10.75" /><g class="terminal ">
<path d="M3121.25 2281h0.0" /><path d="M3183.75 2281h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="2270"></rect><text x="3152.5" y="2285">three</text></g><path d="M3183.75 2281h10" /><path d="M3193.75 2281h10" /><g class="non-terminal ">
<path d="M3203.75 2281h0.0" /><path d="M3283.75 2281h0.0" /><text class="comment" x="3243.75" y="2286">out.d=&quot;3&quot;;</text></g></g><path d="M3294.5 2281a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2311h15.0" /><path d="M3279.5 2311h15.0" /><g class="terminal ">
<path d="M3125.5 2311h0.0" /><path d="M3179.5 2311h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="2300"></rect><text x="3152.5" y="2315">four</text></g><path d="M3179.5 2311h10" /><path d="M3189.5 2311h10" /><g class="non-terminal ">
<path d="M3199.5 2311h0.0" /><path d="M3279.5 2311h0.0" /><text class="comment" x="3239.5" y="2316">out.d=&quot;4&quot;;</text></g></g><path d="M3294.5 2311a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2341h15.0" /><path d="M3279.5 2341h15.0" /><g class="terminal ">
<path d="M3125.5 2341h0.0" /><path d="M3179.5 2341h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="2330"></rect><text x="3152.5" y="2345">five</text></g><path d="M3179.5 2341h10" /><path d="M3189.5 2341h10" /><g class="non-terminal ">
<path d="M3199.5 2341h0.0" /><path d="M3279.5 2341h0.0" /><text class="comment" x="3239.5" y="2346">out.d=&quot;5&quot;;</text></g></g><path d="M3294.5 2341a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2371h19.25" /><path d="M3275.25 2371h19.25" /><g class="terminal ">
<path d="M3129.75 2371h0.0" /><path d="M3175.25 2371h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3129.75" y="2360"></rect><text x="3152.5" y="2375">six</text></g><path d="M3175.25 2371h10" /><path d="M3185.25 2371h10" /><g class="non-terminal ">
<path d="M3195.25 2371h0.0" /><path d="M3275.25 2371h0.0" /><text class="comment" x="3235.25" y="2376">out.d=&quot;6&quot;;</text></g></g><path d="M3294.5 2371a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2401h10.75" /><path d="M3283.75 2401h10.75" /><g class="terminal ">
<path d="M3121.25 2401h0.0" /><path d="M3183.75 2401h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="2390"></rect><text x="3152.5" y="2405">seven</text></g><path d="M3183.75 2401h10" /><path d="M3193.75 2401h10" /><g class="non-terminal ">
<path d="M3203.75 2401h0.0" /><path d="M3283.75 2401h0.0" /><text class="comment" x="3243.75" y="2406">out.d=&quot;7&quot;;</text></g></g><path d="M3294.5 2401a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2431h10.75" /><path d="M3283.75 2431h10.75" /><g class="terminal ">
<path d="M3121.25 2431h0.0" /><path d="M3183.75 2431h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3121.25" y="2420"></rect><text x="3152.5" y="2435">eight</text></g><path d="M3183.75 2431h10" /><path d="M3193.75 2431h10" /><g class="non-terminal ">
<path d="M3203.75 2431h0.0" /><path d="M3283.75 2431h0.0" /><text class="comment" x="3243.75" y="2436">out.d=&quot;8&quot;;</text></g></g><path d="M3294.5 2431a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3090.5 2161a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3110.5 2461h15.0" /><path d="M3279.5 2461h15.0" /><g class="terminal ">
<path d="M3125.5 2461h0.0" /><path d="M3179.5 2461h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3125.5" y="2450"></rect><text x="3152.5" y="2465">nine</text></g><path d="M3179.5 2461h10" /><path d="M3189.5 2461h10" /><g class="non-terminal ">
<path d="M3199.5 2461h0.0" /><path d="M3279.5 2461h0.0" /><text class="comment" x="3239.5" y="2466">out.d=&quot;9&quot;;</text></g></g><path d="M3294.5 2461a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3314.5 2161h10" /><path d="M3324.5 2161h10" /><g class="non-terminal ">
<path d="M3334.5 2161h0.0" /><path d="M3533.5 2161h0.0" /><text class="comment" x="3434" y="2166">out.d4=rules.singleDigit.d;</text></g><path d="M3533.5 2161h10" /><path d="M3543.5 2161h10" /><g>
<path d="M3553.5 2161h0.0" /><path d="M3777.5 2161h0.0" /><g>
<path d="M3553.5 2161h0.0" /><path d="M3777.5 2161h0.0" /><path d="M3553.5 2161h20" /><g>
<path d="M3573.5 2161h0.0" /><path d="M3757.5 2161h0.0" /><g>
<path d="M3573.5 2161h0.0" /><path d="M3667.5 2161h0.0" /><path d="M3573.5 2161h20" /><g>
<path d="M3593.5 2161h0.0" /><path d="M3647.5 2161h0.0" /><g class="terminal ">
<path d="M3593.5 2161h0.0" /><path d="M3647.5 2161h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3593.5" y="2150"></rect><text x="3620.5" y="2165">zero</text></g></g><path d="M3647.5 2161h20" /><path d="M3573.5 2161a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M3593.5 2191h8.5" /><path d="M3639.0 2191h8.5" /><g class="terminal ">
<path d="M3602.0 2191h0.0" /><path d="M3639.0 2191h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3602" y="2180"></rect><text x="3620.5" y="2195">oh</text></g></g><path d="M3647.5 2191a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3667.5 2161h10" /><g class="non-terminal ">
<path d="M3677.5 2161h0.0" /><path d="M3757.5 2161h0.0" /><text class="comment" x="3717.5" y="2166">out.d=&quot;0&quot;;</text></g></g><path d="M3757.5 2161h20" /><path d="M3553.5 2161a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2221h19.25" /><path d="M3738.25 2221h19.25" /><g class="terminal ">
<path d="M3592.75 2221h0.0" /><path d="M3638.25 2221h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="2210"></rect><text x="3615.5" y="2225">one</text></g><path d="M3638.25 2221h10" /><path d="M3648.25 2221h10" /><g class="non-terminal ">
<path d="M3658.25 2221h0.0" /><path d="M3738.25 2221h0.0" /><text class="comment" x="3698.25" y="2226">out.d=&quot;1&quot;;</text></g></g><path d="M3757.5 2221a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2251h19.25" /><path d="M3738.25 2251h19.25" /><g class="terminal ">
<path d="M3592.75 2251h0.0" /><path d="M3638.25 2251h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="2240"></rect><text x="3615.5" y="2255">two</text></g><path d="M3638.25 2251h10" /><path d="M3648.25 2251h10" /><g class="non-terminal ">
<path d="M3658.25 2251h0.0" /><path d="M3738.25 2251h0.0" /><text class="comment" x="3698.25" y="2256">out.d=&quot;2&quot;;</text></g></g><path d="M3757.5 2251a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2281h10.75" /><path d="M3746.75 2281h10.75" /><g class="terminal ">
<path d="M3584.25 2281h0.0" /><path d="M3646.75 2281h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="2270"></rect><text x="3615.5" y="2285">three</text></g><path d="M3646.75 2281h10" /><path d="M3656.75 2281h10" /><g class="non-terminal ">
<path d="M3666.75 2281h0.0" /><path d="M3746.75 2281h0.0" /><text class="comment" x="3706.75" y="2286">out.d=&quot;3&quot;;</text></g></g><path d="M3757.5 2281a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2311h15.0" /><path d="M3742.5 2311h15.0" /><g class="terminal ">
<path d="M3588.5 2311h0.0" /><path d="M3642.5 2311h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="2300"></rect><text x="3615.5" y="2315">four</text></g><path d="M3642.5 2311h10" /><path d="M3652.5 2311h10" /><g class="non-terminal ">
<path d="M3662.5 2311h0.0" /><path d="M3742.5 2311h0.0" /><text class="comment" x="3702.5" y="2316">out.d=&quot;4&quot;;</text></g></g><path d="M3757.5 2311a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2341h15.0" /><path d="M3742.5 2341h15.0" /><g class="terminal ">
<path d="M3588.5 2341h0.0" /><path d="M3642.5 2341h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="2330"></rect><text x="3615.5" y="2345">five</text></g><path d="M3642.5 2341h10" /><path d="M3652.5 2341h10" /><g class="non-terminal ">
<path d="M3662.5 2341h0.0" /><path d="M3742.5 2341h0.0" /><text class="comment" x="3702.5" y="2346">out.d=&quot;5&quot;;</text></g></g><path d="M3757.5 2341a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2371h19.25" /><path d="M3738.25 2371h19.25" /><g class="terminal ">
<path d="M3592.75 2371h0.0" /><path d="M3638.25 2371h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="3592.75" y="2360"></rect><text x="3615.5" y="2375">six</text></g><path d="M3638.25 2371h10" /><path d="M3648.25 2371h10" /><g class="non-terminal ">
<path d="M3658.25 2371h0.0" /><path d="M3738.25 2371h0.0" /><text class="comment" x="3698.25" y="2376">out.d=&quot;6&quot;;</text></g></g><path d="M3757.5 2371a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2401h10.75" /><path d="M3746.75 2401h10.75" /><g class="terminal ">
<path d="M3584.25 2401h0.0" /><path d="M3646.75 2401h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="2390"></rect><text x="3615.5" y="2405">seven</text></g><path d="M3646.75 2401h10" /><path d="M3656.75 2401h10" /><g class="non-terminal ">
<path d="M3666.75 2401h0.0" /><path d="M3746.75 2401h0.0" /><text class="comment" x="3706.75" y="2406">out.d=&quot;7&quot;;</text></g></g><path d="M3757.5 2401a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2431h10.75" /><path d="M3746.75 2431h10.75" /><g class="terminal ">
<path d="M3584.25 2431h0.0" /><path d="M3646.75 2431h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="3584.25" y="2420"></rect><text x="3615.5" y="2435">eight</text></g><path d="M3646.75 2431h10" /><path d="M3656.75 2431h10" /><g class="non-terminal ">
<path d="M3666.75 2431h0.0" /><path d="M3746.75 2431h0.0" /><text class="comment" x="3706.75" y="2436">out.d=&quot;8&quot;;</text></g></g><path d="M3757.5 2431a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M3553.5 2161a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M3573.5 2461h15.0" /><path d="M3742.5 2461h15.0" /><g class="terminal ">
<path d="M3588.5 2461h0.0" /><path d="M3642.5 2461h0.0" /><rect height="22" rx="10" ry="10" width="54" x="3588.5" y="2450"></rect><text x="3615.5" y="2465">nine</text></g><path d="M3642.5 2461h10" /><path d="M3652.5 2461h10" /><g class="non-terminal ">
<path d="M3662.5 2461h0.0" /><path d="M3742.5 2461h0.0" /><text class="comment" x="3702.5" y="2466">out.d=&quot;9&quot;;</text></g></g><path d="M3757.5 2461a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3777.5 2161h10" /><path d="M3787.5 2161h10" /><g class="non-terminal ">
<path d="M3797.5 2161h0.0" /><path d="M3996.5 2161h0.0" /><text class="comment" x="3897" y="2166">out.d5=rules.singleDigit.d;</text></g></g><path d="M4443.0 2161a10 10 0 0 0 10 -10v-2110a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v2710a10 10 0 0 0 10 10" /><g>
<path d="M362.0 2761h0.0" /><path d="M4443.0 2761h0.0" /><g>
<path d="M362.0 2761h0.0" /><path d="M586.0 2761h0.0" /><g>
<path d="M362.0 2761h0.0" /><path d="M586.0 2761h0.0" /><path d="M362.0 2761h20" /><g>
<path d="M382.0 2761h0.0" /><path d="M566.0 2761h0.0" /><g>
<path d="M382.0 2761h0.0" /><path d="M476.0 2761h0.0" /><path d="M382.0 2761h20" /><g>
<path d="M402.0 2761h0.0" /><path d="M456.0 2761h0.0" /><g class="terminal ">
<path d="M402.0 2761h0.0" /><path d="M456.0 2761h0.0" /><rect height="22" rx="10" ry="10" width="54" x="402" y="2750"></rect><text x="429" y="2765">zero</text></g></g><path d="M456.0 2761h20" /><path d="M382.0 2761a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M402.0 2791h8.5" /><path d="M447.5 2791h8.5" /><g class="terminal ">
<path d="M410.5 2791h0.0" /><path d="M447.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="37" x="410.5" y="2780"></rect><text x="429" y="2795">oh</text></g></g><path d="M456.0 2791a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M476.0 2761h10" /><g class="non-terminal ">
<path d="M486.0 2761h0.0" /><path d="M566.0 2761h0.0" /><text class="comment" x="526" y="2766">out.d=&quot;0&quot;;</text></g></g><path d="M566.0 2761h20" /><path d="M362.0 2761a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2821h19.25" /><path d="M546.75 2821h19.25" /><g class="terminal ">
<path d="M401.25 2821h0.0" /><path d="M446.75 2821h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="401.25" y="2810"></rect><text x="424" y="2825">one</text></g><path d="M446.75 2821h10" /><path d="M456.75 2821h10" /><g class="non-terminal ">
<path d="M466.75 2821h0.0" /><path d="M546.75 2821h0.0" /><text class="comment" x="506.75" y="2826">out.d=&quot;1&quot;;</text></g></g><path d="M566.0 2821a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2851h19.25" /><path d="M546.75 2851h19.25" /><g class="terminal ">
<path d="M401.25 2851h0.0" /><path d="M446.75 2851h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="401.25" y="2840"></rect><text x="424" y="2855">two</text></g><path d="M446.75 2851h10" /><path d="M456.75 2851h10" /><g class="non-terminal ">
<path d="M466.75 2851h0.0" /><path d="M546.75 2851h0.0" /><text class="comment" x="506.75" y="2856">out.d=&quot;2&quot;;</text></g></g><path d="M566.0 2851a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2881h10.75" /><path d="M555.25 2881h10.75" /><g class="terminal ">
<path d="M392.75 2881h0.0" /><path d="M455.25 2881h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="392.75" y="2870"></rect><text x="424" y="2885">three</text></g><path d="M455.25 2881h10" /><path d="M465.25 2881h10" /><g class="non-terminal ">
<path d="M475.25 2881h0.0" /><path d="M555.25 2881h0.0" /><text class="comment" x="515.25" y="2886">out.d=&quot;3&quot;;</text></g></g><path d="M566.0 2881a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2911h15.0" /><path d="M551.0 2911h15.0" /><g class="terminal ">
<path d="M397.0 2911h0.0" /><path d="M451.0 2911h0.0" /><rect height="22" rx="10" ry="10" width="54" x="397" y="2900"></rect><text x="424" y="2915">four</text></g><path d="M451.0 2911h10" /><path d="M461.0 2911h10" /><g class="non-terminal ">
<path d="M471.0 2911h0.0" /><path d="M551.0 2911h0.0" /><text class="comment" x="511" y="2916">out.d=&quot;4&quot;;</text></g></g><path d="M566.0 2911a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2941h15.0" /><path d="M551.0 2941h15.0" /><g class="terminal ">
<path d="M397.0 2941h0.0" /><path d="M451.0 2941h0.0" /><rect height="22" rx="10" ry="10" width="54" x="397" y="2930"></rect><text x="424" y="2945">five</text></g><path d="M451.0 2941h10" /><path d="M461.0 2941h10" /><g class="non-terminal ">
<path d="M471.0 2941h0.0" /><path d="M551.0 2941h0.0" /><text class="comment" x="511" y="2946">out.d=&quot;5&quot;;</text></g></g><path d="M566.0 2941a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M382.0 2971h19.25" /><path d="M546.75 2971h19.25" /><g class="terminal ">
<path d="M401.25 2971h0.0" /><path d="M446.75 2971h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="401.25" y="2960"></rect><text x="424" y="2975">six</text></g><path d="M446.75 2971h10" /><path d="M456.75 2971h10" /><g class="non-terminal ">
<path d="M466.75 2971h0.0" /><path d="M546.75 2971h0.0" /><text class="comment" x="506.75" y="2976">out.d=&quot;6&quot;;</text></g></g><path d="M566.0 2971a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M382.0 3001h10.75" /><path d="M555.25 3001h10.75" /><g class="terminal ">
<path d="M392.75 3001h0.0" /><path d="M455.25 3001h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="392.75" y="2990"></rect><text x="424" y="3005">seven</text></g><path d="M455.25 3001h10" /><path d="M465.25 3001h10" /><g class="non-terminal ">
<path d="M475.25 3001h0.0" /><path d="M555.25 3001h0.0" /><text class="comment" x="515.25" y="3006">out.d=&quot;7&quot;;</text></g></g><path d="M566.0 3001a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M382.0 3031h10.75" /><path d="M555.25 3031h10.75" /><g class="terminal ">
<path d="M392.75 3031h0.0" /><path d="M455.25 3031h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="392.75" y="3020"></rect><text x="424" y="3035">eight</text></g><path d="M455.25 3031h10" /><path d="M465.25 3031h10" /><g class="non-terminal ">
<path d="M475.25 3031h0.0" /><path d="M555.25 3031h0.0" /><text class="comment" x="515.25" y="3036">out.d=&quot;8&quot;;</text></g></g><path d="M566.0 3031a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M362.0 2761a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M382.0 3061h15.0" /><path d="M551.0 3061h15.0" /><g class="terminal ">
<path d="M397.0 3061h0.0" /><path d="M451.0 3061h0.0" /><rect height="22" rx="10" ry="10" width="54" x="397" y="3050"></rect><text x="424" y="3065">nine</text></g><path d="M451.0 3061h10" /><path d="M461.0 3061h10" /><g class="non-terminal ">
<path d="M471.0 3061h0.0" /><path d="M551.0 3061h0.0" /><text class="comment" x="511" y="3066">out.d=&quot;9&quot;;</text></g></g><path d="M566.0 3061a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M586.0 2761h10" /><path d="M596.0 2761h10" /><g class="non-terminal ">
<path d="M606.0 2761h0.0" /><path d="M805.0 2761h0.0" /><text class="comment" x="705.5" y="2766">out.d1=rules.singleDigit.d;</text></g><path d="M805.0 2761h10" /><path d="M815.0 2761h10" /><g>
<path d="M825.0 2761h0.0" /><path d="M2017.0 2761h0.0" /><g>
<path d="M825.0 2761h0.0" /><path d="M2017.0 2761h0.0" /><path d="M825.0 2761h20" /><g>
<path d="M845.0 2761h87.75" /><path d="M1909.25 2761h87.75" /><g>
<path d="M932.75 2761h0.0" /><path d="M1387.25 2761h0.0" /><g>
<path d="M932.75 2761h0.0" /><path d="M1387.25 2761h0.0" /><path d="M932.75 2761h20" /><g>
<path d="M952.75 2761h12.75" /><path d="M1354.5 2761h12.75" /><g class="terminal ">
<path d="M965.5 2761h0.0" /><path d="M1036.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="71" x="965.5" y="2750"></rect><text x="1001" y="2765">eleven</text></g><path d="M1036.5 2761h10" /><path d="M1046.5 2761h10" /><g class="terminal ">
<path d="M1056.5 2761h0.0" /><path d="M1195.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1056.5" y="2750"></rect><text x="1126" y="2765">!!out.dd1=&quot;1&quot;;</text></g><path d="M1195.5 2761h10" /><path d="M1205.5 2761h10" /><g class="terminal ">
<path d="M1215.5 2761h0.0" /><path d="M1354.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1215.5" y="2750"></rect><text x="1285" y="2765">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M1367.25 2761h20" /><path d="M932.75 2761a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2791h12.75" /><path d="M1354.5 2791h12.75" /><g class="terminal ">
<path d="M965.5 2791h0.0" /><path d="M1036.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="71" x="965.5" y="2780"></rect><text x="1001" y="2795">twelve</text></g><path d="M1036.5 2791h10" /><path d="M1046.5 2791h10" /><g class="terminal ">
<path d="M1056.5 2791h0.0" /><path d="M1195.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1056.5" y="2780"></rect><text x="1126" y="2795">!!out.dd1=&quot;1&quot;;</text></g><path d="M1195.5 2791h10" /><path d="M1205.5 2791h10" /><g class="terminal ">
<path d="M1215.5 2791h0.0" /><path d="M1354.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1215.5" y="2780"></rect><text x="1285" y="2795">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M1367.25 2791a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2821h4.25" /><path d="M1363.0 2821h4.25" /><g class="terminal ">
<path d="M957.0 2821h0.0" /><path d="M1045.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="88" x="957" y="2810"></rect><text x="1001" y="2825">thirteen</text></g><path d="M1045.0 2821h10" /><path d="M1055.0 2821h10" /><g class="terminal ">
<path d="M1065.0 2821h0.0" /><path d="M1204.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1065" y="2810"></rect><text x="1134.5" y="2825">!!out.dd1=&quot;1&quot;;</text></g><path d="M1204.0 2821h10" /><path d="M1214.0 2821h10" /><g class="terminal ">
<path d="M1224.0 2821h0.0" /><path d="M1363.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1224" y="2810"></rect><text x="1293.5" y="2825">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M1367.25 2821a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2851h4.25" /><path d="M1363.0 2851h4.25" /><g class="terminal ">
<path d="M957.0 2851h0.0" /><path d="M1045.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="88" x="957" y="2840"></rect><text x="1001" y="2855">fourteen</text></g><path d="M1045.0 2851h10" /><path d="M1055.0 2851h10" /><g class="terminal ">
<path d="M1065.0 2851h0.0" /><path d="M1204.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1065" y="2840"></rect><text x="1134.5" y="2855">!!out.dd1=&quot;1&quot;;</text></g><path d="M1204.0 2851h10" /><path d="M1214.0 2851h10" /><g class="terminal ">
<path d="M1224.0 2851h0.0" /><path d="M1363.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1224" y="2840"></rect><text x="1293.5" y="2855">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M1367.25 2851a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2881h8.5" /><path d="M1358.75 2881h8.5" /><g class="terminal ">
<path d="M961.25 2881h0.0" /><path d="M1040.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="961.25" y="2870"></rect><text x="1001" y="2885">fifteen</text></g><path d="M1040.75 2881h10" /><path d="M1050.75 2881h10" /><g class="terminal ">
<path d="M1060.75 2881h0.0" /><path d="M1199.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1060.75" y="2870"></rect><text x="1130.25" y="2885">!!out.dd1=&quot;1&quot;;</text></g><path d="M1199.75 2881h10" /><path d="M1209.75 2881h10" /><g class="terminal ">
<path d="M1219.75 2881h0.0" /><path d="M1358.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1219.75" y="2870"></rect><text x="1289.25" y="2885">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M1367.25 2881a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2911h8.5" /><path d="M1358.75 2911h8.5" /><g class="terminal ">
<path d="M961.25 2911h0.0" /><path d="M1040.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="961.25" y="2900"></rect><text x="1001" y="2915">sixteen</text></g><path d="M1040.75 2911h10" /><path d="M1050.75 2911h10" /><g class="terminal ">
<path d="M1060.75 2911h0.0" /><path d="M1199.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1060.75" y="2900"></rect><text x="1130.25" y="2915">!!out.dd1=&quot;1&quot;;</text></g><path d="M1199.75 2911h10" /><path d="M1209.75 2911h10" /><g class="terminal ">
<path d="M1219.75 2911h0.0" /><path d="M1358.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1219.75" y="2900"></rect><text x="1289.25" y="2915">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M1367.25 2911a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2941h0.0" /><path d="M1367.25 2941h0.0" /><g class="terminal ">
<path d="M952.75 2941h0.0" /><path d="M1049.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="952.75" y="2930"></rect><text x="1001" y="2945">seventeen</text></g><path d="M1049.25 2941h10" /><path d="M1059.25 2941h10" /><g class="terminal ">
<path d="M1069.25 2941h0.0" /><path d="M1208.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1069.25" y="2930"></rect><text x="1138.75" y="2945">!!out.dd1=&quot;1&quot;;</text></g><path d="M1208.25 2941h10" /><path d="M1218.25 2941h10" /><g class="terminal ">
<path d="M1228.25 2941h0.0" /><path d="M1367.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1228.25" y="2930"></rect><text x="1297.75" y="2945">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M1367.25 2941a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M952.75 2971h4.25" /><path d="M1363.0 2971h4.25" /><g class="terminal ">
<path d="M957.0 2971h0.0" /><path d="M1045.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="88" x="957" y="2960"></rect><text x="1001" y="2975">eighteen</text></g><path d="M1045.0 2971h10" /><path d="M1055.0 2971h10" /><g class="terminal ">
<path d="M1065.0 2971h0.0" /><path d="M1204.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1065" y="2960"></rect><text x="1134.5" y="2975">!!out.dd1=&quot;1&quot;;</text></g><path d="M1204.0 2971h10" /><path d="M1214.0 2971h10" /><g class="terminal ">
<path d="M1224.0 2971h0.0" /><path d="M1363.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1224" y="2960"></rect><text x="1293.5" y="2975">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M1367.25 2971a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M932.75 2761a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M952.75 3001h4.25" /><path d="M1363.0 3001h4.25" /><g class="terminal ">
<path d="M957.0 3001h0.0" /><path d="M1045.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="88" x="957" y="2990"></rect><text x="1001" y="3005">nineteen</text></g><path d="M1045.0 3001h10" /><path d="M1055.0 3001h10" /><g class="terminal ">
<path d="M1065.0 3001h0.0" /><path d="M1204.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1065" y="2990"></rect><text x="1134.5" y="3005">!!out.dd1=&quot;1&quot;;</text></g><path d="M1204.0 3001h10" /><path d="M1214.0 3001h10" /><g class="terminal ">
<path d="M1224.0 3001h0.0" /><path d="M1363.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="139" x="1224" y="2990"></rect><text x="1293.5" y="3005">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M1367.25 3001a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M1387.25 2761h10" /><path d="M1397.25 2761h10" /><g class="terminal ">
<path d="M1407.25 2761h0.0" /><path d="M1648.25 2761h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1407.25" y="2750"></rect><text x="1527.75" y="2765">!!out.dd1=rules.teens.dd1;</text></g><path d="M1648.25 2761h10" /><path d="M1658.25 2761h10" /><g class="terminal ">
<path d="M1668.25 2761h0.0" /><path d="M1909.25 2761h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1668.25" y="2750"></rect><text x="1788.75" y="2765">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M1997.0 2761h20" /><path d="M825.0 2761a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M845.0 3031h0.0" /><path d="M1997.0 3031h0.0" /><g>
<path d="M845.0 3031h0.0" /><path d="M1120.5 3031h0.0" /><g>
<path d="M845.0 3031h0.0" /><path d="M1120.5 3031h0.0" /><path d="M845.0 3031h20" /><g>
<path d="M865.0 3031h4.25" /><path d="M1096.25 3031h4.25" /><g class="terminal ">
<path d="M869.25 3031h0.0" /><path d="M940.25 3031h0.0" /><rect height="22" rx="10" ry="10" width="71" x="869.25" y="3020"></rect><text x="904.75" y="3035">twenty</text></g><path d="M940.25 3031h10" /><path d="M950.25 3031h10" /><g class="non-terminal ">
<path d="M960.25 3031h0.0" /><path d="M1096.25 3031h0.0" /><text class="comment" x="1028.25" y="3036">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M1100.5 3031h20" /><path d="M845.0 3031a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3061h4.25" /><path d="M1096.25 3061h4.25" /><g class="terminal ">
<path d="M869.25 3061h0.0" /><path d="M940.25 3061h0.0" /><rect height="22" rx="10" ry="10" width="71" x="869.25" y="3050"></rect><text x="904.75" y="3065">thirty</text></g><path d="M940.25 3061h10" /><path d="M950.25 3061h10" /><g class="non-terminal ">
<path d="M960.25 3061h0.0" /><path d="M1096.25 3061h0.0" /><text class="comment" x="1028.25" y="3066">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M1100.5 3061a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3091h8.5" /><path d="M1092.0 3091h8.5" /><g class="terminal ">
<path d="M873.5 3091h0.0" /><path d="M936.0 3091h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="873.5" y="3080"></rect><text x="904.75" y="3095">forty</text></g><path d="M936.0 3091h10" /><path d="M946.0 3091h10" /><g class="non-terminal ">
<path d="M956.0 3091h0.0" /><path d="M1092.0 3091h0.0" /><text class="comment" x="1024" y="3096">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M1100.5 3091a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3121h8.5" /><path d="M1092.0 3121h8.5" /><g class="terminal ">
<path d="M873.5 3121h0.0" /><path d="M936.0 3121h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="873.5" y="3110"></rect><text x="904.75" y="3125">fifty</text></g><path d="M936.0 3121h10" /><path d="M946.0 3121h10" /><g class="non-terminal ">
<path d="M956.0 3121h0.0" /><path d="M1092.0 3121h0.0" /><text class="comment" x="1024" y="3126">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M1100.5 3121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3151h8.5" /><path d="M1092.0 3151h8.5" /><g class="terminal ">
<path d="M873.5 3151h0.0" /><path d="M936.0 3151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="873.5" y="3140"></rect><text x="904.75" y="3155">sixty</text></g><path d="M936.0 3151h10" /><path d="M946.0 3151h10" /><g class="non-terminal ">
<path d="M956.0 3151h0.0" /><path d="M1092.0 3151h0.0" /><text class="comment" x="1024" y="3156">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M1100.5 3151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3181h0.0" /><path d="M1100.5 3181h0.0" /><g class="terminal ">
<path d="M865.0 3181h0.0" /><path d="M944.5 3181h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="865" y="3170"></rect><text x="904.75" y="3185">seventy</text></g><path d="M944.5 3181h10" /><path d="M954.5 3181h10" /><g class="non-terminal ">
<path d="M964.5 3181h0.0" /><path d="M1100.5 3181h0.0" /><text class="comment" x="1032.5" y="3186">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M1100.5 3181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3211h4.25" /><path d="M1096.25 3211h4.25" /><g class="terminal ">
<path d="M869.25 3211h0.0" /><path d="M940.25 3211h0.0" /><rect height="22" rx="10" ry="10" width="71" x="869.25" y="3200"></rect><text x="904.75" y="3215">eighty</text></g><path d="M940.25 3211h10" /><path d="M950.25 3211h10" /><g class="non-terminal ">
<path d="M960.25 3211h0.0" /><path d="M1096.25 3211h0.0" /><text class="comment" x="1028.25" y="3216">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M1100.5 3211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M845.0 3031a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M865.0 3241h4.25" /><path d="M1096.25 3241h4.25" /><g class="terminal ">
<path d="M869.25 3241h0.0" /><path d="M940.25 3241h0.0" /><rect height="22" rx="10" ry="10" width="71" x="869.25" y="3230"></rect><text x="904.75" y="3245">ninety</text></g><path d="M940.25 3241h10" /><path d="M950.25 3241h10" /><g class="non-terminal ">
<path d="M960.25 3241h0.0" /><path d="M1096.25 3241h0.0" /><text class="comment" x="1028.25" y="3246">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M1100.5 3241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M1120.5 3031h10" /><path d="M1130.5 3031h10" /><g>
<path d="M1140.5 3031h0.0" /><path d="M1364.5 3031h0.0" /><g>
<path d="M1140.5 3031h0.0" /><path d="M1364.5 3031h0.0" /><path d="M1140.5 3031h20" /><g>
<path d="M1160.5 3031h0.0" /><path d="M1344.5 3031h0.0" /><g>
<path d="M1160.5 3031h0.0" /><path d="M1254.5 3031h0.0" /><path d="M1160.5 3031h20" /><g>
<path d="M1180.5 3031h0.0" /><path d="M1234.5 3031h0.0" /><g class="terminal ">
<path d="M1180.5 3031h0.0" /><path d="M1234.5 3031h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1180.5" y="3020"></rect><text x="1207.5" y="3035">zero</text></g></g><path d="M1234.5 3031h20" /><path d="M1160.5 3031a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1180.5 3061h8.5" /><path d="M1226.0 3061h8.5" /><g class="terminal ">
<path d="M1189.0 3061h0.0" /><path d="M1226.0 3061h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1189" y="3050"></rect><text x="1207.5" y="3065">oh</text></g></g><path d="M1234.5 3061a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M1254.5 3031h10" /><g class="non-terminal ">
<path d="M1264.5 3031h0.0" /><path d="M1344.5 3031h0.0" /><text class="comment" x="1304.5" y="3036">out.d=&quot;0&quot;;</text></g></g><path d="M1344.5 3031h20" /><path d="M1140.5 3031a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3091h19.25" /><path d="M1325.25 3091h19.25" /><g class="terminal ">
<path d="M1179.75 3091h0.0" /><path d="M1225.25 3091h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1179.75" y="3080"></rect><text x="1202.5" y="3095">one</text></g><path d="M1225.25 3091h10" /><path d="M1235.25 3091h10" /><g class="non-terminal ">
<path d="M1245.25 3091h0.0" /><path d="M1325.25 3091h0.0" /><text class="comment" x="1285.25" y="3096">out.d=&quot;1&quot;;</text></g></g><path d="M1344.5 3091a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3121h19.25" /><path d="M1325.25 3121h19.25" /><g class="terminal ">
<path d="M1179.75 3121h0.0" /><path d="M1225.25 3121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1179.75" y="3110"></rect><text x="1202.5" y="3125">two</text></g><path d="M1225.25 3121h10" /><path d="M1235.25 3121h10" /><g class="non-terminal ">
<path d="M1245.25 3121h0.0" /><path d="M1325.25 3121h0.0" /><text class="comment" x="1285.25" y="3126">out.d=&quot;2&quot;;</text></g></g><path d="M1344.5 3121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3151h10.75" /><path d="M1333.75 3151h10.75" /><g class="terminal ">
<path d="M1171.25 3151h0.0" /><path d="M1233.75 3151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1171.25" y="3140"></rect><text x="1202.5" y="3155">three</text></g><path d="M1233.75 3151h10" /><path d="M1243.75 3151h10" /><g class="non-terminal ">
<path d="M1253.75 3151h0.0" /><path d="M1333.75 3151h0.0" /><text class="comment" x="1293.75" y="3156">out.d=&quot;3&quot;;</text></g></g><path d="M1344.5 3151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3181h15.0" /><path d="M1329.5 3181h15.0" /><g class="terminal ">
<path d="M1175.5 3181h0.0" /><path d="M1229.5 3181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1175.5" y="3170"></rect><text x="1202.5" y="3185">four</text></g><path d="M1229.5 3181h10" /><path d="M1239.5 3181h10" /><g class="non-terminal ">
<path d="M1249.5 3181h0.0" /><path d="M1329.5 3181h0.0" /><text class="comment" x="1289.5" y="3186">out.d=&quot;4&quot;;</text></g></g><path d="M1344.5 3181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3211h15.0" /><path d="M1329.5 3211h15.0" /><g class="terminal ">
<path d="M1175.5 3211h0.0" /><path d="M1229.5 3211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1175.5" y="3200"></rect><text x="1202.5" y="3215">five</text></g><path d="M1229.5 3211h10" /><path d="M1239.5 3211h10" /><g class="non-terminal ">
<path d="M1249.5 3211h0.0" /><path d="M1329.5 3211h0.0" /><text class="comment" x="1289.5" y="3216">out.d=&quot;5&quot;;</text></g></g><path d="M1344.5 3211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3241h19.25" /><path d="M1325.25 3241h19.25" /><g class="terminal ">
<path d="M1179.75 3241h0.0" /><path d="M1225.25 3241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="1179.75" y="3230"></rect><text x="1202.5" y="3245">six</text></g><path d="M1225.25 3241h10" /><path d="M1235.25 3241h10" /><g class="non-terminal ">
<path d="M1245.25 3241h0.0" /><path d="M1325.25 3241h0.0" /><text class="comment" x="1285.25" y="3246">out.d=&quot;6&quot;;</text></g></g><path d="M1344.5 3241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3271h10.75" /><path d="M1333.75 3271h10.75" /><g class="terminal ">
<path d="M1171.25 3271h0.0" /><path d="M1233.75 3271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1171.25" y="3260"></rect><text x="1202.5" y="3275">seven</text></g><path d="M1233.75 3271h10" /><path d="M1243.75 3271h10" /><g class="non-terminal ">
<path d="M1253.75 3271h0.0" /><path d="M1333.75 3271h0.0" /><text class="comment" x="1293.75" y="3276">out.d=&quot;7&quot;;</text></g></g><path d="M1344.5 3271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3301h10.75" /><path d="M1333.75 3301h10.75" /><g class="terminal ">
<path d="M1171.25 3301h0.0" /><path d="M1233.75 3301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="1171.25" y="3290"></rect><text x="1202.5" y="3305">eight</text></g><path d="M1233.75 3301h10" /><path d="M1243.75 3301h10" /><g class="non-terminal ">
<path d="M1253.75 3301h0.0" /><path d="M1333.75 3301h0.0" /><text class="comment" x="1293.75" y="3306">out.d=&quot;8&quot;;</text></g></g><path d="M1344.5 3301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M1140.5 3031a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M1160.5 3331h15.0" /><path d="M1329.5 3331h15.0" /><g class="terminal ">
<path d="M1175.5 3331h0.0" /><path d="M1229.5 3331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="1175.5" y="3320"></rect><text x="1202.5" y="3335">nine</text></g><path d="M1229.5 3331h10" /><path d="M1239.5 3331h10" /><g class="non-terminal ">
<path d="M1249.5 3331h0.0" /><path d="M1329.5 3331h0.0" /><text class="comment" x="1289.5" y="3336">out.d=&quot;9&quot;;</text></g></g><path d="M1344.5 3331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M1364.5 3031h10" /><path d="M1374.5 3031h10" /><g class="terminal ">
<path d="M1384.5 3031h0.0" /><path d="M1710.5 3031h0.0" /><rect height="22" rx="10" ry="10" width="326" x="1384.5" y="3020"></rect><text x="1547.5" y="3035">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M1710.5 3031h10" /><path d="M1720.5 3031h10" /><g class="terminal ">
<path d="M1730.5 3031h0.0" /><path d="M1997.0 3031h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="1730.5" y="3020"></rect><text x="1863.75" y="3035">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M1997.0 3031a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M2017.0 2761h10" /><path d="M2027.0 2761h10" /><g class="terminal ">
<path d="M2037.0 2761h0.0" /><path d="M2320.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2037" y="2750"></rect><text x="2178.75" y="2765">!!out.d2=rules.doubleDigit.dd1;</text></g><path d="M2320.5 2761h10" /><path d="M2330.5 2761h10" /><g class="terminal ">
<path d="M2340.5 2761h0.0" /><path d="M2624.0 2761h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="2340.5" y="2750"></rect><text x="2482.25" y="2765">out.d3=rules.doubleDigit.dd2;!!</text></g><path d="M2624.0 2761h10" /><path d="M2634.0 2761h10" /><g>
<path d="M2644.0 2761h0.0" /><path d="M3836.0 2761h0.0" /><g>
<path d="M2644.0 2761h0.0" /><path d="M3836.0 2761h0.0" /><path d="M2644.0 2761h20" /><g>
<path d="M2664.0 2761h87.75" /><path d="M3728.25 2761h87.75" /><g>
<path d="M2751.75 2761h0.0" /><path d="M3206.25 2761h0.0" /><g>
<path d="M2751.75 2761h0.0" /><path d="M3206.25 2761h0.0" /><path d="M2751.75 2761h20" /><g>
<path d="M2771.75 2761h12.75" /><path d="M3173.5 2761h12.75" /><g class="terminal ">
<path d="M2784.5 2761h0.0" /><path d="M2855.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2784.5" y="2750"></rect><text x="2820" y="2765">eleven</text></g><path d="M2855.5 2761h10" /><path d="M2865.5 2761h10" /><g class="terminal ">
<path d="M2875.5 2761h0.0" /><path d="M3014.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2875.5" y="2750"></rect><text x="2945" y="2765">!!out.dd1=&quot;1&quot;;</text></g><path d="M3014.5 2761h10" /><path d="M3024.5 2761h10" /><g class="terminal ">
<path d="M3034.5 2761h0.0" /><path d="M3173.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3034.5" y="2750"></rect><text x="3104" y="2765">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M3186.25 2761h20" /><path d="M2751.75 2761a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2791h12.75" /><path d="M3173.5 2791h12.75" /><g class="terminal ">
<path d="M2784.5 2791h0.0" /><path d="M2855.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2784.5" y="2780"></rect><text x="2820" y="2795">twelve</text></g><path d="M2855.5 2791h10" /><path d="M2865.5 2791h10" /><g class="terminal ">
<path d="M2875.5 2791h0.0" /><path d="M3014.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2875.5" y="2780"></rect><text x="2945" y="2795">!!out.dd1=&quot;1&quot;;</text></g><path d="M3014.5 2791h10" /><path d="M3024.5 2791h10" /><g class="terminal ">
<path d="M3034.5 2791h0.0" /><path d="M3173.5 2791h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3034.5" y="2780"></rect><text x="3104" y="2795">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M3186.25 2791a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2821h4.25" /><path d="M3182.0 2821h4.25" /><g class="terminal ">
<path d="M2776.0 2821h0.0" /><path d="M2864.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="2810"></rect><text x="2820" y="2825">thirteen</text></g><path d="M2864.0 2821h10" /><path d="M2874.0 2821h10" /><g class="terminal ">
<path d="M2884.0 2821h0.0" /><path d="M3023.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="2810"></rect><text x="2953.5" y="2825">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 2821h10" /><path d="M3033.0 2821h10" /><g class="terminal ">
<path d="M3043.0 2821h0.0" /><path d="M3182.0 2821h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="2810"></rect><text x="3112.5" y="2825">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M3186.25 2821a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2851h4.25" /><path d="M3182.0 2851h4.25" /><g class="terminal ">
<path d="M2776.0 2851h0.0" /><path d="M2864.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="2840"></rect><text x="2820" y="2855">fourteen</text></g><path d="M2864.0 2851h10" /><path d="M2874.0 2851h10" /><g class="terminal ">
<path d="M2884.0 2851h0.0" /><path d="M3023.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="2840"></rect><text x="2953.5" y="2855">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 2851h10" /><path d="M3033.0 2851h10" /><g class="terminal ">
<path d="M3043.0 2851h0.0" /><path d="M3182.0 2851h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="2840"></rect><text x="3112.5" y="2855">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M3186.25 2851a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2881h8.5" /><path d="M3177.75 2881h8.5" /><g class="terminal ">
<path d="M2780.25 2881h0.0" /><path d="M2859.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2780.25" y="2870"></rect><text x="2820" y="2885">fifteen</text></g><path d="M2859.75 2881h10" /><path d="M2869.75 2881h10" /><g class="terminal ">
<path d="M2879.75 2881h0.0" /><path d="M3018.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2879.75" y="2870"></rect><text x="2949.25" y="2885">!!out.dd1=&quot;1&quot;;</text></g><path d="M3018.75 2881h10" /><path d="M3028.75 2881h10" /><g class="terminal ">
<path d="M3038.75 2881h0.0" /><path d="M3177.75 2881h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3038.75" y="2870"></rect><text x="3108.25" y="2885">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M3186.25 2881a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2911h8.5" /><path d="M3177.75 2911h8.5" /><g class="terminal ">
<path d="M2780.25 2911h0.0" /><path d="M2859.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2780.25" y="2900"></rect><text x="2820" y="2915">sixteen</text></g><path d="M2859.75 2911h10" /><path d="M2869.75 2911h10" /><g class="terminal ">
<path d="M2879.75 2911h0.0" /><path d="M3018.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2879.75" y="2900"></rect><text x="2949.25" y="2915">!!out.dd1=&quot;1&quot;;</text></g><path d="M3018.75 2911h10" /><path d="M3028.75 2911h10" /><g class="terminal ">
<path d="M3038.75 2911h0.0" /><path d="M3177.75 2911h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3038.75" y="2900"></rect><text x="3108.25" y="2915">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M3186.25 2911a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2941h0.0" /><path d="M3186.25 2941h0.0" /><g class="terminal ">
<path d="M2771.75 2941h0.0" /><path d="M2868.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="2771.75" y="2930"></rect><text x="2820" y="2945">seventeen</text></g><path d="M2868.25 2941h10" /><path d="M2878.25 2941h10" /><g class="terminal ">
<path d="M2888.25 2941h0.0" /><path d="M3027.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2888.25" y="2930"></rect><text x="2957.75" y="2945">!!out.dd1=&quot;1&quot;;</text></g><path d="M3027.25 2941h10" /><path d="M3037.25 2941h10" /><g class="terminal ">
<path d="M3047.25 2941h0.0" /><path d="M3186.25 2941h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3047.25" y="2930"></rect><text x="3116.75" y="2945">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M3186.25 2941a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 2971h4.25" /><path d="M3182.0 2971h4.25" /><g class="terminal ">
<path d="M2776.0 2971h0.0" /><path d="M2864.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="2960"></rect><text x="2820" y="2975">eighteen</text></g><path d="M2864.0 2971h10" /><path d="M2874.0 2971h10" /><g class="terminal ">
<path d="M2884.0 2971h0.0" /><path d="M3023.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="2960"></rect><text x="2953.5" y="2975">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 2971h10" /><path d="M3033.0 2971h10" /><g class="terminal ">
<path d="M3043.0 2971h0.0" /><path d="M3182.0 2971h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="2960"></rect><text x="3112.5" y="2975">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M3186.25 2971a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2751.75 2761a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3001h4.25" /><path d="M3182.0 3001h4.25" /><g class="terminal ">
<path d="M2776.0 3001h0.0" /><path d="M2864.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="2990"></rect><text x="2820" y="3005">nineteen</text></g><path d="M2864.0 3001h10" /><path d="M2874.0 3001h10" /><g class="terminal ">
<path d="M2884.0 3001h0.0" /><path d="M3023.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="2990"></rect><text x="2953.5" y="3005">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 3001h10" /><path d="M3033.0 3001h10" /><g class="terminal ">
<path d="M3043.0 3001h0.0" /><path d="M3182.0 3001h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="2990"></rect><text x="3112.5" y="3005">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M3186.25 3001a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M3206.25 2761h10" /><path d="M3216.25 2761h10" /><g class="terminal ">
<path d="M3226.25 2761h0.0" /><path d="M3467.25 2761h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3226.25" y="2750"></rect><text x="3346.75" y="2765">!!out.dd1=rules.teens.dd1;</text></g><path d="M3467.25 2761h10" /><path d="M3477.25 2761h10" /><g class="terminal ">
<path d="M3487.25 2761h0.0" /><path d="M3728.25 2761h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3487.25" y="2750"></rect><text x="3607.75" y="2765">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M3816.0 2761h20" /><path d="M2644.0 2761a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 3031h0.0" /><path d="M3816.0 3031h0.0" /><g>
<path d="M2664.0 3031h0.0" /><path d="M2939.5 3031h0.0" /><g>
<path d="M2664.0 3031h0.0" /><path d="M2939.5 3031h0.0" /><path d="M2664.0 3031h20" /><g>
<path d="M2684.0 3031h4.25" /><path d="M2915.25 3031h4.25" /><g class="terminal ">
<path d="M2688.25 3031h0.0" /><path d="M2759.25 3031h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3020"></rect><text x="2723.75" y="3035">twenty</text></g><path d="M2759.25 3031h10" /><path d="M2769.25 3031h10" /><g class="non-terminal ">
<path d="M2779.25 3031h0.0" /><path d="M2915.25 3031h0.0" /><text class="comment" x="2847.25" y="3036">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M2919.5 3031h20" /><path d="M2664.0 3031a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3061h4.25" /><path d="M2915.25 3061h4.25" /><g class="terminal ">
<path d="M2688.25 3061h0.0" /><path d="M2759.25 3061h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3050"></rect><text x="2723.75" y="3065">thirty</text></g><path d="M2759.25 3061h10" /><path d="M2769.25 3061h10" /><g class="non-terminal ">
<path d="M2779.25 3061h0.0" /><path d="M2915.25 3061h0.0" /><text class="comment" x="2847.25" y="3066">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M2919.5 3061a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3091h8.5" /><path d="M2911.0 3091h8.5" /><g class="terminal ">
<path d="M2692.5 3091h0.0" /><path d="M2755.0 3091h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3080"></rect><text x="2723.75" y="3095">forty</text></g><path d="M2755.0 3091h10" /><path d="M2765.0 3091h10" /><g class="non-terminal ">
<path d="M2775.0 3091h0.0" /><path d="M2911.0 3091h0.0" /><text class="comment" x="2843" y="3096">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M2919.5 3091a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3121h8.5" /><path d="M2911.0 3121h8.5" /><g class="terminal ">
<path d="M2692.5 3121h0.0" /><path d="M2755.0 3121h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3110"></rect><text x="2723.75" y="3125">fifty</text></g><path d="M2755.0 3121h10" /><path d="M2765.0 3121h10" /><g class="non-terminal ">
<path d="M2775.0 3121h0.0" /><path d="M2911.0 3121h0.0" /><text class="comment" x="2843" y="3126">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M2919.5 3121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3151h8.5" /><path d="M2911.0 3151h8.5" /><g class="terminal ">
<path d="M2692.5 3151h0.0" /><path d="M2755.0 3151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3140"></rect><text x="2723.75" y="3155">sixty</text></g><path d="M2755.0 3151h10" /><path d="M2765.0 3151h10" /><g class="non-terminal ">
<path d="M2775.0 3151h0.0" /><path d="M2911.0 3151h0.0" /><text class="comment" x="2843" y="3156">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M2919.5 3151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3181h0.0" /><path d="M2919.5 3181h0.0" /><g class="terminal ">
<path d="M2684.0 3181h0.0" /><path d="M2763.5 3181h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2684" y="3170"></rect><text x="2723.75" y="3185">seventy</text></g><path d="M2763.5 3181h10" /><path d="M2773.5 3181h10" /><g class="non-terminal ">
<path d="M2783.5 3181h0.0" /><path d="M2919.5 3181h0.0" /><text class="comment" x="2851.5" y="3186">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M2919.5 3181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3211h4.25" /><path d="M2915.25 3211h4.25" /><g class="terminal ">
<path d="M2688.25 3211h0.0" /><path d="M2759.25 3211h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3200"></rect><text x="2723.75" y="3215">eighty</text></g><path d="M2759.25 3211h10" /><path d="M2769.25 3211h10" /><g class="non-terminal ">
<path d="M2779.25 3211h0.0" /><path d="M2915.25 3211h0.0" /><text class="comment" x="2847.25" y="3216">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M2919.5 3211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2664.0 3031a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3241h4.25" /><path d="M2915.25 3241h4.25" /><g class="terminal ">
<path d="M2688.25 3241h0.0" /><path d="M2759.25 3241h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3230"></rect><text x="2723.75" y="3245">ninety</text></g><path d="M2759.25 3241h10" /><path d="M2769.25 3241h10" /><g class="non-terminal ">
<path d="M2779.25 3241h0.0" /><path d="M2915.25 3241h0.0" /><text class="comment" x="2847.25" y="3246">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M2919.5 3241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M2939.5 3031h10" /><path d="M2949.5 3031h10" /><g>
<path d="M2959.5 3031h0.0" /><path d="M3183.5 3031h0.0" /><g>
<path d="M2959.5 3031h0.0" /><path d="M3183.5 3031h0.0" /><path d="M2959.5 3031h20" /><g>
<path d="M2979.5 3031h0.0" /><path d="M3163.5 3031h0.0" /><g>
<path d="M2979.5 3031h0.0" /><path d="M3073.5 3031h0.0" /><path d="M2979.5 3031h20" /><g>
<path d="M2999.5 3031h0.0" /><path d="M3053.5 3031h0.0" /><g class="terminal ">
<path d="M2999.5 3031h0.0" /><path d="M3053.5 3031h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2999.5" y="3020"></rect><text x="3026.5" y="3035">zero</text></g></g><path d="M3053.5 3031h20" /><path d="M2979.5 3031a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2999.5 3061h8.5" /><path d="M3045.0 3061h8.5" /><g class="terminal ">
<path d="M3008.0 3061h0.0" /><path d="M3045.0 3061h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3008" y="3050"></rect><text x="3026.5" y="3065">oh</text></g></g><path d="M3053.5 3061a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3073.5 3031h10" /><g class="non-terminal ">
<path d="M3083.5 3031h0.0" /><path d="M3163.5 3031h0.0" /><text class="comment" x="3123.5" y="3036">out.d=&quot;0&quot;;</text></g></g><path d="M3163.5 3031h20" /><path d="M2959.5 3031a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3091h19.25" /><path d="M3144.25 3091h19.25" /><g class="terminal ">
<path d="M2998.75 3091h0.0" /><path d="M3044.25 3091h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3080"></rect><text x="3021.5" y="3095">one</text></g><path d="M3044.25 3091h10" /><path d="M3054.25 3091h10" /><g class="non-terminal ">
<path d="M3064.25 3091h0.0" /><path d="M3144.25 3091h0.0" /><text class="comment" x="3104.25" y="3096">out.d=&quot;1&quot;;</text></g></g><path d="M3163.5 3091a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3121h19.25" /><path d="M3144.25 3121h19.25" /><g class="terminal ">
<path d="M2998.75 3121h0.0" /><path d="M3044.25 3121h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3110"></rect><text x="3021.5" y="3125">two</text></g><path d="M3044.25 3121h10" /><path d="M3054.25 3121h10" /><g class="non-terminal ">
<path d="M3064.25 3121h0.0" /><path d="M3144.25 3121h0.0" /><text class="comment" x="3104.25" y="3126">out.d=&quot;2&quot;;</text></g></g><path d="M3163.5 3121a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3151h10.75" /><path d="M3152.75 3151h10.75" /><g class="terminal ">
<path d="M2990.25 3151h0.0" /><path d="M3052.75 3151h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3140"></rect><text x="3021.5" y="3155">three</text></g><path d="M3052.75 3151h10" /><path d="M3062.75 3151h10" /><g class="non-terminal ">
<path d="M3072.75 3151h0.0" /><path d="M3152.75 3151h0.0" /><text class="comment" x="3112.75" y="3156">out.d=&quot;3&quot;;</text></g></g><path d="M3163.5 3151a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3181h15.0" /><path d="M3148.5 3181h15.0" /><g class="terminal ">
<path d="M2994.5 3181h0.0" /><path d="M3048.5 3181h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3170"></rect><text x="3021.5" y="3185">four</text></g><path d="M3048.5 3181h10" /><path d="M3058.5 3181h10" /><g class="non-terminal ">
<path d="M3068.5 3181h0.0" /><path d="M3148.5 3181h0.0" /><text class="comment" x="3108.5" y="3186">out.d=&quot;4&quot;;</text></g></g><path d="M3163.5 3181a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3211h15.0" /><path d="M3148.5 3211h15.0" /><g class="terminal ">
<path d="M2994.5 3211h0.0" /><path d="M3048.5 3211h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3200"></rect><text x="3021.5" y="3215">five</text></g><path d="M3048.5 3211h10" /><path d="M3058.5 3211h10" /><g class="non-terminal ">
<path d="M3068.5 3211h0.0" /><path d="M3148.5 3211h0.0" /><text class="comment" x="3108.5" y="3216">out.d=&quot;5&quot;;</text></g></g><path d="M3163.5 3211a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3241h19.25" /><path d="M3144.25 3241h19.25" /><g class="terminal ">
<path d="M2998.75 3241h0.0" /><path d="M3044.25 3241h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3230"></rect><text x="3021.5" y="3245">six</text></g><path d="M3044.25 3241h10" /><path d="M3054.25 3241h10" /><g class="non-terminal ">
<path d="M3064.25 3241h0.0" /><path d="M3144.25 3241h0.0" /><text class="comment" x="3104.25" y="3246">out.d=&quot;6&quot;;</text></g></g><path d="M3163.5 3241a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3271h10.75" /><path d="M3152.75 3271h10.75" /><g class="terminal ">
<path d="M2990.25 3271h0.0" /><path d="M3052.75 3271h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3260"></rect><text x="3021.5" y="3275">seven</text></g><path d="M3052.75 3271h10" /><path d="M3062.75 3271h10" /><g class="non-terminal ">
<path d="M3072.75 3271h0.0" /><path d="M3152.75 3271h0.0" /><text class="comment" x="3112.75" y="3276">out.d=&quot;7&quot;;</text></g></g><path d="M3163.5 3271a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3301h10.75" /><path d="M3152.75 3301h10.75" /><g class="terminal ">
<path d="M2990.25 3301h0.0" /><path d="M3052.75 3301h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3290"></rect><text x="3021.5" y="3305">eight</text></g><path d="M3052.75 3301h10" /><path d="M3062.75 3301h10" /><g class="non-terminal ">
<path d="M3072.75 3301h0.0" /><path d="M3152.75 3301h0.0" /><text class="comment" x="3112.75" y="3306">out.d=&quot;8&quot;;</text></g></g><path d="M3163.5 3301a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2959.5 3031a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3331h15.0" /><path d="M3148.5 3331h15.0" /><g class="terminal ">
<path d="M2994.5 3331h0.0" /><path d="M3048.5 3331h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3320"></rect><text x="3021.5" y="3335">nine</text></g><path d="M3048.5 3331h10" /><path d="M3058.5 3331h10" /><g class="non-terminal ">
<path d="M3068.5 3331h0.0" /><path d="M3148.5 3331h0.0" /><text class="comment" x="3108.5" y="3336">out.d=&quot;9&quot;;</text></g></g><path d="M3163.5 3331a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3183.5 3031h10" /><path d="M3193.5 3031h10" /><g class="terminal ">
<path d="M3203.5 3031h0.0" /><path d="M3529.5 3031h0.0" /><rect height="22" rx="10" ry="10" width="326" x="3203.5" y="3020"></rect><text x="3366.5" y="3035">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M3529.5 3031h10" /><path d="M3539.5 3031h10" /><g class="terminal ">
<path d="M3549.5 3031h0.0" /><path d="M3816.0 3031h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="3549.5" y="3020"></rect><text x="3682.75" y="3035">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M3816.0 3031a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M3836.0 2761h10" /><path d="M3846.0 2761h10" /><g class="terminal ">
<path d="M3856.0 2761h0.0" /><path d="M4139.5 2761h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3856" y="2750"></rect><text x="3997.75" y="2765">!!out.d4=rules.doubleDigit.dd1;</text></g><path d="M4139.5 2761h10" /><path d="M4149.5 2761h10" /><g class="terminal ">
<path d="M4159.5 2761h0.0" /><path d="M4443.0 2761h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="4159.5" y="2750"></rect><text x="4301.25" y="2765">out.d5=rules.doubleDigit.dd2;!!</text></g></g><path d="M4443.0 2761a10 10 0 0 0 10 -10v-2710a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v3310a10 10 0 0 0 10 10" /><g>
<path d="M362.0 3361h0.0" /><path d="M4443.0 3361h0.0" /><g>
<path d="M362.0 3361h0.0" /><path d="M1554.0 3361h0.0" /><g>
<path d="M362.0 3361h0.0" /><path d="M1554.0 3361h0.0" /><path d="M362.0 3361h20" /><g>
<path d="M382.0 3361h87.75" /><path d="M1446.25 3361h87.75" /><g>
<path d="M469.75 3361h0.0" /><path d="M924.25 3361h0.0" /><g>
<path d="M469.75 3361h0.0" /><path d="M924.25 3361h0.0" /><path d="M469.75 3361h20" /><g>
<path d="M489.75 3361h12.75" /><path d="M891.5 3361h12.75" /><g class="terminal ">
<path d="M502.5 3361h0.0" /><path d="M573.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="71" x="502.5" y="3350"></rect><text x="538" y="3365">eleven</text></g><path d="M573.5 3361h10" /><path d="M583.5 3361h10" /><g class="terminal ">
<path d="M593.5 3361h0.0" /><path d="M732.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="593.5" y="3350"></rect><text x="663" y="3365">!!out.dd1=&quot;1&quot;;</text></g><path d="M732.5 3361h10" /><path d="M742.5 3361h10" /><g class="terminal ">
<path d="M752.5 3361h0.0" /><path d="M891.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="752.5" y="3350"></rect><text x="822" y="3365">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M904.25 3361h20" /><path d="M469.75 3361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3391h12.75" /><path d="M891.5 3391h12.75" /><g class="terminal ">
<path d="M502.5 3391h0.0" /><path d="M573.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="71" x="502.5" y="3380"></rect><text x="538" y="3395">twelve</text></g><path d="M573.5 3391h10" /><path d="M583.5 3391h10" /><g class="terminal ">
<path d="M593.5 3391h0.0" /><path d="M732.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="593.5" y="3380"></rect><text x="663" y="3395">!!out.dd1=&quot;1&quot;;</text></g><path d="M732.5 3391h10" /><path d="M742.5 3391h10" /><g class="terminal ">
<path d="M752.5 3391h0.0" /><path d="M891.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="752.5" y="3380"></rect><text x="822" y="3395">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M904.25 3391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3421h4.25" /><path d="M900.0 3421h4.25" /><g class="terminal ">
<path d="M494.0 3421h0.0" /><path d="M582.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="3410"></rect><text x="538" y="3425">thirteen</text></g><path d="M582.0 3421h10" /><path d="M592.0 3421h10" /><g class="terminal ">
<path d="M602.0 3421h0.0" /><path d="M741.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="3410"></rect><text x="671.5" y="3425">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 3421h10" /><path d="M751.0 3421h10" /><g class="terminal ">
<path d="M761.0 3421h0.0" /><path d="M900.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="3410"></rect><text x="830.5" y="3425">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M904.25 3421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3451h4.25" /><path d="M900.0 3451h4.25" /><g class="terminal ">
<path d="M494.0 3451h0.0" /><path d="M582.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="3440"></rect><text x="538" y="3455">fourteen</text></g><path d="M582.0 3451h10" /><path d="M592.0 3451h10" /><g class="terminal ">
<path d="M602.0 3451h0.0" /><path d="M741.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="3440"></rect><text x="671.5" y="3455">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 3451h10" /><path d="M751.0 3451h10" /><g class="terminal ">
<path d="M761.0 3451h0.0" /><path d="M900.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="3440"></rect><text x="830.5" y="3455">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M904.25 3451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3481h8.5" /><path d="M895.75 3481h8.5" /><g class="terminal ">
<path d="M498.25 3481h0.0" /><path d="M577.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="498.25" y="3470"></rect><text x="538" y="3485">fifteen</text></g><path d="M577.75 3481h10" /><path d="M587.75 3481h10" /><g class="terminal ">
<path d="M597.75 3481h0.0" /><path d="M736.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="597.75" y="3470"></rect><text x="667.25" y="3485">!!out.dd1=&quot;1&quot;;</text></g><path d="M736.75 3481h10" /><path d="M746.75 3481h10" /><g class="terminal ">
<path d="M756.75 3481h0.0" /><path d="M895.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="756.75" y="3470"></rect><text x="826.25" y="3485">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M904.25 3481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3511h8.5" /><path d="M895.75 3511h8.5" /><g class="terminal ">
<path d="M498.25 3511h0.0" /><path d="M577.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="498.25" y="3500"></rect><text x="538" y="3515">sixteen</text></g><path d="M577.75 3511h10" /><path d="M587.75 3511h10" /><g class="terminal ">
<path d="M597.75 3511h0.0" /><path d="M736.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="597.75" y="3500"></rect><text x="667.25" y="3515">!!out.dd1=&quot;1&quot;;</text></g><path d="M736.75 3511h10" /><path d="M746.75 3511h10" /><g class="terminal ">
<path d="M756.75 3511h0.0" /><path d="M895.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="756.75" y="3500"></rect><text x="826.25" y="3515">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M904.25 3511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3541h0.0" /><path d="M904.25 3541h0.0" /><g class="terminal ">
<path d="M489.75 3541h0.0" /><path d="M586.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="489.75" y="3530"></rect><text x="538" y="3545">seventeen</text></g><path d="M586.25 3541h10" /><path d="M596.25 3541h10" /><g class="terminal ">
<path d="M606.25 3541h0.0" /><path d="M745.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="606.25" y="3530"></rect><text x="675.75" y="3545">!!out.dd1=&quot;1&quot;;</text></g><path d="M745.25 3541h10" /><path d="M755.25 3541h10" /><g class="terminal ">
<path d="M765.25 3541h0.0" /><path d="M904.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="765.25" y="3530"></rect><text x="834.75" y="3545">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M904.25 3541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3571h4.25" /><path d="M900.0 3571h4.25" /><g class="terminal ">
<path d="M494.0 3571h0.0" /><path d="M582.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="3560"></rect><text x="538" y="3575">eighteen</text></g><path d="M582.0 3571h10" /><path d="M592.0 3571h10" /><g class="terminal ">
<path d="M602.0 3571h0.0" /><path d="M741.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="3560"></rect><text x="671.5" y="3575">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 3571h10" /><path d="M751.0 3571h10" /><g class="terminal ">
<path d="M761.0 3571h0.0" /><path d="M900.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="3560"></rect><text x="830.5" y="3575">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M904.25 3571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M469.75 3361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3601h4.25" /><path d="M900.0 3601h4.25" /><g class="terminal ">
<path d="M494.0 3601h0.0" /><path d="M582.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="3590"></rect><text x="538" y="3605">nineteen</text></g><path d="M582.0 3601h10" /><path d="M592.0 3601h10" /><g class="terminal ">
<path d="M602.0 3601h0.0" /><path d="M741.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="3590"></rect><text x="671.5" y="3605">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 3601h10" /><path d="M751.0 3601h10" /><g class="terminal ">
<path d="M761.0 3601h0.0" /><path d="M900.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="3590"></rect><text x="830.5" y="3605">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M904.25 3601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M924.25 3361h10" /><path d="M934.25 3361h10" /><g class="terminal ">
<path d="M944.25 3361h0.0" /><path d="M1185.25 3361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="944.25" y="3350"></rect><text x="1064.75" y="3365">!!out.dd1=rules.teens.dd1;</text></g><path d="M1185.25 3361h10" /><path d="M1195.25 3361h10" /><g class="terminal ">
<path d="M1205.25 3361h0.0" /><path d="M1446.25 3361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1205.25" y="3350"></rect><text x="1325.75" y="3365">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M1534.0 3361h20" /><path d="M362.0 3361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M382.0 3631h0.0" /><path d="M1534.0 3631h0.0" /><g>
<path d="M382.0 3631h0.0" /><path d="M657.5 3631h0.0" /><g>
<path d="M382.0 3631h0.0" /><path d="M657.5 3631h0.0" /><path d="M382.0 3631h20" /><g>
<path d="M402.0 3631h4.25" /><path d="M633.25 3631h4.25" /><g class="terminal ">
<path d="M406.25 3631h0.0" /><path d="M477.25 3631h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="3620"></rect><text x="441.75" y="3635">twenty</text></g><path d="M477.25 3631h10" /><path d="M487.25 3631h10" /><g class="non-terminal ">
<path d="M497.25 3631h0.0" /><path d="M633.25 3631h0.0" /><text class="comment" x="565.25" y="3636">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M637.5 3631h20" /><path d="M382.0 3631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3661h4.25" /><path d="M633.25 3661h4.25" /><g class="terminal ">
<path d="M406.25 3661h0.0" /><path d="M477.25 3661h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="3650"></rect><text x="441.75" y="3665">thirty</text></g><path d="M477.25 3661h10" /><path d="M487.25 3661h10" /><g class="non-terminal ">
<path d="M497.25 3661h0.0" /><path d="M633.25 3661h0.0" /><text class="comment" x="565.25" y="3666">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M637.5 3661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3691h8.5" /><path d="M629.0 3691h8.5" /><g class="terminal ">
<path d="M410.5 3691h0.0" /><path d="M473.0 3691h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="3680"></rect><text x="441.75" y="3695">forty</text></g><path d="M473.0 3691h10" /><path d="M483.0 3691h10" /><g class="non-terminal ">
<path d="M493.0 3691h0.0" /><path d="M629.0 3691h0.0" /><text class="comment" x="561" y="3696">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M637.5 3691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3721h8.5" /><path d="M629.0 3721h8.5" /><g class="terminal ">
<path d="M410.5 3721h0.0" /><path d="M473.0 3721h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="3710"></rect><text x="441.75" y="3725">fifty</text></g><path d="M473.0 3721h10" /><path d="M483.0 3721h10" /><g class="non-terminal ">
<path d="M493.0 3721h0.0" /><path d="M629.0 3721h0.0" /><text class="comment" x="561" y="3726">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M637.5 3721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3751h8.5" /><path d="M629.0 3751h8.5" /><g class="terminal ">
<path d="M410.5 3751h0.0" /><path d="M473.0 3751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="3740"></rect><text x="441.75" y="3755">sixty</text></g><path d="M473.0 3751h10" /><path d="M483.0 3751h10" /><g class="non-terminal ">
<path d="M493.0 3751h0.0" /><path d="M629.0 3751h0.0" /><text class="comment" x="561" y="3756">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M637.5 3751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3781h0.0" /><path d="M637.5 3781h0.0" /><g class="terminal ">
<path d="M402.0 3781h0.0" /><path d="M481.5 3781h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="402" y="3770"></rect><text x="441.75" y="3785">seventy</text></g><path d="M481.5 3781h10" /><path d="M491.5 3781h10" /><g class="non-terminal ">
<path d="M501.5 3781h0.0" /><path d="M637.5 3781h0.0" /><text class="comment" x="569.5" y="3786">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M637.5 3781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3811h4.25" /><path d="M633.25 3811h4.25" /><g class="terminal ">
<path d="M406.25 3811h0.0" /><path d="M477.25 3811h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="3800"></rect><text x="441.75" y="3815">eighty</text></g><path d="M477.25 3811h10" /><path d="M487.25 3811h10" /><g class="non-terminal ">
<path d="M497.25 3811h0.0" /><path d="M633.25 3811h0.0" /><text class="comment" x="565.25" y="3816">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M637.5 3811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M382.0 3631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M402.0 3841h4.25" /><path d="M633.25 3841h4.25" /><g class="terminal ">
<path d="M406.25 3841h0.0" /><path d="M477.25 3841h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="3830"></rect><text x="441.75" y="3845">ninety</text></g><path d="M477.25 3841h10" /><path d="M487.25 3841h10" /><g class="non-terminal ">
<path d="M497.25 3841h0.0" /><path d="M633.25 3841h0.0" /><text class="comment" x="565.25" y="3846">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M637.5 3841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M657.5 3631h10" /><path d="M667.5 3631h10" /><g>
<path d="M677.5 3631h0.0" /><path d="M901.5 3631h0.0" /><g>
<path d="M677.5 3631h0.0" /><path d="M901.5 3631h0.0" /><path d="M677.5 3631h20" /><g>
<path d="M697.5 3631h0.0" /><path d="M881.5 3631h0.0" /><g>
<path d="M697.5 3631h0.0" /><path d="M791.5 3631h0.0" /><path d="M697.5 3631h20" /><g>
<path d="M717.5 3631h0.0" /><path d="M771.5 3631h0.0" /><g class="terminal ">
<path d="M717.5 3631h0.0" /><path d="M771.5 3631h0.0" /><rect height="22" rx="10" ry="10" width="54" x="717.5" y="3620"></rect><text x="744.5" y="3635">zero</text></g></g><path d="M771.5 3631h20" /><path d="M697.5 3631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M717.5 3661h8.5" /><path d="M763.0 3661h8.5" /><g class="terminal ">
<path d="M726.0 3661h0.0" /><path d="M763.0 3661h0.0" /><rect height="22" rx="10" ry="10" width="37" x="726" y="3650"></rect><text x="744.5" y="3665">oh</text></g></g><path d="M771.5 3661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M791.5 3631h10" /><g class="non-terminal ">
<path d="M801.5 3631h0.0" /><path d="M881.5 3631h0.0" /><text class="comment" x="841.5" y="3636">out.d=&quot;0&quot;;</text></g></g><path d="M881.5 3631h20" /><path d="M677.5 3631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3691h19.25" /><path d="M862.25 3691h19.25" /><g class="terminal ">
<path d="M716.75 3691h0.0" /><path d="M762.25 3691h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="3680"></rect><text x="739.5" y="3695">one</text></g><path d="M762.25 3691h10" /><path d="M772.25 3691h10" /><g class="non-terminal ">
<path d="M782.25 3691h0.0" /><path d="M862.25 3691h0.0" /><text class="comment" x="822.25" y="3696">out.d=&quot;1&quot;;</text></g></g><path d="M881.5 3691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3721h19.25" /><path d="M862.25 3721h19.25" /><g class="terminal ">
<path d="M716.75 3721h0.0" /><path d="M762.25 3721h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="3710"></rect><text x="739.5" y="3725">two</text></g><path d="M762.25 3721h10" /><path d="M772.25 3721h10" /><g class="non-terminal ">
<path d="M782.25 3721h0.0" /><path d="M862.25 3721h0.0" /><text class="comment" x="822.25" y="3726">out.d=&quot;2&quot;;</text></g></g><path d="M881.5 3721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3751h10.75" /><path d="M870.75 3751h10.75" /><g class="terminal ">
<path d="M708.25 3751h0.0" /><path d="M770.75 3751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="3740"></rect><text x="739.5" y="3755">three</text></g><path d="M770.75 3751h10" /><path d="M780.75 3751h10" /><g class="non-terminal ">
<path d="M790.75 3751h0.0" /><path d="M870.75 3751h0.0" /><text class="comment" x="830.75" y="3756">out.d=&quot;3&quot;;</text></g></g><path d="M881.5 3751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3781h15.0" /><path d="M866.5 3781h15.0" /><g class="terminal ">
<path d="M712.5 3781h0.0" /><path d="M766.5 3781h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="3770"></rect><text x="739.5" y="3785">four</text></g><path d="M766.5 3781h10" /><path d="M776.5 3781h10" /><g class="non-terminal ">
<path d="M786.5 3781h0.0" /><path d="M866.5 3781h0.0" /><text class="comment" x="826.5" y="3786">out.d=&quot;4&quot;;</text></g></g><path d="M881.5 3781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3811h15.0" /><path d="M866.5 3811h15.0" /><g class="terminal ">
<path d="M712.5 3811h0.0" /><path d="M766.5 3811h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="3800"></rect><text x="739.5" y="3815">five</text></g><path d="M766.5 3811h10" /><path d="M776.5 3811h10" /><g class="non-terminal ">
<path d="M786.5 3811h0.0" /><path d="M866.5 3811h0.0" /><text class="comment" x="826.5" y="3816">out.d=&quot;5&quot;;</text></g></g><path d="M881.5 3811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3841h19.25" /><path d="M862.25 3841h19.25" /><g class="terminal ">
<path d="M716.75 3841h0.0" /><path d="M762.25 3841h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="3830"></rect><text x="739.5" y="3845">six</text></g><path d="M762.25 3841h10" /><path d="M772.25 3841h10" /><g class="non-terminal ">
<path d="M782.25 3841h0.0" /><path d="M862.25 3841h0.0" /><text class="comment" x="822.25" y="3846">out.d=&quot;6&quot;;</text></g></g><path d="M881.5 3841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3871h10.75" /><path d="M870.75 3871h10.75" /><g class="terminal ">
<path d="M708.25 3871h0.0" /><path d="M770.75 3871h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="3860"></rect><text x="739.5" y="3875">seven</text></g><path d="M770.75 3871h10" /><path d="M780.75 3871h10" /><g class="non-terminal ">
<path d="M790.75 3871h0.0" /><path d="M870.75 3871h0.0" /><text class="comment" x="830.75" y="3876">out.d=&quot;7&quot;;</text></g></g><path d="M881.5 3871a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3901h10.75" /><path d="M870.75 3901h10.75" /><g class="terminal ">
<path d="M708.25 3901h0.0" /><path d="M770.75 3901h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="3890"></rect><text x="739.5" y="3905">eight</text></g><path d="M770.75 3901h10" /><path d="M780.75 3901h10" /><g class="non-terminal ">
<path d="M790.75 3901h0.0" /><path d="M870.75 3901h0.0" /><text class="comment" x="830.75" y="3906">out.d=&quot;8&quot;;</text></g></g><path d="M881.5 3901a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M677.5 3631a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M697.5 3931h15.0" /><path d="M866.5 3931h15.0" /><g class="terminal ">
<path d="M712.5 3931h0.0" /><path d="M766.5 3931h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="3920"></rect><text x="739.5" y="3935">nine</text></g><path d="M766.5 3931h10" /><path d="M776.5 3931h10" /><g class="non-terminal ">
<path d="M786.5 3931h0.0" /><path d="M866.5 3931h0.0" /><text class="comment" x="826.5" y="3936">out.d=&quot;9&quot;;</text></g></g><path d="M881.5 3931a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M901.5 3631h10" /><path d="M911.5 3631h10" /><g class="terminal ">
<path d="M921.5 3631h0.0" /><path d="M1247.5 3631h0.0" /><rect height="22" rx="10" ry="10" width="326" x="921.5" y="3620"></rect><text x="1084.5" y="3635">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M1247.5 3631h10" /><path d="M1257.5 3631h10" /><g class="terminal ">
<path d="M1267.5 3631h0.0" /><path d="M1534.0 3631h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="1267.5" y="3620"></rect><text x="1400.75" y="3635">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M1534.0 3631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M1554.0 3361h10" /><path d="M1564.0 3361h10" /><g class="terminal ">
<path d="M1574.0 3361h0.0" /><path d="M1857.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="1574" y="3350"></rect><text x="1715.75" y="3365">!!out.d1=rules.doubleDigit.dd1;</text></g><path d="M1857.5 3361h10" /><path d="M1867.5 3361h10" /><g class="terminal ">
<path d="M1877.5 3361h0.0" /><path d="M2161.0 3361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="1877.5" y="3350"></rect><text x="2019.25" y="3365">out.d2=rules.doubleDigit.dd2;!!</text></g><path d="M2161.0 3361h10" /><path d="M2171.0 3361h10" /><g>
<path d="M2181.0 3361h0.0" /><path d="M2405.0 3361h0.0" /><g>
<path d="M2181.0 3361h0.0" /><path d="M2405.0 3361h0.0" /><path d="M2181.0 3361h20" /><g>
<path d="M2201.0 3361h0.0" /><path d="M2385.0 3361h0.0" /><g>
<path d="M2201.0 3361h0.0" /><path d="M2295.0 3361h0.0" /><path d="M2201.0 3361h20" /><g>
<path d="M2221.0 3361h0.0" /><path d="M2275.0 3361h0.0" /><g class="terminal ">
<path d="M2221.0 3361h0.0" /><path d="M2275.0 3361h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2221" y="3350"></rect><text x="2248" y="3365">zero</text></g></g><path d="M2275.0 3361h20" /><path d="M2201.0 3361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 3391h8.5" /><path d="M2266.5 3391h8.5" /><g class="terminal ">
<path d="M2229.5 3391h0.0" /><path d="M2266.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2229.5" y="3380"></rect><text x="2248" y="3395">oh</text></g></g><path d="M2275.0 3391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2295.0 3361h10" /><g class="non-terminal ">
<path d="M2305.0 3361h0.0" /><path d="M2385.0 3361h0.0" /><text class="comment" x="2345" y="3366">out.d=&quot;0&quot;;</text></g></g><path d="M2385.0 3361h20" /><path d="M2181.0 3361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3421h19.25" /><path d="M2365.75 3421h19.25" /><g class="terminal ">
<path d="M2220.25 3421h0.0" /><path d="M2265.75 3421h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="3410"></rect><text x="2243" y="3425">one</text></g><path d="M2265.75 3421h10" /><path d="M2275.75 3421h10" /><g class="non-terminal ">
<path d="M2285.75 3421h0.0" /><path d="M2365.75 3421h0.0" /><text class="comment" x="2325.75" y="3426">out.d=&quot;1&quot;;</text></g></g><path d="M2385.0 3421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3451h19.25" /><path d="M2365.75 3451h19.25" /><g class="terminal ">
<path d="M2220.25 3451h0.0" /><path d="M2265.75 3451h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="3440"></rect><text x="2243" y="3455">two</text></g><path d="M2265.75 3451h10" /><path d="M2275.75 3451h10" /><g class="non-terminal ">
<path d="M2285.75 3451h0.0" /><path d="M2365.75 3451h0.0" /><text class="comment" x="2325.75" y="3456">out.d=&quot;2&quot;;</text></g></g><path d="M2385.0 3451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3481h10.75" /><path d="M2374.25 3481h10.75" /><g class="terminal ">
<path d="M2211.75 3481h0.0" /><path d="M2274.25 3481h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="3470"></rect><text x="2243" y="3485">three</text></g><path d="M2274.25 3481h10" /><path d="M2284.25 3481h10" /><g class="non-terminal ">
<path d="M2294.25 3481h0.0" /><path d="M2374.25 3481h0.0" /><text class="comment" x="2334.25" y="3486">out.d=&quot;3&quot;;</text></g></g><path d="M2385.0 3481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3511h15.0" /><path d="M2370.0 3511h15.0" /><g class="terminal ">
<path d="M2216.0 3511h0.0" /><path d="M2270.0 3511h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="3500"></rect><text x="2243" y="3515">four</text></g><path d="M2270.0 3511h10" /><path d="M2280.0 3511h10" /><g class="non-terminal ">
<path d="M2290.0 3511h0.0" /><path d="M2370.0 3511h0.0" /><text class="comment" x="2330" y="3516">out.d=&quot;4&quot;;</text></g></g><path d="M2385.0 3511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3541h15.0" /><path d="M2370.0 3541h15.0" /><g class="terminal ">
<path d="M2216.0 3541h0.0" /><path d="M2270.0 3541h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="3530"></rect><text x="2243" y="3545">five</text></g><path d="M2270.0 3541h10" /><path d="M2280.0 3541h10" /><g class="non-terminal ">
<path d="M2290.0 3541h0.0" /><path d="M2370.0 3541h0.0" /><text class="comment" x="2330" y="3546">out.d=&quot;5&quot;;</text></g></g><path d="M2385.0 3541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3571h19.25" /><path d="M2365.75 3571h19.25" /><g class="terminal ">
<path d="M2220.25 3571h0.0" /><path d="M2265.75 3571h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2220.25" y="3560"></rect><text x="2243" y="3575">six</text></g><path d="M2265.75 3571h10" /><path d="M2275.75 3571h10" /><g class="non-terminal ">
<path d="M2285.75 3571h0.0" /><path d="M2365.75 3571h0.0" /><text class="comment" x="2325.75" y="3576">out.d=&quot;6&quot;;</text></g></g><path d="M2385.0 3571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3601h10.75" /><path d="M2374.25 3601h10.75" /><g class="terminal ">
<path d="M2211.75 3601h0.0" /><path d="M2274.25 3601h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="3590"></rect><text x="2243" y="3605">seven</text></g><path d="M2274.25 3601h10" /><path d="M2284.25 3601h10" /><g class="non-terminal ">
<path d="M2294.25 3601h0.0" /><path d="M2374.25 3601h0.0" /><text class="comment" x="2334.25" y="3606">out.d=&quot;7&quot;;</text></g></g><path d="M2385.0 3601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3631h10.75" /><path d="M2374.25 3631h10.75" /><g class="terminal ">
<path d="M2211.75 3631h0.0" /><path d="M2274.25 3631h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2211.75" y="3620"></rect><text x="2243" y="3635">eight</text></g><path d="M2274.25 3631h10" /><path d="M2284.25 3631h10" /><g class="non-terminal ">
<path d="M2294.25 3631h0.0" /><path d="M2374.25 3631h0.0" /><text class="comment" x="2334.25" y="3636">out.d=&quot;8&quot;;</text></g></g><path d="M2385.0 3631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2181.0 3361a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 3661h15.0" /><path d="M2370.0 3661h15.0" /><g class="terminal ">
<path d="M2216.0 3661h0.0" /><path d="M2270.0 3661h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2216" y="3650"></rect><text x="2243" y="3665">nine</text></g><path d="M2270.0 3661h10" /><path d="M2280.0 3661h10" /><g class="non-terminal ">
<path d="M2290.0 3661h0.0" /><path d="M2370.0 3661h0.0" /><text class="comment" x="2330" y="3666">out.d=&quot;9&quot;;</text></g></g><path d="M2385.0 3661a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2405.0 3361h10" /><path d="M2415.0 3361h10" /><g class="non-terminal ">
<path d="M2425.0 3361h0.0" /><path d="M2624.0 3361h0.0" /><text class="comment" x="2524.5" y="3366">out.d3=rules.singleDigit.d;</text></g><path d="M2624.0 3361h10" /><path d="M2634.0 3361h10" /><g>
<path d="M2644.0 3361h0.0" /><path d="M3836.0 3361h0.0" /><g>
<path d="M2644.0 3361h0.0" /><path d="M3836.0 3361h0.0" /><path d="M2644.0 3361h20" /><g>
<path d="M2664.0 3361h87.75" /><path d="M3728.25 3361h87.75" /><g>
<path d="M2751.75 3361h0.0" /><path d="M3206.25 3361h0.0" /><g>
<path d="M2751.75 3361h0.0" /><path d="M3206.25 3361h0.0" /><path d="M2751.75 3361h20" /><g>
<path d="M2771.75 3361h12.75" /><path d="M3173.5 3361h12.75" /><g class="terminal ">
<path d="M2784.5 3361h0.0" /><path d="M2855.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2784.5" y="3350"></rect><text x="2820" y="3365">eleven</text></g><path d="M2855.5 3361h10" /><path d="M2865.5 3361h10" /><g class="terminal ">
<path d="M2875.5 3361h0.0" /><path d="M3014.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2875.5" y="3350"></rect><text x="2945" y="3365">!!out.dd1=&quot;1&quot;;</text></g><path d="M3014.5 3361h10" /><path d="M3024.5 3361h10" /><g class="terminal ">
<path d="M3034.5 3361h0.0" /><path d="M3173.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3034.5" y="3350"></rect><text x="3104" y="3365">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M3186.25 3361h20" /><path d="M2751.75 3361a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3391h12.75" /><path d="M3173.5 3391h12.75" /><g class="terminal ">
<path d="M2784.5 3391h0.0" /><path d="M2855.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2784.5" y="3380"></rect><text x="2820" y="3395">twelve</text></g><path d="M2855.5 3391h10" /><path d="M2865.5 3391h10" /><g class="terminal ">
<path d="M2875.5 3391h0.0" /><path d="M3014.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2875.5" y="3380"></rect><text x="2945" y="3395">!!out.dd1=&quot;1&quot;;</text></g><path d="M3014.5 3391h10" /><path d="M3024.5 3391h10" /><g class="terminal ">
<path d="M3034.5 3391h0.0" /><path d="M3173.5 3391h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3034.5" y="3380"></rect><text x="3104" y="3395">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M3186.25 3391a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3421h4.25" /><path d="M3182.0 3421h4.25" /><g class="terminal ">
<path d="M2776.0 3421h0.0" /><path d="M2864.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="3410"></rect><text x="2820" y="3425">thirteen</text></g><path d="M2864.0 3421h10" /><path d="M2874.0 3421h10" /><g class="terminal ">
<path d="M2884.0 3421h0.0" /><path d="M3023.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="3410"></rect><text x="2953.5" y="3425">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 3421h10" /><path d="M3033.0 3421h10" /><g class="terminal ">
<path d="M3043.0 3421h0.0" /><path d="M3182.0 3421h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="3410"></rect><text x="3112.5" y="3425">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M3186.25 3421a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3451h4.25" /><path d="M3182.0 3451h4.25" /><g class="terminal ">
<path d="M2776.0 3451h0.0" /><path d="M2864.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="3440"></rect><text x="2820" y="3455">fourteen</text></g><path d="M2864.0 3451h10" /><path d="M2874.0 3451h10" /><g class="terminal ">
<path d="M2884.0 3451h0.0" /><path d="M3023.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="3440"></rect><text x="2953.5" y="3455">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 3451h10" /><path d="M3033.0 3451h10" /><g class="terminal ">
<path d="M3043.0 3451h0.0" /><path d="M3182.0 3451h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="3440"></rect><text x="3112.5" y="3455">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M3186.25 3451a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3481h8.5" /><path d="M3177.75 3481h8.5" /><g class="terminal ">
<path d="M2780.25 3481h0.0" /><path d="M2859.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2780.25" y="3470"></rect><text x="2820" y="3485">fifteen</text></g><path d="M2859.75 3481h10" /><path d="M2869.75 3481h10" /><g class="terminal ">
<path d="M2879.75 3481h0.0" /><path d="M3018.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2879.75" y="3470"></rect><text x="2949.25" y="3485">!!out.dd1=&quot;1&quot;;</text></g><path d="M3018.75 3481h10" /><path d="M3028.75 3481h10" /><g class="terminal ">
<path d="M3038.75 3481h0.0" /><path d="M3177.75 3481h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3038.75" y="3470"></rect><text x="3108.25" y="3485">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M3186.25 3481a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3511h8.5" /><path d="M3177.75 3511h8.5" /><g class="terminal ">
<path d="M2780.25 3511h0.0" /><path d="M2859.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2780.25" y="3500"></rect><text x="2820" y="3515">sixteen</text></g><path d="M2859.75 3511h10" /><path d="M2869.75 3511h10" /><g class="terminal ">
<path d="M2879.75 3511h0.0" /><path d="M3018.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2879.75" y="3500"></rect><text x="2949.25" y="3515">!!out.dd1=&quot;1&quot;;</text></g><path d="M3018.75 3511h10" /><path d="M3028.75 3511h10" /><g class="terminal ">
<path d="M3038.75 3511h0.0" /><path d="M3177.75 3511h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3038.75" y="3500"></rect><text x="3108.25" y="3515">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M3186.25 3511a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3541h0.0" /><path d="M3186.25 3541h0.0" /><g class="terminal ">
<path d="M2771.75 3541h0.0" /><path d="M2868.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="2771.75" y="3530"></rect><text x="2820" y="3545">seventeen</text></g><path d="M2868.25 3541h10" /><path d="M2878.25 3541h10" /><g class="terminal ">
<path d="M2888.25 3541h0.0" /><path d="M3027.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2888.25" y="3530"></rect><text x="2957.75" y="3545">!!out.dd1=&quot;1&quot;;</text></g><path d="M3027.25 3541h10" /><path d="M3037.25 3541h10" /><g class="terminal ">
<path d="M3047.25 3541h0.0" /><path d="M3186.25 3541h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3047.25" y="3530"></rect><text x="3116.75" y="3545">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M3186.25 3541a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3571h4.25" /><path d="M3182.0 3571h4.25" /><g class="terminal ">
<path d="M2776.0 3571h0.0" /><path d="M2864.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="3560"></rect><text x="2820" y="3575">eighteen</text></g><path d="M2864.0 3571h10" /><path d="M2874.0 3571h10" /><g class="terminal ">
<path d="M2884.0 3571h0.0" /><path d="M3023.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="3560"></rect><text x="2953.5" y="3575">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 3571h10" /><path d="M3033.0 3571h10" /><g class="terminal ">
<path d="M3043.0 3571h0.0" /><path d="M3182.0 3571h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="3560"></rect><text x="3112.5" y="3575">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M3186.25 3571a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2751.75 3361a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2771.75 3601h4.25" /><path d="M3182.0 3601h4.25" /><g class="terminal ">
<path d="M2776.0 3601h0.0" /><path d="M2864.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2776" y="3590"></rect><text x="2820" y="3605">nineteen</text></g><path d="M2864.0 3601h10" /><path d="M2874.0 3601h10" /><g class="terminal ">
<path d="M2884.0 3601h0.0" /><path d="M3023.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2884" y="3590"></rect><text x="2953.5" y="3605">!!out.dd1=&quot;1&quot;;</text></g><path d="M3023.0 3601h10" /><path d="M3033.0 3601h10" /><g class="terminal ">
<path d="M3043.0 3601h0.0" /><path d="M3182.0 3601h0.0" /><rect height="22" rx="10" ry="10" width="139" x="3043" y="3590"></rect><text x="3112.5" y="3605">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M3186.25 3601a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M3206.25 3361h10" /><path d="M3216.25 3361h10" /><g class="terminal ">
<path d="M3226.25 3361h0.0" /><path d="M3467.25 3361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3226.25" y="3350"></rect><text x="3346.75" y="3365">!!out.dd1=rules.teens.dd1;</text></g><path d="M3467.25 3361h10" /><path d="M3477.25 3361h10" /><g class="terminal ">
<path d="M3487.25 3361h0.0" /><path d="M3728.25 3361h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3487.25" y="3350"></rect><text x="3607.75" y="3365">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M3816.0 3361h20" /><path d="M2644.0 3361a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2664.0 3631h0.0" /><path d="M3816.0 3631h0.0" /><g>
<path d="M2664.0 3631h0.0" /><path d="M2939.5 3631h0.0" /><g>
<path d="M2664.0 3631h0.0" /><path d="M2939.5 3631h0.0" /><path d="M2664.0 3631h20" /><g>
<path d="M2684.0 3631h4.25" /><path d="M2915.25 3631h4.25" /><g class="terminal ">
<path d="M2688.25 3631h0.0" /><path d="M2759.25 3631h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3620"></rect><text x="2723.75" y="3635">twenty</text></g><path d="M2759.25 3631h10" /><path d="M2769.25 3631h10" /><g class="non-terminal ">
<path d="M2779.25 3631h0.0" /><path d="M2915.25 3631h0.0" /><text class="comment" x="2847.25" y="3636">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M2919.5 3631h20" /><path d="M2664.0 3631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3661h4.25" /><path d="M2915.25 3661h4.25" /><g class="terminal ">
<path d="M2688.25 3661h0.0" /><path d="M2759.25 3661h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3650"></rect><text x="2723.75" y="3665">thirty</text></g><path d="M2759.25 3661h10" /><path d="M2769.25 3661h10" /><g class="non-terminal ">
<path d="M2779.25 3661h0.0" /><path d="M2915.25 3661h0.0" /><text class="comment" x="2847.25" y="3666">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M2919.5 3661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3691h8.5" /><path d="M2911.0 3691h8.5" /><g class="terminal ">
<path d="M2692.5 3691h0.0" /><path d="M2755.0 3691h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3680"></rect><text x="2723.75" y="3695">forty</text></g><path d="M2755.0 3691h10" /><path d="M2765.0 3691h10" /><g class="non-terminal ">
<path d="M2775.0 3691h0.0" /><path d="M2911.0 3691h0.0" /><text class="comment" x="2843" y="3696">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M2919.5 3691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3721h8.5" /><path d="M2911.0 3721h8.5" /><g class="terminal ">
<path d="M2692.5 3721h0.0" /><path d="M2755.0 3721h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3710"></rect><text x="2723.75" y="3725">fifty</text></g><path d="M2755.0 3721h10" /><path d="M2765.0 3721h10" /><g class="non-terminal ">
<path d="M2775.0 3721h0.0" /><path d="M2911.0 3721h0.0" /><text class="comment" x="2843" y="3726">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M2919.5 3721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3751h8.5" /><path d="M2911.0 3751h8.5" /><g class="terminal ">
<path d="M2692.5 3751h0.0" /><path d="M2755.0 3751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2692.5" y="3740"></rect><text x="2723.75" y="3755">sixty</text></g><path d="M2755.0 3751h10" /><path d="M2765.0 3751h10" /><g class="non-terminal ">
<path d="M2775.0 3751h0.0" /><path d="M2911.0 3751h0.0" /><text class="comment" x="2843" y="3756">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M2919.5 3751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3781h0.0" /><path d="M2919.5 3781h0.0" /><g class="terminal ">
<path d="M2684.0 3781h0.0" /><path d="M2763.5 3781h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2684" y="3770"></rect><text x="2723.75" y="3785">seventy</text></g><path d="M2763.5 3781h10" /><path d="M2773.5 3781h10" /><g class="non-terminal ">
<path d="M2783.5 3781h0.0" /><path d="M2919.5 3781h0.0" /><text class="comment" x="2851.5" y="3786">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M2919.5 3781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3811h4.25" /><path d="M2915.25 3811h4.25" /><g class="terminal ">
<path d="M2688.25 3811h0.0" /><path d="M2759.25 3811h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3800"></rect><text x="2723.75" y="3815">eighty</text></g><path d="M2759.25 3811h10" /><path d="M2769.25 3811h10" /><g class="non-terminal ">
<path d="M2779.25 3811h0.0" /><path d="M2915.25 3811h0.0" /><text class="comment" x="2847.25" y="3816">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M2919.5 3811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2664.0 3631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2684.0 3841h4.25" /><path d="M2915.25 3841h4.25" /><g class="terminal ">
<path d="M2688.25 3841h0.0" /><path d="M2759.25 3841h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2688.25" y="3830"></rect><text x="2723.75" y="3845">ninety</text></g><path d="M2759.25 3841h10" /><path d="M2769.25 3841h10" /><g class="non-terminal ">
<path d="M2779.25 3841h0.0" /><path d="M2915.25 3841h0.0" /><text class="comment" x="2847.25" y="3846">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M2919.5 3841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M2939.5 3631h10" /><path d="M2949.5 3631h10" /><g>
<path d="M2959.5 3631h0.0" /><path d="M3183.5 3631h0.0" /><g>
<path d="M2959.5 3631h0.0" /><path d="M3183.5 3631h0.0" /><path d="M2959.5 3631h20" /><g>
<path d="M2979.5 3631h0.0" /><path d="M3163.5 3631h0.0" /><g>
<path d="M2979.5 3631h0.0" /><path d="M3073.5 3631h0.0" /><path d="M2979.5 3631h20" /><g>
<path d="M2999.5 3631h0.0" /><path d="M3053.5 3631h0.0" /><g class="terminal ">
<path d="M2999.5 3631h0.0" /><path d="M3053.5 3631h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2999.5" y="3620"></rect><text x="3026.5" y="3635">zero</text></g></g><path d="M3053.5 3631h20" /><path d="M2979.5 3631a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2999.5 3661h8.5" /><path d="M3045.0 3661h8.5" /><g class="terminal ">
<path d="M3008.0 3661h0.0" /><path d="M3045.0 3661h0.0" /><rect height="22" rx="10" ry="10" width="37" x="3008" y="3650"></rect><text x="3026.5" y="3665">oh</text></g></g><path d="M3053.5 3661a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M3073.5 3631h10" /><g class="non-terminal ">
<path d="M3083.5 3631h0.0" /><path d="M3163.5 3631h0.0" /><text class="comment" x="3123.5" y="3636">out.d=&quot;0&quot;;</text></g></g><path d="M3163.5 3631h20" /><path d="M2959.5 3631a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3691h19.25" /><path d="M3144.25 3691h19.25" /><g class="terminal ">
<path d="M2998.75 3691h0.0" /><path d="M3044.25 3691h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3680"></rect><text x="3021.5" y="3695">one</text></g><path d="M3044.25 3691h10" /><path d="M3054.25 3691h10" /><g class="non-terminal ">
<path d="M3064.25 3691h0.0" /><path d="M3144.25 3691h0.0" /><text class="comment" x="3104.25" y="3696">out.d=&quot;1&quot;;</text></g></g><path d="M3163.5 3691a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3721h19.25" /><path d="M3144.25 3721h19.25" /><g class="terminal ">
<path d="M2998.75 3721h0.0" /><path d="M3044.25 3721h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3710"></rect><text x="3021.5" y="3725">two</text></g><path d="M3044.25 3721h10" /><path d="M3054.25 3721h10" /><g class="non-terminal ">
<path d="M3064.25 3721h0.0" /><path d="M3144.25 3721h0.0" /><text class="comment" x="3104.25" y="3726">out.d=&quot;2&quot;;</text></g></g><path d="M3163.5 3721a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3751h10.75" /><path d="M3152.75 3751h10.75" /><g class="terminal ">
<path d="M2990.25 3751h0.0" /><path d="M3052.75 3751h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3740"></rect><text x="3021.5" y="3755">three</text></g><path d="M3052.75 3751h10" /><path d="M3062.75 3751h10" /><g class="non-terminal ">
<path d="M3072.75 3751h0.0" /><path d="M3152.75 3751h0.0" /><text class="comment" x="3112.75" y="3756">out.d=&quot;3&quot;;</text></g></g><path d="M3163.5 3751a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3781h15.0" /><path d="M3148.5 3781h15.0" /><g class="terminal ">
<path d="M2994.5 3781h0.0" /><path d="M3048.5 3781h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3770"></rect><text x="3021.5" y="3785">four</text></g><path d="M3048.5 3781h10" /><path d="M3058.5 3781h10" /><g class="non-terminal ">
<path d="M3068.5 3781h0.0" /><path d="M3148.5 3781h0.0" /><text class="comment" x="3108.5" y="3786">out.d=&quot;4&quot;;</text></g></g><path d="M3163.5 3781a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3811h15.0" /><path d="M3148.5 3811h15.0" /><g class="terminal ">
<path d="M2994.5 3811h0.0" /><path d="M3048.5 3811h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3800"></rect><text x="3021.5" y="3815">five</text></g><path d="M3048.5 3811h10" /><path d="M3058.5 3811h10" /><g class="non-terminal ">
<path d="M3068.5 3811h0.0" /><path d="M3148.5 3811h0.0" /><text class="comment" x="3108.5" y="3816">out.d=&quot;5&quot;;</text></g></g><path d="M3163.5 3811a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3841h19.25" /><path d="M3144.25 3841h19.25" /><g class="terminal ">
<path d="M2998.75 3841h0.0" /><path d="M3044.25 3841h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2998.75" y="3830"></rect><text x="3021.5" y="3845">six</text></g><path d="M3044.25 3841h10" /><path d="M3054.25 3841h10" /><g class="non-terminal ">
<path d="M3064.25 3841h0.0" /><path d="M3144.25 3841h0.0" /><text class="comment" x="3104.25" y="3846">out.d=&quot;6&quot;;</text></g></g><path d="M3163.5 3841a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3871h10.75" /><path d="M3152.75 3871h10.75" /><g class="terminal ">
<path d="M2990.25 3871h0.0" /><path d="M3052.75 3871h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3860"></rect><text x="3021.5" y="3875">seven</text></g><path d="M3052.75 3871h10" /><path d="M3062.75 3871h10" /><g class="non-terminal ">
<path d="M3072.75 3871h0.0" /><path d="M3152.75 3871h0.0" /><text class="comment" x="3112.75" y="3876">out.d=&quot;7&quot;;</text></g></g><path d="M3163.5 3871a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3901h10.75" /><path d="M3152.75 3901h10.75" /><g class="terminal ">
<path d="M2990.25 3901h0.0" /><path d="M3052.75 3901h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2990.25" y="3890"></rect><text x="3021.5" y="3905">eight</text></g><path d="M3052.75 3901h10" /><path d="M3062.75 3901h10" /><g class="non-terminal ">
<path d="M3072.75 3901h0.0" /><path d="M3152.75 3901h0.0" /><text class="comment" x="3112.75" y="3906">out.d=&quot;8&quot;;</text></g></g><path d="M3163.5 3901a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2959.5 3631a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2979.5 3931h15.0" /><path d="M3148.5 3931h15.0" /><g class="terminal ">
<path d="M2994.5 3931h0.0" /><path d="M3048.5 3931h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2994.5" y="3920"></rect><text x="3021.5" y="3935">nine</text></g><path d="M3048.5 3931h10" /><path d="M3058.5 3931h10" /><g class="non-terminal ">
<path d="M3068.5 3931h0.0" /><path d="M3148.5 3931h0.0" /><text class="comment" x="3108.5" y="3936">out.d=&quot;9&quot;;</text></g></g><path d="M3163.5 3931a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M3183.5 3631h10" /><path d="M3193.5 3631h10" /><g class="terminal ">
<path d="M3203.5 3631h0.0" /><path d="M3529.5 3631h0.0" /><rect height="22" rx="10" ry="10" width="326" x="3203.5" y="3620"></rect><text x="3366.5" y="3635">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M3529.5 3631h10" /><path d="M3539.5 3631h10" /><g class="terminal ">
<path d="M3549.5 3631h0.0" /><path d="M3816.0 3631h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="3549.5" y="3620"></rect><text x="3682.75" y="3635">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M3816.0 3631a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M3836.0 3361h10" /><path d="M3846.0 3361h10" /><g class="terminal ">
<path d="M3856.0 3361h0.0" /><path d="M4139.5 3361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3856" y="3350"></rect><text x="3997.75" y="3365">!!out.d4=rules.doubleDigit.dd1;</text></g><path d="M4139.5 3361h10" /><path d="M4149.5 3361h10" /><g class="terminal ">
<path d="M4159.5 3361h0.0" /><path d="M4443.0 3361h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="4159.5" y="3350"></rect><text x="4301.25" y="3365">out.d5=rules.doubleDigit.dd2;!!</text></g></g><path d="M4443.0 3361a10 10 0 0 0 10 -10v-3310a10 10 0 0 1 10 -10" /><path d="M342.0 31a10 10 0 0 1 10 10v3910a10 10 0 0 0 10 10" /><g>
<path d="M362.0 3961h0.0" /><path d="M4443.0 3961h0.0" /><g>
<path d="M362.0 3961h0.0" /><path d="M1554.0 3961h0.0" /><g>
<path d="M362.0 3961h0.0" /><path d="M1554.0 3961h0.0" /><path d="M362.0 3961h20" /><g>
<path d="M382.0 3961h87.75" /><path d="M1446.25 3961h87.75" /><g>
<path d="M469.75 3961h0.0" /><path d="M924.25 3961h0.0" /><g>
<path d="M469.75 3961h0.0" /><path d="M924.25 3961h0.0" /><path d="M469.75 3961h20" /><g>
<path d="M489.75 3961h12.75" /><path d="M891.5 3961h12.75" /><g class="terminal ">
<path d="M502.5 3961h0.0" /><path d="M573.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="71" x="502.5" y="3950"></rect><text x="538" y="3965">eleven</text></g><path d="M573.5 3961h10" /><path d="M583.5 3961h10" /><g class="terminal ">
<path d="M593.5 3961h0.0" /><path d="M732.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="593.5" y="3950"></rect><text x="663" y="3965">!!out.dd1=&quot;1&quot;;</text></g><path d="M732.5 3961h10" /><path d="M742.5 3961h10" /><g class="terminal ">
<path d="M752.5 3961h0.0" /><path d="M891.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="752.5" y="3950"></rect><text x="822" y="3965">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M904.25 3961h20" /><path d="M469.75 3961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M489.75 3991h12.75" /><path d="M891.5 3991h12.75" /><g class="terminal ">
<path d="M502.5 3991h0.0" /><path d="M573.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="71" x="502.5" y="3980"></rect><text x="538" y="3995">twelve</text></g><path d="M573.5 3991h10" /><path d="M583.5 3991h10" /><g class="terminal ">
<path d="M593.5 3991h0.0" /><path d="M732.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="593.5" y="3980"></rect><text x="663" y="3995">!!out.dd1=&quot;1&quot;;</text></g><path d="M732.5 3991h10" /><path d="M742.5 3991h10" /><g class="terminal ">
<path d="M752.5 3991h0.0" /><path d="M891.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="752.5" y="3980"></rect><text x="822" y="3995">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M904.25 3991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4021h4.25" /><path d="M900.0 4021h4.25" /><g class="terminal ">
<path d="M494.0 4021h0.0" /><path d="M582.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="4010"></rect><text x="538" y="4025">thirteen</text></g><path d="M582.0 4021h10" /><path d="M592.0 4021h10" /><g class="terminal ">
<path d="M602.0 4021h0.0" /><path d="M741.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="4010"></rect><text x="671.5" y="4025">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 4021h10" /><path d="M751.0 4021h10" /><g class="terminal ">
<path d="M761.0 4021h0.0" /><path d="M900.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="4010"></rect><text x="830.5" y="4025">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M904.25 4021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4051h4.25" /><path d="M900.0 4051h4.25" /><g class="terminal ">
<path d="M494.0 4051h0.0" /><path d="M582.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="4040"></rect><text x="538" y="4055">fourteen</text></g><path d="M582.0 4051h10" /><path d="M592.0 4051h10" /><g class="terminal ">
<path d="M602.0 4051h0.0" /><path d="M741.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="4040"></rect><text x="671.5" y="4055">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 4051h10" /><path d="M751.0 4051h10" /><g class="terminal ">
<path d="M761.0 4051h0.0" /><path d="M900.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="4040"></rect><text x="830.5" y="4055">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M904.25 4051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4081h8.5" /><path d="M895.75 4081h8.5" /><g class="terminal ">
<path d="M498.25 4081h0.0" /><path d="M577.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="498.25" y="4070"></rect><text x="538" y="4085">fifteen</text></g><path d="M577.75 4081h10" /><path d="M587.75 4081h10" /><g class="terminal ">
<path d="M597.75 4081h0.0" /><path d="M736.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="597.75" y="4070"></rect><text x="667.25" y="4085">!!out.dd1=&quot;1&quot;;</text></g><path d="M736.75 4081h10" /><path d="M746.75 4081h10" /><g class="terminal ">
<path d="M756.75 4081h0.0" /><path d="M895.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="756.75" y="4070"></rect><text x="826.25" y="4085">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M904.25 4081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4111h8.5" /><path d="M895.75 4111h8.5" /><g class="terminal ">
<path d="M498.25 4111h0.0" /><path d="M577.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="498.25" y="4100"></rect><text x="538" y="4115">sixteen</text></g><path d="M577.75 4111h10" /><path d="M587.75 4111h10" /><g class="terminal ">
<path d="M597.75 4111h0.0" /><path d="M736.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="597.75" y="4100"></rect><text x="667.25" y="4115">!!out.dd1=&quot;1&quot;;</text></g><path d="M736.75 4111h10" /><path d="M746.75 4111h10" /><g class="terminal ">
<path d="M756.75 4111h0.0" /><path d="M895.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="756.75" y="4100"></rect><text x="826.25" y="4115">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M904.25 4111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4141h0.0" /><path d="M904.25 4141h0.0" /><g class="terminal ">
<path d="M489.75 4141h0.0" /><path d="M586.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="489.75" y="4130"></rect><text x="538" y="4145">seventeen</text></g><path d="M586.25 4141h10" /><path d="M596.25 4141h10" /><g class="terminal ">
<path d="M606.25 4141h0.0" /><path d="M745.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="606.25" y="4130"></rect><text x="675.75" y="4145">!!out.dd1=&quot;1&quot;;</text></g><path d="M745.25 4141h10" /><path d="M755.25 4141h10" /><g class="terminal ">
<path d="M765.25 4141h0.0" /><path d="M904.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="765.25" y="4130"></rect><text x="834.75" y="4145">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M904.25 4141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4171h4.25" /><path d="M900.0 4171h4.25" /><g class="terminal ">
<path d="M494.0 4171h0.0" /><path d="M582.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="4160"></rect><text x="538" y="4175">eighteen</text></g><path d="M582.0 4171h10" /><path d="M592.0 4171h10" /><g class="terminal ">
<path d="M602.0 4171h0.0" /><path d="M741.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="4160"></rect><text x="671.5" y="4175">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 4171h10" /><path d="M751.0 4171h10" /><g class="terminal ">
<path d="M761.0 4171h0.0" /><path d="M900.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="4160"></rect><text x="830.5" y="4175">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M904.25 4171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M469.75 3961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M489.75 4201h4.25" /><path d="M900.0 4201h4.25" /><g class="terminal ">
<path d="M494.0 4201h0.0" /><path d="M582.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="88" x="494" y="4190"></rect><text x="538" y="4205">nineteen</text></g><path d="M582.0 4201h10" /><path d="M592.0 4201h10" /><g class="terminal ">
<path d="M602.0 4201h0.0" /><path d="M741.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="602" y="4190"></rect><text x="671.5" y="4205">!!out.dd1=&quot;1&quot;;</text></g><path d="M741.0 4201h10" /><path d="M751.0 4201h10" /><g class="terminal ">
<path d="M761.0 4201h0.0" /><path d="M900.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="761" y="4190"></rect><text x="830.5" y="4205">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M904.25 4201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M924.25 3961h10" /><path d="M934.25 3961h10" /><g class="terminal ">
<path d="M944.25 3961h0.0" /><path d="M1185.25 3961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="944.25" y="3950"></rect><text x="1064.75" y="3965">!!out.dd1=rules.teens.dd1;</text></g><path d="M1185.25 3961h10" /><path d="M1195.25 3961h10" /><g class="terminal ">
<path d="M1205.25 3961h0.0" /><path d="M1446.25 3961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="1205.25" y="3950"></rect><text x="1325.75" y="3965">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M1534.0 3961h20" /><path d="M362.0 3961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M382.0 4231h0.0" /><path d="M1534.0 4231h0.0" /><g>
<path d="M382.0 4231h0.0" /><path d="M657.5 4231h0.0" /><g>
<path d="M382.0 4231h0.0" /><path d="M657.5 4231h0.0" /><path d="M382.0 4231h20" /><g>
<path d="M402.0 4231h4.25" /><path d="M633.25 4231h4.25" /><g class="terminal ">
<path d="M406.25 4231h0.0" /><path d="M477.25 4231h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="4220"></rect><text x="441.75" y="4235">twenty</text></g><path d="M477.25 4231h10" /><path d="M487.25 4231h10" /><g class="non-terminal ">
<path d="M497.25 4231h0.0" /><path d="M633.25 4231h0.0" /><text class="comment" x="565.25" y="4236">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M637.5 4231h20" /><path d="M382.0 4231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4261h4.25" /><path d="M633.25 4261h4.25" /><g class="terminal ">
<path d="M406.25 4261h0.0" /><path d="M477.25 4261h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="4250"></rect><text x="441.75" y="4265">thirty</text></g><path d="M477.25 4261h10" /><path d="M487.25 4261h10" /><g class="non-terminal ">
<path d="M497.25 4261h0.0" /><path d="M633.25 4261h0.0" /><text class="comment" x="565.25" y="4266">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M637.5 4261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4291h8.5" /><path d="M629.0 4291h8.5" /><g class="terminal ">
<path d="M410.5 4291h0.0" /><path d="M473.0 4291h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="4280"></rect><text x="441.75" y="4295">forty</text></g><path d="M473.0 4291h10" /><path d="M483.0 4291h10" /><g class="non-terminal ">
<path d="M493.0 4291h0.0" /><path d="M629.0 4291h0.0" /><text class="comment" x="561" y="4296">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M637.5 4291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4321h8.5" /><path d="M629.0 4321h8.5" /><g class="terminal ">
<path d="M410.5 4321h0.0" /><path d="M473.0 4321h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="4310"></rect><text x="441.75" y="4325">fifty</text></g><path d="M473.0 4321h10" /><path d="M483.0 4321h10" /><g class="non-terminal ">
<path d="M493.0 4321h0.0" /><path d="M629.0 4321h0.0" /><text class="comment" x="561" y="4326">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M637.5 4321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4351h8.5" /><path d="M629.0 4351h8.5" /><g class="terminal ">
<path d="M410.5 4351h0.0" /><path d="M473.0 4351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="410.5" y="4340"></rect><text x="441.75" y="4355">sixty</text></g><path d="M473.0 4351h10" /><path d="M483.0 4351h10" /><g class="non-terminal ">
<path d="M493.0 4351h0.0" /><path d="M629.0 4351h0.0" /><text class="comment" x="561" y="4356">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M637.5 4351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4381h0.0" /><path d="M637.5 4381h0.0" /><g class="terminal ">
<path d="M402.0 4381h0.0" /><path d="M481.5 4381h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="402" y="4370"></rect><text x="441.75" y="4385">seventy</text></g><path d="M481.5 4381h10" /><path d="M491.5 4381h10" /><g class="non-terminal ">
<path d="M501.5 4381h0.0" /><path d="M637.5 4381h0.0" /><text class="comment" x="569.5" y="4386">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M637.5 4381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4411h4.25" /><path d="M633.25 4411h4.25" /><g class="terminal ">
<path d="M406.25 4411h0.0" /><path d="M477.25 4411h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="4400"></rect><text x="441.75" y="4415">eighty</text></g><path d="M477.25 4411h10" /><path d="M487.25 4411h10" /><g class="non-terminal ">
<path d="M497.25 4411h0.0" /><path d="M633.25 4411h0.0" /><text class="comment" x="565.25" y="4416">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M637.5 4411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M382.0 4231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M402.0 4441h4.25" /><path d="M633.25 4441h4.25" /><g class="terminal ">
<path d="M406.25 4441h0.0" /><path d="M477.25 4441h0.0" /><rect height="22" rx="10" ry="10" width="71" x="406.25" y="4430"></rect><text x="441.75" y="4445">ninety</text></g><path d="M477.25 4441h10" /><path d="M487.25 4441h10" /><g class="non-terminal ">
<path d="M497.25 4441h0.0" /><path d="M633.25 4441h0.0" /><text class="comment" x="565.25" y="4446">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M637.5 4441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M657.5 4231h10" /><path d="M667.5 4231h10" /><g>
<path d="M677.5 4231h0.0" /><path d="M901.5 4231h0.0" /><g>
<path d="M677.5 4231h0.0" /><path d="M901.5 4231h0.0" /><path d="M677.5 4231h20" /><g>
<path d="M697.5 4231h0.0" /><path d="M881.5 4231h0.0" /><g>
<path d="M697.5 4231h0.0" /><path d="M791.5 4231h0.0" /><path d="M697.5 4231h20" /><g>
<path d="M717.5 4231h0.0" /><path d="M771.5 4231h0.0" /><g class="terminal ">
<path d="M717.5 4231h0.0" /><path d="M771.5 4231h0.0" /><rect height="22" rx="10" ry="10" width="54" x="717.5" y="4220"></rect><text x="744.5" y="4235">zero</text></g></g><path d="M771.5 4231h20" /><path d="M697.5 4231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M717.5 4261h8.5" /><path d="M763.0 4261h8.5" /><g class="terminal ">
<path d="M726.0 4261h0.0" /><path d="M763.0 4261h0.0" /><rect height="22" rx="10" ry="10" width="37" x="726" y="4250"></rect><text x="744.5" y="4265">oh</text></g></g><path d="M771.5 4261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M791.5 4231h10" /><g class="non-terminal ">
<path d="M801.5 4231h0.0" /><path d="M881.5 4231h0.0" /><text class="comment" x="841.5" y="4236">out.d=&quot;0&quot;;</text></g></g><path d="M881.5 4231h20" /><path d="M677.5 4231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4291h19.25" /><path d="M862.25 4291h19.25" /><g class="terminal ">
<path d="M716.75 4291h0.0" /><path d="M762.25 4291h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="4280"></rect><text x="739.5" y="4295">one</text></g><path d="M762.25 4291h10" /><path d="M772.25 4291h10" /><g class="non-terminal ">
<path d="M782.25 4291h0.0" /><path d="M862.25 4291h0.0" /><text class="comment" x="822.25" y="4296">out.d=&quot;1&quot;;</text></g></g><path d="M881.5 4291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4321h19.25" /><path d="M862.25 4321h19.25" /><g class="terminal ">
<path d="M716.75 4321h0.0" /><path d="M762.25 4321h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="4310"></rect><text x="739.5" y="4325">two</text></g><path d="M762.25 4321h10" /><path d="M772.25 4321h10" /><g class="non-terminal ">
<path d="M782.25 4321h0.0" /><path d="M862.25 4321h0.0" /><text class="comment" x="822.25" y="4326">out.d=&quot;2&quot;;</text></g></g><path d="M881.5 4321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4351h10.75" /><path d="M870.75 4351h10.75" /><g class="terminal ">
<path d="M708.25 4351h0.0" /><path d="M770.75 4351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="4340"></rect><text x="739.5" y="4355">three</text></g><path d="M770.75 4351h10" /><path d="M780.75 4351h10" /><g class="non-terminal ">
<path d="M790.75 4351h0.0" /><path d="M870.75 4351h0.0" /><text class="comment" x="830.75" y="4356">out.d=&quot;3&quot;;</text></g></g><path d="M881.5 4351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4381h15.0" /><path d="M866.5 4381h15.0" /><g class="terminal ">
<path d="M712.5 4381h0.0" /><path d="M766.5 4381h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="4370"></rect><text x="739.5" y="4385">four</text></g><path d="M766.5 4381h10" /><path d="M776.5 4381h10" /><g class="non-terminal ">
<path d="M786.5 4381h0.0" /><path d="M866.5 4381h0.0" /><text class="comment" x="826.5" y="4386">out.d=&quot;4&quot;;</text></g></g><path d="M881.5 4381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4411h15.0" /><path d="M866.5 4411h15.0" /><g class="terminal ">
<path d="M712.5 4411h0.0" /><path d="M766.5 4411h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="4400"></rect><text x="739.5" y="4415">five</text></g><path d="M766.5 4411h10" /><path d="M776.5 4411h10" /><g class="non-terminal ">
<path d="M786.5 4411h0.0" /><path d="M866.5 4411h0.0" /><text class="comment" x="826.5" y="4416">out.d=&quot;5&quot;;</text></g></g><path d="M881.5 4411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4441h19.25" /><path d="M862.25 4441h19.25" /><g class="terminal ">
<path d="M716.75 4441h0.0" /><path d="M762.25 4441h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="716.75" y="4430"></rect><text x="739.5" y="4445">six</text></g><path d="M762.25 4441h10" /><path d="M772.25 4441h10" /><g class="non-terminal ">
<path d="M782.25 4441h0.0" /><path d="M862.25 4441h0.0" /><text class="comment" x="822.25" y="4446">out.d=&quot;6&quot;;</text></g></g><path d="M881.5 4441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4471h10.75" /><path d="M870.75 4471h10.75" /><g class="terminal ">
<path d="M708.25 4471h0.0" /><path d="M770.75 4471h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="4460"></rect><text x="739.5" y="4475">seven</text></g><path d="M770.75 4471h10" /><path d="M780.75 4471h10" /><g class="non-terminal ">
<path d="M790.75 4471h0.0" /><path d="M870.75 4471h0.0" /><text class="comment" x="830.75" y="4476">out.d=&quot;7&quot;;</text></g></g><path d="M881.5 4471a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4501h10.75" /><path d="M870.75 4501h10.75" /><g class="terminal ">
<path d="M708.25 4501h0.0" /><path d="M770.75 4501h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="708.25" y="4490"></rect><text x="739.5" y="4505">eight</text></g><path d="M770.75 4501h10" /><path d="M780.75 4501h10" /><g class="non-terminal ">
<path d="M790.75 4501h0.0" /><path d="M870.75 4501h0.0" /><text class="comment" x="830.75" y="4506">out.d=&quot;8&quot;;</text></g></g><path d="M881.5 4501a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M677.5 4231a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M697.5 4531h15.0" /><path d="M866.5 4531h15.0" /><g class="terminal ">
<path d="M712.5 4531h0.0" /><path d="M766.5 4531h0.0" /><rect height="22" rx="10" ry="10" width="54" x="712.5" y="4520"></rect><text x="739.5" y="4535">nine</text></g><path d="M766.5 4531h10" /><path d="M776.5 4531h10" /><g class="non-terminal ">
<path d="M786.5 4531h0.0" /><path d="M866.5 4531h0.0" /><text class="comment" x="826.5" y="4536">out.d=&quot;9&quot;;</text></g></g><path d="M881.5 4531a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M901.5 4231h10" /><path d="M911.5 4231h10" /><g class="terminal ">
<path d="M921.5 4231h0.0" /><path d="M1247.5 4231h0.0" /><rect height="22" rx="10" ry="10" width="326" x="921.5" y="4220"></rect><text x="1084.5" y="4235">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M1247.5 4231h10" /><path d="M1257.5 4231h10" /><g class="terminal ">
<path d="M1267.5 4231h0.0" /><path d="M1534.0 4231h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="1267.5" y="4220"></rect><text x="1400.75" y="4235">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M1534.0 4231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M1554.0 3961h10" /><path d="M1564.0 3961h10" /><g class="terminal ">
<path d="M1574.0 3961h0.0" /><path d="M1857.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="1574" y="3950"></rect><text x="1715.75" y="3965">!!out.d1=rules.doubleDigit.dd1;</text></g><path d="M1857.5 3961h10" /><path d="M1867.5 3961h10" /><g class="terminal ">
<path d="M1877.5 3961h0.0" /><path d="M2161.0 3961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="1877.5" y="3950"></rect><text x="2019.25" y="3965">out.d2=rules.doubleDigit.dd2;!!</text></g><path d="M2161.0 3961h10" /><path d="M2171.0 3961h10" /><g>
<path d="M2181.0 3961h0.0" /><path d="M3373.0 3961h0.0" /><g>
<path d="M2181.0 3961h0.0" /><path d="M3373.0 3961h0.0" /><path d="M2181.0 3961h20" /><g>
<path d="M2201.0 3961h87.75" /><path d="M3265.25 3961h87.75" /><g>
<path d="M2288.75 3961h0.0" /><path d="M2743.25 3961h0.0" /><g>
<path d="M2288.75 3961h0.0" /><path d="M2743.25 3961h0.0" /><path d="M2288.75 3961h20" /><g>
<path d="M2308.75 3961h12.75" /><path d="M2710.5 3961h12.75" /><g class="terminal ">
<path d="M2321.5 3961h0.0" /><path d="M2392.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2321.5" y="3950"></rect><text x="2357" y="3965">eleven</text></g><path d="M2392.5 3961h10" /><path d="M2402.5 3961h10" /><g class="terminal ">
<path d="M2412.5 3961h0.0" /><path d="M2551.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2412.5" y="3950"></rect><text x="2482" y="3965">!!out.dd1=&quot;1&quot;;</text></g><path d="M2551.5 3961h10" /><path d="M2561.5 3961h10" /><g class="terminal ">
<path d="M2571.5 3961h0.0" /><path d="M2710.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2571.5" y="3950"></rect><text x="2641" y="3965">out.dd2=&quot;1&quot;;!!</text></g></g><path d="M2723.25 3961h20" /><path d="M2288.75 3961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 3991h12.75" /><path d="M2710.5 3991h12.75" /><g class="terminal ">
<path d="M2321.5 3991h0.0" /><path d="M2392.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2321.5" y="3980"></rect><text x="2357" y="3995">twelve</text></g><path d="M2392.5 3991h10" /><path d="M2402.5 3991h10" /><g class="terminal ">
<path d="M2412.5 3991h0.0" /><path d="M2551.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2412.5" y="3980"></rect><text x="2482" y="3995">!!out.dd1=&quot;1&quot;;</text></g><path d="M2551.5 3991h10" /><path d="M2561.5 3991h10" /><g class="terminal ">
<path d="M2571.5 3991h0.0" /><path d="M2710.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2571.5" y="3980"></rect><text x="2641" y="3995">out.dd2=&quot;2&quot;;!!</text></g></g><path d="M2723.25 3991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4021h4.25" /><path d="M2719.0 4021h4.25" /><g class="terminal ">
<path d="M2313.0 4021h0.0" /><path d="M2401.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2313" y="4010"></rect><text x="2357" y="4025">thirteen</text></g><path d="M2401.0 4021h10" /><path d="M2411.0 4021h10" /><g class="terminal ">
<path d="M2421.0 4021h0.0" /><path d="M2560.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2421" y="4010"></rect><text x="2490.5" y="4025">!!out.dd1=&quot;1&quot;;</text></g><path d="M2560.0 4021h10" /><path d="M2570.0 4021h10" /><g class="terminal ">
<path d="M2580.0 4021h0.0" /><path d="M2719.0 4021h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2580" y="4010"></rect><text x="2649.5" y="4025">out.dd2=&quot;3&quot;;!!</text></g></g><path d="M2723.25 4021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4051h4.25" /><path d="M2719.0 4051h4.25" /><g class="terminal ">
<path d="M2313.0 4051h0.0" /><path d="M2401.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2313" y="4040"></rect><text x="2357" y="4055">fourteen</text></g><path d="M2401.0 4051h10" /><path d="M2411.0 4051h10" /><g class="terminal ">
<path d="M2421.0 4051h0.0" /><path d="M2560.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2421" y="4040"></rect><text x="2490.5" y="4055">!!out.dd1=&quot;1&quot;;</text></g><path d="M2560.0 4051h10" /><path d="M2570.0 4051h10" /><g class="terminal ">
<path d="M2580.0 4051h0.0" /><path d="M2719.0 4051h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2580" y="4040"></rect><text x="2649.5" y="4055">out.dd2=&quot;4&quot;;!!</text></g></g><path d="M2723.25 4051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4081h8.5" /><path d="M2714.75 4081h8.5" /><g class="terminal ">
<path d="M2317.25 4081h0.0" /><path d="M2396.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2317.25" y="4070"></rect><text x="2357" y="4085">fifteen</text></g><path d="M2396.75 4081h10" /><path d="M2406.75 4081h10" /><g class="terminal ">
<path d="M2416.75 4081h0.0" /><path d="M2555.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2416.75" y="4070"></rect><text x="2486.25" y="4085">!!out.dd1=&quot;1&quot;;</text></g><path d="M2555.75 4081h10" /><path d="M2565.75 4081h10" /><g class="terminal ">
<path d="M2575.75 4081h0.0" /><path d="M2714.75 4081h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2575.75" y="4070"></rect><text x="2645.25" y="4085">out.dd2=&quot;5&quot;;!!</text></g></g><path d="M2723.25 4081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4111h8.5" /><path d="M2714.75 4111h8.5" /><g class="terminal ">
<path d="M2317.25 4111h0.0" /><path d="M2396.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2317.25" y="4100"></rect><text x="2357" y="4115">sixteen</text></g><path d="M2396.75 4111h10" /><path d="M2406.75 4111h10" /><g class="terminal ">
<path d="M2416.75 4111h0.0" /><path d="M2555.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2416.75" y="4100"></rect><text x="2486.25" y="4115">!!out.dd1=&quot;1&quot;;</text></g><path d="M2555.75 4111h10" /><path d="M2565.75 4111h10" /><g class="terminal ">
<path d="M2575.75 4111h0.0" /><path d="M2714.75 4111h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2575.75" y="4100"></rect><text x="2645.25" y="4115">out.dd2=&quot;6&quot;;!!</text></g></g><path d="M2723.25 4111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4141h0.0" /><path d="M2723.25 4141h0.0" /><g class="terminal ">
<path d="M2308.75 4141h0.0" /><path d="M2405.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="96.5" x="2308.75" y="4130"></rect><text x="2357" y="4145">seventeen</text></g><path d="M2405.25 4141h10" /><path d="M2415.25 4141h10" /><g class="terminal ">
<path d="M2425.25 4141h0.0" /><path d="M2564.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2425.25" y="4130"></rect><text x="2494.75" y="4145">!!out.dd1=&quot;1&quot;;</text></g><path d="M2564.25 4141h10" /><path d="M2574.25 4141h10" /><g class="terminal ">
<path d="M2584.25 4141h0.0" /><path d="M2723.25 4141h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2584.25" y="4130"></rect><text x="2653.75" y="4145">out.dd2=&quot;7&quot;;!!</text></g></g><path d="M2723.25 4141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4171h4.25" /><path d="M2719.0 4171h4.25" /><g class="terminal ">
<path d="M2313.0 4171h0.0" /><path d="M2401.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2313" y="4160"></rect><text x="2357" y="4175">eighteen</text></g><path d="M2401.0 4171h10" /><path d="M2411.0 4171h10" /><g class="terminal ">
<path d="M2421.0 4171h0.0" /><path d="M2560.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2421" y="4160"></rect><text x="2490.5" y="4175">!!out.dd1=&quot;1&quot;;</text></g><path d="M2560.0 4171h10" /><path d="M2570.0 4171h10" /><g class="terminal ">
<path d="M2580.0 4171h0.0" /><path d="M2719.0 4171h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2580" y="4160"></rect><text x="2649.5" y="4175">out.dd2=&quot;8&quot;;!!</text></g></g><path d="M2723.25 4171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2288.75 3961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2308.75 4201h4.25" /><path d="M2719.0 4201h4.25" /><g class="terminal ">
<path d="M2313.0 4201h0.0" /><path d="M2401.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2313" y="4190"></rect><text x="2357" y="4205">nineteen</text></g><path d="M2401.0 4201h10" /><path d="M2411.0 4201h10" /><g class="terminal ">
<path d="M2421.0 4201h0.0" /><path d="M2560.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2421" y="4190"></rect><text x="2490.5" y="4205">!!out.dd1=&quot;1&quot;;</text></g><path d="M2560.0 4201h10" /><path d="M2570.0 4201h10" /><g class="terminal ">
<path d="M2580.0 4201h0.0" /><path d="M2719.0 4201h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2580" y="4190"></rect><text x="2649.5" y="4205">out.dd2=&quot;9&quot;;!!</text></g></g><path d="M2723.25 4201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M2743.25 3961h10" /><path d="M2753.25 3961h10" /><g class="terminal ">
<path d="M2763.25 3961h0.0" /><path d="M3004.25 3961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="2763.25" y="3950"></rect><text x="2883.75" y="3965">!!out.dd1=rules.teens.dd1;</text></g><path d="M3004.25 3961h10" /><path d="M3014.25 3961h10" /><g class="terminal ">
<path d="M3024.25 3961h0.0" /><path d="M3265.25 3961h0.0" /><rect height="22" rx="10" ry="10" width="241" x="3024.25" y="3950"></rect><text x="3144.75" y="3965">out.dd2=rules.teens.dd2;!!</text></g></g><path d="M3353.0 3961h20" /><path d="M2181.0 3961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2201.0 4231h0.0" /><path d="M3353.0 4231h0.0" /><g>
<path d="M2201.0 4231h0.0" /><path d="M2476.5 4231h0.0" /><g>
<path d="M2201.0 4231h0.0" /><path d="M2476.5 4231h0.0" /><path d="M2201.0 4231h20" /><g>
<path d="M2221.0 4231h4.25" /><path d="M2452.25 4231h4.25" /><g class="terminal ">
<path d="M2225.25 4231h0.0" /><path d="M2296.25 4231h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2225.25" y="4220"></rect><text x="2260.75" y="4235">twenty</text></g><path d="M2296.25 4231h10" /><path d="M2306.25 4231h10" /><g class="non-terminal ">
<path d="M2316.25 4231h0.0" /><path d="M2452.25 4231h0.0" /><text class="comment" x="2384.25" y="4236">out.tensPlace=&quot;2&quot;;</text></g></g><path d="M2456.5 4231h20" /><path d="M2201.0 4231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4261h4.25" /><path d="M2452.25 4261h4.25" /><g class="terminal ">
<path d="M2225.25 4261h0.0" /><path d="M2296.25 4261h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2225.25" y="4250"></rect><text x="2260.75" y="4265">thirty</text></g><path d="M2296.25 4261h10" /><path d="M2306.25 4261h10" /><g class="non-terminal ">
<path d="M2316.25 4261h0.0" /><path d="M2452.25 4261h0.0" /><text class="comment" x="2384.25" y="4266">out.tensPlace=&quot;3&quot;;</text></g></g><path d="M2456.5 4261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4291h8.5" /><path d="M2448.0 4291h8.5" /><g class="terminal ">
<path d="M2229.5 4291h0.0" /><path d="M2292.0 4291h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2229.5" y="4280"></rect><text x="2260.75" y="4295">forty</text></g><path d="M2292.0 4291h10" /><path d="M2302.0 4291h10" /><g class="non-terminal ">
<path d="M2312.0 4291h0.0" /><path d="M2448.0 4291h0.0" /><text class="comment" x="2380" y="4296">out.tensPlace=&quot;4&quot;;</text></g></g><path d="M2456.5 4291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4321h8.5" /><path d="M2448.0 4321h8.5" /><g class="terminal ">
<path d="M2229.5 4321h0.0" /><path d="M2292.0 4321h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2229.5" y="4310"></rect><text x="2260.75" y="4325">fifty</text></g><path d="M2292.0 4321h10" /><path d="M2302.0 4321h10" /><g class="non-terminal ">
<path d="M2312.0 4321h0.0" /><path d="M2448.0 4321h0.0" /><text class="comment" x="2380" y="4326">out.tensPlace=&quot;5&quot;;</text></g></g><path d="M2456.5 4321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4351h8.5" /><path d="M2448.0 4351h8.5" /><g class="terminal ">
<path d="M2229.5 4351h0.0" /><path d="M2292.0 4351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2229.5" y="4340"></rect><text x="2260.75" y="4355">sixty</text></g><path d="M2292.0 4351h10" /><path d="M2302.0 4351h10" /><g class="non-terminal ">
<path d="M2312.0 4351h0.0" /><path d="M2448.0 4351h0.0" /><text class="comment" x="2380" y="4356">out.tensPlace=&quot;6&quot;;</text></g></g><path d="M2456.5 4351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4381h0.0" /><path d="M2456.5 4381h0.0" /><g class="terminal ">
<path d="M2221.0 4381h0.0" /><path d="M2300.5 4381h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2221" y="4370"></rect><text x="2260.75" y="4385">seventy</text></g><path d="M2300.5 4381h10" /><path d="M2310.5 4381h10" /><g class="non-terminal ">
<path d="M2320.5 4381h0.0" /><path d="M2456.5 4381h0.0" /><text class="comment" x="2388.5" y="4386">out.tensPlace=&quot;7&quot;;</text></g></g><path d="M2456.5 4381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4411h4.25" /><path d="M2452.25 4411h4.25" /><g class="terminal ">
<path d="M2225.25 4411h0.0" /><path d="M2296.25 4411h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2225.25" y="4400"></rect><text x="2260.75" y="4415">eighty</text></g><path d="M2296.25 4411h10" /><path d="M2306.25 4411h10" /><g class="non-terminal ">
<path d="M2316.25 4411h0.0" /><path d="M2452.25 4411h0.0" /><text class="comment" x="2384.25" y="4416">out.tensPlace=&quot;8&quot;;</text></g></g><path d="M2456.5 4411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2201.0 4231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2221.0 4441h4.25" /><path d="M2452.25 4441h4.25" /><g class="terminal ">
<path d="M2225.25 4441h0.0" /><path d="M2296.25 4441h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2225.25" y="4430"></rect><text x="2260.75" y="4445">ninety</text></g><path d="M2296.25 4441h10" /><path d="M2306.25 4441h10" /><g class="non-terminal ">
<path d="M2316.25 4441h0.0" /><path d="M2452.25 4441h0.0" /><text class="comment" x="2384.25" y="4446">out.tensPlace=&quot;9&quot;;</text></g></g><path d="M2456.5 4441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /></g></g><path d="M2476.5 4231h10" /><path d="M2486.5 4231h10" /><g>
<path d="M2496.5 4231h0.0" /><path d="M2720.5 4231h0.0" /><g>
<path d="M2496.5 4231h0.0" /><path d="M2720.5 4231h0.0" /><path d="M2496.5 4231h20" /><g>
<path d="M2516.5 4231h0.0" /><path d="M2700.5 4231h0.0" /><g>
<path d="M2516.5 4231h0.0" /><path d="M2610.5 4231h0.0" /><path d="M2516.5 4231h20" /><g>
<path d="M2536.5 4231h0.0" /><path d="M2590.5 4231h0.0" /><g class="terminal ">
<path d="M2536.5 4231h0.0" /><path d="M2590.5 4231h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2536.5" y="4220"></rect><text x="2563.5" y="4235">zero</text></g></g><path d="M2590.5 4231h20" /><path d="M2516.5 4231a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2536.5 4261h8.5" /><path d="M2582.0 4261h8.5" /><g class="terminal ">
<path d="M2545.0 4261h0.0" /><path d="M2582.0 4261h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2545" y="4250"></rect><text x="2563.5" y="4265">oh</text></g></g><path d="M2590.5 4261a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2610.5 4231h10" /><g class="non-terminal ">
<path d="M2620.5 4231h0.0" /><path d="M2700.5 4231h0.0" /><text class="comment" x="2660.5" y="4236">out.d=&quot;0&quot;;</text></g></g><path d="M2700.5 4231h20" /><path d="M2496.5 4231a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4291h19.25" /><path d="M2681.25 4291h19.25" /><g class="terminal ">
<path d="M2535.75 4291h0.0" /><path d="M2581.25 4291h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2535.75" y="4280"></rect><text x="2558.5" y="4295">one</text></g><path d="M2581.25 4291h10" /><path d="M2591.25 4291h10" /><g class="non-terminal ">
<path d="M2601.25 4291h0.0" /><path d="M2681.25 4291h0.0" /><text class="comment" x="2641.25" y="4296">out.d=&quot;1&quot;;</text></g></g><path d="M2700.5 4291a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4321h19.25" /><path d="M2681.25 4321h19.25" /><g class="terminal ">
<path d="M2535.75 4321h0.0" /><path d="M2581.25 4321h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2535.75" y="4310"></rect><text x="2558.5" y="4325">two</text></g><path d="M2581.25 4321h10" /><path d="M2591.25 4321h10" /><g class="non-terminal ">
<path d="M2601.25 4321h0.0" /><path d="M2681.25 4321h0.0" /><text class="comment" x="2641.25" y="4326">out.d=&quot;2&quot;;</text></g></g><path d="M2700.5 4321a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4351h10.75" /><path d="M2689.75 4351h10.75" /><g class="terminal ">
<path d="M2527.25 4351h0.0" /><path d="M2589.75 4351h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2527.25" y="4340"></rect><text x="2558.5" y="4355">three</text></g><path d="M2589.75 4351h10" /><path d="M2599.75 4351h10" /><g class="non-terminal ">
<path d="M2609.75 4351h0.0" /><path d="M2689.75 4351h0.0" /><text class="comment" x="2649.75" y="4356">out.d=&quot;3&quot;;</text></g></g><path d="M2700.5 4351a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4381h15.0" /><path d="M2685.5 4381h15.0" /><g class="terminal ">
<path d="M2531.5 4381h0.0" /><path d="M2585.5 4381h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2531.5" y="4370"></rect><text x="2558.5" y="4385">four</text></g><path d="M2585.5 4381h10" /><path d="M2595.5 4381h10" /><g class="non-terminal ">
<path d="M2605.5 4381h0.0" /><path d="M2685.5 4381h0.0" /><text class="comment" x="2645.5" y="4386">out.d=&quot;4&quot;;</text></g></g><path d="M2700.5 4381a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4411h15.0" /><path d="M2685.5 4411h15.0" /><g class="terminal ">
<path d="M2531.5 4411h0.0" /><path d="M2585.5 4411h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2531.5" y="4400"></rect><text x="2558.5" y="4415">five</text></g><path d="M2585.5 4411h10" /><path d="M2595.5 4411h10" /><g class="non-terminal ">
<path d="M2605.5 4411h0.0" /><path d="M2685.5 4411h0.0" /><text class="comment" x="2645.5" y="4416">out.d=&quot;5&quot;;</text></g></g><path d="M2700.5 4411a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4441h19.25" /><path d="M2681.25 4441h19.25" /><g class="terminal ">
<path d="M2535.75 4441h0.0" /><path d="M2581.25 4441h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2535.75" y="4430"></rect><text x="2558.5" y="4445">six</text></g><path d="M2581.25 4441h10" /><path d="M2591.25 4441h10" /><g class="non-terminal ">
<path d="M2601.25 4441h0.0" /><path d="M2681.25 4441h0.0" /><text class="comment" x="2641.25" y="4446">out.d=&quot;6&quot;;</text></g></g><path d="M2700.5 4441a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4471h10.75" /><path d="M2689.75 4471h10.75" /><g class="terminal ">
<path d="M2527.25 4471h0.0" /><path d="M2589.75 4471h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2527.25" y="4460"></rect><text x="2558.5" y="4475">seven</text></g><path d="M2589.75 4471h10" /><path d="M2599.75 4471h10" /><g class="non-terminal ">
<path d="M2609.75 4471h0.0" /><path d="M2689.75 4471h0.0" /><text class="comment" x="2649.75" y="4476">out.d=&quot;7&quot;;</text></g></g><path d="M2700.5 4471a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4501h10.75" /><path d="M2689.75 4501h10.75" /><g class="terminal ">
<path d="M2527.25 4501h0.0" /><path d="M2589.75 4501h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2527.25" y="4490"></rect><text x="2558.5" y="4505">eight</text></g><path d="M2589.75 4501h10" /><path d="M2599.75 4501h10" /><g class="non-terminal ">
<path d="M2609.75 4501h0.0" /><path d="M2689.75 4501h0.0" /><text class="comment" x="2649.75" y="4506">out.d=&quot;8&quot;;</text></g></g><path d="M2700.5 4501a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M2496.5 4231a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M2516.5 4531h15.0" /><path d="M2685.5 4531h15.0" /><g class="terminal ">
<path d="M2531.5 4531h0.0" /><path d="M2585.5 4531h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2531.5" y="4520"></rect><text x="2558.5" y="4535">nine</text></g><path d="M2585.5 4531h10" /><path d="M2595.5 4531h10" /><g class="non-terminal ">
<path d="M2605.5 4531h0.0" /><path d="M2685.5 4531h0.0" /><text class="comment" x="2645.5" y="4536">out.d=&quot;9&quot;;</text></g></g><path d="M2700.5 4531a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M2720.5 4231h10" /><path d="M2730.5 4231h10" /><g class="terminal ">
<path d="M2740.5 4231h0.0" /><path d="M3066.5 4231h0.0" /><rect height="22" rx="10" ry="10" width="326" x="2740.5" y="4220"></rect><text x="2903.5" y="4235">!!out.dd1=rules.tensPlace.tensPlace;</text></g><path d="M3066.5 4231h10" /><path d="M3076.5 4231h10" /><g class="terminal ">
<path d="M3086.5 4231h0.0" /><path d="M3353.0 4231h0.0" /><rect height="22" rx="10" ry="10" width="266.5" x="3086.5" y="4220"></rect><text x="3219.75" y="4235">out.dd2=rules.singleDigit.d!!</text></g></g><path d="M3353.0 4231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M3373.0 3961h10" /><path d="M3383.0 3961h10" /><g class="terminal ">
<path d="M3393.0 3961h0.0" /><path d="M3676.5 3961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3393" y="3950"></rect><text x="3534.75" y="3965">!!out.d3=rules.doubleDigit.dd1;</text></g><path d="M3676.5 3961h10" /><path d="M3686.5 3961h10" /><g class="terminal ">
<path d="M3696.5 3961h0.0" /><path d="M3980.0 3961h0.0" /><rect height="22" rx="10" ry="10" width="283.5" x="3696.5" y="3950"></rect><text x="3838.25" y="3965">out.d4=rules.doubleDigit.dd2;!!</text></g><path d="M3980.0 3961h10" /><path d="M3990.0 3961h10" /><g>
<path d="M4000.0 3961h0.0" /><path d="M4224.0 3961h0.0" /><g>
<path d="M4000.0 3961h0.0" /><path d="M4224.0 3961h0.0" /><path d="M4000.0 3961h20" /><g>
<path d="M4020.0 3961h0.0" /><path d="M4204.0 3961h0.0" /><g>
<path d="M4020.0 3961h0.0" /><path d="M4114.0 3961h0.0" /><path d="M4020.0 3961h20" /><g>
<path d="M4040.0 3961h0.0" /><path d="M4094.0 3961h0.0" /><g class="terminal ">
<path d="M4040.0 3961h0.0" /><path d="M4094.0 3961h0.0" /><rect height="22" rx="10" ry="10" width="54" x="4040" y="3950"></rect><text x="4067" y="3965">zero</text></g></g><path d="M4094.0 3961h20" /><path d="M4020.0 3961a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M4040.0 3991h8.5" /><path d="M4085.5 3991h8.5" /><g class="terminal ">
<path d="M4048.5 3991h0.0" /><path d="M4085.5 3991h0.0" /><rect height="22" rx="10" ry="10" width="37" x="4048.5" y="3980"></rect><text x="4067" y="3995">oh</text></g></g><path d="M4094.0 3991a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M4114.0 3961h10" /><g class="non-terminal ">
<path d="M4124.0 3961h0.0" /><path d="M4204.0 3961h0.0" /><text class="comment" x="4164" y="3966">out.d=&quot;0&quot;;</text></g></g><path d="M4204.0 3961h20" /><path d="M4000.0 3961a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4021h19.25" /><path d="M4184.75 4021h19.25" /><g class="terminal ">
<path d="M4039.25 4021h0.0" /><path d="M4084.75 4021h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="4039.25" y="4010"></rect><text x="4062" y="4025">one</text></g><path d="M4084.75 4021h10" /><path d="M4094.75 4021h10" /><g class="non-terminal ">
<path d="M4104.75 4021h0.0" /><path d="M4184.75 4021h0.0" /><text class="comment" x="4144.75" y="4026">out.d=&quot;1&quot;;</text></g></g><path d="M4204.0 4021a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4051h19.25" /><path d="M4184.75 4051h19.25" /><g class="terminal ">
<path d="M4039.25 4051h0.0" /><path d="M4084.75 4051h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="4039.25" y="4040"></rect><text x="4062" y="4055">two</text></g><path d="M4084.75 4051h10" /><path d="M4094.75 4051h10" /><g class="non-terminal ">
<path d="M4104.75 4051h0.0" /><path d="M4184.75 4051h0.0" /><text class="comment" x="4144.75" y="4056">out.d=&quot;2&quot;;</text></g></g><path d="M4204.0 4051a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4081h10.75" /><path d="M4193.25 4081h10.75" /><g class="terminal ">
<path d="M4030.75 4081h0.0" /><path d="M4093.25 4081h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="4030.75" y="4070"></rect><text x="4062" y="4085">three</text></g><path d="M4093.25 4081h10" /><path d="M4103.25 4081h10" /><g class="non-terminal ">
<path d="M4113.25 4081h0.0" /><path d="M4193.25 4081h0.0" /><text class="comment" x="4153.25" y="4086">out.d=&quot;3&quot;;</text></g></g><path d="M4204.0 4081a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4111h15.0" /><path d="M4189.0 4111h15.0" /><g class="terminal ">
<path d="M4035.0 4111h0.0" /><path d="M4089.0 4111h0.0" /><rect height="22" rx="10" ry="10" width="54" x="4035" y="4100"></rect><text x="4062" y="4115">four</text></g><path d="M4089.0 4111h10" /><path d="M4099.0 4111h10" /><g class="non-terminal ">
<path d="M4109.0 4111h0.0" /><path d="M4189.0 4111h0.0" /><text class="comment" x="4149" y="4116">out.d=&quot;4&quot;;</text></g></g><path d="M4204.0 4111a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4141h15.0" /><path d="M4189.0 4141h15.0" /><g class="terminal ">
<path d="M4035.0 4141h0.0" /><path d="M4089.0 4141h0.0" /><rect height="22" rx="10" ry="10" width="54" x="4035" y="4130"></rect><text x="4062" y="4145">five</text></g><path d="M4089.0 4141h10" /><path d="M4099.0 4141h10" /><g class="non-terminal ">
<path d="M4109.0 4141h0.0" /><path d="M4189.0 4141h0.0" /><text class="comment" x="4149" y="4146">out.d=&quot;5&quot;;</text></g></g><path d="M4204.0 4141a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4171h19.25" /><path d="M4184.75 4171h19.25" /><g class="terminal ">
<path d="M4039.25 4171h0.0" /><path d="M4084.75 4171h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="4039.25" y="4160"></rect><text x="4062" y="4175">six</text></g><path d="M4084.75 4171h10" /><path d="M4094.75 4171h10" /><g class="non-terminal ">
<path d="M4104.75 4171h0.0" /><path d="M4184.75 4171h0.0" /><text class="comment" x="4144.75" y="4176">out.d=&quot;6&quot;;</text></g></g><path d="M4204.0 4171a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4201h10.75" /><path d="M4193.25 4201h10.75" /><g class="terminal ">
<path d="M4030.75 4201h0.0" /><path d="M4093.25 4201h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="4030.75" y="4190"></rect><text x="4062" y="4205">seven</text></g><path d="M4093.25 4201h10" /><path d="M4103.25 4201h10" /><g class="non-terminal ">
<path d="M4113.25 4201h0.0" /><path d="M4193.25 4201h0.0" /><text class="comment" x="4153.25" y="4206">out.d=&quot;7&quot;;</text></g></g><path d="M4204.0 4201a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4231h10.75" /><path d="M4193.25 4231h10.75" /><g class="terminal ">
<path d="M4030.75 4231h0.0" /><path d="M4093.25 4231h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="4030.75" y="4220"></rect><text x="4062" y="4235">eight</text></g><path d="M4093.25 4231h10" /><path d="M4103.25 4231h10" /><g class="non-terminal ">
<path d="M4113.25 4231h0.0" /><path d="M4193.25 4231h0.0" /><text class="comment" x="4153.25" y="4236">out.d=&quot;8&quot;;</text></g></g><path d="M4204.0 4231a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /><path d="M4000.0 3961a10 10 0 0 1 10 10v280a10 10 0 0 0 10 10" /><g>
<path d="M4020.0 4261h15.0" /><path d="M4189.0 4261h15.0" /><g class="terminal ">
<path d="M4035.0 4261h0.0" /><path d="M4089.0 4261h0.0" /><rect height="22" rx="10" ry="10" width="54" x="4035" y="4250"></rect><text x="4062" y="4265">nine</text></g><path d="M4089.0 4261h10" /><path d="M4099.0 4261h10" /><g class="non-terminal ">
<path d="M4109.0 4261h0.0" /><path d="M4189.0 4261h0.0" /><text class="comment" x="4149" y="4266">out.d=&quot;9&quot;;</text></g></g><path d="M4204.0 4261a10 10 0 0 0 10 -10v-280a10 10 0 0 1 10 -10" /></g></g><path d="M4224.0 3961h10" /><path d="M4234.0 3961h10" /><g class="non-terminal ">
<path d="M4244.0 3961h0.0" /><path d="M4443.0 3961h0.0" /><text class="comment" x="4343.5" y="3966">out.d5=rules.singleDigit.d;</text></g></g><path d="M4443.0 3961a10 10 0 0 0 10 -10v-3910a10 10 0 0 1 10 -10" /></g><path d="M4463.0 31h10" /><g class="non-terminal ">
<path d="M4473.0 31h0.0" /><path d="M4784.0 31h0.0" /><text class="comment" x="4628.5" y="36">out.zip=out.d1+out.d2+out.d3+out.d4+out.d5;</text></g></g><path d="M4784.0 31h10" /><path d="M4794.0 31h10" /><g class="non-terminal ">
<path d="M4804.0 31h0.0" /><path d="M4968.0 31h0.0" /><text class="comment" x="4886" y="36">out.zip=rules.zip.zip;</text></g></g><path d="M4968.0 31h20" /><path d="M50.0 31a10 10 0 0 1 10 10v4510a10 10 0 0 0 10 10" /><g>
<path d="M70.0 4561h2025.5" /><path d="M2942.5 4561h2025.5" /><g>
<path d="M2095.5 4561h0.0" /><path d="M2751.5 4561h0.0" /><g>
<path d="M2095.5 4561h0.0" /><path d="M2751.5 4561h0.0" /><path d="M2095.5 4561h20" /><g>
<path d="M2115.5 4561h272.5" /><path d="M2459.0 4561h272.5" /><g class="terminal ">
<path d="M2388.0 4561h0.0" /><path d="M2459.0 4561h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2388" y="4550"></rect><text x="2423.5" y="4565">repeat</text></g></g><path d="M2731.5 4561h20" /><path d="M2095.5 4561a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2115.5 4591h227.0" /><path d="M2504.5 4591h227.0" /><g class="terminal ">
<path d="M2342.5 4591h0.0" /><path d="M2413.5 4591h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2342.5" y="4580"></rect><text x="2378" y="4595">please</text></g><path d="M2413.5 4591h10" /><path d="M2423.5 4591h10" /><g class="terminal ">
<path d="M2433.5 4591h0.0" /><path d="M2504.5 4591h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2433.5" y="4580"></rect><text x="2469" y="4595">repeat</text></g></g><path d="M2731.5 4591a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2095.5 4561a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2115.5 4621h227.0" /><path d="M2504.5 4621h227.0" /><g class="terminal ">
<path d="M2342.5 4621h0.0" /><path d="M2413.5 4621h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2342.5" y="4610"></rect><text x="2378" y="4625">repeat</text></g><path d="M2413.5 4621h10" /><path d="M2423.5 4621h10" /><g class="terminal ">
<path d="M2433.5 4621h0.0" /><path d="M2504.5 4621h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2433.5" y="4610"></rect><text x="2469" y="4625">please</text></g></g><path d="M2731.5 4621a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2095.5 4561a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2115.5 4651h171.5" /><path d="M2560.0 4651h171.5" /><g class="terminal ">
<path d="M2287.0 4651h0.0" /><path d="M2358.0 4651h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2287" y="4640"></rect><text x="2322.5" y="4655">please</text></g><path d="M2358.0 4651h10" /><g>
<path d="M2368.0 4651h0.0" /><path d="M2487.5 4651h0.0" /><path d="M2368.0 4651h20" /><g>
<path d="M2388.0 4651h4.25" /><path d="M2463.25 4651h4.25" /><g class="terminal ">
<path d="M2392.25 4651h0.0" /><path d="M2463.25 4651h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2392.25" y="4640"></rect><text x="2427.75" y="4655">repeat</text></g></g><path d="M2467.5 4651h20" /><path d="M2368.0 4651a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2388.0 4681h4.25" /><path d="M2463.25 4681h4.25" /><g class="terminal ">
<path d="M2392.25 4681h0.0" /><path d="M2463.25 4681h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2392.25" y="4670"></rect><text x="2427.75" y="4685">ripeet</text></g></g><path d="M2467.5 4681a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2368.0 4651a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2388.0 4711h4.25" /><path d="M2463.25 4711h4.25" /><g class="terminal ">
<path d="M2392.25 4711h0.0" /><path d="M2463.25 4711h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2392.25" y="4700"></rect><text x="2427.75" y="4715">reepit</text></g></g><path d="M2467.5 4711a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2368.0 4651a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2388.0 4741h0.0" /><path d="M2467.5 4741h0.0" /><g class="terminal ">
<path d="M2388.0 4741h0.0" /><path d="M2467.5 4741h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2388" y="4730"></rect><text x="2427.75" y="4745">reepeet</text></g></g><path d="M2467.5 4741a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /></g><path d="M2487.5 4651h10" /><g class="terminal ">
<path d="M2497.5 4651h0.0" /><path d="M2560.0 4651h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2497.5" y="4640"></rect><text x="2528.75" y="4655">again</text></g></g><path d="M2731.5 4651a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2095.5 4561a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2115.5 4771h166.5" /><path d="M2565.0 4771h166.5" /><g>
<path d="M2282.0 4771h0.0" /><path d="M2401.5 4771h0.0" /><path d="M2282.0 4771h20" /><g>
<path d="M2302.0 4771h4.25" /><path d="M2377.25 4771h4.25" /><g class="terminal ">
<path d="M2306.25 4771h0.0" /><path d="M2377.25 4771h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2306.25" y="4760"></rect><text x="2341.75" y="4775">repeat</text></g></g><path d="M2381.5 4771h20" /><path d="M2282.0 4771a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2302.0 4801h4.25" /><path d="M2377.25 4801h4.25" /><g class="terminal ">
<path d="M2306.25 4801h0.0" /><path d="M2377.25 4801h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2306.25" y="4790"></rect><text x="2341.75" y="4805">ripeet</text></g></g><path d="M2381.5 4801a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2282.0 4771a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2302.0 4831h4.25" /><path d="M2377.25 4831h4.25" /><g class="terminal ">
<path d="M2306.25 4831h0.0" /><path d="M2377.25 4831h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2306.25" y="4820"></rect><text x="2341.75" y="4835">reepit</text></g></g><path d="M2381.5 4831a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2282.0 4771a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2302.0 4861h0.0" /><path d="M2381.5 4861h0.0" /><g class="terminal ">
<path d="M2302.0 4861h0.0" /><path d="M2381.5 4861h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2302" y="4850"></rect><text x="2341.75" y="4865">reepeet</text></g></g><path d="M2381.5 4861a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /></g><path d="M2401.5 4771h10" /><g class="terminal ">
<path d="M2411.5 4771h0.0" /><path d="M2474.0 4771h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2411.5" y="4760"></rect><text x="2442.75" y="4775">again</text></g><path d="M2474.0 4771h10" /><path d="M2484.0 4771h10" /><g class="terminal ">
<path d="M2494.0 4771h0.0" /><path d="M2565.0 4771h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2494" y="4760"></rect><text x="2529.5" y="4775">please</text></g></g><path d="M2731.5 4771a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2095.5 4561a10 10 0 0 1 10 10v310a10 10 0 0 0 10 10" /><g>
<path d="M2115.5 4891h0.0" /><path d="M2731.5 4891h0.0" /><g>
<path d="M2115.5 4891h0.0" /><path d="M2218.0 4891h0.0" /><path d="M2115.5 4891h20" /><g>
<path d="M2135.5 4891h0.0" /><path d="M2198.0 4891h0.0" /><g class="terminal ">
<path d="M2135.5 4891h0.0" /><path d="M2198.0 4891h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2135.5" y="4880"></rect><text x="2166.75" y="4895">could</text></g></g><path d="M2198.0 4891h20" /><path d="M2115.5 4891a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2135.5 4921h8.5" /><path d="M2189.5 4921h8.5" /><g class="terminal ">
<path d="M2144.0 4921h0.0" /><path d="M2189.5 4921h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2144" y="4910"></rect><text x="2166.75" y="4925">can</text></g></g><path d="M2198.0 4921a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2218.0 4891h10" /><g class="terminal ">
<path d="M2228.0 4891h0.0" /><path d="M2273.5 4891h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2228" y="4880"></rect><text x="2250.75" y="4895">you</text></g><path d="M2273.5 4891h10" /><path d="M2283.5 4891h10" /><g class="terminal ">
<path d="M2293.5 4891h0.0" /><path d="M2364.5 4891h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2293.5" y="4880"></rect><text x="2329" y="4895">please</text></g><path d="M2364.5 4891h10" /><g>
<path d="M2374.5 4891h0.0" /><path d="M2494.0 4891h0.0" /><path d="M2374.5 4891h20" /><g>
<path d="M2394.5 4891h4.25" /><path d="M2469.75 4891h4.25" /><g class="terminal ">
<path d="M2398.75 4891h0.0" /><path d="M2469.75 4891h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2398.75" y="4880"></rect><text x="2434.25" y="4895">repeat</text></g></g><path d="M2474.0 4891h20" /><path d="M2374.5 4891a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2394.5 4921h4.25" /><path d="M2469.75 4921h4.25" /><g class="terminal ">
<path d="M2398.75 4921h0.0" /><path d="M2469.75 4921h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2398.75" y="4910"></rect><text x="2434.25" y="4925">ripeet</text></g></g><path d="M2474.0 4921a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2374.5 4891a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2394.5 4951h4.25" /><path d="M2469.75 4951h4.25" /><g class="terminal ">
<path d="M2398.75 4951h0.0" /><path d="M2469.75 4951h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2398.75" y="4940"></rect><text x="2434.25" y="4955">reepit</text></g></g><path d="M2474.0 4951a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2374.5 4891a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2394.5 4981h0.0" /><path d="M2474.0 4981h0.0" /><g class="terminal ">
<path d="M2394.5 4981h0.0" /><path d="M2474.0 4981h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2394.5" y="4970"></rect><text x="2434.25" y="4985">reepeet</text></g></g><path d="M2474.0 4981a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /></g><path d="M2494.0 4891h10" /><g class="terminal ">
<path d="M2504.0 4891h0.0" /><path d="M2558.0 4891h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2504" y="4880"></rect><text x="2531" y="4895">that</text></g><path d="M2558.0 4891h10" /><path d="M2568.0 4891h10" /><g class="terminal ">
<path d="M2578.0 4891h0.0" /><path d="M2640.5 4891h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2578" y="4880"></rect><text x="2609.25" y="4895">again</text></g><path d="M2640.5 4891h10" /><path d="M2650.5 4891h10" /><g class="terminal ">
<path d="M2660.5 4891h0.0" /><path d="M2731.5 4891h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2660.5" y="4880"></rect><text x="2696" y="4895">please</text></g></g><path d="M2731.5 4891a10 10 0 0 0 10 -10v-310a10 10 0 0 1 10 -10" /></g></g><path d="M2751.5 4561h10" /><path d="M2761.5 4561h10" /><g class="non-terminal ">
<path d="M2771.5 4561h0.0" /><path d="M2942.5 4561h0.0" /><text class="comment" x="2857" y="4566">out.universal=&quot;repeat&quot;;</text></g></g><path d="M4968.0 4561a10 10 0 0 0 10 -10v-4510a10 10 0 0 1 10 -10" /><path d="M50.0 31a10 10 0 0 1 10 10v4960a10 10 0 0 0 10 10" /><g>
<path d="M70.0 5011h1826.25" /><path d="M3141.75 5011h1826.25" /><g>
<path d="M1896.25 5011h0.0" /><path d="M2957.75 5011h0.0" /><g>
<path d="M1896.25 5011h0.0" /><path d="M2957.75 5011h0.0" /><path d="M1896.25 5011h20" /><g>
<path d="M1916.25 5011h317.5" /><path d="M2620.25 5011h317.5" /><g>
<path d="M2233.75 5011h0.0" /><path d="M2620.25 5011h0.0" /><path d="M2233.75 5011h20" /><g>
<path d="M2253.75 5011h142.0" /><path d="M2458.25 5011h142.0" /><g class="terminal ">
<path d="M2395.75 5011h0.0" /><path d="M2458.25 5011h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2395.75" y="5000"></rect><text x="2427" y="5015">agent</text></g></g><path d="M2600.25 5011h20" /><path d="M2233.75 5011a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5041h129.25" /><path d="M2471.0 5041h129.25" /><g class="terminal ">
<path d="M2383.0 5041h0.0" /><path d="M2471.0 5041h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2383" y="5030"></rect><text x="2427" y="5045">operator</text></g></g><path d="M2600.25 5041a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5071h103.75" /><path d="M2496.5 5071h103.75" /><g class="terminal ">
<path d="M2357.5 5071h0.0" /><path d="M2496.5 5071h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2357.5" y="5060"></rect><text x="2427" y="5075">representative</text></g></g><path d="M2600.25 5071a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5101h75.25" /><path d="M2525.0 5101h75.25" /><g class="terminal ">
<path d="M2329.0 5101h0.0" /><path d="M2366.0 5101h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2329" y="5090"></rect><text x="2347.5" y="5105">no</text></g><path d="M2366.0 5101h10" /><path d="M2376.0 5101h10" /><g class="terminal ">
<path d="M2386.0 5101h0.0" /><path d="M2525.0 5101h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2386" y="5090"></rect><text x="2455.5" y="5105">representative</text></g></g><path d="M2600.25 5101a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5131h103.75" /><path d="M2496.5 5131h103.75" /><g class="terminal ">
<path d="M2357.5 5131h0.0" /><path d="M2496.5 5131h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2357.5" y="5120"></rect><text x="2427" y="5135">represehnative</text></g></g><path d="M2600.25 5131a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5161h75.25" /><path d="M2525.0 5161h75.25" /><g class="terminal ">
<path d="M2329.0 5161h0.0" /><path d="M2366.0 5161h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2329" y="5150"></rect><text x="2347.5" y="5165">no</text></g><path d="M2366.0 5161h10" /><path d="M2376.0 5161h10" /><g class="terminal ">
<path d="M2386.0 5161h0.0" /><path d="M2525.0 5161h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2386" y="5150"></rect><text x="2455.5" y="5165">represehnative</text></g></g><path d="M2600.25 5161a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5191h96.5" /><path d="M2503.75 5191h96.5" /><g class="terminal ">
<path d="M2350.25 5191h0.0" /><path d="M2412.75 5191h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2350.25" y="5180"></rect><text x="2381.5" y="5195">human</text></g><path d="M2412.75 5191h10" /><path d="M2422.75 5191h10" /><g class="terminal ">
<path d="M2432.75 5191h0.0" /><path d="M2503.75 5191h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2432.75" y="5180"></rect><text x="2468.25" y="5195">person</text></g></g><path d="M2600.25 5191a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v190a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5221h0.0" /><path d="M2600.25 5221h0.0" /><g class="terminal ">
<path d="M2253.75 5221h0.0" /><path d="M2341.75 5221h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2253.75" y="5210"></rect><text x="2297.75" y="5225">customer</text></g><path d="M2341.75 5221h10" /><path d="M2351.75 5221h10" /><g class="terminal ">
<path d="M2361.75 5221h0.0" /><path d="M2441.25 5221h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2361.75" y="5210"></rect><text x="2401.5" y="5225">service</text></g><path d="M2441.25 5221h10" /><path d="M2451.25 5221h10" /><g class="terminal ">
<path d="M2461.25 5221h0.0" /><path d="M2600.25 5221h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2461.25" y="5210"></rect><text x="2530.75" y="5225">representative</text></g></g><path d="M2600.25 5221a10 10 0 0 0 10 -10v-190a10 10 0 0 1 10 -10" /><path d="M2233.75 5011a10 10 0 0 1 10 10v220a10 10 0 0 0 10 10" /><g>
<path d="M2253.75 5251h51.0" /><path d="M2549.25 5251h51.0" /><g class="terminal ">
<path d="M2304.75 5251h0.0" /><path d="M2341.75 5251h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2304.75" y="5240"></rect><text x="2323.25" y="5255">no</text></g><path d="M2341.75 5251h10" /><path d="M2351.75 5251h10" /><g class="terminal ">
<path d="M2361.75 5251h0.0" /><path d="M2449.75 5251h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2361.75" y="5240"></rect><text x="2405.75" y="5255">customer</text></g><path d="M2449.75 5251h10" /><path d="M2459.75 5251h10" /><g class="terminal ">
<path d="M2469.75 5251h0.0" /><path d="M2549.25 5251h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2469.75" y="5240"></rect><text x="2509.5" y="5255">service</text></g></g><path d="M2600.25 5251a10 10 0 0 0 10 -10v-220a10 10 0 0 1 10 -10" /></g></g><path d="M2937.75 5011h20" /><path d="M1896.25 5011a10 10 0 0 1 10 10v250a10 10 0 0 0 10 10" /><g>
<path d="M1916.25 5281h0.0" /><path d="M2937.75 5281h0.0" /><g class="terminal ">
<path d="M1916.25 5281h0.0" /><path d="M1953.25 5281h0.0" /><rect height="22" rx="10" ry="10" width="37" x="1916.25" y="5270"></rect><text x="1934.75" y="5285">no</text></g><path d="M1953.25 5281h10" /><g>
<path d="M1963.25 5281h0.0" /><path d="M2245.25 5281h0.0" /><path d="M1963.25 5281h20" /><g>
<path d="M1983.25 5281h32.75" /><path d="M2192.5 5281h32.75" /><g class="terminal ">
<path d="M2016.0 5281h0.0" /><path d="M2061.5 5281h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2016" y="5270"></rect><text x="2038.75" y="5285">i&apos;d</text></g><path d="M2061.5 5281h10" /><path d="M2071.5 5281h10" /><g class="terminal ">
<path d="M2081.5 5281h0.0" /><path d="M2135.5 5281h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2081.5" y="5270"></rect><text x="2108.5" y="5285">like</text></g><path d="M2135.5 5281h10" /><path d="M2145.5 5281h10" /><g class="terminal ">
<path d="M2155.5 5281h0.0" /><path d="M2192.5 5281h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2155.5" y="5270"></rect><text x="2174" y="5285">to</text></g></g><path d="M2225.25 5281h20" /><path d="M1963.25 5281a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5311h0.0" /><path d="M2225.25 5311h0.0" /><g class="terminal ">
<path d="M1983.25 5311h0.0" /><path d="M2011.75 5311h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="1983.25" y="5300"></rect><text x="1997.5" y="5315">i</text></g><path d="M2011.75 5311h10" /><path d="M2021.75 5311h10" /><g class="terminal ">
<path d="M2031.75 5311h0.0" /><path d="M2094.25 5311h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2031.75" y="5300"></rect><text x="2063" y="5315">would</text></g><path d="M2094.25 5311h10" /><path d="M2104.25 5311h10" /><g class="terminal ">
<path d="M2114.25 5311h0.0" /><path d="M2168.25 5311h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2114.25" y="5300"></rect><text x="2141.25" y="5315">like</text></g><path d="M2168.25 5311h10" /><path d="M2178.25 5311h10" /><g class="terminal ">
<path d="M2188.25 5311h0.0" /><path d="M2225.25 5311h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2188.25" y="5300"></rect><text x="2206.75" y="5315">to</text></g></g><path d="M2225.25 5311a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M1963.25 5281a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5341h41.25" /><path d="M2184.0 5341h41.25" /><g class="terminal ">
<path d="M2024.5 5341h0.0" /><path d="M2053.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2024.5" y="5330"></rect><text x="2038.75" y="5345">i</text></g><path d="M2053.0 5341h10" /><path d="M2063.0 5341h10" /><g class="terminal ">
<path d="M2073.0 5341h0.0" /><path d="M2127.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2073" y="5330"></rect><text x="2100" y="5345">need</text></g><path d="M2127.0 5341h10" /><path d="M2137.0 5341h10" /><g class="terminal ">
<path d="M2147.0 5341h0.0" /><path d="M2184.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2147" y="5330"></rect><text x="2165.5" y="5345">to</text></g></g><path d="M2225.25 5341a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M1963.25 5281a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5371h41.25" /><path d="M2184.0 5371h41.25" /><g class="terminal ">
<path d="M2024.5 5371h0.0" /><path d="M2053.0 5371h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2024.5" y="5360"></rect><text x="2038.75" y="5375">i</text></g><path d="M2053.0 5371h10" /><path d="M2063.0 5371h10" /><g class="terminal ">
<path d="M2073.0 5371h0.0" /><path d="M2127.0 5371h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2073" y="5360"></rect><text x="2100" y="5375">want</text></g><path d="M2127.0 5371h10" /><path d="M2137.0 5371h10" /><g class="terminal ">
<path d="M2147.0 5371h0.0" /><path d="M2184.0 5371h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2147" y="5360"></rect><text x="2165.5" y="5375">to</text></g></g><path d="M2225.25 5371a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M1963.25 5281a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5401h74.0" /><path d="M2151.25 5401h74.0" /><g class="terminal ">
<path d="M2057.25 5401h0.0" /><path d="M2102.75 5401h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2057.25" y="5390"></rect><text x="2080" y="5405">may</text></g><path d="M2102.75 5401h10" /><path d="M2112.75 5401h10" /><g class="terminal ">
<path d="M2122.75 5401h0.0" /><path d="M2151.25 5401h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2122.75" y="5390"></rect><text x="2137" y="5405">i</text></g></g><path d="M2225.25 5401a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M1963.25 5281a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5431h74.0" /><path d="M2151.25 5431h74.0" /><g class="terminal ">
<path d="M2057.25 5431h0.0" /><path d="M2102.75 5431h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2057.25" y="5420"></rect><text x="2080" y="5435">can</text></g><path d="M2102.75 5431h10" /><path d="M2112.75 5431h10" /><g class="terminal ">
<path d="M2122.75 5431h0.0" /><path d="M2151.25 5431h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2122.75" y="5420"></rect><text x="2137" y="5435">i</text></g></g><path d="M2225.25 5431a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M1963.25 5281a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M1983.25 5461h69.75" /><path d="M2155.5 5461h69.75" /><g class="terminal ">
<path d="M2053.0 5461h0.0" /><path d="M2098.5 5461h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2053" y="5450"></rect><text x="2075.75" y="5465">let</text></g><path d="M2098.5 5461h10" /><path d="M2108.5 5461h10" /><g class="terminal ">
<path d="M2118.5 5461h0.0" /><path d="M2155.5 5461h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2118.5" y="5450"></rect><text x="2137" y="5465">me</text></g></g><path d="M2225.25 5461a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /></g><g>
<path d="M2245.25 5281h0.0" /><path d="M2421.75 5281h0.0" /><path d="M2245.25 5281h20" /><g>
<path d="M2265.25 5281h8.5" /><path d="M2393.25 5281h8.5" /><g class="terminal ">
<path d="M2273.75 5281h0.0" /><path d="M2336.25 5281h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2273.75" y="5270"></rect><text x="2305" y="5285">speak</text></g><path d="M2336.25 5281h10" /><path d="M2346.25 5281h10" /><g class="terminal ">
<path d="M2356.25 5281h0.0" /><path d="M2393.25 5281h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2356.25" y="5270"></rect><text x="2374.75" y="5285">to</text></g></g><path d="M2401.75 5281h20" /><path d="M2245.25 5281a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2265.25 5311h0.0" /><path d="M2401.75 5311h0.0" /><g class="terminal ">
<path d="M2265.25 5311h0.0" /><path d="M2327.75 5311h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2265.25" y="5300"></rect><text x="2296.5" y="5315">speak</text></g><path d="M2327.75 5311h10" /><path d="M2337.75 5311h10" /><g class="terminal ">
<path d="M2347.75 5311h0.0" /><path d="M2401.75 5311h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2347.75" y="5300"></rect><text x="2374.75" y="5315">with</text></g></g><path d="M2401.75 5311a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2245.25 5281a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2265.25 5341h12.75" /><path d="M2389.0 5341h12.75" /><g class="terminal ">
<path d="M2278.0 5341h0.0" /><path d="M2332.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2278" y="5330"></rect><text x="2305" y="5345">talk</text></g><path d="M2332.0 5341h10" /><path d="M2342.0 5341h10" /><g class="terminal ">
<path d="M2352.0 5341h0.0" /><path d="M2389.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2352" y="5330"></rect><text x="2370.5" y="5345">to</text></g></g><path d="M2401.75 5341a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /></g><g>
<path d="M2421.75 5281h0.0" /><path d="M2856.75 5281h0.0" /><path d="M2421.75 5281h20" /><g>
<path d="M2441.75 5281h0.0" /><path d="M2836.75 5281h0.0" /><g class="terminal ">
<path d="M2441.75 5281h0.0" /><path d="M2470.25 5281h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2441.75" y="5270"></rect><text x="2456" y="5285">a</text></g><path d="M2470.25 5281h10" /><path d="M2480.25 5281h10" /><g class="terminal ">
<path d="M2490.25 5281h0.0" /><path d="M2578.25 5281h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2490.25" y="5270"></rect><text x="2534.25" y="5285">customer</text></g><path d="M2578.25 5281h10" /><path d="M2588.25 5281h10" /><g class="terminal ">
<path d="M2598.25 5281h0.0" /><path d="M2677.75 5281h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2598.25" y="5270"></rect><text x="2638" y="5285">service</text></g><path d="M2677.75 5281h10" /><path d="M2687.75 5281h10" /><g class="terminal ">
<path d="M2697.75 5281h0.0" /><path d="M2836.75 5281h0.0" /><rect height="22" rx="10" ry="10" width="139" x="2697.75" y="5270"></rect><text x="2767.25" y="5285">representative</text></g></g><path d="M2836.75 5281h20" /><path d="M2421.75 5281a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5311h79.5" /><path d="M2757.25 5311h79.5" /><g class="terminal ">
<path d="M2521.25 5311h0.0" /><path d="M2549.75 5311h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2521.25" y="5300"></rect><text x="2535.5" y="5315">a</text></g><path d="M2549.75 5311h10" /><path d="M2559.75 5311h10" /><g class="terminal ">
<path d="M2569.75 5311h0.0" /><path d="M2657.75 5311h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2569.75" y="5300"></rect><text x="2613.75" y="5315">customer</text></g><path d="M2657.75 5311h10" /><path d="M2667.75 5311h10" /><g class="terminal ">
<path d="M2677.75 5311h0.0" /><path d="M2757.25 5311h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2677.75" y="5300"></rect><text x="2717.5" y="5315">service</text></g></g><path d="M2836.75 5311a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2421.75 5281a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5341h137.75" /><path d="M2699.0 5341h137.75" /><g class="terminal ">
<path d="M2579.5 5341h0.0" /><path d="M2616.5 5341h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2579.5" y="5330"></rect><text x="2598" y="5345">an</text></g><path d="M2616.5 5341h10" /><path d="M2626.5 5341h10" /><g class="terminal ">
<path d="M2636.5 5341h0.0" /><path d="M2699.0 5341h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2636.5" y="5330"></rect><text x="2667.75" y="5345">agent</text></g></g><path d="M2836.75 5341a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /><path d="M2421.75 5281a10 10 0 0 1 10 10v70a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5371h125.0" /><path d="M2711.75 5371h125.0" /><g class="terminal ">
<path d="M2566.75 5371h0.0" /><path d="M2603.75 5371h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2566.75" y="5360"></rect><text x="2585.25" y="5375">an</text></g><path d="M2603.75 5371h10" /><path d="M2613.75 5371h10" /><g class="terminal ">
<path d="M2623.75 5371h0.0" /><path d="M2711.75 5371h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2623.75" y="5360"></rect><text x="2667.75" y="5375">operator</text></g></g><path d="M2836.75 5371a10 10 0 0 0 10 -10v-70a10 10 0 0 1 10 -10" /><path d="M2421.75 5281a10 10 0 0 1 10 10v100a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5401h157.75" /><path d="M2679.0 5401h157.75" /><g class="terminal ">
<path d="M2599.5 5401h0.0" /><path d="M2679.0 5401h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2599.5" y="5390"></rect><text x="2639.25" y="5405">someone</text></g></g><path d="M2836.75 5401a10 10 0 0 0 10 -10v-100a10 10 0 0 1 10 -10" /><path d="M2421.75 5281a10 10 0 0 1 10 10v130a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5431h153.5" /><path d="M2683.25 5431h153.5" /><g class="terminal ">
<path d="M2595.25 5431h0.0" /><path d="M2683.25 5431h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2595.25" y="5420"></rect><text x="2639.25" y="5435">somebody</text></g></g><path d="M2836.75 5431a10 10 0 0 0 10 -10v-130a10 10 0 0 1 10 -10" /><path d="M2421.75 5281a10 10 0 0 1 10 10v160a10 10 0 0 0 10 10" /><g>
<path d="M2441.75 5461h137.75" /><path d="M2699.0 5461h137.75" /><g class="terminal ">
<path d="M2579.5 5461h0.0" /><path d="M2608.0 5461h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2579.5" y="5450"></rect><text x="2593.75" y="5465">a</text></g><path d="M2608.0 5461h10" /><path d="M2618.0 5461h10" /><g class="terminal ">
<path d="M2628.0 5461h0.0" /><path d="M2699.0 5461h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2628" y="5450"></rect><text x="2663.5" y="5465">person</text></g></g><path d="M2836.75 5461a10 10 0 0 0 10 -10v-160a10 10 0 0 1 10 -10" /></g><path d="M2856.75 5281h10" /><g class="terminal ">
<path d="M2866.75 5281h0.0" /><path d="M2937.75 5281h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2866.75" y="5270"></rect><text x="2902.25" y="5285">please</text></g></g><path d="M2937.75 5281a10 10 0 0 0 10 -10v-250a10 10 0 0 1 10 -10" /></g></g><path d="M2957.75 5011h10" /><path d="M2967.75 5011h10" /><g class="non-terminal ">
<path d="M2977.75 5011h0.0" /><path d="M3141.75 5011h0.0" /><text class="comment" x="3059.75" y="5016">out.universal=&quot;agent&quot;;</text></g></g><path d="M4968.0 5011a10 10 0 0 0 10 -10v-4960a10 10 0 0 1 10 -10" /><path d="M50.0 31a10 10 0 0 1 10 10v5440a10 10 0 0 0 10 10" /><g>
<path d="M70.0 5491h2204.0" /><path d="M2764.0 5491h2204.0" /><g>
<path d="M2274.0 5491h0.0" /><path d="M2587.0 5491h0.0" /><g class="terminal ">
<path d="M2274.0 5491h0.0" /><path d="M2345.0 5491h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2274" y="5480"></rect><text x="2309.5" y="5495">please</text></g><path d="M2345.0 5491h10" /><g>
<path d="M2355.0 5491h0.0" /><path d="M2506.0 5491h0.0" /><path d="M2355.0 5491h20" /><g>
<path d="M2375.0 5491h28.5" /><path d="M2457.5 5491h28.5" /><g class="terminal ">
<path d="M2403.5 5491h0.0" /><path d="M2457.5 5491h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2403.5" y="5480"></rect><text x="2430.5" y="5495">wait</text></g></g><path d="M2486.0 5491h20" /><path d="M2355.0 5491a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2375.0 5521h0.0" /><path d="M2486.0 5521h0.0" /><g class="terminal ">
<path d="M2375.0 5521h0.0" /><path d="M2429.0 5521h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2375" y="5510"></rect><text x="2402" y="5525">hold</text></g><path d="M2429.0 5521h10" /><path d="M2439.0 5521h10" /><g class="terminal ">
<path d="M2449.0 5521h0.0" /><path d="M2486.0 5521h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2449" y="5510"></rect><text x="2467.5" y="5525">on</text></g></g><path d="M2486.0 5521a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2506.0 5491h10" /><g class="terminal ">
<path d="M2516.0 5491h0.0" /><path d="M2587.0 5491h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2516" y="5480"></rect><text x="2551.5" y="5495">please</text></g></g><path d="M2587.0 5491h10" /><path d="M2597.0 5491h10" /><g class="non-terminal ">
<path d="M2607.0 5491h0.0" /><path d="M2764.0 5491h0.0" /><text class="comment" x="2685.5" y="5496">out.universal=&quot;wait&quot;;</text></g></g><path d="M4968.0 5491a10 10 0 0 0 10 -10v-5440a10 10 0 0 1 10 -10" /><path d="M50.0 31a10 10 0 0 1 10 10v5500a10 10 0 0 0 10 10" /><g>
<path d="M70.0 5551h2083.5" /><path d="M2884.5 5551h2083.5" /><g>
<path d="M2153.5 5551h0.0" /><path d="M2714.5 5551h0.0" /><g>
<path d="M2153.5 5551h0.0" /><path d="M2714.5 5551h0.0" /><path d="M2153.5 5551h20" /><g>
<path d="M2173.5 5551h183.75" /><path d="M2510.75 5551h183.75" /><g class="terminal ">
<path d="M2357.25 5551h0.0" /><path d="M2402.75 5551h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2357.25" y="5540"></rect><text x="2380" y="5555">new</text></g><path d="M2402.75 5551h10" /><path d="M2412.75 5551h10" /><g class="terminal ">
<path d="M2422.75 5551h0.0" /><path d="M2510.75 5551h0.0" /><rect height="22" rx="10" ry="10" width="88" x="2422.75" y="5540"></rect><text x="2466.75" y="5555">customer</text></g></g><path d="M2694.5 5551h20" /><path d="M2153.5 5551a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2173.5 5581h0.0" /><path d="M2694.5 5581h0.0" /><g class="terminal ">
<path d="M2173.5 5581h0.0" /><path d="M2202.0 5581h0.0" /><rect height="22" rx="10" ry="10" width="28.5" x="2173.5" y="5570"></rect><text x="2187.75" y="5585">I</text></g><path d="M2202.0 5581h10" /><g>
<path d="M2212.0 5581h0.0" /><path d="M2388.5 5581h0.0" /><path d="M2212.0 5581h20" /><g>
<path d="M2232.0 5581h41.25" /><path d="M2327.25 5581h41.25" /><g class="terminal ">
<path d="M2273.25 5581h0.0" /><path d="M2327.25 5581h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2273.25" y="5570"></rect><text x="2300.25" y="5585">have</text></g></g><path d="M2368.5 5581h20" /><path d="M2212.0 5581a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2232.0 5611h0.0" /><path d="M2368.5 5611h0.0" /><g class="terminal ">
<path d="M2232.0 5611h0.0" /><path d="M2294.5 5611h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2232" y="5600"></rect><text x="2263.25" y="5615">don&apos;t</text></g><path d="M2294.5 5611h10" /><path d="M2304.5 5611h10" /><g class="terminal ">
<path d="M2314.5 5611h0.0" /><path d="M2368.5 5611h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2314.5" y="5600"></rect><text x="2341.5" y="5615">have</text></g></g><path d="M2368.5 5611a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2212.0 5581a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2232.0 5641h0.0" /><path d="M2368.5 5641h0.0" /><g class="terminal ">
<path d="M2232.0 5641h0.0" /><path d="M2294.5 5641h0.0" /><rect height="22" rx="10" ry="10" width="62.5" x="2232" y="5630"></rect><text x="2263.25" y="5645">don&apos;t</text></g><path d="M2294.5 5641h10" /><path d="M2304.5 5641h10" /><g class="terminal ">
<path d="M2314.5 5641h0.0" /><path d="M2368.5 5641h0.0" /><rect height="22" rx="10" ry="10" width="54" x="2314.5" y="5630"></rect><text x="2341.5" y="5645">know</text></g></g><path d="M2368.5 5641a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /></g><g>
<path d="M2388.5 5581h0.0" /><path d="M2694.5 5581h0.0" /><path d="M2388.5 5581h20" /><g>
<path d="M2408.5 5581h114.5" /><path d="M2560.0 5581h114.5" /><g class="terminal ">
<path d="M2523.0 5581h0.0" /><path d="M2560.0 5581h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2523" y="5570"></rect><text x="2541.5" y="5585">it</text></g></g><path d="M2674.5 5581h20" /><path d="M2388.5 5581a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2408.5 5611h110.25" /><path d="M2564.25 5611h110.25" /><g class="terminal ">
<path d="M2518.75 5611h0.0" /><path d="M2564.25 5611h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2518.75" y="5600"></rect><text x="2541.5" y="5615">one</text></g></g><path d="M2674.5 5611a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /><path d="M2388.5 5581a10 10 0 0 1 10 10v40a10 10 0 0 0 10 10" /><g>
<path d="M2408.5 5641h0.0" /><path d="M2674.5 5641h0.0" /><g>
<path d="M2408.5 5641h0.0" /><path d="M2494.0 5641h0.0" /><path d="M2408.5 5641h20" /><g>
<path d="M2428.5 5641h4.25" /><path d="M2469.75 5641h4.25" /><g class="terminal ">
<path d="M2432.75 5641h0.0" /><path d="M2469.75 5641h0.0" /><rect height="22" rx="10" ry="10" width="37" x="2432.75" y="5630"></rect><text x="2451.25" y="5645">an</text></g></g><path d="M2474.0 5641h20" /><path d="M2408.5 5641a10 10 0 0 1 10 10v10a10 10 0 0 0 10 10" /><g>
<path d="M2428.5 5671h0.0" /><path d="M2474.0 5671h0.0" /><g class="terminal ">
<path d="M2428.5 5671h0.0" /><path d="M2474.0 5671h0.0" /><rect height="22" rx="10" ry="10" width="45.5" x="2428.5" y="5660"></rect><text x="2451.25" y="5675">the</text></g></g><path d="M2474.0 5671a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g><path d="M2494.0 5641h10" /><g class="terminal ">
<path d="M2504.0 5641h0.0" /><path d="M2583.5 5641h0.0" /><rect height="22" rx="10" ry="10" width="79.5" x="2504" y="5630"></rect><text x="2543.75" y="5645">account</text></g><path d="M2583.5 5641h10" /><path d="M2593.5 5641h10" /><g class="terminal ">
<path d="M2603.5 5641h0.0" /><path d="M2674.5 5641h0.0" /><rect height="22" rx="10" ry="10" width="71" x="2603.5" y="5630"></rect><text x="2639" y="5645">number</text></g></g><path d="M2674.5 5641a10 10 0 0 0 10 -10v-40a10 10 0 0 1 10 -10" /></g></g><path d="M2694.5 5581a10 10 0 0 0 10 -10v-10a10 10 0 0 1 10 -10" /></g></g><path d="M2714.5 5551h10" /><path d="M2724.5 5551h10" /><g class="non-terminal ">
<path d="M2734.5 5551h0.0" /><path d="M2884.5 5551h0.0" /><text class="comment" x="2809.5" y="5556">out.__garbage__=true</text></g></g><path d="M4968.0 5551a10 10 0 0 0 10 -10v-5500a10 10 0 0 1 10 -10" /></g></g><path d="M4988.0 31h10" /><path d="M 4998.0 31 h 20 m -10 -10 v 20 m 10 -20 v 20"></path></g><style>/* <![CDATA[ */
	svg.railroad-diagram {
		background-color:hsl(30,20%,95%);
	}
	svg.railroad-diagram path {
		stroke-width:3;
		stroke:black;
		fill:rgba(0,0,0,0);
	}
	svg.railroad-diagram text {
		font:bold 14px monospace;
		text-anchor:middle;
	}
	svg.railroad-diagram text.label{
		text-anchor:start;
	}
	svg.railroad-diagram text.comment{
		font:italic 12px monospace;
	}
	svg.railroad-diagram rect{
		stroke-width:3;
		stroke:black;
		fill:hsl(120,100%,90%);
	}
	svg.railroad-diagram rect.group-box {
		stroke: gray;
		stroke-dasharray: 10 5;
		fill: none;
	}

/* ]]> */
</style></svg>ading ROOT (63).svg…]()





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
