# UFOs
Module 11

## Overview of the project:
The purpose of this project was to help Dana build a dynamic webpage where users can filter the data table. In addition to the `date`, we added more filters for the `city`, `state`, `country` and `shape`.

## Results:
•	First, we removed the filter `button` from the `index.html` file and added four new items to the unordered list `<ul/>`.

![unordered_list](Resources/unordered_list.png)

•	Next, in the JavaScript app, we created an empty variable `var filters = {};` to hold the changed element in the filters.
•	We then inserted an event listener using `d3` to check for changes in the input placeholder just before the `buildTable(tableData);` function.
o	`d3.selectAll("input").on("change", updateFilters);`
•	We modified the `updateFilters()` function, by first creating a variable for the changed element using `d3.select(this)`, then saving the value of those element into a new variable. We also saved the id of the modified filters to a variable and used an if-else statement to use or not each filters.

![updateFilters](Resources/updateFilters.png)

•	Lastly, we rebuilt the filtered table with a loop that check for matching key: values. 

![filterTable](Resources/filterTable.png)

In the new webpage, a user can enter between one and five search criteria, and the table will be return with the filtered results as the example below.

![table_example](Resources/table_example.png)

## Summary:
•	In a summary, this new table is working properly but to clear the filters, we must either delete all entry and press `ENTER` or go back up to the top of the page to refresh the page by clicking on UFO sightings. 
•	To improve this page, we could add a `CLEAR` button close to the filters.
•	Also, I did not like the label and placeholder on the same line as it made everything not aligned, so I reduced the size from `col-md-3` to `col-md-2`. The same works for large screen, but it does not work for mobile device. The code `col-xs-2` or `col-sm-2` did not squeezed the filters to force the placeholder below the label. We would need to work on other alignment methods, which might be what was done in the module since the final picture of the table shows placeholders below the label despite using `col-md-3`.
