# Table Generation Scripts

Contained here are 5 scripts used to generate tables for the wiki.

commonElements.js contains functions and classes that create common wiki elements

keyFormatters.js contains functions to format the properties of objects contained within the various arrays in the game's source.

selectionFunctions.js contains functions that return a boolean value to serve as a condition to extract subsets from object arrays

sortFunctions.js contains functions to be used with the Array.Sort method to sort object array subsets.

tableMakers.js contains functions which generate tables and some pages for the wiki.

## Process for creating a new table:

1. Create a subset of an object array in the game using getObjectArraySubset. (Optional if using the whole array)
2. Sort the array if neccesarry using Array.Sort (Optional if array is already sorted correctly)
3. Create a new tableSpecMaker object and use appendColumn to specify the columns of the table.
4. Feed the sorted array subset and the tableSpec property of your tableSpecMaker into formatObjectArrayAsTable function.
5. Return the string generated by formatObjectArrayAsTable.