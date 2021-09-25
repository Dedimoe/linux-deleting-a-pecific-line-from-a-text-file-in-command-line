# linux-deleting-a-pecific-line-from-a-text-file-in-command-line
Linux: Deleting a Specific Line From a Text File in Command Line

On Linux, how to deleting a specific line from a text file in command line ?

For example, file.txt:
```
this line 1
line 2
line 3
line 4
line 5
line 6
```

with ```sed``` command :
```
sed -i '2d' file.txt
```

Note: ```-i``` means edit the filea, ```d``` is the command to delete, 2 means the 2nd line.

The output file content will be:
```
this line 1
line 3
line 4
line 5
line 6
```

Remove the last line:
```
sed '$d' file.txt
```

Remove all empty lines:
```
sed '/^$/d' file.txt
```
or
```
sed '/./!d' file.txt
```

Remove lines from 5 to 7:
```
sed '5,7d' file.txt
```

Remove the line matching by a regular expression ```Abcde```:
```
sed '/oops/d' file.txt
```
