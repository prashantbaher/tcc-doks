---
title: VBA Arrays
url: /vba/arrays/
weight: 14
---

Most programming languages support `arrays`. An *array* is a group of variables that share a common name. 

You refer to a *specific variable* in the `array` by using the *array name* and an *index number* in *parentheses*. 

For example, you can define an array of 12 string variables to hold the names of the months of the year. 

If you name the array `MonthNames`, you can refer to the first element of the array as `MonthNames(1)`, the second element as `MonthNames(2)`, and so on. 

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Dim MonthNames("Jan", "Feb", "Mar", "April", "May", "Jun", "July", "Aug", "Sep", "Oct", "Nov", "Dec") As string
print(MonthNames(1))    'print Feb
```

{{< /tab >}}
{{< /tabs >}}

## Declaring Arrays

Before you can use an `array`, you must declare it. No exceptions. 

Unlike normal *variables*, VBA is very strict about this rule. 

You declare an array with a `Dim` or `Public` statement, just as you declare a regular variable. 

However, you also need to specify the number of elements in the array. 

You do this by specifying the *first index number*, the keyword To, and the last index number — all inside parentheses. 

The following example shows how to declare an array of **100 integers**: 

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Dim MyArray(1 To 100) As Integer
```

{{< /tab >}}
{{< /tabs >}}

When you declare an `array`, you can choose to specify only the *upper index*. 

VBA assumes that 0 is the *lower index*. Therefore, both of the following statements declare the same *101-element* array: 

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Dim MyArray(0 To 100) As Integer
Dim MyArray(100)
```

{{< /tab >}}
{{< /tabs >}}

{{< callout context="note" title="Note" icon="outline/info-circle" >}}

If you want VBA to assume that **1** (rather than **0**) is the *lower index* for your arrays, include the following statement in the Declarations section of your module: 

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Option Base 1
```

{{< /tab >}}
{{< /tabs >}}

This statement forces VBA to use **1** as the first index number for arrays that declare only the *upper index*. 

If above statement is present, the following statements are identical, both declaring a 100-element array: 

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Dim MyArray(1 To 100) As Integer
Dim MyArray(100)
```

{{< /tab >}}
{{< /tabs >}}

{{< /callout >}}

There are two other arrays

* Multi-dimensional array

* Dynamic array

But I don’t think these two are that much useful for us to learn hence we **will not** delve into them.

Next post will be about ***VBA Functions***.
