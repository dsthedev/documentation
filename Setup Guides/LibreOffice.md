# LibreOffice

## Calc

* Turn off Automatic URL Recognition: `Tools > AutoCorrect > Options` and uncheck *"URL Recognition"*
* Add "zebra" striping to rows or columns:
  * Create your styles first, then add them with `Format > Styles > New Style` using unique and semantic names
  * Highlight the rows desired to stripe and go to `Format > Conditional Formatting > Conditional`
  * Use the following in combination for simple striping:
    * `ISODD()` or `ISEVEN()`
    * `ISROW()` or `ISCOLUMN()`
    * **Example**:  `ISODD(ROW())` to apply a style to every other row, starting with the first selected
* Use top cell in columns as filter dropdowns: `Data > Autofilter`


