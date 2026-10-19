# Release notes

<!-- do not remove -->

## 0.0.7
- `assemble_book(pages, …)` assembles pages already read, a vault's after its proofread is accepted, say. It is `read_book`'s assembly half and `read_book` calls it. A verse read without its `n` takes the number it closes on (`॥ १२ ॥`, Tamil numerals too); blocks with no text go. `cont`, `openers` and `renumber` (each chapter's numbers mended) are options. It returns the prose it left out as `left`.
- Every akṣara mend is noted in `probs` as `<page>: <chapter>.<verse>: akṣaras mended`.
- `read_book` takes `openers` and `renumber`, and passes anything else to `read_doc`: `cache`, `redo`, `clean`, `tries`, `spread`, `strips`, `progress`, `pii`. Its result carries `left`, the reading's `cost`, and the pages `failed`, `unread` and `blocked`.
- Needs vishalakshi 0.1.25.

## 0.0.6
- `fix_chapters`: a `start` row's `printed` picks between two verses of one number in a chapter, by the page it is on (`'p0108a'`) or which one it is (2 is the second); a `fix_all` row replaces every occurrence. `apply_fixes` takes `fix_all` too.
- `assemble(openers=True)`: an unnumbered block closed by ॥ (a maṅgala) stays a verse of its own, `n` None, in the chapter of the verse after it; `mend` and `renumber` leave it where it is.
- `cut_by_plan` notes each cut in `probs`; a plan row's third value is why.
- The index shows every public function, run on the three sample books.

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
