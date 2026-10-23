# Pouch Math

Event roasted almond pouch, week, cost and time arithmetic. The 440 almonds at 12 almonds a pouch take 37 pouches, the last pouch holding 8 almonds.

## Named constants

None. Every number is the owner's own entry.

## What it computes

- **The pouches truth** - the almonds (1 to 1000000) divided by the almonds a pouch (1 to 1000), rounded up, with what the last pouch holds.
- **The weeks truth** - the almonds divided by the almonds used a week (1 to 100000), with the almonds left for the next week.
- **The cost truth** - the pouches (1 to 100000) times the pouch price ($0.01 to $999.99) to the cent, and spread over the almonds, half rounded up.
- **The time truth** - the almonds divided by the almonds packed a minute (1 to 100), rounded up, in minutes and in hours and minutes.

## Boundary

Arithmetic only. Counting applied as written. It has not seen any almond, pouch or venue and does not know whether almonds will really stay fresh, a supplier will run out or a price will hold, and it gives no verdict that a pouch is worth its price or an almond is right for an event. Every number is the owner's own entry.

## Files

- `index.html` - landing page with the boundary and starting examples.
- `app.html` - the calculator; every pouch recomputes on each keystroke.
- `engine.js` - the four truths, shared by the page and the tests.
- `oracle.py` - an independent Python re-implementation; writes `expected.json`.
- `test.js` - runs the engine against `expected.json` (99 cases, 20 error cases).

## Tests

```
python3 oracle.py
node test.js
```
