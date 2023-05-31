# Preparation of data for the modelling

## Initial steps

  - Read data into R
  - Remove practice blocks
  - Rename malformed column names
  - Clean malformed value strings
  - Recode salience factors to short form
  - Remove unused columns
  - Convert Correct column to logical type
  - Categorise trials into types (both (both attrs satisfy criteria),
    neither (neither attr satisfies criteria), psing (price only
    satisfies criteria) and rsing (rating only satisfies criteria))
  - Add Accept column (did they accept the hotel)
  - Rename and remove columns
  - Change subject\_id to factor

## Filtering data

  - Remove all rows with NA values (Only trials where there was no
    response)
  - Remove all subjects that have less than 80% correct responses in
    each of the four trial types listed above (both, psing, rsing,
    neither)
  - Filter the rows to only select ones where the rule being applied was
    to accept if both attrs were suitable
  - Save the data to disk

## Prior to model fitting

After reading in the previously saved data, but before fitting a few
more changes are made to the data, namely:

  - New rt column which is previous RT/1000 (is Response time in
    seconds, not milliseconds)
  - Rename subject\_id to subject
  - accept column is logical Accept column with 1 added (Accept == 2,
    Reject == 1) - needed for rtdists
  - Decaptialise Price and Rating column names
  - Add columns to hold the names of drift parameters to be used for
    each attr/response combination, helper for the log likelihood
    methods)
