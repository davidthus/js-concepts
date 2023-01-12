# JS-CONCEPTS

## my documentation for [33-js-concepts](https://github.com/leonardomso/33-js-concepts)

check the diff branches for the docs

# Event loop

Js is single-threaded so it can only do one thing at a time, therefore it has the event loop to help with async operations.

When an async operations appears in the call stack, it gets sent to the LIBUV API to get processed; after it has finished processing the operation, its callback gets passed in to the event queue(first in, first out data structure) so it can wait to get put into the call stack, the event loop will check if the event queue is empty and if it isn't, it will propagate the callback to the call stack.
