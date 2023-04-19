#batch  #function   
```batch
CALL :basic_function
::seperate the Function Body and the main
EXIT /B %ERRORLEVEL% 

:: Function Body
:basic_function
SET n=Harry
ECHO My name is %n%
```