# sourcestyling
Various source styling standards

# c++

This section defines the source style for c++ code used in the repository.
The style will be complete once all of the basic c++ structures are defined.

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
