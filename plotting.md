## Plotting for publication 

### Using `ggplot`

To add 

### In R base graphics (From Scott)

Labels in R can be annoying to figure out. Here are some code bits that may help? If none of these work, you may find an answer by typing `?plotmath` at the R console prompt.

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


If you need to use a raw operator, make a valid expression of it by using NAs: 

```R
expression(NA %+-% NA)
```

Note that one can create experssions that would not make sense in R:
```R
expression("mean" %+-% "SD")
```


