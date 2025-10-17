# PowerShell-Tips

```
Today's Powershell tip is:
 
Out-GridView or OGV, this will output into a separate window that you can search & read in
 
Example Command: Get-Command | OGV (This will show all available commands in your powershell session in the grid view)
```


```
Today's Powershell tip is:
 
Get-Help, (The standard cmdlet format is Verb-Noun) this will display help for any cmdlet as long as there are help files available. Furthermore, you can add the -showwindow parameter to more easily see the full documentation.
 
Example Command: Get-Help Get-Member -showwindow
```


```
Today's Powershell tip is:
 
ConvertTo-Json: This will convert your object to a json
 
Example Command:    
PowerShell
    $myObject = @{
        Name = "John Doe"
        Age = 30
        City = "Tampa"
    }
    $myObject | ConvertTo-Json
```


```
Today's Powershell tip is:
CTRL + R in the powershell terminal, you can then search your previous commands, especially if you use UVPy and are looking for a command you used previously. If you want to find the next instance of your search, continue pressing CTRL + R after entering your search. Pressing CTRL + S will go backwards one option (or forward depending on how you look at it)
```


```
Today's Powershell tip is:

Set-Clipboard, You can use this to add the output of your statement to your clipboard
 
Example: Get-ChildItem |OGV -passthru | Set-Clipboard
This will Get-ChildItem (the alias for this command is ls or dir), then output to gridview, the passthru flag will allow you to select one or multiple items from the grid view. After pressing "Ok" it will add your selection to the clipboard
```


```
Today's Powershell tip is:
 
Array Lists, you can use array lists when you will be adding or removing from the list frequently 
 
Example: Here is how you would declare a new array list instead of an array
 
$myArrayList = New-Object -TypeName System.Collections.ArrayList
```


```
Today's Powershell tip is:
 
Get-Content, This cmdlet retrieves the content of an item at a specified path such as a text file. You can store this in a variable to use later such as for comparing with Compare-Object
 
Example command: Get-Content -Path "C:\Path\To\YourFile.txt"
 
```


```
Today's Powershell Tip is:
 
Get-Date, This will.... Get the current date and time!
 
Example command: (Get-Date).AddDays(-90) This will display the date -90 days from today (90 days in the past)
 
If you would like the date format as dd/mm/yyyy, you can use the following command 
 
(Get-Date).AddDays(-90).ToString("MM/dd/yyyy")
 
```


```
Today's Powershell tip of the day is:
 
You can drag a file or folder from the File Explorer into PowerShell to get the full path!
```

```
Today's Powershell tip of the day is:
 
ls env:, this will let you see all of the environment variables on your system
 
To view the value of one of the environment variables use, $env:PATH. You can also wrap the text better for the first command using ls env: |Format-table -wrap -autosize
```

```
Today's Powershell tip of the day is:



Select-Object *, When an object is written to the console, PowerShell by default hides many of its properties. This is to make the output easier to read, but it can hide many useful properties that you may not know exist.



Example Command: Get-Process | Select-Object -First 1 * vs Get-Process | Select-Object -First 1. The * will give many more properties
```
