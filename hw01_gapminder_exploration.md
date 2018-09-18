In this assignment, I am exploring the gapminder data frame used in the
class.

### Loading data frame

    library(gapminder)

### Exploring data frame

*str()* and *summary()* commands provide an overview of the data frame

    str(gapminder)

    ## Classes 'tbl_df', 'tbl' and 'data.frame':    1704 obs. of  6 variables:
    ##  $ country  : Factor w/ 142 levels "Afghanistan",..: 1 1 1 1 1 1 1 1 1 1 ...
    ##  $ continent: Factor w/ 5 levels "Africa","Americas",..: 3 3 3 3 3 3 3 3 3 3 ...
    ##  $ year     : int  1952 1957 1962 1967 1972 1977 1982 1987 1992 1997 ...
    ##  $ lifeExp  : num  28.8 30.3 32 34 36.1 ...
    ##  $ pop      : int  8425333 9240934 10267083 11537966 13079460 14880372 12881816 13867957 16317921 22227415 ...
    ##  $ gdpPercap: num  779 821 853 836 740 ...

    summary(gapminder)

    ##         country        continent        year         lifeExp     
    ##  Afghanistan:  12   Africa  :624   Min.   :1952   Min.   :23.60  
    ##  Albania    :  12   Americas:300   1st Qu.:1966   1st Qu.:48.20  
    ##  Algeria    :  12   Asia    :396   Median :1980   Median :60.71  
    ##  Angola     :  12   Europe  :360   Mean   :1980   Mean   :59.47  
    ##  Argentina  :  12   Oceania : 24   3rd Qu.:1993   3rd Qu.:70.85  
    ##  Australia  :  12                  Max.   :2007   Max.   :82.60  
    ##  (Other)    :1632                                                
    ##       pop              gdpPercap       
    ##  Min.   :6.001e+04   Min.   :   241.2  
    ##  1st Qu.:2.794e+06   1st Qu.:  1202.1  
    ##  Median :7.024e+06   Median :  3531.8  
    ##  Mean   :2.960e+07   Mean   :  7215.3  
    ##  3rd Qu.:1.959e+07   3rd Qu.:  9325.5  
    ##  Max.   :1.319e+09   Max.   :113523.1  
    ## 

Data frames can consists of lists of different data types(as can be seen
in output of *str(gapminder)*). To extract and explore a single variable
from a data frame **$** sign can be used.

    table(gapminder$continent)

    ## 
    ##   Africa Americas     Asia   Europe  Oceania 
    ##      624      300      396      360       24

#### Dimensions:

    dim(gapminder)

    ## [1] 1704    6

    ncol(gapminder)

    ## [1] 6

    nrow(gapminder)

    ## [1] 1704

### Data Visualization

Also, we can plot using R markdown for improved data visualization

    barplot(table(gapminder$continent))

![](hw01_gapminder_exploration_files/figure-markdown_strict/unnamed-chunk-5-1.png)

    plot(lifeExp~year,gapminder)

![](hw01_gapminder_exploration_files/figure-markdown_strict/unnamed-chunk-5-2.png)
