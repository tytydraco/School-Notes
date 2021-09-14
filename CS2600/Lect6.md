# Lect 6

## Ram segments
### Stack
- Kernel allocates some for us to use
- Temporary storage
- FILO / LIFO
- Variables that are declared in a function live here
  - Removed when no longer needed
- Functions get their own frame in the stack
  - Little containers for their variables
  - Stacked on top of the previous frame
  - Value can be returned to the caller


### Heap
- Kernel controls this, we can't use it
- We must ask kernel for permission
- We don't need to allocate size before hand, we can do it during runtime
  - Think `malloc()`

### Static
- Use for variables that live for a long time
- Global variables stored in static secton
- You can put a static variable inside a function
  - It will have a lifetime beyond the function
  - It will only be assigned ONCE

### Text
- Holds functions that we define or use

## Loops
### Do-whole
- Instead of doing the check first, we do the action first, then the check
- For sure execute once at least