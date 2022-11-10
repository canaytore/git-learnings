# Delete files

There are two different techniques that we could use for deleting files.

## Alternative #1

The first technique is to just delete the file ourself. Let's say we just drag it down to our trash and now the file has been deleted. It's moved outside the project, which in git's terms is being deleted.

```$ git status```

```
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    file_to_delete.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

So if we want to commit this change to our repository, then we need to tell git to add this change. So we'll do it just like we did with an add, but we'll use ```$ git rm``` and then the file name. 

```$ git rm file_to_delete.txt```

```rm 'file_to_delete.txt'```

If get status, we'll see that it's now in our staging area. As a deleted file waiting to go into our repository. 

```$ git status```

```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    file_to_delete.txt
```

Then we can just commit that change ```$ git commit -m ""```, delete the file. Now that change has been made. If we go back and do get status again, we'll see the working tree is clean. 

```$ git commit -m "delete the file"```

```
[master d837081] delete the file
 1 file changed, 1 deletion(-)
 delete mode 100644 file_to_delete.txt
```

```$ git status```

```
On branch master
nothing to commit, working tree clean
```

## Alternative #2

As an alternative way, we can tell git to remove it (just type ```$ git rm```, and then the name of that file)

```$ git rm file_to_delete.txt```

```rm 'file_to_delete.txt'```

The file is now gone, and it's not in our trash, either. It has been removed using a UNIX remove command, so it has been permanently removed. 

But notice now when I do get status, it has already added it to our staging directory. So this is a little more convenient. This allows us to do both steps at once, instead of going and removing the file and then telling git to also remove it, we can just do it all in one step. 

```$ git status```

```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    file_to_delete.txt
```

```$ git commit -m "delete the file"```

```
[master 71ce59a] delete the file
 1 file changed, 1 deletion(-)
 delete mode 100644 file_to_delete.txt
```

Now that file has been deleted.

So if we want to keep a copy of the file around, and we just want it outside the project, then drag the file and then tell git about it (i.e. Alternative #1). But if we really just want to permanently delete it, it may be more convenient to just tell git about it and let it do it's leading for us. (i.e. Alternative #2)

## Alternative #3 by using ```$ git clean```

```$ git clean -i``` -> interactive

```$ git clean -n``` -> would remove

```$ git clean -f``` -> force to remove
