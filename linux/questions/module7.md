1. Which SQL command is used to remove a row of data in a database table? DELETE FROM is used to delete a row of data in the form of DELETE FROM database WHERE x='y'; 
1. How do you determine the return value of a script in your shell? echo $? will show you the return value of the last command run in the shell. 
1. Which bash scripting command will read a line of text the user has input? The read command is used to read user input in bash scripts. 
1. Which command is used to loop over a sequence in bash scripting? 'for' is used to loop over a specified sequence, eg. 'for x in 1 2 3', whereas 'while' will loop over a condition. 
1. Which SQL command is used to put new data into a database table? INSERT is used to add new data to a database in the form of INSERT into tablename VALUES ( value, value ); 
1. Which switch can be used to test if a file exists in a bash script? if -f will test if a file exists. 
1. Which keyword is used to start a code block if an 'if' condition is not met? 'else' is used to start a block of commands that will be run if the original 'if' statement condition is not met. 'then' is used if the condition statement *is* met. 
1. In which of the following files can a regular user store bash-specific configuration to be executed only at login? While ~/.profile can be used, it's not bash specific. A regular user cannot edit the other files. 
1. Which bash setting will stop the > redirect from overwriting an existing file? set -o noclobber will stop the > redirect from overwriting files. 
1. What does function a { echo $1; } ; a a b c output? $1 will only match the first argument passed to the function, so only 'a' is printed. 
