:arrow_left: Back to [[Commands Reference|Scripting-Guide#commands-reference]]

**TODO** clean this up, for now collect snippets

There are the `if` and `branch` commands to implement conditional execution of other commands. The difference is that `if` takes argument expressions, while `branch` takes a command list and then does its own evaluation.

The following example shows a method definition, using `if` with `(…)` syntax for its arguments:

```ini
# COMMAND: Return path to item data (never empty, unlike `d.base_path`);
#          multi-file items return a path ending with a '/'. 
method.insert = d.data_path, simple,\
    "if=(d.is_multi_file),\
        (cat, (d.directory), /),\
        (cat, (d.directory), /, (d.name))"
```