---
title: Declaring and Scoping of Variables
url: /vba/declaring-and-scoping-of-variables/
weight: 8
---

If you read the previous topics, you now know a bit about 🚀**[Variables](/vba/variables) and [Data-types](/vba/programming-concepts#data-types-in-vba)**.

In this topic, you discover how to **declare** a `variable` as a certain *data type*.

If you don’t *declare* the *data type* for a `variable` you use in a `VBA routine`, `VBA` uses the default data type: `Variant`.

*Data stored* as a `Variant` acts like a **chameleon**; it changes type depending on what you do with it.

For example, if a *variable* is a `Variant` data type and contains a text string that looks like a number (such as “123”), you can use this *variable* for `string` manipulations as well as `numeric` calculations.

`VBA` automatically handles the conversion. Letting `VBA` handle data types may seem like an easy way out — but remember that you sacrifice speed and memory.

Before you use *variables* in a `procedure`, it’s an excellent practice to *declare* your variables — that is, tell `VBA` each variable’s data type.

Declaring your *variables* makes your program run **faster** and use memory *more efficiently*.

The default *data type*, `Variant`, causes `VBA` to repeatedly perform time consuming checks and reserve more memory than necessary.

If `VBA` knows a *variable’s data type*, it doesn’t have to investigate and can reserve just enough memory to store the data.

To force yourself to declare all the variables you use, include the following as the first statement in your `VBA` module:

```vb
Option Explicit
```

When this *statement* is present, you won’t be able to run your code if it contains any undeclared *variables*.

You need to use `Option Explicit` only once: at the *beginning* of your module, prior to the declaration of any procedures in the module.

Keep in mind that the `Option Explicit` statement applies only to the module in which it resides.

If you have more than one `VBA` module in a **project**, you need an `Option Explicit` statement for each module.

Suppose that you use an *undeclared variable* (that is, a `Variant`) named `myDimension`.

At some point in your routine, you insert the following statement:

```vb
myDimnsion = 11
```

This misspelled *variable*, which is difficult to spot, will probably cause your routine to give incorrect results.

If you use `Option Explicit` at the beginning of your module (forcing you to declare the `myDimension` variable), `VBE` generates an error if it encounters a misspelled variation of that variable.

To ensure that the `Option Explicit` statement is inserted automatically whenever you insert a new `VBA` module; turn on the *Require Variable Definition option*.

You find it in the **Editor tab** of the **Options dialog box** (in the VBE, choose **Tools -> Options**).

{{< callout context="note" title="Note" icon="outline/info-circle" >}}

> I highly recommend doing so.

{{< /callout >}}

Declaring your variables also lets you take advantage of a shortcut that can save some typing.

Just type the first two or three characters of the variable name, and then press `Ctrl + Space`.

The `VBE` will either complete the entry for you or — if the choice is ambiguous — show you a list of matching words to select from.

In fact, this slick trick works with *reserved words* and *functions*, too.

You now know the advantages of declaring *variables*, but how do you do this?

The most common way is to use a `Dim` statement.

Here are some examples of variables being declared:

```vb
Dim YourName as String
Dim PartLength as Long
Dim bRet as Boolean
Dim X
```

The first *three* variables are declared as a specific *data type*.

The last variable, **X**, is not declared as a specific *data type*, so it’s treated as a `Variant` (it can be anything).

Besides `Dim`, `VBA` has *three* other keywords that are used to declare variables:

* Static
* Public
* Private

I explain more about the `Dim, Static, Public`, and `Private` keywords later on, but first I must cover two other topics that are relevant here: **a variable’s scope** and **a variable’s life**.

Recall that your code can have any number of `VBA modules` and a `VBA module` can have any number of `Sub` and `Function` procedures. 

A variable’s scope determines which modules and procedures can use the variable. 

Below Table describes the scopes:

### VBA’s Variable’s Scope

| Scope                        | How the Variable is Declared                                                                                      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------|
| Procedure only              | By using a **Dim** or a **Static** statement in the procedure that uses the variable.                              |
| Module only                 | By using a **Dim** or a **Private** statement before the first **Sub** or **Function** statement in the module.     |
| All procedures in all modules | By using a **Public** statement before the first **Sub** or **Function** statement in the module.                   |

If you get confused keep reading next post on these topics.

Next post will be about ***Variable Scope***.
