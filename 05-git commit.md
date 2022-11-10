# git ```commit```

Make some changes in working directory (e.g. adding test/test_file_01.txt)

```$ git status```

```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test/

nothing added to commit but untracked files present (use "git add" to track)
```

```$ git add .\test\test_file_01.txt``` or to add all changes ```$ git add .``` (or to add the files starting with test ```$ git add test*```)

```$ git status```

```
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   test/test_file_01.txt
```

```$ git commit -m "Add test file to test directory"```

```$ git log```

```
commit 717a79f0eef419fa3bd7211e1d72c8d26567f186 (HEAD -> master)
Author: Can Aytoere
Date:   Mon Oct 31 20:00:00 2022 +0100

    Add test file to test directory
```

**Shortcut** of committing all changes

```$ git commit -am "Add test file to test directory"``` 

## Multiline commit messages

```$ git commit -a``` 

```hint: Waiting for your editor to close the file...```

Then the editor will be opened, and we could provide multiline commit message there. As soon as we save and close it, it will direct back to the command line.

