### TEJP - part 2
*This is a blog series about my quest to write a two way binding javascript library for browsers. [Read Part 1 - Introduction here](http://hampuspersson.se/2014/05/tejp-a-series/).*

So, to be able to succeed the first step has to be a definition of what success looks like. In other words, what features are required by my library? Right now I think that the best architecture is to split the library in two:

- A object.watch type library that can monitor objects and report changes to them.
- A library that can act as a layer between my object.watch library and the DOM.

First, a list of the features I think are required for an object.watch library:

- Set watchers on objects (including primitive types, arrays and objects).
- Get watchers
- Delete watchers.
- Publish events when a watch object has changed or has been deleted.
- Subscribe to object changed events.

And the DOM update module needs to be able to:

- Bind DOM nodes to objects. An infinite number of nodes should be bindable to each object.
- Update specific parts of the DOM.

Not too long of a list, but I'm sure it's incomplete at this moment. So the part about knowing what success looks like to be able to succeed is probably BS. I'll just know when I have succeeded.

As the object.watch functionality is what intrigues me most that is where I'll start. The repo is available at [https://github.com/hmps/tejp](https://github.com/hmps/tejp).