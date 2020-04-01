---
name: Dataset
about: Request a dataset
title: ''
labels: dataset
assignees:

---

### Describe the dataset

A concise decsription of the purpose of this dataset. Please be careful to consider cross-over between already existing datasets in this repository. 

### Additional context

[Add screenshots](https://help.github.com/en/articles/file-attachments-on-issues-and-pull-requests) or any other context about the dataset here.

### Data dictionary entry

Please provide the `typeof()` each `column` present in the `dataset` and a brief `definition`, in the format of r2dii's `data_dictionary` using [this](https://docs.google.com/spreadsheets/d/1af4Q7gd7e-Msc7uyUbDEEfb04T_N_q1rzkhqKYSQeX4/edit?ts=5da860c1#gid=0) google sheet as a template. 

### Checklist for developers checklist to add `newdata`

[`?r2dii.usethis::use_r2dii_data()`](https://2degreesinvesting.github.io/r2dii.usethis/reference/use_r2dii_data.html)

* [ ] Add "data-raw/newdata.csv" 
* [ ] Add "data-raw/data_dictionary/newdata.csv" 
* [ ] In "data-raw/newdata.R", add something like: 
  ```
  # Source: @<contributor> <URL to issue or pull request>
  newdata <- readr::read_csv(here::here("data-raw", "newdata.csv"))
  use_data(newdata, overwrite = TRUE)
  ```
* [ ] `usethis::use_r("newdata")`. Document `newdata` 
* [ ] `usethis::use_test("newdata")`. Add regression tests of `newdata` 
* [ ] `source("data-raw/data_dictionary.R"); devtools::load_all()` 
* [ ] `usethis::use_test("data_dictionary")`. Test `data_dictionary` includes `newdata` 
