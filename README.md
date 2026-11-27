# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
```
Create a directory named "my-folder"
```
<img width="737" height="137" alt="image" src="https://github.com/user-attachments/assets/23022d4d-8b04-4867-8a28-2ab09a77f44c" />


## COMMAND AND OUTPUT
```
Remove the directory "my-folder"
```
<img width="563" height="102" alt="image" src="https://github.com/user-attachments/assets/b456ea04-4b3a-4a6e-865f-4a6cd8657638" />


## COMMAND AND OUTPUT

```
Create the file Rose.txt
<img width="730" height="205" alt="image" src="https://github.com/user-attachments/assets/9a46ed8e-e84b-40d1-9f48-f3a33af637bb" />


## COMMAND AND OUTPUT

```
Create the file hello.txt using echo and redirection
```
<img width="797" height="158" alt="image" src="https://github.com/user-attachments/assets/44d7d654-b62e-48f0-bd14-01d3a5057f78" />


## COMMAND AND OUTPUT
```
Copy the file hello.txt into the file hello1.txt
```
<img width="621" height="65" alt="image" src="https://github.com/user-attachments/assets/7a478cb6-c6e5-4fef-8000-3d3d3f1a0c3e" />

## COMMAND AND OUTPUT
```
Remove the file hello1.txt
```
<img width="447" height="85" alt="image" src="https://github.com/user-attachments/assets/eacfcb8b-f179-4c8a-8e4c-470250a4f03b" />


## COMMAND AND OUTPUT
```
List out the file hello1.txt in the current directory
```
<img width="517" height="157" alt="image" src="https://github.com/user-attachments/assets/5d6c7258-caf2-4044-a3c6-9fff4f1bf9cb" />

## COMMAND AND OUTPUT
```
List out all the associated file extensions
```
<img width="356" height="582" alt="image" src="https://github.com/user-attachments/assets/c2f2b5ba-2619-4902-a225-ca172c2cd634" />

## COMMAND AND OUTPUT

```
Compare the file hello.txt and rose.txt
```
<img width="497" height="195" alt="image" src="https://github.com/user-attachments/assets/6834194d-d54d-420a-9ae9-1ba41cd663fe" />




## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```



## OUTPUT

<img width="450" height="158" alt="image" src="https://github.com/user-attachments/assets/4080bab5-16a6-4091-92d3-d3d5c0a24860" />



Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)

:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

## OUTPUT
<img width="451" height="190" alt="image" src="https://github.com/user-attachments/assets/9f47a140-6afe-4ed7-9bda-26d50bd50364" />





Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT

<img width="411" height="242" alt="image" src="https://github.com/user-attachments/assets/ea80cd34-7a2d-478d-9ea1-621a6adfeb96" />




Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT
<img width="446" height="207" alt="image" src="https://github.com/user-attachments/assets/2aa7ebda-620a-4b62-99b9-1aca5055c56e" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.
```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

## OUTPUT
<img width="347" height="355" alt="image" src="https://github.com/user-attachments/assets/9ec06a22-5ba8-4ced-9e7b-04fe2a31ff19" />


# RESULT:
The commands/batch files are executed successfully.
