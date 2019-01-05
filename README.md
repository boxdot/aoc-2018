# Advent of Code 2018

Solutions of puzzles are in Rust. Parsing of input is done most of the time by using the [`text_io`] crate.

## What did I learn

Rust related:

* Iterators are awesome! [`itertools`] gives you even more iterators.
* In-place unit tests are exactly what you want.
* Strings consist of UTF8 chars, but there are function to work with ASCII like [`to_ascii_uppercase`] (cf. day 5).
* [`BinaryHeap`] in Rust is a max-heap, for min-heap you need to define an inverse order (cf. day 7). And there is a crate [`revord`] which does it for you.
* [`nom`] is very powerful for parsing! In my case, it helped me to parse nested expressions (cf. day 20).
* Sometimes [`HashMap`] API is slightly verbose (cf. [day 22, L93] in Dijkstra's shortest path).
* [`BinaryHeap`] does not have increase/decrease functions for modifying elements, use [`priority_queue`] crate instead (cf. day 22).
* Not to fight with borrow checker, you can use indexes, however be prepared to be hit by bugs (cf. day 24).

Algorithms related:

* Day 7: Lexicographic Topological Sort
* Day 15: I can write RPG's. 🙂
* Day 20: Generator of strings from simple regex-like expressions
* Days 19 + 21: Loop unrolling is hard in compilers (did it just manually).
* Day 23: Spatial search and line/plane sweep (which did not work and where I spent most of the time). Also there are some nice solutions on the internet using powerful solvers like [`Z3`].

[day 22, L93]: blob/master/src/day22.rs#L93
[`itertools`]: https://crates.io/crates/itertools
[`BinaryHeap`]: https://doc.rust-lang.org/std/collections/struct.BinaryHeap.html
[`revord`]: https://crates.io/crates/revord
[`nom`]: https://crates.io/crates/nom
[`text_io`]: https://crates.io/crates/text_io
[`HashMap`]: https://doc.rust-lang.org/std/collections/struct.HashMap.html
[`priority_queue`]: https://crates.io/crates/priority_queue
[`Z3`]: https://github.com/Z3Prover/z3
[`to_ascii_uppercase`]: https://doc.rust-lang.org/std/primitive.char.html#method.to_ascii_uppercase
