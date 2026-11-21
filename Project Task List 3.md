# Project Task List 3

**Team members:** Wise and Josh

## 1. Project Topic

**Personal To-Do List Manager**

## 2. Main Purpose of the Script

A terminal-based script that helps users manage personal tasks through a simple interactive menu. Users can add, view, edit, and delete tasks; mark tasks as complete or incomplete; and view tasks by priority. Task data is saved in a text file so it remains available between sessions.

## 3. Menu Structure

```text
Personal To-Do List Manager
1. Add a new task
2. View all tasks
3. View tasks by priority
4. Edit a task
5. Delete a task
6. Mark a task as complete or incomplete
7. Exit
```

After an operation, the script returns to the main menu. Selecting Exit closes the script; successful changes are saved immediately.

## 4. List of Features

- **Automatic storage initialization:** Check for `todo.txt` when the script starts and create an empty file if it does not exist. Preserve existing task data when the file is already present.
- **Task creation / Add new task:** Append a new task with a unique ID, a required title or short description, optional details, and a priority of High, Medium, or Low. New tasks start with a To-do status.
- **Empty input validation:** Reject a task title or description that is empty or contains only whitespace, display an error message, and prompt the user again.
- **View all tasks:** Display tasks in a clear, numbered list showing each task's ID, title, priority, and completion status. Include optional details when provided.
- **View tasks by priority:** Ask the user to select High, Medium, or Low and display tasks matching that priority. Show a clear message if no tasks match.
- **Edit a task:** Allow the user to update an existing task's title, optional details, or priority using its task ID.
- **Task update validation:** Before editing, deleting, or changing a task's status, check that `todo.txt` contains tasks and that the selected task ID exists. Reject invalid selections with a clear error message. Validate edited titles and priorities before saving changes.
- **Delete a task:** Remove the selected task from storage and display a success message.
- **Task status management:** Allow users to mark a task as Complete or return it to To-do.
- **Persistent storage:** Load existing tasks when needed and save successful additions, edits, deletions, and status changes to `todo.txt`.
- **Menu and priority validation:** Reject unsupported menu options and priority selections, explain the accepted choices, and prompt again.

## 5. Required Input from the User

| Operation | Required input |
| --- | --- |
| Navigate the menu | A menu option from 1 to 7 |
| Add a task | A non-blank title or short description and a priority: High, Medium, or Low; details are optional |
| View all tasks | No additional input |
| View tasks by priority | A priority: High, Medium, or Low |
| Edit a task | An existing task ID, the field to edit, and its replacement value; titles must remain non-blank, details may be cleared, and priorities must be valid |
| Delete a task | An existing task ID |
| Change task status | An existing task ID and the desired status: Complete or To-do |
| Exit | Menu option 7 |

## 6. Expected Output

- An interactive main menu with clear prompts and consistent navigation.
- A numbered task list showing task IDs, titles, priorities, statuses, and any optional details.
- A filtered task list for the selected priority, or a message such as `No High-priority tasks found.`
- Confirmation messages after successful additions, edits, deletions, and status changes.
- Validation messages such as `Task description cannot be blank.`, `Invalid priority. Choose High, Medium, or Low.`, and `Task ID not found.`
- A message such as `No tasks available.` when a view or update is requested while storage is empty.
- Updated task data in `todo.txt`, available the next time the script runs.

Example task display:

```text
No.  Task ID  Title                     Priority  Status
1    1        Finish project proposal   High      To-do
2    2        Review class notes        Medium    Complete
```

## 7. File Names That Will Be Used or Created

| File name | Purpose |
| --- | --- |
| `todo.sh` | Main shell script containing the menu, task operations, validation, and storage logic |
| `todo.txt` | Task data file, created automatically by the script if missing; stores each task's ID, title, optional details, priority, and status |

## Team Responsibilities

### Josh — Task Creation, Editing, and Deletion

- Implement adding tasks with a title, optional details, and priority.
- Validate non-blank titles and accepted priority values during creation and editing.
- Implement editing and deleting tasks by ID.
- Check for empty storage and nonexistent task IDs before editing or deleting.
- Use the shared storage format for all changes and verify that unrelated tasks remain intact.

### Wise — Menu, Task Views, Status, and Storage

- Build the interactive menu, navigation, and menu input validation.
- Implement the numbered task list and priority-filtered view.
- Implement marking tasks Complete or To-do, including empty-storage and task-ID checks.
- Implement automatic creation of `todo.txt` and shared file loading and saving logic.
- Keep prompts, empty-list messages, and success and error messages clear and consistent.

### Shared Responsibilities

- Agree on a single task record format and a unique-ID strategy before implementation.
- Integrate Josh's task operations with Wise's menu and storage functions.
- Test missing and empty storage, blank titles, invalid priorities, nonexistent IDs, and persistence after restarting the script.
- Review each other's work, maintain project documentation, and prepare the final demonstration together.
