---
title: Array functions
editable: false
sourcePath: en/_api-ref/datalens/function-ref/array-functions.md
---


# Array functions


## [ARR_STR](ARR_STR.md)

**Syntax:**`ARR_STR( array [ , delimiter [ , null_str ] ] )`

Concatenates elements of the array `array` using `delimiter` as a delimiter (comma by default) and `null_str` as a null string (null items are skipped by default).

See also [STR](STR.md)



## [ARRAY](ARRAY.md)

**Syntax:**`ARRAY( value_1, value_2, value_3 [ , ... ] )`

Returns an array containing the passed values.



## [CONTAINS](CONTAINS_ARRAY.md)

**Syntax:**`CONTAINS( array, value )`

Returns `TRUE` if `array` contains `value`.



## [COUNT_ITEM](COUNT_ITEM.md)

**Syntax:**`COUNT_ITEM( array, value )`

Returns the number of elements in the array `array` equal to `value`. Type of `value` must match type of `array` elements.



## [GET_ITEM](GET_ITEM.md)

**Syntax:**`GET_ITEM( array, index )`

Returns the element with the index `index` from the array `array`. Index must be any integer. Indexes in an array begin with one.



## [SLICE](SLICE.md)

**Syntax:**`SLICE( array, offset, length )`

Returns the part of array `array` of length `length` starting from index `offset`. Indexes in an array begin with one.



## [STARTSWITH](STARTSWITH_ARRAY.md)

**Syntax:**`STARTSWITH( array_1, array_2 )`

Returns `TRUE` if `array_1` starts with `array_2`.



## [UNNEST](UNNEST.md)

**Syntax:**`UNNEST( array )`

Expands the `array` array expression to a set of rows.


