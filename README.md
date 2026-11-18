# Documents Editor.
Personal Project. My idea is to create something similar to Notepadd++. Using Rust for the core (to learn)

## Useful Resources

### Learning Rust

- [The Rust Book](https://doc.rust-lang.org/book/): the official book and the most complete resource. Key topics: ownership, borrowing, structs/enums, traits and error handling (`Result`).
- [Rust by Example](https://doc.rust-lang.org/rust-by-example/): runnable examples for quick reference.
- [Rustlings](https://github.com/rust-lang/rustlings): short exercises to practice and learn to read compiler messages (`cargo install rustlings`).

### Building an editor

- [hecto: Build Your Own Text Editor in Rust](https://flenker.bearblog.dev/hecto/): step-by-step tutorial (a Rust reimplementation of kilo) for a terminal editor. The 2024 version is unfinished; the older one is complete but outdated.
- [Pound: Build Your Text Editor With Rust](https://medium.com/@otukof/build-your-text-editor-with-rust-678a463f968b): an alternative to hecto with less theory and more code.
- [Helix (source code)](https://github.com/helix-editor/helix): a real editor in Rust built on Ropey, useful as an architecture reference.

### Buffer data structures

- [The Piece Table (Darren Burns)](https://dev.to/_darrenburns/the-piece-table---the-unsung-hero-of-your-text-editor-al8): a clear explanation of the piece table and why it makes undo simpler.
- [VS Code: Text Buffer Reimplementation](https://code.visualstudio.com/blogs/2018/03/23/text-buffer-reimplementation): why and how VS Code moved its buffer to a piece table.
- [Piece table (Wikipedia)](https://en.wikipedia.org/wiki/Piece_table): quick summary and references.
- [Text editing algorithms (Bill Mill's notes)](https://notes.billmill.org/programming/text_editors/Text_editing_algorithms.html): a collection of readings, including the classic paper "Data Structures for Text Sequences" (Crowley, 1998).

### Libraries

- [crossterm](https://docs.rs/crossterm): cross-platform keyboard input and terminal control.
- [ratatui](https://ratatui.rs): a library for terminal user interfaces, with step-by-step tutorials.
- [unicode-segmentation](https://docs.rs/unicode-segmentation): splits text into graphemes so the cursor moves correctly over accents and emojis.
- [unicode-width](https://docs.rs/unicode-width): on-screen width of each character (wide characters, emojis).
- [Ropey](https://docs.rs/ropey/): a UTF-8 rope for editors. To read and compare against after building my own buffer.

### Additional reading
 
- [The Craft of Text Editing (Finseth)](https://web.mit.edu/~yandros/doc/craft-text-editing/): free classic book on text editor design (editing models, redisplay, command loop).
- [xi-editor documentation](https://xi-editor.github.io): explains the design of a Rust editor built on a persistent rope and a CRDT. The project is discontinued, but the docs are still worth reading.
- [Lapce](https://github.com/lapce/lapce): a Rust editor with a graphical interface, considered a spiritual successor to xi. An architecture reference for moving to a GUI.
- [Learn Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/): ownership, lifetimes and unsafe applied to linked structures. Preparation for trees and ropes.
- [Crafting Interpreters](https://craftinginterpreters.com): free book. Chapter 4 (Scanning) teaches how to write a tokenizer, which is what syntax highlighting needs.
- [Build Your Own Text Editor (kilo, in C)](https://viewsourcecode.org/snaptoken/kilo/index.html): the original tutorial that hecto is based on. Its array-of-lines buffer does not scale to complex operations.
