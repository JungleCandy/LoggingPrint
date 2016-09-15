# LoggingPrint

A Swift . convenience function for printing to the console only when the build setting for "Active Complilation
Conditions" (SWIFT_ACTIVE_COMPILATION_CONDITIONS) defines `DEBUG`

The textual representation is obtained from the `object` using `String(reflecting:)` which works for _any_ type. To
provide a custom format for the output make your object conform to `CustomDebugStringConvertible` and provide your
format in the `debugDescription` parameter.

Through the magic of default function parameter values, the output contains:

- Whether the call is being made on the UI or a background thread.
- The name of the file.
- The name of the function
- The line number where the print statement is located.

## Requirements

The latest version requires Swift 3.0 and Xcode 8.

## Usage

The same way as you would use a `print()` statement. 

## Installation

Just add the file to your project, and define `DEBUG` in your project's _Active Complilation Conditions_ setting.

If you are using Carthage add this to your Cartfile

``` shell

github "JungleCandy/LoggingPrint" >= 2.0

```

then drag the `LoggingPrint.swift` file out of the Checkouts folder and into your project.



