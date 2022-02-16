# Demo of Poetry Behavior

## Reproduction Steps

```
$ git clone ...
$ cd poetry-remove-untracked
$ git checkout before
$ poetry install --remove-untracked
$ git checkout after
$ poetry install --remove-untracked
$ ls "$(poetry env list --full-path | cut -d ' ' -f 1)/lib/python3.10/site-packages/poetry_remove"*
```

This will show that multiple versions are installed rather than just one.
