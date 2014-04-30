Websheets
=========

Make JavaScript web applications based on Excel spreadsheets!

This project aims to combine the following technologies:

- [SheetJS/js-xlsx](https://github.com/SheetJS/js-xlsx), a library for parsing XLSX files
- [josh3ennett/excelFormulaUtilitiesJS](https://github.com/josh3ennett/excelFormulaUtilitiesJS), a library for parsing Excel formulas into JavaScript code
- [sutoiku/formula.js](https://github.com/sutoiku/formula.js), an implementation of Excel functions in JavaScript

The goal is to make it easy to interoperate spreadsheet programming and JavaScript web programming.

### API Goal

    var book = requireSheet("workbook.xlsx");
    var sheet = book["Sheet 1"]; // or book[0]
    
    // make a function that inputs values and returns the results from a different cell
    var func = makeFunction(sheet, ["A1", "A2"], "A3");
    
    func(1, 2) // 3