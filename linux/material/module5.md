# THE COMMAND LINE

`bash` is the most often/widely used

the other ones are `zsh`, `ksh`, `sh`, ...

`env` - gets environment variables (temporary)

`history` - shows the whole history of the current terminal window

manuals - there are 9 different types

`man <type> <page>`

`man time` => TIME(1)

`man 3 time` => TIME(3)

`manpath` - where the man pages are stored

`uname` - system information

### Quoting, type and which

Quoting stuff we don't want to do anything special

`echo ls ; data` => does not work

quoted: `echo 'ls ; date'` => works

`echo ls \; date` => escaping the character also works

`type`: tells you what type the command is

`type type` => `type` is a shell builtin

`type ls` => `ls` is aliased to `ls --color=auto`

`type time` => `time` is a shell keyword

`type less` => `less` is `/usr/bin/less`

`which`: like `type`, but tells you where the command is located

### Process text streams

`cat` - used to concatenate or print to screen

`cut` - remove sections from each line of files

(`cut -c<num> <filename>` - return the <num>th item from every line of file)

(`cut -c<num1>-<num2> <filename>` - return the items between <num1> and <num2> from every line of file)

`expand` - turn tab into 8 spaces

`unexpand` - turn every group of 8 spaces into a tab

`wc` - newline count, word count and byte count

`wc -l` => just the line count

`fmt` - splits the file into multiple readable lines

`head` - gives the top (default 10) lines of the text file (`-n` changes num of lines)

`tail` - gives the bottom (default 10) lines of the text file (`-n` changes num of lines)

`join` - joins 2 texts by correlating lines

`less` - page by page

`nl` - adds line numbers to the files

`od` - dumps file in octal form

`paste` - same as join but combines any line regardless of matching fields, separated by a tab

`pr` - formats the file with date, filename and page number at the top

`sed` - complex operations with text (`-e` flag allows regular expressions) `s` (substitution command of `sed`)

`sed` in action: `echo day | sed -e s/day/night/`

`sort` - sorts by alphabetical order

`split` - splits the file into multiple files (~ 1000 lines each)

`tr` - translates or deletes characters in a text (-d flags deletes)

`uniq` - puts repeating lines adjacent of each other

### `cat` and `sums`

##### cats

`bzcat` - decompress compressed files with `bzip2` alg

`bunzip2` - returns the previous file (decompressed)

`zcat` - `bzcat` for `gzip`

`gunzip` - `bunzip2` for `gzip`

`xzcat` - `bzcat` for `xz`

`unxz` - `bunzip2` for `xz`

##### sums

***md5sum***

***sha256sum***

***sha512sum***

`file` - gives information about the file

`tar` - creates a tar archive

[(*options for tar*) `cvf` - create verbose filename (most common options for tar)]

`zx` - zipped extract

`dd` - used for duplication (good for iso replacement - Ubuntu.dd e.g)

[DD often used as: `dd if=<input> of=<output> {some options}`]

`xxd` - hex dump

### Streams, pipes and redirects

1. STDIN - 0
2. STDOUT - 1
3. STDERR - 2

`>` - redirects all the text before it to a file, [**overwrite**]

`>>` - appends to a file redirected to [**append**]

`<` - redirects input

`&` - copy to another file descriptor

`xargs` - .forEach(x => ...)

`tee` - copy input to each file

### Processes

`ping` - pings a computer and gives back time

Ctrl + z || `bg` - background

`fg` - foreground

`nohup` - does not show the output of an executed command

`ping google.com &` - & in the end backgrounds the operation, but the output can still be seen

`kill(all)` - kills a process

### Kill signals

| Signal  | Meaning of signal              |
| ------- | ------------------------------ |
| SIGINT  | interruption signal - Ctrl + C |
| SIGKILL | kill signal                    |
| SIGSTOP | pause signal - Ctrl + Z        |
| SIGTERM | termination signal             |

`top` - proto task manager

`free` - shows info about memory

`watch (-n <num>)` - run commands periodically (every `<num>` seconds)

`tmux` - terminal multiplexer (similar to screen)

`tmux Ctrl + B` - sends a command to terminal

`tmux shift + 5` - splits the screen vertically (like atom files when dragged)

`Ctrl + b && Ctrl + c` - makes a new terminal window

`Ctrl + 0` - returns to the first terminal [with index 0]

### Modify process execution priorities

**Nice** value determines how much CPU time a process will get (-20 - highest priority, 19 - lowest priority)

usage: `nice <val> <command>`

`renice`: changes nice value; usage: `sudo renice <newval> -p <PID>`

### Regex & symbols

regex

Sequence of symbols and chars

Express a string or pattern

Searched for within text

##### Symbol

`|` - or => gray|grey

`()` - grouping => gr(a|e)y

`$` - `EOL` => end of line

`^` - `SOL` => start of line

`.` - any character

##### Quantifiers

`?` - 1 or 0 occurrence(s) of the preceding element => colou?r

`*` - 0 or more occurrences => ab*c === ac, abc, abbc, abbbc, ...

`+` - 1 or more occurrences of the preceding element => ab+c === abc, abbc, abbbc, ...

`{n}` - the preceeding item is matched exactly n times

`{min,}` - at least min times a match

`{min, max}` - between min and max

`grep` - **globally search for a regular expression and print**

There are `grep`, `egrep`, `fgrep`

`egrep` = `grep -E`

`sed` can be used with regex

##### Vi

1. Editing mode
2. Command mode
3. Visual mode

**Vim shortcuts:**

+ h - move left
+ j - move down
+ k - move up
+ l - move right

+ `/:text:` - search for :text: in file
+ `n after search` - next found item
+ `?init` - look for text backwards
+ `dd` - completely delete the line
+ `p` - paste the line after the cursor line
+ `yy` - copy the line
+ `num<command>` - do a command num times
+ `x` - delete characters
+ `:<number>` - colon number: go to line
+ `$` - go to line end
+ `^` - go to line start
+ `i` - go into insert mode
+ `a` - go into append mode
+ `esc` - leave the editing mode
+ `o` - editing mode + newline
+ `:wq` - save and exit
+ `shift + zz` - save and exit
+ `:q` - quit
+ `:q!a` - quit w/o saving
+ `:w` - save progress

##### Other common editors

1. **emacs**
2. **nano**
3. **vim**

`$EDITOR` is the default editor environment variable
