# Git Stash
```
    [do some work]
    [get interrupted]
    git stash
    [deal with interruption]
    git stash pop
```
Questions:
1. What is Git Stash used for?
2. How can we choose a stash from multiple stashes?
3. For a file named "Test_File", if you firstly append a line "First change" to the file, and stash it, then you append another line "Second change", and using `git stash` again, when you use `stash pop`, by default, which content will be appended to your original file?

## Useful commands of Git Stash
```
git log --graph --all --decorate
git stash list
git stash show <ID> #e.g. git stash show stash@{0}
git stash show --patch <ID>
git stash apply <ID>
git stash drop <ID>
```

