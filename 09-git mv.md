# Move and rename files

There are two techniques for moving and renaming files - very similar to deleting files.

## Alternative #1

For the first, we're going to make changes to the file name directly in the operating system, not through the command line. Suppose that we have changed "test_file.txt" to "renamed_file.txt"

```$ git status```

```
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    test_file.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        renamed_file.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

It's listing the operation as two separate events, it's not linking them together as being a rename. So let's add both of these to staging, as if we're going to commit them. 

```$ git rm test_file.txt```

```$ git add renamed_file.txt```

```$ git status```

```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    test_file.txt -> renamed_file.txt
```  
        
Git recognizes that these two files are similar. Now that they both are in the staging tree together it recognizes that the files are pretty similar. Now, we're pretty much ready to proceed with committing the changes.

## Alternative #2

The second one like when we're deleting files, we can do directly from the command line. Moving a file and renaming a file are the same thing because moving a file to a new file path, is a way of renaming it. It's the same file, it's just got a different path to it. So we're actually going to "move" as the way to rename it. 

```$ git mv test_file.txt renamed_file.txt```  

```$ git status```

```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    test_file.txt -> renamed_file.txt
```

### Changing the path (e.g. adding into a folder)

```$ git mv test_file.txt folder_01/renamed_file.txt```  

```$ git status```

```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    test_file.txt -> folder_01/test_file.txt
```

It's more efficient to do it with a few command instead of doing it the first technique.

So moving and renaming are synonomus and there's two ways that we could accomplish - the command line is more efficient.
