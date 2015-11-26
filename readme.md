# Sass boilerplate

* [Bourbon](http://bourbon.io/docs/)
* [Neat](http://thoughtbot.github.io/neat-docs/latest/)
* [Basscss](http://www.basscss.com/docs/)

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

/* objects */
.o-media {}

/* utilities */
.u-wrapper {}
.is- {}
.has- {}

/* responsive classes */
.u-hidden@lg {}

/* templates */
.t-home {}
.t-category {}
```


### How do you order your CSS properties?

```css
.selector {
    /* Box model */
    /* Flex */
    /* Other */
    /* Position */
    /* Transition */
    /* Typography */
}
```
