
# Responsive Tables - A magical journey
[Brace yourselves, Responsive tables are coming]

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

## 'Responsive tables' as a flexible reusable (Styleguide) component

- Being responsive must be optional
- Vertical scrollbars is a valid option
- Collapse by rows if content is arranged horizontally
- Collapse by columns if content is arranged vertically
- Collapse to tabs or accordions

---

## Limitations of standard table markup
(<table> or display:table)

- Not as accessible as you might think
    + No way to make a screen reader read verticaly down columns
    + <thead>, <th> and 'scope' dont really help at all

- Collapsing responsively by 'columns' is harder than ruling 7 kingdoms

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

[Example: http://codepen.io/davidelrizzo/pen/eJwqzp?editors=1100]

---

- Set the flex 'order' by row to instantly create a vertical table
- This is still as accessible as it was before!

[Example: http://codepen.io/davidelrizzo/pen/dGBxje?editors=1000]

---

- Style cells individually in any pattern you require
- Fix cell border duplication with negative margins

[Example: http://codepen.io/davidelrizzo/pen/BjgXGg?editors=1100]

---

- collapse everything with 'display:block' on small screens

[Example: http://codepen.io/davidelrizzo/pen/GobVLe?editors=1100]

---

## Now we can collapsing to Tabs or Accordions

- Tab and accordion markup sits IN the table in a logical position
- Toggle either row or column depending on table
- Use 'display:none' to toggle for both visual users and screen readers

- [Example: http://codepen.io/davidelrizzo/pen/qbeWWK?editors=1010]

---

 Use flex to align cell content in any way

[Example: http://codepen.io/davidelrizzo/pen/PZMYWw?editors=0100]

---

Easily add column margins by offsetting cell widths

[Example: http://codepen.io/davidelrizzo/pen/LGwPeq]

---

Zebra stripe the table.. ok you can't do this in pure CSS :(

[Example: http://codepen.io/davidelrizzo/pen/BjXBrz?editors=0110]

---

Emulate column spans with manual cell width
- LIMITATION: There is no way to do rowspans on a flex table :(

[Example: http://codepen.io/davidelrizzo/pen/gPVbYe?editors=1100]

---

So flexy.. use it with any type of markup

[Example: http://codepen.io/davidelrizzo/pen/VeoeqB?editors=1000]

---

### That guy we love to hate (IE)
Only IE9 and below does not support flex. These old browsers will simply see the mobile version (graceful degradation FTW)

---
