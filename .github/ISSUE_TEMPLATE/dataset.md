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

Please provide the `typeof()` each `column` present in the `dataset` and a brief `definition`, in the format of r2dii's [`data_dictionary`](https://2degreesinvesting.github.io/r2dii.dataraw/reference/data_dictionary.html). You may attach a .csv file or create a `tibble::tribble()` ([`create_data_dictionary()`](https://2degreesinvesting.github.io/r2dii.dataraw/reference/data_dictionary.html) may help). For example:

```
tibble::tribble(
  ~dataset,   ~column,                 ~typeof,     ~definition,
  "loanbook", "id_loan",               "character", "Unique loan identifier",
  "loanbook", "loan_size_outstanding", "double",    "Amount drawn by borrower from total credit limit"
)
```
