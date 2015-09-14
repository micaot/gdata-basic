# gdata-basic

This code makes use of the Google API for retrieve the data from a Google Spreadsheet in the JSON format by using JSONP. Once the data are in this format, we will be able to manage them by means a callback function.

It is necessary to make the spreadsheet pubic by its configuration. 

The process follows two steps:

1. Execute the function to load the data in JSON format.
2. Execute the callback function.

The spreadsheet id is in its URL:

https://docs.google.com/spreadsheets/d/the-spreadsheet-id/edit#gid=0

The worksheet id is always "od6" for the first worksheet.

The first step is performed by running a script that is called in the following URL:

https://spreadsheets.google.com/feeds/cells/the-spreadsheet-id/od6/public/values?alt=json-in-script&callback=callback_function

URL in the response function is specified to run immediately, once the data is obtained in JSON format.

callback_function (json) {
// Process the JSON data
}
