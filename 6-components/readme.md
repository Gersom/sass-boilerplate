# Components

Discrete, complete chunks of UI.

Format:

```css
.c-component-name[<element>|<modifier>] {}
```

Example:

```css
.c-modal {}				/* block */

  .c-modal__title {}	/* child */

.c-modal--gallery {}	/* modifiers */

/* other component */
.c-blog-post {}
```

* Components are implementation-specific bits of UI.
* They are quite safe to modify.
* Anything with a leading c- is a specific thing.

# Stateful Namespaces

Format:

```css
.c-component-name[<element>|<modifier>] {}
```

Example:

```css
.is-open {}
.has-dropdown {}
```

* States are very temporary.
* Ensure that States are easily noticed and understood in our HTML.
* Never write a bare State class.
