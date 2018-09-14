# sourcestyling
Various source styling standards

# c++

This section defines the source style for c++ code used in the repository.
The style will be complete once all of the basic c++ structures are defined.

## Primitive and Complex Datatype Identifiers

Primitives should be obvious. The complex datatypes included below would be implemented
elsewhere. Unless there is a certain distinction (See Class Datamembers), the guidelines set by this document will apply to each datatype in Namespace, Class, and Function scopes.

### Variables

```c
snake_case
// or
snakecase
```

### Constants

```c
UPPER_CASE_SNAKE_CASE
// or
SNAKECASE
```
### Primitive Datatypes

```c
// Variables
int shoe_count;
int shoecount;

// Constants
int SHOE_BOX_VOLUME;
int SHOEBOX_VOLUME;
int SHOEBOXES;
```

### Complex Datatypes

```c
// Variables
Cookie peanut_butter_cookie;
Cookie peanutbuttercookie;
Cookie vanillacookie;

// Constants
Cookie VANILLA_WAFER;
Cookie VANILLAWAFER;
Cookie SNICKERDOOLE_COOKIE;
```

### Class Datamembers

```c
class Cookie{

...

private:

  ...

  // Primitives
  bool isround_;
  bool is_round_;
  
  // Complex
  Ingredient flour_;
  Ingredient egg_;
  
  ...
  
 public:
 
  ...
 
  // Primitive
  unsigned int flavorrating_;
  unsigned int flavor_rating_;
  
  // Complex
  Shape shape_;
  
  ...
 
};

```

## Procedure, Function, and Method Identifiers
These guidelines are for program and class procedure, function, and methods that are inline, static, or out-of-line.
Currently, there are no name distinctions for the specified codeblock variants previously specified in this section.

```c

// Examples for Function and Procedures (Typically defined within a namespace)

namespace Library{

  // ...

  // Program, Library, or API Function
  uint32_t AddNumbers(uint32_t, uint32_t);
  bool IsOddNumber(int32_t);
  static uint32_t TotalAdditions();
  
  // ...

  // Program, Library, or API Procedure
  void PrintNumber(uint32_t);
  void CleanUp();
  static void IncrementInstances();
  
  // ...
  
};
```



