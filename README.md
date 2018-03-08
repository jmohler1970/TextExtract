

# Installation

The primary file is at `model/textextract.cfc`. The other files are used as a sample application and are NOT required for operation. This ColdFusion Component can be installed with other components.

## Working with FW/1

This ColdFusion Component is not a Service. `Setup` needs to be called in order for `getNextLineTokens()` to work.
This ColdFusion Component is not a Bean. It not backed by any database or data store.


# Functions

## Setup()

`boolean Setup(required string fileToProcess, array fixedLen = [])`

fileToProcess: Pass in a full path to the file to process. The extension will determine how it will be processed.

fixedLen: Array of cutoff points for fixed width files. Each element in the array is the width of the column. This is a required field if the text file is fixed width. This field is ignored if the the text file is non fixed width.

If the fileToProcess is successfully loaded, true is returned. Else false.

## getNextLineTokens()

`array getNextLineTokens()`

Lines in the text file are consumed one by one and an array is returned.

# Testing

Testing with SeleniumIDE can be done by opening `tests/basic.test.html`.

# 3rd Party Tools

- jQuery
- Bootstrap
- Bootswatch
- FW/1
- SeleniumIDE
