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
