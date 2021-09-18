# CXX-ClangFormat
The ClangFormat configuration for all Chrones projects

**Why would you want to use that?** \
Every modern and professional project needs guidelines on how the code is formatted and ect. Chrones provides it's own configuration file, which we think is the most clean and modern code style.

# Guidelines

## Naming Convetion
```cpp
// aNyCase for specific macros
#define mAcRooo 

// UPPERCASE followed with PascalCase
#define CHRONES_MyMacro

// PascalCase for global variables
inline int MyGlobalVar = 0;

// PascalCase for global constans
inline const int MyGlobalConst = 0;

// PascalCase for classes and structs
class MyClass 
{
public:
  // PascalCase for class members
  int ClassMember1 = 11;
  
  // PascalCase for static class members
  static int StaticClassMember1 = 11;
  
  // PascalCase for class functions
  int ClassFunction1();
  
  // PascalCase for static class functions
  static int StaticClassFunction1();
  
  // camelCase for function arguments
  void MyFunc(int arg1, int myDevice)
  {
    // camelCase for local variables
    int myLocalVar;
  }
};
```

## Formatting
```cpp
#define MY_MACRO \
void Macro()     \
{                \
}               

// Single line
int MyVar1 = 10; 

// Multiline (if to long)
MyVeryLongClassNameBecauseIWantSo MyVeryLongVariableNameLolLol =
  10;
  
// Multiline (if to long)
MyVeryLongClassNameBecauseIWantSo MyVeryLongFunctionNameLolLol(
  int arg1, ...
)
{
  ...
}

// Single line
class MyClass : virtual MyBaseClass { };

// Multiline (if to long)
class MySecondClass
  : virtual MyBaseClass
  , MyClass
{
  void Func()
  {
    ...
    if (myVar == 1) { ShortStuff(); };
    
    if (myVar == 1)
    {
      doThisLongStuff();
      ...
    }
    else if (myVar == 2)
    {
      doThatLongStuff();
      ...
    }
    else
    {
      blaBlaBla();
    }
    
    while (true)
    {
      helpMeee("!!");
    }
    
    for (int i = 0; i < 10; i++)
    {
      for (auto i2 : myVar2)
      {
        doHere();
      }
    }
    
    // You can use these
    {
      // Use this for short lambdas inside of functions: []{ 
      auto myLambda = []{ 
        ...
      };
    }
  }
}

// Pointer on the left side
int* MyPointer = nullptr;

// Exception
int *pointer, *pointer2;

// Use this for long lambdas
auto myLambda = []
{
  
};
```
