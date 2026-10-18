# Release notes

<!-- do not remove -->

## 0.0.3
- `assemble(kinds=)`: `None` takes every block but headings and colophons as verse.
- A block's text is kept as read, a leading break and an empty block included; vedicreader's 28 cached books assemble identically.

## 0.0.2
- Needs vishalakshi>=0.1.21, which resolves model names such as `claude/sonnet`.

## 0.0.1
- `read_book`: a book of verses read through vishalakshi into chapters, with the problems a proofreader should see; `book_md`.
- `vnum`, `mend`, `renumber`, `assemble`, `check_counts`, `fix_aksharas`, `bad_aksharas`.
