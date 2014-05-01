## Plotting for publication (From Scott)

Labels in R can be annoying to figure out. Here are some code bits that may help? 

Label the value of a parameter (m) used in the plot.

```R
eval(paste("m = ", m))
```

Label the value of VLE used in plot, which is part of a list of objects in a3 (and called g in that list)
LE is subscript to V with V[LE] (superscript is ^)

```R
substitute(paste(V[LE],"=",g),a3)
```

Use italics in a label

```R
expression(paste("Strength of stabilizing selection ", italic(s)))
```

Use math symbols (see ?plotmath). 
With i subscript [i]

```R
expression(paste("Local adaptation ",bar(L)[i]))
```

With many subscripts and with greek letters

```R
expression(paste("Mean phenotype ",bar(mu)[i][,][z]))
```
