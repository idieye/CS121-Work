Huckfinn
========================================================

<style>
.hiword {background : pink;}
</style>

From R to HTML

```r
formatWord <- function(word, translation, class) {
    paste("<span class='", class, "' title='", translation, "'>", word, "</span>")
    # insert NA
}
```


```r
cat(formatWord("hello", "hi there", "hiword"))
```

<span class=' hiword ' title=' hi there '> hello </span>


```r
Words <- c("Mr", "Mme", "Dude", "Mlle")
Tools <- c("Mister Malthus", "Madame Cury", NA, "Mademoiselle Sall")
styles <- c("Hey Sir", "hiword", "", "Hola Demoiselle")
```



```r
for (k in 1:length(Words)) cat(formatWord(Words[k], Tools[k], styles[k]))
```

<span class=' Hey Sir ' title=' Mister Malthus '> Mr </span><span class=' hiword ' title=' Madame Cury '> Mme </span><span class='  ' title=' NA '> Dude </span><span class=' Hola Demoiselle ' title=' Mademoiselle Sall '> Mlle </span>
