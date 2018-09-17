# sourcestyling
Various source styling standards

# c++

This section defines the source style for c++ code used in the repository.
The style will be complete once all of the basic c++ structures are defined.

## General Guidelines

### Scrapped 
At the time of writing, this guideline will scrap the following,

#### 'Global' Variables, Constants, Functions and Procedures
```cpp
...
#include <iostream>

// As forward declarations, but not limited to
uint32_t AddNumbers(uint32_t, uint32_t);
uint32_t supercounter = 0;

int main(){
  // Some groundbreaking code here
}
```

As a rule of thumb, datatypes and codeblocks that should have their own identifiers, and should be declared within a specific scope.

## Primitive and Complex Datatype Identifiers

Primitives should be obvious. The complex datatypes included below would be implemented
elsewhere. Unless there is a certain distinction (See Class Datamembers), the guidelines set by this document will apply to each datatype in Namespace, Class, and Function scopes.

### Variables

```cpp
snake_case
// or
snakecase
```

### Constants

```cpp
UPPER_CASE_SNAKE_CASE
// or
UPPERCASE_SNAKECASE
```
### Primitive Datatypes

```cpp
// Variables
int shoe_count;
int shoecount;

// Constants
const int SHOE_BOX_VOLUME;
const int SHOEBOX_VOLUME;
const int SHOEBOXES;
```

### Complex Datatypes

```cpp
// Variables
Cookie peanut_butter_cookie;
Cookie peanutbuttercookie;
Cookie vanillacookie;

// Constants
const Cookie VANILLA_WAFER;
const Cookie VANILLAWAFER;
const Cookie SNICKERDOODLE_COOKIE;
```

### Class Datamembers
Class Datamembers will follow the specifed guidelines for Primitive and Complex Datatypes as variable and constants.
Additionally, each identifier will terminate with an underscore `_` as to not clash with accessor methods.

```cpp
class Cookie{

private:

  // Primitives
  bool isround_;
  bool is_round_;
  
  // Complex
  Ingredient flour_;
  Ingredient egg_;

 public:
 
  // Primitive
  unsigned int flavorrating_;
  unsigned int flavor_rating_;
  
  // Complex
  Shape shape_;
 
};
```

## Codeblock and Scope Identifiers
These guidelines apply to codeblocks that normally require identifiers such as, Namespaces, Functions, Procedures, and Classes.
The purpose for the style are to make a distinction of datatype, function, and procedures' origin belonging to each scope.
The trend will continue for nested scopes.

### Namespace Identifiers
Namespace identifiers, like Class, Function, and Procedure Identifiers, will be capitalized.

```cpp
namespace Library{

// Code goes here

};
```

### Class Identifiers
Class Identifiers will be Capitalized

```cpp
class Cookie{

// Code goes here

};
```

### Procedure, Function, and Method Identifiers
These guidelines are for Namespace and Class procedure, function, and methods that are inline, static, or out-of-line.
Currently, there are no name distinctions between the codeblock variants previously specified in this section, since the purpose
is to identify a codeblock's scope.

#### Namespace Function and Procedure Identifiers
```cpp

// Examples for Function and Procedures (Typically defined within a namespace)
namespace Library{

  // Program, Library, or API Function
  uint32_t AddNumbers(uint32_t, uint32_t);
  bool IsOddNumber(int32_t);
  static uint32_t TotalAdditions();

  // Program, Library, or API Procedure
  void PrintNumber(uint32_t);
  void CleanUp();
  static void IncrementInstances();
   
};
```

#### Class Method and Procedure Identifiers

```cpp
class Cookie{

private:

  // Private Method Examples
  bool FinishedBaking();
  static uint32_t BatchCount();

public:
  
  // Public Method Examples
  Shape const& Shape() const;
  bool IsRound() const;
  void Bake();
  
};
```

## Comments
Comments are required to be included in every file, as well as preceding codeblocks that establish their own scope; e.g. Namespaces, Functions and Procedures, and classes.
Commentblocks should be topped off with a border, using a character that conforms with previous comments, as wide as the longest line.
The following examples will use the `-` character.

### Comments for arbritrary files
This guideline follows header(.hpp) and implementation(.cpp) files;
```cpp
// ------------------------------------------
// @file: filename.xpp
// @author: Jimmy McCoy, Susie Anderson, ...
// @description: Declaration of amazing code.
```

### Comments for Functions, Procedures, and Methods
Function;
```cpp
// --------------------------------------------------------------------------------------
// @author: Ron Weasley
// @function: BakeCookies
// @parameters: CookieSheet
// @return: Amount of Baked Cookies
// @description: Bake the cookies in the sheet, and report the amount of successful bakes
uint32_t BakeCookies(CookieSheet const& cookie_sheet) const{
...
}
```
Procedure;
```cpp
// --------------------------------------------
// @author: Anton Chigurh
// @procedure: PackageCookies
// @parameters: none
// @decription: Stores the cookies after baking
void PackageCookies(){
...
}
```
Method as a Function;
```cpp
// -----------------------------------------------------------------------------
// @author: Rick Deckard
// @class: Baker
// @function: TakeOrder
// @parameters: Customer
// @return: Total Orders
// @description: Takes the customer order, and report the amount of total orders
uint32_t Baker::TakeOrder(Customer const& customer){
...
}
```
Method as a Procedure
```cpp
// -------------------------------------------------------
// @author: Winston Smith
// @class: Baker
// @procedure: CleanUp
// @parameters: DirtyList
// @description: Clean up based on items within the dirty list
void Baker::CleanUp(DirtyList& dirtylist){
...
}
```

### Namespace comments
Namespace will follow a similar style. 

```cpp
// @author: Hugo Stiglitz
// @namespace: Bakery Library
// @description: Bakery program scope
namespace Bakey{
...
};

```
