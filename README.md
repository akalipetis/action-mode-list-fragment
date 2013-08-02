# Action Mode List Fragment
ListFragment implementation, for handling ActionMode showup and management using the AppCompat library and being backwards compatible to 2.1.

## Installation
The Action Mode List Fragment library is gradle-ready, having the required structrure, files and dependencies. You only have to add it as a module in Android Studio and it will plug-n-play! To do this, follow these steps:

1. Clone the project in a directory.
2. Copy and paste the action\_mode\_list\_fragment folder, under your project folder
3. Go to project structure (CMD+Down Arrow on a Mac) and select your module (not the project)
4. Switch to dependencies tab and add action\_mode\_list\_fragment as a module dependency using the '+' sign located bottom left
5. Change settings.gradle to include the following:
_include ':YOUR\_APPLICATION\_HERE', ':action\_mode\_list\_fragment'_

## Usage
This library is used in conjuction with the AppCompat library that was recently released - while it can be easily transformed to play with Actionbar Sherlock too. In order for the library to function properly, you must remember to call the superclass functions just at the start of the methods you @Override. Also, there is just one more thing to remember, if you use onListItemClick method, you have to check if getListView().getChoiceMode() == ListView.CHOICE\_MODE\_NONE ||  getListView().getChoiceMode() == ListView.CHOISE\_MODE\_SINGLE and continue only if true, otherwise return since this should be hanlded by the ActinMode.

## Example
The library includes an example showing some basic functionality and including a custom extension of RelativeLayout whihch is going to be needed in order to visually show the user his selections.