## A New Family of Software Anti-Patterns: Linguistic Anti-Patterns

```
Year: 2013
Conf: European Conference on Software Maintenance and Reengineering
Cites: 10 (This is max. I found)
```

### Summary
This paper introduces the definition of software linguistic antipatterns, and defines a family of them, i.e., those related to inconsistencies: 
  + Between method signatures, documentation, and behavior, and 
  + Between attribute names, types, and comments.
![image](https://cloud.githubusercontent.com/assets/1433964/13293420/9a9e81d6-daed-11e5-928f-923768a011ec.png)

### [Datasets](http://www.ptidej.net/downloads/replications/wcre12a/OnlineExperimentsData.rar)
![image](https://cloud.githubusercontent.com/assets/1433964/13293451/bb9573ea-daed-11e5-879c-4626d7e2b90a.png)

### LAPD: Linguistic Anti-Pattern Detector
1. **Fact extraction from source code:** They use the srcml tool, which parses source code and produces an XML-based parse tree. With this step, we identify the various source code elements of interest for our analysis, namely attribute names and types, method names, etc.
2. **Analysis of source code identifiers and comments:** After having extracted terms, they perform a part of speech
analysis using the Stanford natural language parser. This allows them to: (i) identify whether a term is a noun, an adjective, an adverb or other parts-of-speech; (ii) distinguish singular from plural nouns; and (iii) identify dependencies between words, e.g., between subjects and predicates, as well as negative forms, e.g., not possible.
3. **Relating terms occurring in source code and comments:** The last part of the analysis aims at relating terms appearing in various source code elements and comments. (We can use LDA)

## Baseline results

![image](https://cloud.githubusercontent.com/assets/1433964/13294248/181263fa-daf1-11e5-9896-fc21a1ae2838.png)
