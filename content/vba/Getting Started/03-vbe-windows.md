---
title: VBE Windows
url: /vba/vba-windows/
weight: 3
---

In this post we look at the following windows in `Visual Basic Editor`:

1. Project Window
2. Code Window

## Project Window

When you are working in `VBE`, each file open is called a Project.  
You can think of a `project` as a `collection` of objects.

You can *expand* a project by clicking the plus sign (+) at the left of the project’s name in the Project window.

*Contract* a project by clicking the minus sign (-) to the left of the project’s name in the Project window. Or you can simply *double-click* the items to expand or contract them.

Every project expands to show at least one node. In our previous image we have `SOLIDWORKS Objects`. This node expands to show an item for Solidworks application.

If the project has any `VBA` module, the project listing also shows a `Module node`.

A project can also contain a node called `Forms`, which contains `UserForm objects` (which hold custom dialog boxes).

The concept of `Object` may not be clear to you at this moment. However, things become much clearer in subsequent topics.

Don’t be too concerned if you don’t understand what’s going on at this point.

### Adding a New VBA Module

Follow the steps below to add a new VBA module to a project:

1. Select the project's name in the Project Window.
2. Select **Insert → Module**.

or

1. Right-click the project’s name.
2. Select **Insert → Module** from the shortcut menu.

When you record a macro or create a blank macro, `Solidworks` automatically adds a module to hold the code.

### Removing a VBA Module

If you want to remove a module from the Project window, follow the steps below:

1. Select the module's name in the Project Window.
2. Select **File → Remove**.

Or

1. Right-click the module’s name.
2. Select **Remove** from the shortcut menu.

`VBE` always tries to keep you from doing something that you will regret, hence it will ask if you want to export the code in the module before deleting the code.

And in most cases, you don’t want to export. If you do want to export the code, please see the next section.

### Exporting and Importing Objects

Every object in a `VBA project` can be saved to a separate file. Saving an individual object in a project is known as **exporting**.

The reason for exporting a file is that you can also **import** objects into a project.

Exporting and importing objects might be useful if you want to use a particular object (such as a VBA module or a UserForm) in a different project.

Below are the steps to export an object:

1. Select an object in the Project window.
2. Select **File → Export File** or press `Ctrl + E`.

You get a dialog box that asks for a filename. Note that the object remains in the original project; only a copy of the object is exported.

Importing an object is also a similar process, which is shown below:

1. Select the project’s name in the Explorer window.
2. Select **File → Import File** or press `Ctrl + M`.

You get a dialog box that asks for a file. Locate the file and click open.

You should only import a file if it was exported by using the **File → Export File** command.

## Code Window

As you become proficient with `VBA`, you spend a lot of time working in the `Code window`.

Macros that you record are stored in a module, and you can type `VBA code` *directly* into a VBA module.

### Minimize and Maximize Code Windows

If you have several projects open, the `VBE` may have lots of Code windows at any given time. Below is an example of this.

![Visual-basic-editor](2.Example_of_Many_code_window.PNG)

`Code windows` are much like your files opened in `Solidworks`. You can minimize them, maximize them, resize them, hide them, and so on.

Most people find it much easier to *maximize* the `code window` that they are working on. Doing so lets you see more code and keeps you from getting distracted.

To maximize the `Code window`, click the maximize button in its *title bar* or just *double-click* the title bar of the Code window to maximize it.

To restore a window to its original size, click the restore button. When the Code window is maximized, its title bar is not visible, so you will find the restore below the `VBE title bar`.

Sometimes you want to have two or more `Code windows` visible.

For example, you may want to compare the code in two modules or copy code from one module to another.

You can arrange the windows manually, or use the **Window → Tile Horizontally** or **Window → Tile Vertically** command to arrange them automatically.

You can quickly switch among code windows by pressing `Ctrl + Tab`. If you repeat that key combination, you keep cycling through all the open code windows.

Pressing `Ctrl + Shift + Tab` cycles through the windows in reverse order.

Minimizing a window gets it out of the way. You can also click the window close button in a Code window’s title bar to close the window completely. (Closing a window just hides it; you won’t lose anything.)

To open it again, just double-click the appropriate object in the Project window. Working with these Code windows sounds more difficult than it really is.

### Creating a Module

In general, a `VBA module` can hold **three** types of code:

1. **Declaration**: One or more information statements that you provide to `VBA`. For example, you can declare the data type for variables you plan to use, or set some other module-wide options.
2. **Sub procedures**: A set of programming instructions that perform some actions.
3. **Function procedures**: A set of programming instructions that return a single value.

A single `VBA module` can store any number of `Sub procedures`, `Function procedures`, and `declarations`.

Well, there is a limit – about 64,000 characters per module. It is very rare that anybody reaches that limit, but if someone does, the solution is simply to insert a new module.

How you organize a `VBA module` is totally up to you. Some people prefer to keep all their VBA code in a *single module*; others (like me) like to split up the code into `several different modules or even classes`. It is a personal choice, like arranging furniture.

### Inserting VBA Code into a Module

An empty `VBA module` is like the **fake** food you see in advertisements. It looks good but it does not really do much.

Before you can do anything meaningful, you must have some `VBA code` in the `VBA module`. You can insert VBA code into a VBA module in three ways:

1. Insert code directly into the code window.
2. Use the macro recorder to record your actions and convert them into VBA code.
3. Copy the code from one module and paste it into another module.

### Entering Code Directly into a Module

Sometimes the best route is the most `direct one`. Entering the `code directly` involves typing the code via your keyboard.

Entering and editing text in a VBA module works as you might expect. You can select, copy, cut, paste, and do other things as you do in other word processing software.

Use the `Tab` key to indent some of the lines to make your code easier to read. This is not necessary, but it is a good habit to acquire.

As you go through, you will understand why indenting code lines is helpful.

A single line of `VBA code` can be as long as you like.

However, you may want to use the `line-continuation` character to break up a lengthy line of code.

To continue a single line of code (also known as a `statement`) from one line to the next, end the first line with a space followed by an underscore (`_`). Then continue the `statement` on the next line.

Below is an example of a single statement split into two lines:

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
set swPart = swApp.NewDocument(swApp.GetUserPreferenceStringValue _
    (swUserPreferenceStringValue_e.swDefaultTemplatePart),0,0,0)
```

{{< /tab >}}
{{< /tabs >}}

This statement would perform the same way if it were entered in a single line (with no continuation characters).

Notice that I indented the second line of the statement. Indenting is optional but it clarifies the fact that these lines are not separate statements.

{{< callout context="note" title="Note" icon="outline/info-circle" >}}
If you are wondering what the above statement does, then the answer is: it opens a new part with the `default part template` in *SolidWorks*. This code is ***not*** inserted using the macro recorder; instead, I wrote it manually to find a default part template and use that template to open a new part.
{{< /callout >}}

The engineers who designed `VBE` knew that people like us would be making mistakes. Therefore, the VBE has multiple levels of Undo and Redo.

If you deleted a statement that you should not have, use the **Undo** button on the toolbar (or press `Ctrl+Z`) until the statement shows up.

After undoing, you can use the **Redo** button to perform the changes you have undone. This redo/undo stuff is much like you use in other software. Until you use it, you cannot understand.

Ready to enter some `live code`? Try the following steps:

1. Go to your VBE.
2. Double-click your module if it is not open.
3. Go to the Code Window.
4. Type the following code into the `Code window`:

{{< tabs "vba-code" >}}
{{< tab "vba" >}}

```vb {lineNos=true lineNoStart=1}
Sub GuessName()
    Msg = "Is this a CAD Software?"
    Ans = MsgBox(Msg, vbYesNo)
    If Ans = vbNo Then MsgBox "Oh, that’s fine."
    If Ans = vbYes Then MsgBox "You must be joking!"
End Sub
```

{{< /tab >}}
{{< /tabs >}}

5. Make sure the cursor is located anywhere within the text you typed, and then press `F5` to execute the procedure.

`F5` is a shortcut for the **Run → Run Sub/UserForm** command.

If you entered the code correctly, `VBE` will execute the procedure, and you can respond to the simple dialog box as shown in the figure below.

![Visual-basic-editor](3.Guess_Name_Dialog_box.PNG)

When you enter the code listed in `step 4`, you might notice that the `VBE` makes some adjustments to the text you enter.

For example, after you type the `Sub` statement, the `VBE` automatically inserts the `End Sub` statement, and if you omit the space before or after an equal sign, the `VBE` inserts the space for you.

Also, the `VBE` changes the color and capitalization of some text. This is all perfectly normal. It is just VBE’s way of keeping things neat and readable.

If you followed the previous steps, you just wrote a `VBA Sub procedure`, also known as a `macro`.

When you press `F5`, VBE executes the code and follows the instructions.

In other words, VBE evaluates each statement and does what you told it to do.

This simple macro uses the following concepts:

- Defining a Sub procedure (the first line).
- Assigning values to variables (`Msg` and `Ans`).
- Using a built-in VBA function (`MsgBox`).
- Using built-in VBA constants (`vbYesNo`, `vbNo`, and `vbYes`).
- Using an If-Then construct (twice).
- Ending a Sub procedure (the last line).

### Using the Macro Recorder

Another way you can get code into a `VBA module` is by recording your actions, using the in-built `macro recorder`.

By the way, there is absolutely **no way** you can record the `GuessName` procedure shown in the preceding section.

You can record only things that you can do directly in *Solidworks*.

Displaying a message box is not in the application's normal repertoire. The macro recorder is useful, but in many cases, you’ll probably need to enter at least some code manually.

We have already seen how macros are recorded. So there is no need for us to go over the same thing twice. If you want to see how it is done, go to [VBA in Solidworks topic](/solidworks-macros/vba-in-solidworks).

### Copying VBA Code

The final method for getting `code` into a `VBA module` is to copy it from another module or from some other place (such as a website, e.g., Solidworks forum).

For example, a `Sub or Function procedure` that you write for one project might also be useful in another project.

Instead of *wasting time* `re-entering` the code, you can activate the module and use the normal Clipboard copy-and-paste procedures.

After pasting it into a `VBA module`, you can modify the code if necessary.

You’ll also find lots of VBA code examples on the web.

If you’d like to try them, select the code in your browser and press `Ctrl+C` to *copy* it. Then, activate a module and press `Ctrl+V` to *paste* it.

Next post will be about `Sub and Function Procedures`.
