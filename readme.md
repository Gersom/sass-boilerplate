# Sass boilerplate
>v.0.0.3

Contains:

* [Bourbon](http://bourbon.io/docs/)
* [Neat](http://thoughtbot.github.io/neat-docs/latest/)
* [Basscss](http://www.basscss.com/docs/)
* [Nudge](https://github.com/csswizardry/nudge)

Inspiration:

* [Itcss](https://speakerdeck.com/dafed/managing-css-projects-with-itcss)
* [Inuitcss](https://github.com/inuitcss/getting-started)


### What naming convention use?

Use [Bemit](http://csswizardry.com/2015/08/bemit-taking-the-bem-naming-convention-a-step-further/)

```css
/* components */
.c-blog {}
.c-blog__title {}

.c-blog-post {}
.c-blog-post__time {}

/* modifiers */
.c--featured {}
/* states */
.is-stateOfComponent {}
.has- {}

/* objects */
.o-media {}

/* theme */
.t-theme-name {}
.t-light {}

/* utilities */
.u-wrapper {}

/* responsive classes */
.u-hidden\@lg {}
```


### How do you order your CSS properties?

```css
.selector {
    /* other */
    /* box model */
    /* typography */
    /* position */
}
```


### Namespaces

[Methods for Theming](https://speakerdeck.com/csswizardry/4half-methods-for-theming-in-s-css)

`o-`: Signify that something is an Object, and that it may be used in any number of unrelated contexts to the one you can currently see it in. Making modifications to these types of class could potentially have knock-on effects in a lot of other unrelated places. Tread carefully.

`c-`: Signify that something is a Component. This is a concrete, implementation-specific piece of UI. All of the changes you make to its styles should be detectable in the context you’re currently looking at. Modifying these styles should be safe and have no side effects.

`u-`: Signify that this class is a Utility class. It has a very specific role (often providing only one declaration) and should not be bound onto or changed. It can be reused and is not tied to any specific piece of UI. You will probably recognise this namespace from libraries and methodologies like SUIT.

`t-`: Signify that a class is responsible for adding a Theme to a view. It lets us know that UI Components’ current cosmetic appearance may be due to the presence of a theme.

`s-`: Signify that a class creates a new styling context or Scope. Similar to a Theme, but not necessarily cosmetic, these should be used sparingly—they can be open to abuse and lead to poor CSS if not used wisely.

`is-, has-`: Signify that the piece of UI in question is currently styled a certain way because of a state or condition. This stateful namespace is gorgeous, and comes from SMACSS. It tells us that the DOM currently has a temporary, optional, or short-lived style applied to it due to a certain state being invoked.


### Directory structure

1. `Settings`
    * Globally-available settings.
    * Config switches.
    * Brand colours, etc.
2. `Tools`
    * Globally-available tools.
    * Public mixins.
    * Helper functions.
3. `Generic`
    * Ground zero styles.
    * Low-specificity, far-reaching.
    * Resets, Normalize.css, etc.
4. `Base`
    * Unclassed HTML elements.
    * H1–H6, basic links, lists, etc.
    * Last layer we see type selectors (e.g. a {},  blockquote {}).
5. `Objects`
    * OOCSS.
    * Design patterns.
    * No cosmetics.
    * Begin using classes exclusively.
    * Agnostically named (e.g. .o-list {}).
6. `Components`
    * Designed pieces of UI.
    * Still only using classes.
    * More explicitly named (e.g. .c-products-list {}).
7. `Trumps`
    * Overrides, helpers, utilities.
    * Only affect one piece of the DOM at a time.
    * Usually carry !important.
