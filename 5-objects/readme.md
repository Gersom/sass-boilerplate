# Objects

Objects, abstractions, and design patterns.

Format:

```css
.o-object-name[<element>|<modifier>] {}
```

Example:

```css
.o-layout {}

	.o-layout__item {}

.o-layout--fixed {}
```

* Objects are abstract.
* They can be used in any number of places across the project—places you might not have even seen.
* Avoid modifying their styles.
* Be careful around anything with a leading `o-`.
