# git ```log```

```$ git log```

```$ git log -n 5``` -> limits the logs - gets only the latest 5 logs

```$ git log --since=2019-01-01``` -> limits the logs - gets since the given date

```$ git log --until=2019-01-01``` -> limits the logs - gets until the given date

```$ git log --author="Can"``` -> limits the logs - gets only the author is me

```$ git log --grep="Init"```	-> limits the logs - gets the commits contain 'Init'

```$ git log --grep="Bugfix"```	-> limits the logs - gets the commits contain 'Bugfix'

```$ git log --since=2019-03-01 --until=2019-03-31 --author="Can" --grep="refactor"``` -> limits the logs - given multiple conditions

```$ git log --oneline``` -> gives the logs in a compact structure

then we could have a look at the commit by using ```$ git show a1b2c3d4e --color-word```