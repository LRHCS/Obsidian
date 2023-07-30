#C  #Structure   
## Create a Structure
```C
struct MyStructure {   // Structure declaration  
  int myNum;           // Member (int variable)  
  char myLetter;       // Member (char variable)  
}; // End the structure with a semicolon

int main() {  
  struct myStructure s1; 
  return 0;  
}
```

## Access Structure Member
```C
// Create a structure called myStructure  
struct myStructure {  
  int myNum;  
  char myLetter;  
};  
  
int main() {  
  // Create a structure variable of myStructure called **s1**  
  struct myStructure s1;  
  
  // Assign values to members of s1  
  s1.myNum = 13;  
  s1.myLetter = 'B';  
  
  // Print values  
  printf("My number: %d\n", s1.myNum);  
  printf("My letter: %c\n", s1.myLetter);  
  
  return 0;  
}
```

## String in a Structure(With strcpy)
```C
struct myStructure {  
  int myNum;  
  char myLetter;  
  char myString[30]; // String  
};  
  
int main() {  
  struct myStructure s1;  
  
  // Assign a value to the string using the strcpy function  
  strcpy(s1.myString, "Some text");  
  
  // Print the value  
  printf("My string: %s", s1.myString);  
  
  return 0;  
}
```