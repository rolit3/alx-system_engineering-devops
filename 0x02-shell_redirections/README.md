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

#####  9. Duplicate last line : Write a script that duplicates the last line of the file iacta -> The file iacta will be in the working directory
>>
