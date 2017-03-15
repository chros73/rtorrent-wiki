**TODO** clean this up, for now collect snippets

There are the `if` and `branch` commands to implement conditional execution of other commands. The difference is that `if` takes an expression for the condition, while `branch` takes a command name (and evaluates it).

The following example shows a method definition, using `if` with `(…)` syntax for its arguments:

```ini
# COMMAND: Return path to item data (never empty, unlike `d.base_path`)
method.insert = d.data_path, simple,\
    "if=(d.is_multi_file), (cat, (d.directory)), (cat, (d.directory), /, (d.name))"
```
