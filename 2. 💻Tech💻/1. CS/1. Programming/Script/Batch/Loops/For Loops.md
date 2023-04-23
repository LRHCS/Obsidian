#batch   #loops   

```batch
::/l = list  first one is begin the second 1 is increment 123 is the end %%a is the variable
:: for /l {%%|%}<variable> in (<start#>,<step#>,<end#>) do <command> [<commandlinepptions>]
@echo off
for /l %%a in (1;1;123) do (
	echo %%a
)
```