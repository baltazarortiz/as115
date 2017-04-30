# as115
The as31 assembler used for MIT's 6.115 course (Microcontrollers Lab) loaded with extra preprocessing directives that makes it nicer to use.

## Using

`as115.py` located in the root folder can be used as a python script by running `python as115.py` (with the appropriate arguments). If the computer you are using does not have python installed, you can use the standalone executable located in the root folder called `as115.exe` by running `as115.exe` (also with the appropriate arguments). This executable was generated using PyInstaller, and can be generated for any platform (though this one is specifically targeted for Windows). You may find it useful to copy these two files to a directory in your `PATH`.

## Features

* Allows you to place `.inc` directive anywhere in an assembly file that tells the preprocessor to insert the contents of a given file in your assembly file. I made it so that I could distribute large projects over multiple files. Check out the files in the `Test` directory for usage.

* Allows you to place `.define` directive of the form SYMBOL, VALUE anywhere in an assembly file that tells the preprocessor to replace any future appearances of SYMBOL with VALUE, and appends a comment noting the substitution to maintain readability. While the builtin .equ directive is still more useful for numeric constants, .define allows for aliasing of specific port bits and easier aliasing of registers.

* Automatically ends your files with a newline character so as31 won't complain.

## Known Issues

* Error messages won't give the right line numbers.

## Documentation

Do `python as115.py -h` for usage. It should be identical to the usage of `as31`.
