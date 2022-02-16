# Demo of Poetry Behavior

## Reproduction Steps

```
$ git clone https://github.com/kkirsche/poetry-remove-untracked.git
$ cd poetry-remove-untracked
$ git checkout before
$ poetry install --remove-untracked
$ git checkout after
$ poetry install --remove-untracked
$ ls "$(poetry env list --full-path | cut -d ' ' -f 1)/lib/python3.10/site-packages/poetry_remove"*
❯ ls "$(poetry env list --full-path | cut -d ' ' -f 1)/lib/python3.10/site-packages/poetry_remove"*
 /Users/kkirsche/Library/Caches/pypoetry/virtualenvs/poetry-remove-untracked-q73-lADw-py3.10/lib/python3.10/site-packages/poetry_remove_untracked.pth

/Users/kkirsche/Library/Caches/pypoetry/virtualenvs/poetry-remove-untracked-q73-lADw-py3.10/lib/python3.10/site-packages/poetry_remove_untracked-0.1.0.dist-info:
 INSTALLER   METADATA   RECORD

/Users/kkirsche/Library/Caches/pypoetry/virtualenvs/poetry-remove-untracked-q73-lADw-py3.10/lib/python3.10/site-packages/poetry_remove_untracked-0.2.0.dist-info:
 INSTALLER   METADATA   RECORD

```

This will show that multiple versions are installed rather than just one.
