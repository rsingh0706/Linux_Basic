

### The ls command is commonly used to identify the files and directories in the working directory. This command is one of the many often-used Linux commands that you should know.


1. Listing Files and Directories

```bash
ls
```

2. Listing with Detailed Information
   Use Case: Shows a detailed list, including file permissions, owner, group, size, and modification date.

```bash
ls -l
```

3. Listing Hidden Files
   Use Case: Lists all files, including hidden files (files starting with a dot).

```bash
ls -a
```

4. Sorting Files
   Use Case: Sorts files by:
    -t: Modification time (newest first).
    -S: File size (largest first).
    -r: Reverse order.

```bash
ls -t
```

5. Listing with Human-Readable Sizes
   Use Case: Displays file sizes in a human-readable format (KB, MB, GB).

```bash
ls -lh
```

6. Recursive Listing
   Use Case: Lists files and directories recursively.

```bash
ls -R
```

7. Combining Options
   Use Case: Combines multiple options for a comprehensive view.
   Lists all files (including hidden), with detailed information and human-readable sizes.

```bash
ls -lha
```


### The pwd command is mostly used to print the current working directory on your terminal. It is also one of the most commonly used commands. 

 
1. Confirm Current Location in the File System
   Use pwd to check where you are in the directory structure.

```bash
pwd
```

2. Combine with Other Commands, Helpful when scripting to provide context-aware execution.

```bash
pwd >> log.txt
```


### This mkdir command allows you to create fresh directories in the terminal itself. The default syntax is mkdir directory name and the new directory will be created.


1. Create a Single Directory

```bash
mkdir my_folder
```

2. Create Multiple Directories at Once

```bash
mkdir folder1 folder2 folder3
```

3. Create Nested Directories

```bash
mkdir -p parent/child/grandchild
```

4. Set Permissions While Creating

```bash
mkdir -m 755 secure_folder
```


### The cd command is used to navigate between directories. It requires either the full path or the directory name, depending on your current working directory. If you run this command without any options, it will take you to your home folder. Keep in mind that it can only be executed by users with sudo privileges.


1. Change to a Specific Directory

```bash
cd /home/anuj/Documents
```

2. Move Up One Directory

```bash
cd ..
```

3. Move to the Home Directory

```bash
cd  & cd ~
```

4. Change to the Previous Directory

```bash
cd -
```

5. Change to the Root Directory

```bash
cd /
```

6. Change to a Directory with Spaces

```bash
cd "My Documents"
```


###  The rmdir command is used to delete permanently an empty directory. To perform this command the user running this command must be having sudo privileges in the parent directory. 


1. Remove a Single Empty Directory

```bash
mkdir empty_dir
rmdir empty_dir
```

2. Using -p to Remove Parent Directories

```bash
mkdir -p parent_dir/child_dir
rmdir -p parent_dir/child_dir
```

 3. Use rmdir only for empty directories.

```bash
rm -r directory_name
```


### The cp command of Linux is equivalent to copy-paste and cut-paste in Windows. 


1. Basic Syntax

```bash
cp [OPTIONS] SOURCE DESTINATION
```

2. To copy a file named file1.txt to file2.txt in the same directory:

```bash
cp file1.txt file2.txt
```

3. To copy file1.txt to the /home/anuj/Documents/ directory:

```bash
cp file1.txt /home/anuj/Documents/
```

4. To copy a directory dir1 (including its contents) to dir2:

```bash
cp -r dir1 dir2
```

5. To copy file1.txt to file2.txt but get a confirmation before overwriting:

```bash
cp -i file1.txt file2.txt
```

6. To copy file1.txt while preserving its attributes like timestamps and permissions:

```bash
cp -p file1.txt file2.txt
echo "Hello, World!" > file1.txt
echo "hello i am rahul" >> file1.txt
```

7. Verbose Output

```bash 
cp -v file1.txt /home/anuj/Documents/
```

8. Archive a Directory

```bash
cp -a dir1 dir2
```


### The mv command is generally used for renaming and move  the files in Linux.


1. Moving a File

```bash
mv file1.txt /home/anuj/Documents/
```

2. Renaming a File

```bash
mv file1.txt renamed_file1.txt
```

3. Moving Multiple Files

```bash
mv file1.txt file2.txt /home/anuj/Documents/
```

4. Renaming a Directory

```bash
mv my_folder renamed_folder
```

5. Moving Hidden Files

```bash
mv .hidden_file /home/anuj/Documents/
```

6. Moving and Renaming Simultaneously

```bash
mv file1.txt /home/anuj/Documents/renamed_file1.txt
```


### rm command in Linux is generally used to delete the files created in the directory. 


1. Remove a File

```bash
rm file.txt
```

2. Prompt Before Deleting a File, You will see a confirmation like:

```bash
rm -i file.txt
```

3. Force Remove a File

```bash
rm -f file.txt
touch file.txt         # Create an empty file named file.txt
chmod 444 file.txt     # Change permissions to read-only (write-protected)
ls -l file.txt         # View the file permissions
```

4. Remove Multiple Files

```bash
rm file1.txt file2.txt
```

5. Remove an Empty Directory

```bash
rm -d empty_directory
```

6. Recursively Remove a Directory and Its Contents

```bash
rm -r my_directory
```

7. Force Remove a Directory and Its Contents

```bash
rm -rf my_directory
```






















  

