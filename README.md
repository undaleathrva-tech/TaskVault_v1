# TaskVault_v1
# This is version 1 for TaskVault application. The first project made by LooK...

# What application will do..

# First start-up
## The application will ask the user to create a user_name
## The primary details of the user will be taken from the user. 
### Eg. DOB
## Once the user enters the necessary details, the console will open up with greetings. 

## The Console
### The console will be ran using the main.py file.
### The main.py will have access to the CSV file only during the very first creation of it.
### The CSV can no longer be altered using the main.py
### A new CSV file will be createed to store the users data as soon as the console opens for the very first time.
### The user will interact with the application through this console.
### The consloe will be responsible of handling all the commands that user gives to it.
### the console will display the number of tsks of the day, the day, date and exact time with user_name and number of tasks completed in the following manner

| User_Name     Tasks     Task_Completed |
| Day           Date      Time           |

### These rows will remain intact even if te content below it scrols. Like a rigid data.
### The console will always be ready for the user input. Without a cursor blinking. It is just annoying.
### The console will wait for the user at '>' mark.
### User will start to enter the command fronm this mark. \
### If a command that is not recognizable by the console (One which is not defined) the consloe will prompt the user with "Command not Recognized" and the again will stay at '>'

## The Command File

### The commands will be handled, all commands in a seperate python file. 
### This is the only file that will have a direct access to the CSV file.
### The commands to this file will be given through the main.py
### This file will do the necessary changes to the CSV file and return a confirmation message to main.py.
### Each command will be handled in a seperate function. 
### The command file won't have any main function. 
### Following are the commands and what will they do

## The Commands

### ts add (Add task):
    Once this command is fetched by the command file, the command file will prompt the user with an interface for the details of the task to be entered. 
    This interface will ask the user to enter the exact task, the priority of the task, the due date of the task and the due time of the task, and for repetition.
    Once these fileds are entered, the task will be added to the CSV file.
    User can just see the discription he entered on the console. and the serial number. 
    The serial number will be alloted according to the priority of the task.

### ts view (List down taks):
    This command will list down all the tasks of the day to the user. 
    The task that are incomplete will be listed first according to their priority
    Task's completed will be displayed at the very end with the order thay were completed (With a strike if possible)

### ts vall (List down all the tasksfor the comming week):
    This command will list down all the tasks for the comming next 7 days. 
    The tasks that are incomplete will be listed first with the date and priority order.
    Under the same date, the completed tasks will also be displayed in the order they are completed.


### ts slec (To select a particular task according to its serial number in the list)
    This command selects the task specified in the list
    The command needs a arguement to be provided.
    If no arguement is provided, the command asks the user to specify the task number.
    If the task number is not in the list, the command asks to select a valid and exisiting serial number.

### ts asprior (Assigns priority to the selected task):
    This command will assign the priority to the task that has been selected.
    Here priority will be H (for high), M (For med) and L (for low).
    Once the priority is been alloted to a task, the task will be then moved up or down as per it's position in the list.

### ts sch (To allot a due date and time to the task):
    This command will prompt the user to (assign) change the scheduled day and time of the selected task.

### ts mkcom (To mark a task completed):
    This command marks the selected task completed and removes it from the list.

### ts rm (Removes the selected task):
    This command removes the selected task from the list, not matter whether it is completed or not.
    Before removing, the command will confirm from the user that it wants to, specifically remove the task or not. 

### ts comp (Lists down the completed tasks):
    Lists down the completed tasks of the day in the order they are completed.
    The completed tasks won't be shown on the screen, hence to view them, this command is necessary

### ts rep (Repeat a task):
    This command helps to set a repeater to the selected task.
    The command asks for the start date and the end date, for, when to start the repetiotion ad when to end it. 
    The task will be added to the everyday list till the last date specified


## The CSV File
### This CSV file will store the data of the tasks entered by the user. 
#### Eg. Task_Serial_Number | Task_ID | Task_Priority | Entry_Date | Entry_Time | Due_Date | Due_Time | Completion_Date | Completion_Time | Removal_Date | Removal_Time
### The command will be responsible for any change of data in the CSV file.. 
### Everything regarding the a particular task will be fetched from the CSV file only.
### A hidden and secured copy of the CSV file will be maintained without the user knowing it on the users device. SO if any manual changes are made to the CSV file, the changes can be undone by refrencing the the hidden CSV

## Add a 'help' command


Additions
To check every time during input if the user wants to exit or not.. Even in the Commands file.. 
