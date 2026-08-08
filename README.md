# RandomWalkJava

A random-walk "mosaic" animation in Java, built with Gradle. Based on the `RandomMosaicWalk` example
from David Eck's [*Introduction to Programming Using Java*, Section 4.7](https://math.hws.edu/javanotes/c4/s7.html).

The program fills a grid of colored squares, then moves a single "disturbance" randomly around the
grid, recoloring each square it visits as it goes.

## Files

- **`RandomWalk.java`** — this is the file you'll work in. It has `main()` and the program logic:
  filling the grid with random colors, moving the disturbance, and choosing new colors.
- `Mosaic.java` — the drawing library/API (opens the window, sets a square's color, adds delays). You
  shouldn't need to edit this.
- `MosaicCanvas.java` — the underlying canvas implementation that `Mosaic` wraps. You shouldn't need to
  touch this either.

## Running It

This project uses the Gradle wrapper, so there's nothing extra to install. From the project's root
folder (the one with the `gradlew` file):

```bash
./gradlew run
```

If something's misbehaving or you want a fresh build:

```bash
./gradlew clean
./gradlew build
```

## Background

The original write-up — including why the program is split into `fillWithRandomColors`,
`changeToRandomColor`, and `randomMove` subroutines instead of one long `main()` — is in Eck's
[Section 4.7, "More on Program Design"](https://math.hws.edu/javanotes/c4/s7.html). Worth a read if
you're curious about the design reasoning, not just the code.