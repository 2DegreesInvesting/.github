---
name: Dataset
about: Request a dataset
title: ''
labels: dataset
assignees:

---

### Describe the dataset

A concise decsription of the purpose of this dataset.

### Is this object indivisable?

Can this object be created by combining several already existing objects? If so, should this be a feature request instead?

### Additional context

[Add screenshots](https://help.github.com/en/articles/file-attachments-on-issues-and-pull-requests) or any other context about the dataset here.

### Data dictionary entry

Please provide a brief `definition` of each `column` present in the `dataset`, in the format of r2dii's [`data_dictionary`](https://2degreesinvesting.github.io/r2dii.dataraw/reference/data_dictionary.html).

For example:

``` r
new_dataset <- tibble::tribble(
  ~dataset,   ~column,          ~definition,              ~typeof,
  "loanbook", "id_loan",        "Unique loan identifier", "character",
  "loanbook", "another_column", "Another definition",     "`typeof(column)`",
)

new_dataset
#> # A tibble: 2 x 4
#>   dataset  column         definition             typeof          
#>   <chr>    <chr>          <chr>                  <chr>           
#> 1 loanbook id_loan        Unique loan identifier character       
#> 2 loanbook another_column Another definition     `typeof(column)`
```
