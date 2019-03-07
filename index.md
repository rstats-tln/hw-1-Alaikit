Homework 1: ggplot2
================
Dmitri Pismennõi
2019-03-07

``` r
library(ggplot2)
```

By using *mpg* dataset:

1.  Map a continuous variable to color, size, and shape. How do these
    aesthetics behave differently for categorical vs. continuous
    variables?

<!-- end list -->

  - Color

<!-- end list -->

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, colour = cty))
```

![](index_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

  - Size

<!-- end list -->

``` r
#ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, shape = cty)) This creates an error
```

  - Shape

<!-- end list -->

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, size = cty))
```

![](index_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

2.  What happens if you map the same variable to multiple
aesthetics?

<!-- end list -->

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, colour = cty, size = cty))
```

![](index_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

3.  What does the stroke aesthetic do? What shapes does it work with?
    (Hint: use
?geom\_point)

<!-- end list -->

``` r
#Stroke controls the width of the border of certain shapes. Those shapes which have borders are the only ones that stroke can alter.
```

4.  What happens if you map an aesthetic to something other than a
    variable name, like aes(colour = displ \<
5)?

<!-- end list -->

``` r
ggplot(data = mpg) + geom_point(mapping = aes(x = displ, y = hwy, colour = displ < 5))
```

![](index_files/figure-gfm/unnamed-chunk-7-1.png)<!-- --> \`\`\`
