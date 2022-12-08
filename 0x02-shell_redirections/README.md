# 0x02-shell_redirections

##### 0. Hello World :  Write a script that prints “Hello, World”, followed by a new line to the standard output.
> Easy, nothing special, juste use echo command to display the text

##### 1. Confused smiley :
> Use "" to avoid <"> and <'> being interpreted

##### 2. Let's display a file : Display the content of the /etc/passwd file.
> Just use a *content displayer command* like *cat* or *less* to display the content of */etc/passwd*

##### 3. What about 2? : Display the content of /etc/passwd and /etc/hosts
> Same as 2, just add  *a aspace( )* between the both file directory

##### 4. Last lines of a file : Display the last 10 lines of /etc/passwd
> Use tail command with -n 10 FILENAME

##### 5. I'd prefer the first ones actually : Display the first 10 lines of /etc/passwd
>use 'head -10' to the file /etc/passwd

##### 6. Line #2  : Write a script that displays the third line of the file iacta. | The file iacta will be in the working directory | You’re not allowed to use sed
> Use head command with '|' and tail -n the last line (-n 3) since 'head 3' display the third entry of my file
##### 7. It is a good file that cuts iron without making a noise : Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.
> This was not simple and quit difficult. But easy when you understand the process. 
> They are some special chars that requires '' to be considered ass a part of the title. For example : 
>> if I want \ in my file name, i need to try *touch 'my\filename.txt'*. output -> my\filename.txt 
>> if I want my file contains single quote '. then i will need to write the name inside double quotes ""->  *touch "Rollin's_file.txt"* Output -> Rollin's_file.txt
>> the rule is reversed with double quote "" -> *touch 'this is my "file".txt' Output -> this is my "file".txt
>> if file name must contains \, you must keep it inside single quote ''. 
>> The file name must be inside *'' single quotes* for these chars : *-, #, ;, !, @, (, ), <, >, \, " *
>> The file name must be preceded of *\* if the next *char is espace*
>> No need action when it concerns these chars : *+%^&[]{}_=?.:~* and * *star*
>> If the file name must contains *, '* and *"* together, then, you need to combine the rules. Here is an exmple:
>> file name: $'thismy"file"\name'
>> dealing : '$' "'thismy" '"file"\' "name'"
>> That is ! {Of course, you should noot add the spaces. I added them to make my explain easy}

##### 8. Save current state of directory : Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
>Redirect the output of ls -la in a file (ls_cwd_content) 

##### 9. Duplicate last line : Write a script that duplicates the last line of the file iacta -> The file iacta will be in the working directory
>> Use tail -1 iacta >> iacta

##### 10. No more javascript : Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
>> Modern version of find command has *-delete* option that allow found item being directly delected. It avoid us use -exec rm {} \ command. in the command, it is important to use "" instead of '' for specifying the files like "*.js" instead of '*.js'

##### 11. Don't just count your directories, make your directories count mandatory : Write a script that counts the number of directories and sub-directories in the current directory.    The current and parent directories should not be taken into accountHidden directories should be counted
>>mindepth avoid us counting the current dir : find -mindepth 1 -type d | wc -l 

##### 12. What’s new : Create a script that displays the 10 newest files in the current directory - Requirements: One file per line - Sorted from the newest to the oldest
>ls -t option sort by time, head display by default top 10 element

##### 13. Being unique is better than being perfect : Create a script that takes a list of words as input and prints only words that appear exactly once.
> we sort the output, then we use pip and uniq -u the output sorted

##### 14. It must be in that file : Display lines containing the pattern “root” from the file /etc/passwd
> We grep the output of /etc/passwd

##### 15. Count that word : Display the number of lines that contain the pattern “bin” in the file /etc/passwd
>we grep 'bin' of output and wc -l the grepped content

##### 16. What's next?  : Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.
> grep "root"  -A 3 option of /etc/passwd will help because -A 3 means display 3 lines after matching lines 

##### 17. I hate bins : Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.
> grep -v search for inverted match

##### 18. Letters only please : Display all lines of the file /etc/ssh/sshd_config starting with a letter.
> grep -i with ^[a-z] on the file will search all entry from a to z 

##### 19. A to Z : Replace all characters A and c from input to Z and e respectively.
> tr command allow us to translate or delete a char tr "A" "Z" means A will be replaced by Z

##### 20. Without C, you would live in hiago : Create a script that removes all letters c and C from input.
> tr -d "AB" will delete AB from input

##### 21. esreveR : Write a script that reverse its input.
> rev command on an input reverse content

##### 22. DJ Cut Killer : Write a script that displays all users and their home directories, sorted by users. - Based on the the /etc/passwd file
> cut -d from : and -f of 1-6, then sort the output
