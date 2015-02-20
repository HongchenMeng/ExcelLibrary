# ExcelLibrary

The aim of this project is to simplify reading from and writing to Excel workbooks (.xlsx). It consists of the following six classes:

* `Workbook`
* `WorkbookOptions`
* `Sheet`
* `Row`
* `Column`
* `Cell`

Here's an example to get you started:

    Workbook workbook = new Workbook();
    workbook.Open("Book1.xlsx");
    Sheet sheet = workbook.Sheet("Sheet1");
    Row row = sheet.Row(2);
    Cell cell = row.Cell(3);
    string text = cell.Value;

See the wiki for more examples.

## Limitations

The following things have been considered outside the scope of the project:

* All file formats except `.xslx`.
* Formulas
* Formatting properties

Also, the library will not create new workbooks _per se_, but this can be achieved by including a template workbook in your project and copy it whenever you need to create a workbook.

## Dependencies

The only dependency is .NET Framework 4.5. This makes ExcelLibrary very small (less than 25 kb) and easy to include in other solutions.

## Data types

The library can distinguish values of different data types (using the `Cell.Type` property).

## Querying

Most collections in the library (e.g. `Workbook.Sheets` or `Row.Cells`) is of type `IEnumerable<T>`. This allows you to use LINQ queries of unlimited complexity to find exactly what you need.

## Documentation

Since a software library is only as useful as its documentation, this library aspires to be well-documented.
