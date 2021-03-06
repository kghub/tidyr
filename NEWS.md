# tidyr 0.2.0.9000

* `expand_` does SE evaluation correctly so you can pass it a character vector
  of columns names (or list of formulas etc) (#70).

# tidyr 0.2.0

## New functions

* Experimental `expand()` function (#21).

* Experiment `unnest()` function for converting named lists into
  data frames. (#3, #22)

## Bug fixes and minor improvements

* `extract_numeric()` preserves negative signs (#20).

* `gather()` has better defaults if `key` and `value` are not supplied.
  If `...` is ommitted, `gather()` selects all columns (#28). Performance
  is now comparable to `reshape2::melt()` (#18).

* `separate()` gains `extra` argument which lets you control what happens
  to extra pieces. The default is to throw an "error", but you can also
  "merge" or "drop".

* `spread()` gains `drop` argument, which allows you to preserve missing
  factor levels (#25). It converts factor value variables to character vectors, 
  instead of embedding a matrix inside the data frame (#35).
