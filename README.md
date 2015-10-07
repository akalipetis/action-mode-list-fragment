# Action Mode List Fragment
ListFragment implementation, for handling ActionMode showup and management using the AppCompat library and being backwards compatible to 2.1.

## Installation in Android Studio
The Action Mode List Fragment library is gradle-ready, having the required structrure, files and dependencies. You only have to add it as a module in Android Studio and it will plug-n-play! To do this, follow these steps:

1. Clone the project in a directory, or download the archive from the Downloads below.
2. Copy and paste the action\_mode\_list\_fragment folder, under your project folder
3. Go to project structure (CMD+Down Arrow on a Mac) and select your module (not the project)
4. Switch to dependencies tab and add action\_mode\_list\_fragment as a module dependency using the '+' sign located bottom left
5. Change settings.gradle to include the following: _include ':YOUR\_APPLICATION\_HERE', ':action\_mode\_list\_fragment'_

## Installation in Eclipse
Even though it was made for Android Studio, you can easily use the library with Eclipse too!

1. Clone the project in a directory, or download the archive from the Downloads below, or even add it as a submodule in your git repo.
2. Copy and paste the action\_mode\_list\_fragment folder, under your project folder
3. Import it as _Existing Android Source Code_
4. Go to project properties for __Action Mode List Fragment library project__ (CMD+I on a Mac), switch to Android tab on the left and include AppCompat library in your project. For a guide on how to add AppCompat library to your project, you can check this [link](http://developer.android.com/tools/support-library/setup.html)
5. Go to project properties for your __main project__ (CMD+I on a Mac), switch to Android tab on the left and add it as a library project.

## Usage
This library is used in conjunction with the AppCompat library that was recently released - while it can be easily transformed to play with Actionbar Sherlock too. In order for the library to function properly, you must remember to call the superclass functions at the beggining of the methods you @Override. Also, there is just one more thing to remember, if you use onListItemClick method, you have to check

	if getListView().getChoiceMode() == ListView.CHOICE_MODE_NONE ||  getListView().getChoiceMode() == ListView.CHOISE_MODE_SINGLE

and continue only if true, otherwise return, since this should be hanlded by the ActionMode.

## Example
The library includes an example showing some basic functionality and including a custom extension of RelativeLayout whihch is going to be needed in order to visually show the user his selections.

## Downloads
You can always download just the library, instead of cloning it. There are two versions, one for importing into Android Studio and one for Eclipse. You can find them below

1. [Android Studio](https://bitbucket.org/akalipetis/action-mode-list-fragment/downloads/android_studio.tar.bzip2)
2. [Eclipse](https://bitbucket.org/akalipetis/action-mode-list-fragment/downloads/eclipse.tar.bzip2)

### License
	The MIT License (MIT)
	 
	Copyright (c) 2013 Antonis Kalipetis <akalipetis@gmail.com>.
	
	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is
	furnished to do so, subject to the following conditions:
	
	The above copyright notice and this permission notice shall be included in
	all copies or substantial portions of the Software.
	
	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
	THE SOFTWARE.