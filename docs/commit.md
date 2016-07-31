## Commit

[^1]

<img class="alignnone" src="https://lh3.googleusercontent.com/zEnthrU_Gj29HHXPQuqzxKB9AmJb2JrEeNNyj3yfts9K=w1011-h697-no" alt="" />

```shell
# Add file contents to the index
git add [filename]
# Record changes to the repository
git commit -m [message]
# Reset current HEAD to the specified state
git reset HEAD~1
# Switch branches or restore working tree files
git checkout HEAD~2
```

### View Status

```shell
git status
git log
git log --since=2015-12-01
git log --until=2015-12-01
git log --author="magizbox"
git log --grep="Init"
git log --oneline origin/master
```

[^1]: <a href="http://git-scm.com/book/ca/v1/Git-Basics-Recording-Changes-to-the-Repository" target="_blank">http://git-scm.com/book/ca/v1/Git-Basics-Recording-Changes-to-the-Repository</a>
