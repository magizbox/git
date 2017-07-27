# Git Configurations

## How do I force git to use LF instead of CR+LF under windows?

The proper way to get LF endings in Windows is to first set core.autocrlf to false:

```
git config --global core.autocrlf false
```

## Suggested Readings

* [How do I force git to use LF instead of CR+LF under windows?](http://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-windows)
