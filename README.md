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
<img width="592" height="116" alt="image" src="https://github.com/user-attachments/assets/7632550b-2e39-42c2-9431-8cde91589d32" />

## COMMAND AND OUTPUT
```
Remove the directory "my-folder"
```
<img width="587" height="80" alt="image" src="https://github.com/user-attachments/assets/b67d074c-c051-4db4-a45d-4fe2887df0f7" />

## COMMAND AND OUTPUT

```
Create the file Rose.txt
```
<img width="658" height="172" alt="image" src="https://github.com/user-attachments/assets/2c35eb72-e077-43b3-8cfa-1ced6e08d36c" />

## COMMAND AND OUTPUT

```
Create the file hello.txt using echo and redirection
```
<img width="675" height="137" alt="image" src="https://github.com/user-attachments/assets/1ae23f9a-a52f-44e3-85e0-d033ae6308c9" />

## COMMAND AND OUTPUT
```
Copy the file hello.txt into the file hello1.txt
```
<img width="542" height="66" alt="image" src="https://github.com/user-attachments/assets/0d77959f-487e-4fee-b62f-00b33c419137" />

## COMMAND AND OUTPUT
```
Remove the file hello1.txt
```
<img width="463" height="75" alt="image" src="https://github.com/user-attachments/assets/666176eb-0085-4e4c-96bd-aab62c55df90" />

## COMMAND AND OUTPUT
```
List out the file hello1.txt in the current directory
```
<img width="570" height="145" alt="image" src="https://github.com/user-attachments/assets/012b254d-eb5c-4d03-af30-aff367456c57" />

## COMMAND AND OUTPUT
```
List out all the associated file extensions
```
<img width="807" height="905" alt="image" src="https://github.com/user-attachments/assets/b4c5e69b-ffc2-48ab-89bc-98e927f90496" />

## COMMAND AND OUTPUT

```
Compare the file hello.txt and rose.txt
```
<img width="617" height="247" alt="image" src="https://github.com/user-attachments/assets/1b68aee0-a230-41b1-b363-7d5716ca2c3d" />



## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=John
echo Hello, %name%!
pause
```



## OUTPUT

<img width="467" height="156" alt="image" src="https://github.com/user-attachments/assets/7d96775a-d163-4799-9ec5-b6282e1b126a" />


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
<img width="737" height="281" alt="image" src="https://github.com/user-attachments/assets/60e89f6a-8ea0-4acf-b439-5ad73a03bba5" />




Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT


<img width="495" height="240" alt="image" src="https://github.com/user-attachments/assets/c30ca40f-5a5c-4055-a175-20dc55c0267d" />


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

<img width="672" height="290" alt="image" src="https://github.com/user-attachments/assets/3c0ecef0-5872-4465-a467-b4e8ddada2e0" />


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

<img width="695" height="478" alt="image" src="https://github.com/user-attachments/assets/20a24690-ce4e-4213-9ef3-491ecbc7c3b2" />


# RESULT:
The commands/batch files are executed successfully.
