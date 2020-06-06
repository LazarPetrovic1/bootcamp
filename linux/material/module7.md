# Configure terminal

Configuration files
+ Allow us to change how our shell works
+ Define path, environment variables
+ Set up aliases
+ System wide - `/etc/bash.bashrc` & `/etc/profile`
+ Local `~/.bash_profile`,` ~/.bashrc` & `~/.profile`
+ Action specific `~/.bash_login` & `~/.bash_logout`

`set -o noclobber` - cannot overwrite files

`set -o xtrace` - get the command back the way bash interprets it

### Customize and write simple scripts

#! - hash bang

+ First line of a script
+ provides the full path to the interpreter

`if/else`

```bash
if [condition]
then
	# stuff to do
else
	# other stuff to do
fi
```

`for`

```bash
for VARIABLE in 1 2 3 4 5
do
	# stuff
	# stuff
done
```

`seq <num>` - print a sequence of numbers

```bash
for VAR in `seq 5` # backticks important
# other stuff

var = 'hi'

while

while condition
do
# stuff
done
```

`read` - captures user input

```bash
echo 'Enter your name'
read name
echo "Hello, $name!"
```

`functions`

```bash
# No return
function myfunc {
	echo $1 $2 $3
}

# Return value
check: echo $?
```

Chained commands

`&&` - and

`||` - or

`|` - pipe

`;` - execute the next command regardless of the outcome

```bash
ping -c1 google.com && echo "Google is alive!" || echo "Google is dead."
# if ping works, the first echo will come through, else the second will
```
### SQL data management

Structured query language with numeric IDs

commands

| SQL COMMAND                     | MEANING                                           |
| ------------------------------- | ------------------------------------------------- |
| `INSERT`                        | put a row of data in db                           |
| `UPDATE`                        | updates a row of data in db                       |
| `SELECT`                        | selects a row of data in a db based on conditions |
| `DELETE`                        | delete a row of data in db                        |
| `FROM`                          | selects the table you are selecting the data from |
| `WHERE`                         | defines the SELECT condition                      |
| `GROUP BY`                      | data grouping                                     |
| `ORDER BY`                      | data ordering                                     |
| `JOIN`                          | joins 2 tables which share a column of data       |
| `SHOW DATABASES`                | shows dbs                                         |
| `CREATE DATABASE <name>`        | makes db                                          |
| `USE <db>`                      | uses db                                           |
| `SHOW TABLES`                   | shows tables                                      |
| `CREATE TABLE <name> (<stuff>)` | creates a table                                   |
| `DESCRIBE <db>`                 | shows db structure                                |
