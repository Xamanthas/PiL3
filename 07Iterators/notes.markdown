Chapter 7: Iterators and the Generic for
========================================

- An iterator is any construction that allows you to *iterate* over the elements
  of a collection
- They are typically represented by functions (closures) in Lua
- A closure iterator involves two functions: the closure itself and a *factory*,
  which creates the closure and it's nonlocal variables
- Iterators may not be easy to write, but they are easy to use
- The generic for does all the bookkeeping for an iteration loop and it also
  keeps an *invariant state variable* and a *control variable*
- When the first variable, which is called the control variable, is `nil`, the
  loop ends
- With the invariant state and the control variable, we can write *stateless
  iterators* (like `ipairs()`, which is also stateless)
- Complex states can be stored in the invariant state variable by using a
  table
- True iterators are functions that do the iteration themselfes, they take an
  anonymous function as argument and call that for every element
- True iterators were popular when the for loop wasn't in Lua yet, they have
  some drawbacks (like difficult parallel iteration)