﻿# Task-Tracker
https://roadmap.sh/projects/task-tracker-js

# Task Tracker

A simple Task Tracker web application built with HTML, CSS, and JavaScript, allowing users to create tasks, mark them as complete, and delete them. The completed tasks are automatically moved to the end of the list with a strikethrough effect.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [File Structure](#file-structure)
- [Setup Instructions](#setup-instructions)
- [Code Documentation](#code-documentation)
  - [HTML Structure](#html-structure)
  - [CSS Styling](#css-styling)
  - [JavaScript Functionality](#javascript-functionality)
    - [Adding Tasks](#adding-tasks)
    - [Toggling Task Completion](#toggling-task-completion)
    - [Deleting Tasks](#deleting-tasks)
    - [Rendering Tasks](#rendering-tasks)

## Features
- Add new tasks to the list.
- Toggle task completion using checkboxes.
- Delete tasks using the delete button.
- Completed tasks move to the bottom and are shown with a strikethrough.

## Technologies Used
- **HTML** - For the basic structure.
- **CSS** - For styling the interface.
- **JavaScript** - For task management functionality.

## File Structure
- `index.html` - Main HTML file containing the structure and JavaScript code.
- `style` - Inline CSS styling for the application.

## Setup Instructions
1. Clone or download the repository.
2. Open the `index.html` file in a web browser to start using the Task Tracker.

## Code Documentation

### HTML Structure
The HTML structure consists of:
- A `div` with the class `task-tracker` that serves as the main container.
- A `h2` tag for the application title.
- A `div` with the class `task-input` containing:
  - An `input` field for entering task descriptions.
  - A button to add tasks to the list.
- An unordered list (`ul`) with the ID `taskList` to display all tasks.

### CSS Styling
The CSS styles provide a clean and minimalistic look:
- Basic layout styling for centering the `task-tracker` container.
- Custom styling for `task-input`, `task-item`, and various interactive elements.
- Styles for completed tasks include `text-decoration: line-through` and a lighter color.

### JavaScript Functionality
The JavaScript handles the main task management functionalities. 

#### Adding Tasks
1. The `addTask` function:
   - Retrieves and trims the input value from `taskInput`.
   - Pushes a new task object (containing `description` and `completed` properties) to the `tasks` array if the input is valid.
   - Calls `renderTasks` to update the displayed task list.

2. The `Enter` key event listener:
   - Adds a task when the `Enter` key is pressed in the input field.

#### Toggling Task Completion
1. The `toggleComplete` function:
   - Toggles the `completed` status of a task based on its index.
   - Calls `renderTasks` to refresh the task list.

#### Deleting Tasks
1. The `deleteTask` function:
   - Removes a task from the `tasks` array by its index.
   - Calls `renderTasks` to update the displayed list.

#### Rendering Tasks
1. The `renderTasks` function:
   - Clears the current task list (`taskList`).
   - Sorts the `tasks` array to place incomplete tasks at the top.
   - For each task in `sortedTasks`, it:
     - Creates a list item (`li`) and assigns the appropriate classes based on task completion status.
     - Adds a checkbox to toggle completion, the task description, and a delete button.
     - Appends each task item to the `taskList` unordered list.

---

