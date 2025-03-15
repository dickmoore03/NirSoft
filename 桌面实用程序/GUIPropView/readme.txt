


GUIPropView v1.31
Copyright (c) 2016 - 2025 Nir Sofer
Web site: https://www.nirsoft.net



Description
===========

GUIPropView displays extensive information about all windows currently
opened on your system. The upper pane of GUIPropView displays all top
level windows, and when you select a window in the upper pane, the lower
pane displays the list of all child windows of the selected top level
window.
You can also select one or more windows and then do some actions on them
like close, hide, show, minimize, maximize, disable, enable, and so on...

Be aware that GUIPropView is a replacement for my very old WinLister tool.



System Requirements
===================

This utility works on any version of Windows, starting from Windows XP
and up to Windows 11. Both 32-bit and 64-bit systems are supported.



Versions History
================


* Version 1.31:
  o Added 'Unicode' column, which specifies whether the window is
    Unicode (Yes) or ANSI (No).
  o Added 'Process User' and 'Process Elevated' columns.

* Version 1.30:
  o Added 'FocusKeyText' action to the /Action command, which sets
    the keybaord focus to the specified window and then sends keystrokes
    to this window according to the specfied text.
  o For example: this command sends 'RegEdit.exe' keystrokes to the
    Explorer 'Run' dialog-box:
    GUIPropView.exe /Action FocusKeyText "RegEdit.exe"
    Process:Explorer.exe Class:#32770 Title:Run Child.ID:1001
  o Added 'FocusKeyPress' action to the /Action command, which sets
    the keybaord focus to the specified window and then sends the
    specified key combination to this window.
  o For example: this command sends Ctrl+A (Select All) and Ctrl+C
    (Copy to the clipboard) to the opened window of Notepad:
    GUIPropView.exe /Action FocusKeyPress "Ctrl+A Ctrl+C"
    Process:notepad.exe Visible:Yes

* Version 1.26:
  o Added 'WindowCount' action to the /Action command, which returns
    the number of windows that match the specified properties.
  o Added /RunAsAdmin command-line option for running GUIPropView as
    administrator.

* Version 1.25:
  o Added 'Sort By' toolbar buttons.
  o Added 'Black Background' option (Under the View menu). When it's
    turned on, the main tables are displayed in black background and
    white text, instead of default system colors.

* Version 1.24:
  o Added 'Z-order' column to the top level windows list

* Version 1.23:
  o Added option to choose another font (name and size) to display in
    the main window.

* Version 1.22:
  o Added option to change the sorting column from the menu (TopLevel
    -> Sort By and Child -> Sort By). Like the column header click
    sorting, if you click again the same sorting menu item, it'll switch
    between ascending and descending order. Also, if you hold down the
    shift key while choosing the sort menu item, you'll get a secondary
    sorting.

* Version 1.21:
  o Added /Filter command-line option, which allows you to export
    into a file only the Windows that match the specified filter.
  o The filter is the same filter used for the /Action command, for
    example:
    GUIPropView.exe /shtml "c:\temp\windows1.html" /Filter
    Process:explorer.exe State:Normal

* Version 1.20:
  o Added 'Hide Windows Without Title' option (Under TopLevel menu).
  o Added some accelerator keys to the TopLevel menu.
  o Added 'Always On Top' option.

* Version 1.16:
  o Fixed bug: The TopMost action (/Action command) didn't work
    properly.
  o Fixed some high DPI mode issues.

* Version 1.15:
  o Added 'Put Icon On Tray' option.
  o Added 'Start As Hidden' option. When this option and 'Put Icon On
    Tray' option are turned on, the main window of GUIPropView will be
    invisible on start.

* Version 1.14:
  o Added 'Copy Clicked Cell' option to the right-click context menu,
    which copies to the clipboard the text of cell that you right-clicked
    with the mouse.

* Version 1.13:
  o Added new action to the /Action command-line option: 'BringToTop'.
  o Added 'Select All' and 'Deselect All' to the 'Column Settings'
    window.

* Version 1.12:
  o /Action command now returns a value that specifies whether the
    action succeeded or failed: 0 = Action Succeeded, 1 = The specified
    action is invalid, 2 = Cannot find any window that matches the
    specified properties

* Version 1.11:
  o Added new actions to the /Action command-line option:
    MouseClickPos and MouseDblClickPos.

* Version 1.10:
  o Added /Action command-line option - powerful command that allows
    you to do many things (Hide, show, disable, enable, and more...) on
    the desired windows, according to their properties (Class Name,
    Title, Process, and so on...)

* Version 1.07:
  o Fixed bug: clicking the column header of the lower pane (child
    windows) sorted the column of the upper pane.

* Version 1.06:
  o Added /cfg command-line option to start GUIPropView with the
    specified config file.
  o Added 'Add Header Line To CSV/Tab-Delimited File' option (Turned
    on by default).

* Version 1.05:
  o Added 'Font Name' and 'Monitor' columns.

* Version 1.00 - First release.



Start Using GUIPropView
=======================

GUIPropView doesn't require any installation process or additional DLL
files. In order to start using it, simply run the executable file -
GUIPropView.exe After running GUIPropView, the main window displays the
list of windows currently opened on your system. The upper pane of
GUIPropView displays all top level windows, while the lower pane lists
the child windows of the top-level window you choose in the upper pane.
By default, GUIPropView doesn't display the invisible top level windows,
but you can change it by turning on the 'Display Hidden Windows' and
'Display Windows With (0, 0) Size' options (Under the TopLevel menu).



Using the target icon
=====================

In order to find a specific window inside GUIPropView, simply drag the
target icon on the toolbar into the window you want to inspect.
GUIPropView will automatically select the top level window (in the upper
pane) and then the child window (in the lower pane)



Columns of Top Level Windows
============================


* Handle:Handle of the window.
* Title:Title of the window.
* State:State of the window (Normal, Minimized, Maximized).
* Visible:Specifies whether the window is visible (Yes or No).
* Position:The position of the window (Left, Top).
* Size:The size of the window (Width, Height).
* Class Name:The name of the window class.
* Style:Window style information (Popup, Child, Overlapped, Top Most,
  Tool Window, App Window, Transparent)
* Process ID:ID of the process that created this window.
* Thread ID:ID of the thread that created this window.
* Parent Handle:Handle of the parent window.
* Process Filename:Procoss filename according to the process ID.
* Process User:The user name of the process that created the window.
* Process Elevated:Displays 'Yes' if the process is elevated ('Run As
  Administrator')
* Instance Filename:Instance Filename according to the instance handle
  of this window.
* Class Module Filename:Class module filename according to the class
  module handle of this window.
* Style Value:Style value as hexadecimal number.
* ExStyle Value:Extended style value as hexadecimal number.
* Instance Handle
* Class Module Handle
* Class WNDPROC Address
* Class Atom
* Font Name
* Monitor
* Unicode



Columns of Child Windows
========================


* Handle:Handle of the window.
* Parent Handle:Handle of the parent window.
* Text:Text stored or displayed by this window.
* Enabled:Specifies whether the window is enabled (Yes or No)
* Visible:Specifies whether the window is visible (Yes or No).
* Position:The position of the window (Left, Top).
* Size:The size of the window (Width, Height).
* Class Name:The name of the window class.
* Process ID:ID of the process that created this window.
* Thread ID:ID of the thread that created this window.
* ID:ID of the window.
* Style Value:Style value as hexadecimal number.
* ExStyle Value:Extended style value as hexadecimal number.
* Instance Handle
* Class Module Handle
* Class WNDPROC Address
* Class Atom
* Process Filename:Procoss filename according to the process ID.
* Instance Filename:Instance Filename according to the instance handle
  of this window.
* Class Module Filename:Class module filename according to the class
  module handle of this window.
* Z-order:Numeric value that represents the Z-order of the child
  windows.
* Font Name
* Unicode



/Action Command-Line Option
===========================

/Action is a powerful command that allows you to do many things (Hide,
show, disable, enable, and more...) on the desired windows, according to
their properties (Class Name, Title, Process, and so on...)

The general syntax of the /Action command:
/Action [Action] {Action Parameters} [Property1:Value1]
[Property2:Value2] [Property3:Value3]....

The following actions are available:
* WindowCount - Returns the number of windows that match the specified
  properties.
* Show - Make the specified windows visible
* Hide - Make the specified windows invisible.
* HideSwitch - Make the specified windows visible if they are hidden
  and make the specified windows invisible if they are visible.
* HideShow - Hide the window and then show it again.
* Close - Close the specified windows.
* SetText [Window Text] - Set the text or title of the specified
  windows.
* Disable - Disable the specified windows.
* Enable - Enable the specified windows.
* Maximize - maximize the specified windows.
* Minimize - minimize the specified windows.
* Center - center the specified windows.
* TopMost - Make the specified window top most.
* NoTopMost - Make the specified window non-top most.
* TopMostSwitch - Switch between top-most and non-top-most state.
* Focus - Set the focus to the specified child window.
* SwitchTo - Switch to the specified window.
* BringToTop - Bring the window to the top, without setting the focus
  to this window.
* Flash [Count] [Flash Rate] - Flash the specified window. [Count]
  specifies the number of times to flash and [Flash Rate] specifies the
  flash rate in milliseconds.
* DisableTaskbarGrouping - Disable the taskbar grouping of the
  specified windows.
* EnableTaskbarGrouping- Enable the taskbar grouping of the specified
  windows.
* ButtonClick - Click the specified button (Works only for standard
  button/check-boxes of Windows, it's done by sending BN_CLICKED message)
* MouseClick [Button] - Send mouse-click message to the specified
  window. In the [Button] parameter you should specify Left,Right, or
  Middle.
* MouseClickPos [Button] [x] [y] - Send mouse-click message to the
  specified window at the X,Y position. In the [Button] parameter you
  should specify Left,Right, or Middle.
* MouseDblClickPos [Button] [x] [y] - Send mouse double-click message
  to the specified window at the X,Y position. In the [Button] parameter
  you should specify Left,Right, or Middle.
* Style [Add | Remove | Set] [Style Value] - Add, remove or set the
  Style of window. You should specify the [Style Value] as hexadecimal
  number.
* ExStyle [Add | Remove | Set] [Style Value] - Add, remove or set the
  ExStyle of window. You should specify the [Style Value] as hexadecimal
  number.
* Transparent [Alpha | Color] [Value] - Make the window transparent.
  There are 2 modes: Alpha and Color. On Alpha mode, you should specify a
  value between 0 (completely transparent) and 255 (opaque). On Color
  mode - only the specified color will be transparent. The color is
  specified as hexadecimal number (e.g: 80FFFF).
* SendCommand [Command ID] - Send WM_COMMAND message with the specified
  ID in order to execute the desired menu item. In order to find the
  correct Command ID, you can use the Spy++ tool of Microsoft or any
  other tool that hooks the WM_COMMAND message. You can also use the
  TraceMenuID of NirSoft to get the IDs of menu items.
* SendCommandChild [Command ID] - Similar to SendCommand, but it also
  send the WM_COMMAND message to all child Windows.
* SetSize [Width] [Height] - Set the width and height of the specified
  window.
* ChangeSize [Width Change] [Height Change] - Change the width and
  height of the specified window. For example, if you specify ChangeSize
  10 -10 , 10 pixels will be added to the current width and 10 pixels
  will be subtracted from the current height.
* SetPos [Left] [Top] - Set the top and left position of the specified
  window.
* ChangePos [Left Change] [Top Change] - Change the top and left
  position of the specified window.
* SetFont [Font Name, Font Size, Font Weight, {Italic}, {Underline}] -
  Set the font of the specified window. Setting a font only works for
  standard Windows controls. Also, the font is created by running code
  inside the process that owns the window, so if the process is 64-bit,
  you should use the 64-bit version of GUIPropView. Here's some example
  for font strings you can specify in SetFont: "Segoe Print,10,400"
  "Arial,12,700,Italic" "Arial,12,400,Underline" (The font string must be
  in quotes !)
* FocusKeyText [Keyboard Text] - Set the keyboard focus to the
  specified window and then send keystrokes to this window according to
  the specfied text.
* FocusKeyPress [Key Combination] - Set the keybaord focus to the
  specified window and then sends the specified key combination to this
  window. You can use multiple key combinations in one command ,
  delimited by space character (but the entire key combination string
  must be in quotes !), for exmaple: "Alt+Ctrl+P Ctrl+S" , "Ctrl+Shift+A
  X Y Z".
  You can use the following keys in the Key Combination string:
  0-9,A-Z,F1-F24,shift,leftshift,rightshift,ctrl,leftctrl,rightctrl,alt,lef
  tmenu,rightmenu,enter,esc,spc,down,up,left,right,home,end,
  insert,delete,plus,comma,minus,period,lwin,rwin,apps,pageup,pagedown,tab,
  multiply,add,subtract,seperator,divide,cancel,backspace,pause,capslock,nu
  mlock,scroll,printscreen.
  Alternatively, you can also specify the virtual key code instead of key
  name, as decimal number or hexadecimal number, for example: "Ctrl+65" ,
  "Ctrl+0x41"

The Property:Value section specifies the properties of the windows to
find for doing the desired action. For example, if you want to do
something on all Explorer windows, you should specify -
Class:CabinetWClass Process:Explorer.exe
Here's the basic rules for using the Property:Value section:

* You can specify multiple Property:Value entries.
* When there is a space inside the value, you must put the entire
  Property:Value entry in quotes (For example: "Title:My Title")
* For string properties (Class, Title) you can specify wildcard (For
  example: Title:*Google* )
* For integer properties (ID, ZOrder, Width, Height) you can specify
  multiple numbers in comma-delimited list (For example: 1,2,5) or
  specify range using colon character (For example, width between 50 and
  100 - Width:50:100 )
* For boolean properties (Visible, Enabled) you can specify Yes/No, 1/0
  , or True/False.
* If you want to do an action on child window, you should specify the
  properties of the top-level window first, and then the child window,
  using 'Child.' prefix in the property name. For example, if you have
  top-level window that its class name is MyClass and you want to disable
  its child window with ID=1005:
  Disable Class:MyClass Child.ID:1005

The following properties are available:
* Visible - Specifies whether the desired windows are visible (Yes or
  No).
* Enabled - Specifies whether the desired windows are enabled (Yes or
  No).
* Class - Specifies the class name of the desired windows. Wildcard is
  allowed.
* Title - Specifies the title or text of the desired windows. Wildcard
  is allowed.
* Text - The same as the Title property.
* Process - Specifies the process ID or process filename of the desired
  windows.
* ID - Specifies the ID of the desired windows. This property is useful
  for child windows (Child.ID)
* Atom - Specifies the class Atom of the desired windows.
* Thread - Specifies the Thread ID of the desired windows.
* ZOrder - Specifies the ZOrder of the desired windows.
* Width - Specifies the width of the desired windows, in pixels. You
  can specify range, for example: Width:50:100
* Height - Specifies the Height of the desired windows, in pixels. You
  can specify range, for example: Height:50:100
* Top - Specifies the top position of the desired windows. You can
  specify range, for example: Top:50:100
* Left - Specifies the left position of the desired windows. You can
  specify range, for example: Left:50:100
* Monitor - Specifies the monitor name where the desired windows are
  located.
* Handle - Specifies the handle of the desired Window as Hexadecimal
  number. You can specify multiple handles as comma delimited list
  (Handle:004707F6,00320C62)
* State - Specifies the State of the desired Window (Minimized,
  Maximized, or Normal).
For every property, you can specify 'Child.' prefix (e.g: Child.Class) if
you want to do the action on child windows.

Here's some examples for using the /Action command:
* Disable start button on Windows 7: (On Windows 7, the start button is
  a top-level window)
  GUIPropView.exe /Action Disable Process:Explorer.exe Class:Button
  Title:Start Visible:Yes Width:40:60
* Disable start button on Windows 10: (On Windows 10, the start button
  is a child window)
  GUIPropView.exe /Action Disable Class:Shell_TrayWnd Child.Class:Start
  Child.Width:40:60
* Minimize all Explorer windows:
  GUIPropView.exe /Action Minimize Class:CabinetWClass
  Process:Explorer.exe Visible:Yes
* Close all Explorer windows:
  GUIPropView.exe /Action Close Class:CabinetWClass Process:Explorer.exe
  Visible:Yes
* Change the style of all opened Explorer windows to tool window style
  (WS_EX_TOOLWINDOW = 00000080)
  GUIPropView.exe /Action ExStyle Add 00000080 Class:CabinetWClass
  Process:Explorer.exe Visible:Yes
* Click the Browse button of the Explorer 'Run' dialog-box:
  GUIPropView.exe /Action ButtonClick Process:Explorer.exe Class:#32770
  Title:Run Child.ID:12288
* Put 'Hello World' in the filename text-box of the Explorer 'Run'
  dialog-box:
  GUIPropView.exe /Action SetText "Hello World" Process:Explorer.exe
  Class:#32770 Title:Run Child.ID:1001
* Hide the status bar of the GUIPropView tool:-)
  GUIPropView.exe /Action Hide Class:GUIPropView
  Child.Class:msctls_statusbar32
* Disable task bar grouping of all opened Firefox Windows:
  GUIPropView.exe /Action DisableTaskbarGrouping Class:MozillaWindowClass
  Visible:Yes
* Close Firefox window opened in NirSoft Web site:
  GUIPropView.exe /Action Close Class:MozillaWindowClass Visible:Yes
  Title:NirSoft*
* Close all windows on monitor \\.\DISPLAY2
  GUIPropView.exe /Action Close Monitor:\\.\DISPLAY2
* Make the window of Notepad a little transparent:
  GUIPropView.exe /Action Transparent Alpha 220 Class:Notepad
* Switch to 'Large Icons' mode in all opened Explorer Windows:
  GUIPropView.exe /Action SendCommand 28751 Class:CabinetWClass
  Child.Class:ShellTabWindowClass
* Increase the width of the Run dialog-box of Windows Explorer and the
  combo-box inside it (ID=12298) by 250 pixels:
  GUIPropView.exe /Action ChangeSize 250 0 Process:Explorer.exe Title:Run
  GUIPropView.exe /Action ChangeSize 250 0 Process:Explorer.exe Title:Run
  Child.ID:12298
* Change the font of GUIPropView ( upper and lower panes):
  GUIPropView.exe /Action SetFont "Segoe Print,10,400" Class:GUIPropView
  Visible:Yes Child.Class:SysListView32
* Double-click the icon on the desktop at position (20,20)
  GUIPropView.exe /Action MouseDblClickPos Left 20 20 Visible:Yes
  Process:Explorer.exe Class:Progman Child.Class:SysListView32
* Right-click the icon on desktop at position (20,20)
  GUIPropView.exe /Action MouseClickPos Right 20 20 Visible:Yes
  Process:Explorer.exe Class:Progman Child.Class:SysListView32
* Get the number of visible Firefox windows (The value is returned in
  %errorlevel% variable)
  GUIPropView.exe /Action WindowCount Process:firefox.exe Visible:Yes
* Send 'RegEdit.exe' keystrokes to the Explorer 'Run' dialog-box:
  GUIPropView.exe /Action FocusKeyText "RegEdit.exe" Process:Explorer.exe
  Class:#32770 Title:Run Child.ID:1001
* Send Ctrl+A (Select All) and Ctrl+C (Copy to the clipboard) to the
  opened window of Notepad:
  GUIPropView.exe /Action FocusKeyPress "Ctrl+A Ctrl+C"
  Process:notepad.exe Visible:Yes



/Action Return Value
====================

When using /Action , GUIPropView.exe returns one of the following values:
(You can get the return value from %errorlevel% in a batch file)
* 0 - Action Succeeded
* 1 - The specified action is invalid.
* 2 - Cannot find any window that matches the specified properties.

Example for batch file that shows the return value: (You have to put the
text below inside .cmd file and then run it inside command-prompt window)
GUIPropView.exe /Action Minimize Class:MozillaWindowClass Visible:Yes
echo %errorlevel%

If you specify 'WindowCount' as the action, then the return value is the
number of windows that match the specified properties.



Save Command-Line Options
=========================



/ParentWindow <Window Handle>
If this parameter is specified with the other save parameters (/stext,
/scomma, and so on) then the GUIPropView will export the child windows
list of the specified window, for example:
GUIPropView.exe /ParentWindow 00C00A34 /scomma "c:\temp\child.csv"

If this parameter is not specified, GUIPropView will export the top-level
windows list.

/stext <Filename>
Save the windows list into a simple text file.

/stab <Filename>
Save the windows list into a tab-delimited text file.

/scomma <Filename>
Save the windows list into a comma-delimited text file (csv).

/stabular <Filename>
Save the windows list into a tabular text file.

/shtml <Filename>
Save the windows list into HTML file (Horizontal).

/sverhtml <Filename>
Save the windows list into HTML file (Vertical).

/sxml <Filename>
Save the windows list into XML file.

/sort <column>
This command-line option can be used with other save options for sorting
by the desired column. The <column> parameter can specify the column
index (0 for the first column, 1 for the second column, and so on) or the
name of the column, like "Record ID" and "Event ID". You can specify the
'~' prefix character (e.g: "~Channel") if you want to sort in descending
order. You can put multiple /sort in the command-line if you want to sort
by multiple columns.



/Filter [Property1:Value1] [Property2:Value2] [Property3:Value3]....
This command allows you to export only the Windows that match the
specfied filter. It's the same filter used in the /Action command.

For example, the following command saves the top-level Windows of
explorer.exe process in Normal state to html file:
GUIPropView.exe /shtml "c:\temp\windows1.html" /filter
process:explorer.exe State:Normal

The following command exports all child Windows that their class is
'Button' to comma-delimited file:
GUIPropView.exe /scomma "c:\temp\windows1.csv" /filter Visible:Yes
Child.Class:Button

/cfg <Filename>
Start GUIPropView with the specified configuration file. For example:
GUIPropView.exe /cfg "c:\config\gpv.cfg"
GUIPropView.exe /cfg "%AppData%\GUIPropView.cfg"

/RunAsAdmin
Runs GUIPropView as administrator.



Translating GUIPropView to other languages
==========================================

In order to translate GUIPropView to other language, follow the
instructions below:
1. Run GUIPropView with /savelangfile parameter:
   GUIPropView.exe /savelangfile
   A file named GUIPropView_lng.ini will be created in the folder of
   GUIPropView utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run GUIPropView, and all
   translated strings will be loaded from the language file.
   If you want to run GUIPropView without the translation, simply rename
   the language file, or move it to another folder.



License
=======

This utility is released as freeware. You are allowed to freely
distribute this utility via floppy disk, CD-ROM, Internet, or in any
other way, as long as you don't charge anything for this and you don't
sell it or distribute it as a part of commercial product. If you
distribute this utility, you must include all files in the distribution
package, without any modification !



Disclaimer
==========

The software is provided "AS IS" without any warranty, either expressed
or implied, including, but not limited to, the implied warranties of
merchantability and fitness for a particular purpose. The author will not
be liable for any special, incidental, consequential or indirect damages
due to loss of data or any other reason.



Feedback
========

If you have any problem, suggestion, comment, or you found a bug in my
utility, you can send a message to nirsofer@yahoo.com
