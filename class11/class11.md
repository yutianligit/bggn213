---
title: "class11"
output: 
  html_document: 
    keep_md: yes
---



##PDB statistics

Q1: What proportion of PDB entries does X-ray crystallography account for? What proportion of
structures are protein?
89.51%

```r
#import our PDB statistics CSV file and calculate percent structures by experimental method
pdbstats <- read.csv("Data Export Summary.csv", row.names = 1)
#Calculate and assign numbers with a category
percent <- (pdbstats$Total / sum(pdbstats$Total))*100
names(percent) <- row.names(pdbstats)
percent
```

```
##               X-Ray                 NMR Electron Microscopy 
##         89.51673340          8.71321614          1.51239392 
##               Other        Multi Method 
##          0.16986775          0.08778879
```



Q2: Type HIV in the search box on the home page and determine how many HIV-1 protease
structures are in the current PDB?


