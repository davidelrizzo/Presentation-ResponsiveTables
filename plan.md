# Responsive Tables - A journey through Westeros

Blurb: "What looks like a table, is laid out like a table, but isn't a table? Table markup isn't as accessible as you'd think and collapsing by columns is surprisingly difficult. How can we get layout like tables with accessibility and responsiveness? Flexbox of course!"

[Brace yourselves, Responsive tables are coming!]

---

DAVIDE L RIZZO
@davidelrizzo

Melbourne based UX & Front-End 12+ years

SUNCORP GROUP: Personal, Business, Life Insurance & Banking
Suncorp, AAMI, GIO, Bingle, Just Car, Shannons, Apia... and many more

---

## Comparison Tables

[examples:https://www.aami.com.au/car-insurance.html]

(Understand that the horiz & vert alignment is what's important)

---

## 'Responsive tables' as a flexible reusable component
(for styleguides)

- Being responsive must be optional
- Vertical scrollbars is a valid option
- Collapse by rows if content is arranged horizontally
- Collapse by columns if content is arranged vertically
- Collapsing to tabs or accordions would be even better!

---

## Limitations of standard table markup
(<table> or display:table)

- Not as accessible as you might think
    + No way to make a screen reader read verticaly down columns
    + <thead>, <th> and 'scope' dont really help at all

- Collapsing responsively by 'columns' is a nightmare

---

## Less perfect ways to build a responsive table

IDEA: Generate a second responsive table and toggle on breakpoint
CONS: Code duplication/bloat. Will duplicate unique IDs inside a table.

IDEA: Rearrange the table with JS on breakpoint 
CONS: Requires JS & screen events, Must re-initialize contents on change

IDEA: Switch from <table> to display:flex
CONS: Simply not possible to do vertical/horizontal & collapse row/column with the same markup

---

## Doing it right: FLEXBOX!

- Order markup exactly how you would read it, use semantic headers & text
- Abandon all concept of 'row' wrappers
- Set the width of each cell as a percentage based on number of columns/rows (sorry no auto sized column widths)
[Example]

---

- Set the flex 'order' by row to instantly create a vertical table
- This is still as accessible as it was before!
[Example] 

---

- Style cells individually in any pattern you require
- Fix cell border duplication with negative margin
- Add a 'stripped' variant
[Example]

---

- collapse everything with 'display:block' on small screens
[Example]

---

## Now show off by collapsing to Tabs or Accordions

- Tab and accordion markup sits IN the table in a logical position
- Toggle either row or column depending on table
- Use 'display:none' to toggle for both visual users and screen readers
- [Example]

---

Use flex to align cell content in any way
[Example]

---

Easily add column margins by offsetting cell widths
[Example]

---

Zebra stripe the table.. ok you cant do this in pure CSS :(
[Example]

---

Emulate column spans with manual cell width
- There is no way to do rowspans on a flex table :(
[Example]

---

So flexy.. use it with any other markup!
[Example: Box]
[Example: List]
[Example: Definition list]
[Example: Table]

---

### That guy we love to hate (IE)
Only IE9 and below does not support flex. These old browsers will simply see the mobile version (still functionally working!)

---
