Exercise 4.3
============

> Many people argue that repeat-until is sldom used, and therefore
> it should not be present in a minimalistic language like Lua. What 
> do you think?

A `repeat-until` loop is similar to a `do-while` loop in C and it's derivatives
because the loop's contents are run once before the condition is evaluated.
This behavior is not used too often, but sometimes it's needed. You can
simulate such a loop with a while loop, but doing so is awkward and doesn't
tell the reader of the code right away what you intend the loop to do, so I do
think that such a construction has it's place in Lua.
