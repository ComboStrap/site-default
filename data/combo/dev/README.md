# Dev


## About
This repository is used to develop and test the [.gitignore](../../../.gitignore) file.



## Test

* The following should return nothing as the path should be not ignored.
```bash
cat data/combo/dev/gitignore_included.txt | git check-ignore --stdin
```

* The following diff should return nothing. `git check-ignore` should return all path as they should be excluded. 
```bash
diff <(cat data/combo/dev/gitignore_excluded.txt) <(cat data/combo/dev/gitignore_excluded.txt | git check-ignore --stdin)
```
