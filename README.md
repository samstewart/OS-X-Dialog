## Summary
*osx_dialog* is a simple tool which allows developers to easily collect user input via GUI dialog boxes on Mac OS X. It uses AppleScript to show the dialogs but wraps everything in an accessible bash interface.

## Usage
Using *osx_dialog is simple, simply include the dialog functions via "source" command:
`source osx_dialog.sh`

Each dialog is wrapped in a unix function declaration for maximum modularity so you only need call the function and handle the result.

## Example

    user_confirm=$(confirm_dialog "Sure to delete?")

This calls the `confirm_dialog` function to show a confirmation dialog with the prompt "Sure to delete?". The result (0 or 1) is stored in the `user_confirm` variable.

### Available Dialogs
You can display three different types of dialogs.
    1. Folder Dialog
    2. Text input dialog
    3. Confirm dialog

### Folder Dialog
The `folder_dialog` function simply allows the user to choose a folder from their file system. It consumes no arguments and simply returns the absolute folder path.

### Text Input Dialog
The `text_dialog` shows a dialog prompting the user for a single line of input. It accepts one parameter which sets the prompt text and returns the users response.

### Confirmation Dialog
The `confirm_dialog` simply shows an alert with an "OK" or "Cancel" button and returns 1 or 0 respectively. It accepts one parameter which sets the prompt text.