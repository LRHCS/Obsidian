 #batch #if_else   

```batch
:: the normal compare
if 1 == 1 (
	echo true
)

:: compare with a variable
set p = 1
if p == 1 (
	echo true
)
:: at this on it see if the test.txt exist if yes it will writ the things in test.txt and open the file up, else it will return a error
if exist test.txt (

    echo exist

    echo This is a test> test.txt

    echo 123>> test.txt

    echo 245.67>> test.txt

    start test.txt

) else (

    echo Error

)
```