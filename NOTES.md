# Elm Workshop Notes

## Day 1
Wednesday, August 15, 2018

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
