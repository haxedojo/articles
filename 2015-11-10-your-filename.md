# The functional fold

Functional programming is an awesome tool. It challenges the mind, but once the challenge is overcome, we find ourselves with a new way of expressing thoughts. A way that is often more concise and easier to reason about than imperative solutions.

At this point, you have most likely become aware of the `map` and `filter` methods available on `Array` instances. You may also have toyed with `Lambda` on occasion. We will rebuild these concepts from scratch and see what we can learn in doing so.

To do this, let us start by defining our own list data structure:

```haxe
enum List<T> {
  Empty;
  Node(head:T, rest:List<T>);
}
```

This allows us to represent lists, e.g. a list of the integers `1`, `2` and `3` would be `Node(1, Node(2, Node(3, Empty)))`. Given that Haxe already offers us arrays and lists, this is not exactly the paramount of usefulness. But remember, we are building this from scratch and with very little code, we actually got quite far: http://try.haxe.org/#8fF5d

Here goes the final state: http://try.haxe.org/#B7eB3