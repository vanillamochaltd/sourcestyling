# sourcestyling
Various source styling standards

# c++

This section defines the source style for c++ code used in the repository.
The style will be complete once all of the basic c++ structures are defined.

## Primitive and Complex data types

Primitives should be obvious. The complex datatypes included below would be implemented
elsewhere.

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
### Primitive datatypes

```c
// Variables
int shoe_count;
int shoecount;

// Constants
int SHOE_BOX_VOLUME;
int SHOEBOX_VOLUME;
int SHOEBOXES;
```

### Complex datatypes

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

### Class datamembers

```c
class Cookie{

...

private:

  ...

  // Primtives
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



