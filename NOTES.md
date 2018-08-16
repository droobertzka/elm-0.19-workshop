# Elm Workshop Notes

## Day 1
Wednesday, August 15, 2018
-----------------------------------

### 0.19.0 Changes
* _Union Types_ are now referred to as _Custom Types_

### Reasons to use Elm
* fast & reliable (no runtime exceptions)
* hiring is easier & quality of candidates is high
* cohesive ecosystem

### QUESTIONS
* Source maps for Elm?
  * Not needed as much because you don't need to debug runtime errors
* Reasons for differences in syntax
  * e.g. -- vs // for comments, whitespace instead of parens, commas at beginning of lines
* Are there any new JS language features that Elm uses for compile targets where it'd be useful to specify a browser target? (e.g. Typed Lists vs Arrays)
  * No, Elm targets ES3 and some ES5 where necessary (Frame Animations?).
  * Elm is designed to compile to WebAssembly when WebAssembly is ready (needs garbage collector, etc.)
  * Lists compile to "Linked Lists" in JS
* Reasoning behind _List.map_ vs a generic _map_ function?
  * designed purposely to be explicit for readability (and probably to make compiling & error messages easier)

### COMMENTS
* Elm slack - there is a Minneapolis room
* Good idea bringing TypeScript in for comparison


## Day 2
Thursday, August 16, 2018
-----------------------------------

**Bound vs Unbound type variables**
* bound type variables (e.g. List _number_, number is an Int or Float)
* unbound type variable is like List _a_

**Open vs Closed Records**
* when dealing with a record, you can accept it as { r | prop : String } where all we care is that the record has a property named "prop" which is a string. Then, we can still pass the whole record along but only deal with that single prop.
* ! - Open records are somewhat discouraged because their existence in Elm has been called into question due to considerations when compiling into WebAssembly.

**Phantom types**

**Type Parameter Design**
* List (Attribute msg)
  * Give me a list of attributes with variables of ANY type
* List (Attribute Msg)
  * Give me a list of attributes with variables with a type of _Msg_ (however that's defined)
* List (Attribute Never)
  * Only ever give me a list of attributes with unbound variables

