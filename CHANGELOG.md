# Release notes

<!-- do not remove -->

## 0.0.5
- Pages may keep their blocks under `items`; a reader's `head` is a `heading` (`KINDS`, `kind`, `blocks`). Every function that reads pages takes both.
- `join_cont` and `assemble(cont=)`: a block a page break cut rejoined, a hyphenated word mended.
- `assemble_colophon`: chapters cut at the colophons that number and name them, with parts, commentator's colophons and sections, and restarts split.
- `norm`, `virama`, `deva`: typing slips in Devanagari.
- `repairs`: `drop_pages`; `fix_chapters` (fix, slip, doubt, note, number, drop, missing, recut, start rows keyed by chapter and verse); `sutras`.
- `editions`: `cut` and `numbering` (verses into titles), `witness_verses`, `letters`, `text_changes`, `ref_check`, `move_lines` (against another edition), `verse_text`, `lev`, `disagree`, `compare` (two readings of a page).

## 0.0.4
- `repairs`: `apply_fixes` (fix, doubt, slip, number, drop, missing rows), `number_runs`, `borrow_numbers`, `cut_by_plan`.
- `vnum` reads Tamil numbers with ௰ ௱ ௲ (௬௱௨ is 602); `pick='first'`.
- `assemble(notes=, number_from_note=)`: an urai, gloss or commentary goes into its verse's notes, and may number it; a `start` block opens a chapter.
- `read_book` takes `kinds`, `notes`, `number_from_note`, `fixes`.
- The index shows three of vedicreader's books: the Bṛhajjātaka, the Vidhānamālai, Uromarishi's Pañcapakṣi.

## 0.0.3
- `assemble(kinds=)`: `None` takes every block but headings and colophons as verse.
- A block's text is kept as read, a leading break and an empty block included; vedicreader's 28 cached books assemble identically.

## 0.0.2
- Needs vishalakshi>=0.1.21, which resolves model names such as `claude/sonnet`.

## 0.0.1
- `read_book`: a book of verses read through vishalakshi into chapters, with the problems a proofreader should see; `book_md`.
- `vnum`, `mend`, `renumber`, `assemble`, `check_counts`, `fix_aksharas`, `bad_aksharas`.
