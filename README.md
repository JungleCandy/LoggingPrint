# LoggingPrint

A Swift 2 convenience function for printing to the console only when `-D DEBUG`
is defined in the _Other Swift Flags_ setting.

The textual representation is obtained using protocol conformance, in the
following order of preference: `CustomDebugStringConvertible` and
`CustomStringConvertible`. Do not overload this function for your type. Instead,
adopt one of these protocols.

Through the magic of default function parameter values, the output contains:

- Whether the call is being made on the UI or a background thread.
- The name of the file.
- The name of the function
- The line number where the print statement is located.

## Usage

The same way as you would use a `print()` statement. 

## Installation

Just add the file to your project, and define `-D DEBUG`
in your project's _Other Swift Flags_ setting.

If you are using Carthage add this to your Cartfile

``` shell

github "JungleCandy/LoggingPrint"

```

then drag the `LoggingPrint.swift` file out of the Checkouts folder and into your project.



