Categories


The Report Editor for a pivot table contains several categories you can use to help build a report.
You can add fields into the following categories:


- Rows and Columns will appear in the row and column headers of your pivot table report.

- Values will appear in the body of your pivot table.
These values will allow you to draw conclusions from data in your Row and Column categories.

- Filters allow you to hide certain data points that you don't want appear in your pivot table.

Note: You can't add the same field to multiple categories of your pivot table report because it would create duplicate calculations in the table.



Fields


A field is a subset of your data that appears in a column of your spreadsheet.
The column header is the name of the field.
Adding fields to categories in the Report Editor will populate data into your pivot table report.

To add a field:


1. Open the Report Editor in your pivot table.

2. Next to the name of a category, click Add field to see a list of all available fields.

3. Choose the field you want to add into the pivot table report.
- Once added, you can drag a field into another category.
- To remove a field, click the X in the top right of the field.
- Multiple fields can be added to each category.

4. Repeat steps 2 and 3 for each additional field. Multiple fields can be added to each category.



Calculated Fields


If you want to add a field to your pivot table that performs calculations based on other fields in your pivot table, you can add a calculated field.


1. Open the Report Editor in your pivot table.

2. Next to "Values", click Add field.
Note that calculated fields can only be added to the "Values" section of a pivot table.

3. Choose Calculated Field.

4. Next to "Name," add the name you want to use and, under "Formula," the formula for your calculation based on other fields in the pivot table.
Any fields used in the formula will be summarized using the SUM function by default, but you can use a custom function instead by switching to Custom next to "Summarize by".
If the formula for a Calculated Field includes any field names that contain spaces or other non-alphanumeric symbols, you'll need to include single quotes around that field name (e.g., = ‘Field 1’ + ‘Field 2’).