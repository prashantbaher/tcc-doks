---
title: VBA Functions that do more
url: /vba/functions-that-do-more/
weight: 16
---

A few VBA `functions` go above and beyond the call of duty. Rather than simply return a value, these functions have some useful side effects. 

Below table lists them.

| Function                | What it does                                                                                                                                         |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsgBox                  | Displays a handy dialog box containing a message and buttons. The function returns a code that identifies which button the user clicks.              |
| InputBox                | Displays a simple dialog box that asks the user for some input. The function returns whatever the user enters into the dialog box.                   |
| Shell                   | Executes another program. The function returns the task ID (a unique identifier) of the other program (or an error if the function can’t start it).  |
| GetObject/CreateObject  | Returns/Create a reference to an object provided by an ActiveX component. (If you don't understand, don't bother about it. Just remember we use this function for checking & creating objects in later topics) |


---

## Discovering VBA functions

How do we find out which function does VBA provides? 

The best source is the *Visual Basic Help system* in build in your CAD Application. 

I compiled a partial list of `functions`, which I share with you in following Table. 

I omitted some of the more specialized or obscure functions. 

For complete details on a particular function, type the function name into a VBA module, move the cursor anywhere in the text, and press `F1`. 


| Function    | What is does                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------|
| Abs         | Returns a number’s absolute value.                                                            |
| Array       | Returns a variant containing an array.                                                        |
| Asc         | Converts the first character of a string to its ASCII value.                                  |
| Atn         | Returns the arctangent of a number.                                                           |
| Choose      | Returns a value from a list of items.                                                         |
| Chr         | Converts an ANSI value to a string.                                                           |
| Cos         | Returns a number’s cosine.                                                                    |
| CurDir      | Returns the current path.                                                                     |
| Date        | Returns the current system date.                                                              |
| DateAdd     | Returns a date to which a specified time interval has been added — for example, one month from a particular date. |
| DatePart    | Returns an integer containing the specified part of a given date — for example, a date’s day of the year. |
| DateSerial  | Converts a date to a serial number.                                                           |
| DateValue   | Converts a string to a date.                                                                  |
| Day         | Returns the day of the month from a date value.                                               |
| Dir         | Returns the name of a file or directory that matches a pattern.                               |
| Erl         | Returns the line number that caused an error.                                                 |
| Err         | Returns the error number of an error condition.                                               |
| Error       | Returns the error message that corresponds to an error number.                                |
| Exp         | Returns the base of the natural logarithm (e) raised to a power.                              |
| FileLen     | Returns the number of bytes in a file.                                                        |
| Fix         | Returns a number’s integer portion.                                                           |
| Format      | Displays an expression in a particular format.                                                |
| GetSetting  | Returns a value from the Windows registry.                                                    |
| Hex         | Converts from decimal to hexadecimal.                                                         |
| Hour        | Returns the hours portion of a time.                                                          |
| InputBox    | Displays a box to prompt a user for input.                                                    |
| InStr       | Returns the position of a string within another string.                                       |
| Int         | Returns the integer portion of a number.                                                      |
| IPmt        | Returns the interest payment for an annuity or loan.                                          |
| IsArray     | Returns True if a variable is an array.                                                       |
| IsDate      | Returns True if an expression is a date.                                                      |
| IsEmpty     | Returns True if a variable has not been initialized.                                          |
| IsError     | Returns True if an expression is an error value.                                              |
| IsMissing   | Returns True if an optional argument was not passed to a procedure.                           |
| IsNull      | Returns True if an expression contains no valid data.                                         |
| IsNumeric   | Returns True if an expression can be evaluated as a number.                                   |
| IsObject    | Returns True if an expression references an OLE Automation object.                            |
| LBound      | Returns the smallest subscript for a dimension of an array.                                   |
| LCase       | Returns a string converted to lowercase.                                                      |
| Left        | Returns a specified number of characters from the left of a string.                           |
| Len         | Returns the number of characters in a string.                                                 |
| Log         | Returns the natural logarithm of a number to base.                                            |
| LTrim       | Returns a copy of a string, with any leading spaces removed.                                  |
| Mid         | Returns a specified number of characters from a string.                                       |
| Minutes     | Returns the minutes portion of a time value.                                                  |
| Month       | Returns the month from a date value.                                                          |
| MsgBox      | Displays a message box and (optionally) returns a value.                                      |
| Now         | Returns the current system date and time.                                                     |
| RGB         | Returns a numeric RGB value representing a color.                                             |
| Replace     | Replaces a substring in a string with another substring.                                      |
| Right       | Returns a specified number of characters from the right of a string.                          |
| Rnd         | Returns a random number between 0 and 1.                                                      |
| RTrim       | Returns a copy of a string, with any trailing spaces removed.                                 |
| Second      | Returns the seconds portion of a time value.                                                  |
| Sgn         | Returns an integer that indicates a number’s sign.                                            |
| Shell       | Runs an executable program.                                                                   |
| Sin         | Returns a number’s sine.                                                                      |
| Space       | Returns a string with a specified number of spaces.                                           |
| Split       | Splits a string into parts, using a delimiting character.                                     |
| Sqr         | Returns a number’s square root.                                                               |
| Str         | Returns a string representation of a number.                                                  |
| StrComp     | Returns a value indicating the result of a string comparison.                                 |
| String      | Returns a repeating character or string.                                                      |
| Tan         | Returns a number’s tangent.                                                                   |
| Time        | Returns the current system time.                                                              |
| Timer       | Returns the number of seconds since midnight.                                                 |
| TimeSerial  | Returns the time for a specified hour, minute, and second.                                    |
| TimeValue   | Converts a string to a time serial number.                                                    |
| Trim        | Returns a string without leading or trailing spaces.                                          |
| TypeName    | Returns a string that describes a variable’s data type.                                       |
| UBound      | Returns the largest available subscript for an array’s dimension.                             |
| UCase       | Converts a string to uppercase.                                                               |
| Val         | Returns the numbers contained in a string.                                                    |
| VarType     | Returns a value indicating a variable’s subtype.                                              |
| Weekday     | Returns a number representing a day of the week.                                              |
| Year        | Returns the year from a date value.                                                           |
