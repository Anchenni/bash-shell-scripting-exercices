# Bash Shell Scripting Exercises:

Practice and refine your Bash shell scripting skills with these exercises. From simple tasks to more complex challenges, these exercises provide hands-on opportunities to enhance your proficiency in automating tasks and managing Unix-like systems. Enjoy the journey of becoming a more skilled scripter!

Let's start with some basic exercises to get you comfortable with navigating the file system and working with files and directories.

**Exercise 1: Navigating the File System**

1. Open your terminal (Zsh OR bash) if it's not already open.

2. Use the `pwd` command to print your current working directory (the directory you are currently in). Note the directory path.

3. Use the `ls` command to list the contents of your current directory.

4. Use the `cd` command to change to a different directory. You can use either an absolute path (e.g., `/Users/yourusername/Documents`) or a relative path (e.g., `Desktop` if it's in your current directory).

5. Use `pwd` again to confirm that you are now in the new directory.

**Exercise 2: Working with Files and Directories**

1. Create a new directory called "ShellExercises" in your home directory.

2. Use the `cd` command to navigate into the "ShellExercises" directory.

3. Inside "ShellExercises," create three new files named "file1.txt," "file2.txt," and "file3.txt."

4. Use the `ls` command to verify that the three files were created.

5. Create a new subdirectory within "ShellExercises" called "Subdirectory."

6. Move "file2.txt" into the "Subdirectory" directory.

7. Use the `ls` command to confirm that "file2.txt" is no longer in the main directory but is now inside "Subdirectory."

**Exercise 3: File Manipulation**

1. Navigate into the "Subdirectory" directory.

2. Use the `cat` command to view the contents of "file2.txt."

3. Create a new file named "newfile.txt" inside the "Subdirectory" directory. You can use the `touch` command to create an empty file.

4. Use the `mv` command to rename "newfile.txt" to "renamedfile.txt."

5. Use the `rm` command to delete "renamedfile.txt."

**Exercise 4: Additional Commands**

1. Navigate back to the "ShellExercises" directory.

2. Use the `find` command to search for all `.txt` files within the "ShellExercises" directory and its subdirectories.

3. Use the `grep` command to search for a specific word or phrase within one of the `.txt` files in the "ShellExercises" directory.

`grep` is a powerful command-line utility for searching text using regular expressions. It's a handy tool for finding specific patterns or words within files. Let's dive deeper into using `grep` and explore some of its more advanced options and use cases.

**Exercise 5: Advanced `grep` Usage**

In this exercise, we'll cover some advanced `grep` techniques and options:

1. **Search Multiple Files**: You can use `grep` to search for a word or pattern in multiple files at once. Navigate to your "ShellExercises" directory and try this:

   ```bash
   grep "example" *.txt
   ```

   This command will search for the word "example" in all `.txt` files in the current directory and display the lines containing the word.

2. **Case-Insensitive Search**: Use the `-i` option to perform a case-insensitive search. For example:

   ```bash
   grep -i "example" file1.txt
   ```

   This will find "example" regardless of whether it's uppercase or lowercase in the file.

3. **Count Matches**: To count the number of times a word or pattern appears in a file, use the `-c` option:

   ```bash
   grep -c "example" file1.txt
   ```

   This will return the count of occurrences of "example" in `file1.txt`.

4. **Search for Inverted Matches**: Use the `-v` option to invert the match, meaning it will display lines that don't contain the specified word or pattern. For example:

   ```bash
   grep -v "example" file1.txt
   ```

   This will display all lines in `file1.txt` that do not contain "example."

5. **Regular Expressions**: `grep` supports regular expressions for more complex pattern matching. For example, to find lines containing any word starting with "ex," use:

   ```bash
   grep '\bex\w*' file1.txt
   ```

   This will match words like "example," "exercise," and so on.

6. **Recursive Search**: To search for a word or pattern in all files within a directory and its subdirectories, use the `-r` (or `-R`) option:

   ```bash
   grep -r "example" ~/ShellExercises/
   ```

   This command searches for "example" recursively in all files under the "ShellExercises" directory.

7. **Display Line Numbers**: You can use the `-n` option to display line numbers along with matching lines:

   ```bash
   grep -n "example" file1.txt
   ```

   This will show line numbers for each matching line in `file1.txt`.

Take your time to experiment with these `grep` options and use cases. `grep` is a versatile tool for text searching and pattern matching, and mastering its various options can be incredibly useful for working with text data on the command line. 

Let's move on to the next set of exercises to further enhance your knowledge of working with the shell.

**Exercise 8: Working with Text Files**

In this exercise, we'll perform various tasks with text files using common shell commands.

1. **Creating a New Text File**: Use the `touch` command to create a new text file called "mytextfile.txt" in the "ShellExercises" directory.

2. **Appending Text**: Use the `echo` command to append the text "Hello, world!" to "mytextfile.txt."

3. **Viewing File Content**: Use the `cat` command to view the content of "mytextfile.txt."

4. **Redirecting Output**: Use the `echo` command to add the text "This is a new line." to "mytextfile.txt" without overwriting the existing content. Hint: You can use the `>>` operator for this.

5. **Viewing the Modified Content**: Use the `cat` command again to view the modified content of "mytextfile.txt."

**Exercise 9: File Permissions**

In this exercise, we'll work with file permissions to change who can read and write to a file.

1. **Check File Permissions**: Use the `ls -l` command to view the permissions of "mytextfile.txt." Take note of the file's permissions and owner.

2. **Change File Permissions**: Use the `chmod` command to change the permissions of "mytextfile.txt" so that only the owner can read and write to it. Hint: You can use `chmod 600 mytextfile.txt` for this.

3. **Verify Permissions**: Use `ls -l` again to verify that the permissions have been changed accordingly.

**Exercise 10: Compressing and Archiving Files**

In this exercise, we'll use commands to compress and archive files into a single file.

1. **Create a Directory**: Use the `mkdir` command to create a new directory called "MyFiles" inside the "ShellExercises" directory.

2. **Move Files**: Move "mytextfile.txt" to the "MyFiles" directory.

3. **Compress Files**: Use the `tar` command to create a compressed archive (tarball) of the "MyFiles" directory. The command might look like this:

   ```bash
   tar -czvf MyFiles.tar.gz MyFiles/
   ```

   This command creates a compressed file named "MyFiles.tar.gz" containing the contents of the "MyFiles" directory.

4. **List Archive Contents**: Use the `tar` command to list the contents of the archive without extracting them. Hint: You can use `tar -tzvf MyFiles.tar.gz` for this.

5. **Extract Archive**: Use the `tar` command to extract the contents of "MyFiles.tar.gz" into a new directory called "ExtractedFiles." Hint: You can use `tar -xzvf MyFiles.tar.gz -C ExtractedFiles/` for this.


**Exercise 11: Working with Directories**

In this exercise, we'll perform various tasks involving directories using common shell commands.

1. **Create Subdirectories**: Inside the "ShellExercises" directory, create two subdirectories named "FolderA" and "FolderB" using the `mkdir` command.

2. **List Directory Contents**: Use the `ls` command to list the contents of the "ShellExercises" directory, including the subdirectories you just created.

3. **Rename a Directory**: Rename "FolderB" to "RenamedFolder" using the `mv` command.

4. **Copy Files**: Copy "mytextfile.txt" from "FolderA" to "RenamedFolder" using the `cp` command.

5. **Remove a Directory and Its Contents**: Delete "FolderA" and its contents (including "mytextfile.txt") using the `rm` command with the `-r` (or `-rf`) option. Be cautious when using the `rm -r` command, as it deletes files and directories recursively.

**Exercise 12: Process Management**

In this exercise, we'll work with processes and learn how to manage them.

1. **Run a Background Process**: Use the `sleep` command to run a background process that sleeps for 10 seconds. You can run it like this:

   ```bash
   sleep 10 &
   ```

   This will run the `sleep` command in the background.

2. **List Running Processes**: Use the `ps` command to list all running processes. Look for the `sleep` process you started in the previous step.

3. **Stop a Process**: Use the `kill` command to stop the `sleep` process you started. You'll need to provide the process ID (PID) of the `sleep` process. You can find the PID from the `ps` output.

4. **List Running Processes Again**: Use the `ps` command to confirm that the `sleep` process has been stopped.

5. **View Process Tree**: Use the `pstree` command to view the process tree, which shows the relationships between processes. This can be useful for understanding how processes are related to each other.


**Exercise 13: Environment Variables**

In this exercise, we'll work with environment variables, which are variables that store information that the shell and programs can use.

1. **View Environment Variables**: Use the `env` command to view a list of environment variables and their values. This will display a lot of information.

2. **Display a Specific Environment Variable**: Use the `echo` command to display the value of a specific environment variable. For example, to display the value of the `USER` variable (which typically stores your username), you can use:

   ```bash
   echo $USER
   ```

3. **Create a Custom Environment Variable**: Create a custom environment variable called `MY_VARIABLE` and set it to a value of your choice. For example:

   ```bash
   export MY_VARIABLE="Hello, Shell!"
   ```

4. **Display the Custom Environment Variable**: Use `echo` to display the value of your custom environment variable `MY_VARIABLE`.

**Exercise 14: Redirecting Input and Output**

In this exercise, we'll explore input and output redirection, which allows you to control where command input comes from and where output goes.

1. **Redirect Output to a File**: Use the `ls` command to list the contents of your home directory and redirect the output to a file called "home_contents.txt." This will save the list of files and directories to a text file.

   ```bash
   ls > home_contents.txt
   ```

2. **View the Contents of the Redirected File**: Use the `cat` command to view the contents of "home_contents.txt" and confirm that the output was redirected correctly.

3. **Redirect Input from a File**: Create a new text file called "input_file.txt" with some text content. Then, use the `wc` command to count the number of lines in the file, but this time, redirect the input from "input_file.txt."

   ```bash
   wc -l < input_file.txt
   ```

   This will count the lines in "input_file.txt" without displaying the file's content.

**Exercise 15: Pipes**

In this exercise, we'll use pipes to combine multiple commands to perform more complex operations.

1. **List Files in Home Directory**: Use the `ls` command to list the files and directories in your home directory.

2. **Filter the List with `grep`**: Pipe the output of the `ls` command into `grep` to filter the list to show only files that have "file" in their names. For example:

   ```bash
   ls | grep "file"
   ```

   This will list files with "file" in their names.

3. **Sort and Display**: Pipe the filtered list into the `sort` command to sort the list alphabetically. For example:

   ```bash
   ls | grep "file" | sort
   ```

   This will list the filtered files in alphabetical order.



**Exercise 16: Writing and Running Shell Scripts**

In this exercise, we'll create a simple shell script, make it executable, and run it.

1. **Create a Shell Script**: Using a text editor of your choice (e.g., `nano`, `vim`, or `code`), create a new file named `myscript.sh`. Inside this file, add the following lines:

   ```bash
   #!/bin/bash
   echo "Hello, this is my first shell script!"
   ```

   This script simply echoes a message to the terminal.

2. **Make the Script Executable**: To make the script executable, use the `chmod` command:

   ```bash
   chmod +x myscript.sh
   ```

   This command gives the script execute permissions.

3. **Run the Script**: Execute the script by running:

   ```bash
   ./myscript.sh
   ```

   You should see the message "Hello, this is my first shell script!" displayed in the terminal.

**Exercise 17: Shell Script with Arguments**

In this exercise, we'll modify the shell script to accept command-line arguments.

1. **Modify the Shell Script**: Edit the `myscript.sh` file and replace its contents with the following script:

   ```bash
   #!/bin/bash
   if [ $# -eq 0 ]; then
       echo "Usage: ./myscript.sh <name>"
   else
       echo "Hello, $1! This is my first shell script."
   fi
   ```

   This script checks if a command-line argument is provided. If an argument is given, it greets the user with their name; otherwise, it provides usage instructions.

2. **Make the Script Executable**: If you haven't already made the script executable, use the `chmod` command as shown in Exercise 16.

3. **Run the Script with an Argument**: Execute the script with your name as an argument:

   ```bash
   ./myscript.sh John
   ```

   Replace "John" with your name. The script should greet you with your name.

4. **Run the Script Without an Argument**: Execute the script without providing an argument to see the usage instructions:

   ```bash
   ./myscript.sh
   ```

**Exercise 18: Conditional Statements**

In this exercise, we'll create a shell script that uses conditional statements to check a condition and perform different actions.

1. **Create a New Shell Script**: Create a new shell script named `check_number.sh` and open it in your text editor.

2. **Write the Script**: Add the following content to the script:

   ```bash
   #!/bin/bash

   echo "Enter a number:"
   read number

   if [ $number -gt 10 ]; then
       echo "The number is greater than 10."
   elif [ $number -eq 10 ]; then
       echo "The number is equal to 10."
   else
       echo "The number is less than 10."
   fi
   ```

   This script prompts the user for a number, checks if it's greater than, equal to, or less than 10, and provides an appropriate message.

3. **Make the Script Executable**: If you haven't already made the script executable, use the `chmod` command as shown in previous exercises.

4. **Run the Script**: Execute the script:

   ```bash
   ./check_number.sh
   ```

   Enter different numbers to see how the script responds based on the condition.

**Exercise 19: Loops in Shell Scripts**

In this exercise, we'll create a shell script that uses loops to perform repetitive tasks.

1. **Create a New Shell Script**: Create a new shell script named `countdown.sh` and open it in your text editor.

2. **Write the Script**: Add the following content to the script:

   ```bash
   #!/bin/bash

   echo "Enter a number to start the countdown:"
   read countdown_number

   if [[ $countdown_number =~ ^[0-9]+$ ]]; then
       echo "Starting countdown from $countdown_number..."
       while [ $countdown_number -ge 0 ]; do
           echo $countdown_number
           sleep 1
           countdown_number=$((countdown_number-1))
       done
       echo "Blast off!"
   else
       echo "Invalid input. Please enter a positive integer."
   fi
   ```

   This script prompts the user for a number, checks if it's a positive integer, and then counts down from that number to zero, displaying each number with a one-second delay.

3. **Make the Script Executable**: If you haven't already made the script executable, use the `chmod` command as shown in previous exercises.

4. **Run the Script**: Execute the script:

   ```bash
   ./countdown.sh
   ```

   Enter a positive integer to start the countdown.

**Exercise 20: Functions in Shell Scripts**

In this exercise, we'll create a shell script that defines and uses functions to perform specific tasks.

1. **Create a New Shell Script**: Create a new shell script named `math_operations.sh` and open it in your text editor.

2. **Write the Script**: Add the following content to the script:

   ```bash
   #!/bin/bash

   # Define a function to add two numbers
   add() {
       result=$(( $1 + $2 ))
       echo "The sum of $1 and $2 is $result"
   }

   # Define a function to subtract two numbers
   subtract() {
       result=$(( $1 - $2 ))
       echo "The difference between $1 and $2 is $result"
   }

   # Define a function to multiply two numbers
   multiply() {
       result=$(( $1 * $2 ))
       echo "The product of $1 and $2 is $result"
   }

   # Define a function to divide two numbers
   divide() {
       result=$(awk "BEGIN {printf \"%.2f\", $1 / $2}")
       echo "The division of $1 by $2 is $result"
   }

   # Main script
   echo "Enter two numbers:"
   read num1
   read num2

   add $num1 $num2
   subtract $num1 $num2
   multiply $num1 $num2
   divide $num1 $num2
   ```

   This script defines four functions for basic math operations (addition, subtraction, multiplication, and division) and then prompts the user for two numbers and performs these operations on the numbers.

3. **Make the Script Executable**: If you haven't already made the script executable, use the `chmod` command as shown in previous exercises.

4. **Run the Script**: Execute the script:

   ```bash
   ./math_operations.sh
   ```

   Enter two numbers to perform the math operations.

