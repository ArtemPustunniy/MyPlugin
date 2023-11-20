# Plugin `CheckList`

#### This plugin is designed for busy developers who do not want to miss any of the assigned tasks and complete their tasks on time.

# This plugin includes the following functionality:
##  Available hotkeys:
1. Open your CheckList(**Cntrl + 1 Cntrl + 2**)
2. Create a new CheckList(**Cntrl + '**)
3. Completely remove existing CheckList (**Cntrl + 1 Cntrl + 1**)

# Describing:
### When you open CheckList, a window opens that displays a list of your tasks. In the upper right corner of the window there is a toolbar with three functional buttons:
1. `addButton` This button is responsible for adding a new task to the CheckList. Each task must begin with its serial number. For example, "1 Start".
2. `correctButton` This button is responsible for confirming the changes made.
3. `delButton` This button is responsible for deleting a specific task. 

# Step-by-step instructions for the user:
### Creating a new CheckList instance:
1. To create a new CheckList instance, you need to press the hotkey combination Cntrl + '. After this, a message will appear in the lower right corner of your screen notifying you
  about the successful creation of a new instance. The inscription has the following content: "Your CheckList was succesfully created!".
### Working with an existing CheckList.
1. To access an existing CheckList instance, you need to press the hotkey combination Cntrl + 1 Cntrl + 2. After this, a new window will open at the top center of your screen, which initially will not contain anything except an empty input field and a toolbar at the top of this window.
2. To add a new task to your CheckList, you must enter the task in the input field. It is necessary that it either begins with a unique key, for example, with a task number, or simply has a unique value, since there cannot be two identical tasks. For the fastest and most accurate removal, the first option is recommended. After this, you need to press the `addButton` button in the toolbar. After this, the program will process your task and add it to your CheckList.
3. To delete a completed task, you can do one of the following steps:
   1) Enter the unique number that the completed task has, and when it is highlighted in blue, simply press the `delButton`. After this, the task will be deleted. A notification about this will be displayed in a pop-up window at the bottom of the screen.
   2) Start entering the content of the completed task. If a task has a unique value, then only that one will be deleted. If several tasks have a similar beginning, then you need to find the one you need in your CheckList and click on it with the left button of the computer mouse. After that, press the `delButton` button in the toolbar. After this it will be deleted. 
### Removing the entire CheckList:
1. To delete the entire CheckList, you need to press the hotkey combination Cntrl + 1 Cntrl + 1. After this, a notification about successful deletion will be displayed in the lower right corner of the screen.

# The plugin manifest is written in the `package.json` file

# Description of JS functions responsible for the operation of the plugin. These functions are written in the JS file `extension.js`:
### The activate function, which will be called if the plugin was activated by an event specified in the manifest. Inside it, plugin commands are registered, which are written in package.json in the list of “activationEvents” commands. Commands:
1. Registering the `owlscheck.startOwlsCheck` command. The result is a notification displayed on the screen.
2. Registering the `owlscheck.deleteCheckList` command. The result is a notification displayed on the screen and in the console.
3. Registering the `owlscheck.openCheckList` command:
   + At this stage, the CheckList window is created. A field for entering tasks is created, as well as toolbar buttons.
   + After creating the toolbar, all the functionality that the CheckList has is spelled out.
   + The event parameter defines the selection of a button, which, when pressed, executes certain logic.
   + After defining an event, an action is selected: deleting, adding a new task, or confirming the action.
### The deactivate function, which will be called if the plugin was activated by an event not from the manifest (it is not necessary to write anything here, since if launched unexpectedly, the plugin should not perform any actions)
Author: **Pustynnyj Artem Sergeevich(M3114)**  
My GitHub: `https://github.com/ArtemPustunniy`