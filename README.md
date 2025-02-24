# Uncommon HTML Bug: Accessing Property of Null Object

This repository demonstrates an uncommon bug in HTML that arises from attempting to access a property of a null object within embedded Javascript code.  The bug is subtle and can be difficult to track down because it's not directly related to HTML syntax errors.  The solution involves robust null checking before accessing object properties.

## Bug Description

The `bug.html` file contains a script that attempts to access the `innerHTML` property of an element that doesn't exist. This leads to a runtime error because `document.getElementById('nonExistentElement')` returns `null` and attempting to access a property of `null` throws a TypeError.

## Solution

The `bugSolution.html` file provides a corrected version.  It uses a conditional statement to check if the element exists before attempting to access its properties. This prevents the error and makes the code more robust.