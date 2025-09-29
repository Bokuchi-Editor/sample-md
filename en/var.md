<!-- @var title: Local Variable Test -->
<!-- @var author: Test User -->
<!-- @var date: 2025-09-10 -->
<!-- @var version: 1.0.0 -->

# {{title}}

This document is a test of the local variable feature.

## Basic Information

- **Author**: {{author}}
- **Date**: {{date}}
- **Version**: {{version}}

## Comparison with Global Variables

By going to [Settings] > Global Variables > Add New Variable
and setting "Variable Name" = globalVar, "Value" = Global,
the following display will change in the preview with variables applied.

Value set by global variable: **{{globalVar}}**

## Priority of Local Variables

Local variables take precedence over global variables.
Try registering a global variable and see if the following display changes.
Also, try deleting the variable declaration at the beginning and see if the display changes.

Local variable `title` value: {{title}}
Local variable `author` value: {{author}}
