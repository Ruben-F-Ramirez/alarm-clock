# Alarm Clock Program

## Overview
This project is a simple alarm clock implemented in C. It allows users to create and manage alarms using a linked list structure. Users can schedule alarms, edit existing alarms, cancel specific alarms, delete all alarms, and display scheduled alarms.

## Features
- **Initialize a New Alarm List:** Users can create a new list to store alarms.
- **Schedule a New Alarm:** Allows setting alarms with a specific time and days of the week.
- **Edit an Existing Alarm:** Users can modify an existing alarm time.
- **Cancel an Alarm:** Removes a specific alarm from the list.
- **Delete All Alarms:** Clears the entire list of alarms.
- **Display Scheduled Alarms:** Lists all the currently set alarms.
- **Exit the Program:** Terminates execution and frees allocated memory.

## File Structure
- `main.c`: Contains the implementation of the alarm clock program.
- `README.md`: Documentation for the project.

## Compilation and Execution
### Prerequisites
- A C compiler such as `gcc`.

### Steps to Compile and Run
1. Open a terminal and navigate to the project directory.
2. Compile the program using:
   ```bash
   gcc main.c -o alarm_clock
   ```
3. Run the executable:
   ```bash
   ./alarm_clock
   ```

## Menu Options
When the program runs, users can select from the following menu options:
```
1. Initialize a new list
2. Schedule a new alarm
3. Edit an alarm
4. Cancel an existing alarm
5. Cancel all alarms
6. Display the list of scheduled alarms
7. Exit
```

## Data Structures
The program uses a linked list to manage alarms:
```c
typedef struct node {
    struct node *next;
    int alarm_time;
    int day[LENGTH];
} node;
```
Each alarm stores:
- `alarm_time`: Time in military format (HHMM).
- `day[LENGTH]`: An array indicating the days of the week the alarm is set for.
- `next`: Pointer to the next alarm in the list.

## Functions
### Core Functions
- `bool createList(node **Headptr)`: Initializes a new alarm list.
- `bool insert(node **Headptr, int alarm, int *day)`: Inserts an alarm in chronological order.
- `void delete_list(node **Headptr)`: Deletes all alarms in the list.
- `void delete_alarm(node **head, int key)`: Removes an alarm based on time.
- `void Display(node **Headptr)`: Displays all scheduled alarms.
- `void alarm()`: Main function handling user interactions.

## Example Usage
```
Please type the number of the menu option you would like.
1. Initialize a new list
2. Schedule a new alarm.
3. Edit an alarm
4. Cancel an existing alarm
5. Cancel all alarms
6. Display the list of scheduled alarms
7. Exit
```
Users can enter the corresponding number to perform an operation.

## Author
Ruben Ramirez (ID: 0432694)

## License
This project is open-source and available for use under the MIT License.
