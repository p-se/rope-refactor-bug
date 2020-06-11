# How to reproduce

Open project and file `main.py`. Try to refactor function `foo` and give it another name.

## Result

```text
Refactor failed. Syntax error in file <other_file.py> line <1>: Missing parentheses in call to 'print'. Did you mean print("asdf")?
[<FrameSummary file /home/user/.vscode/extensions/ms-python.python-2020.5.86398/pythonFiles/refactor.py, line 382 in watch>, <FrameSummary file /home/user/.vscode/extensions/ms-python.python-2020.5.86398/pythonFiles/refactor.py, line 348 in _process_request>, <FrameSummary file /home/user/.vscode/extensions/ms-python.python-2020.5.86398/pythonFiles/refactor.py, line 260 in _rename>, <FrameSummary file /home/user/.vscode/extensions/ms-python.python-2020.5.86398/pythonFiles/refactor.py, line 129 in refactor>, <FrameSummary file /home/user/.vscode/extensions/ms-python.python-2020.5.86398/pythonFiles/refactor.py, line 157 in onRefactor>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/refactor/rename.py, line 97 in get_changes>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/refactor/rename.py, line 195 in rename_in_module>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/refactor/occurrences.py, line 76 in find_occurrences>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/utils/__init__.py, line 12 in _wrapper>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/refactor/occurrences.py, line 392 in source_code>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/utils/__init__.py, line 12 in _wrapper>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/refactor/occurrences.py, line 412 in pymodule>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/project.py, line 116 in get_pymodule>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/pycore.py, line 142 in resource_to_pyobject>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/pycore.py, line 254 in get_pymodule>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/pyobjectsdef.py, line 162 in __init__>, <FrameSummary file /home/user/.local/lib/python3.8/site-packages/rope/base/pyobjectsdef.py, line 191 in _init_source>]
```

## Expected behavior

The refactoring should have been completed successfully as `other_file.py` is
excluded in `settings.json` and not visible in the Explorer nor find- and
openable using Ctrl+P.

```json
{
  "files.exclude": {
    "other_file.py": true
  }
}
```
