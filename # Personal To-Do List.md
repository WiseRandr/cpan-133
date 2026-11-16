# Personal To-Do List

## Description

A terminal-based task management application that allows users to fully manage personal to-do items from the command line through an interactive menu system. The program supports end-to-end task operations, including creating tasks with a title and optional details, viewing tasks in a clear numbered list, editing task content, deleting tasks, and marking tasks as complete or incomplete.

Tasks are organized for easier tracking using both date-based and category-based grouping, allowing users to review work by schedule and by type. The application uses file-based storage to persist all task data between sessions, ensuring that tasks remain available after the program closes. The interface is designed to be simple, fast, and beginner-friendly, with consistent prompts and straightforward navigation so users can manage their tasks efficiently without needing a graphical interface.

## List of Goals:

(By Josh)

- Allow users to add new tasks with a title.
- Support editing and deleting existing tasks.
- Save tasks to a file so they persist after closing the program.

(By Cyrus)

- Support marking tasks as completed or back in To-do.
- Allow users to group tasks by category. (a user will be able to create the group and then add the tasks to that group)

(By Wise)

- Build an interactive menu for task management.
- Keep the interface simple, fast, and beginner-friendly.
- Let users view all tasks in a clear, numbered list.

## Describe the responsibilities of each group member

### Josh - Task CRUD and Data Entry Flow

- Implement the core task creation workflow (add task title).
- Build edit and delete operations for existing tasks.
- Validate user input for task fields to prevent empty or invalid entries.
- Coordinate data format requirements with the persistence feature.

### Cyrus - Task Status, Grouping, and Persistence Support

- Implement marking tasks as complete or incomplete.
- Add category-based grouping and display logic.
- Implement and maintain task file save/load behavior with consistent formatting.
- Verify saved data remains accurate after updates, deletions, and status changes.

### Wise - Menu System and User Experience

- Build the interactive terminal menu and navigation flow.
- Implement the numbered list view for tasks.
- Connect menu options to all major features (add, edit, delete, complete, group, save/load).
- Keep the interface clean, readable, and beginner-friendly through consistent prompts and messages.

### Shared Team Responsibilities

- Define and agree on a single task data structure used across all features.
- Review each other's code and test merged features together.
- Resolve integration issues and keep documentation up to date.
- Prepare the final demo and presentation with clear feature ownership.
