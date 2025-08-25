# Tips and Tricks 

Here are some examples that are more complex than could be taught, but will be good to learn and incorporate on your own.

### Debugging

#### Shell options

It is useful during script development to turn on some features that change the default behavior of the shell.

#### `-n`: Read commands in script, but do not execute them

Here is “syntax_error.bash”:

```
#!/usr/bin/env bash
 
echo "this line is fine" 
echo "this line is not
```

```
$ bash -n syntax_error.bash
syntax_error.sh: line 5: unexpected EOF while looking for matching `"'
syntax_error.sh: line 6: syntax error: unexpected end of file

$ bash syntax_error.bash 
this line is fine
syntax_error.sh: line 5: unexpected EOF while looking for matching `"'
syntax_error.sh: line 6: syntax error: unexpected end of file
```

This example has a non-destructive first line, but consider an example where you don't want to run heavy commands, or try to delete a file, that only works the first time during debugging.

#### `-e` pipefail: Prevent the script from continuing after an error.




