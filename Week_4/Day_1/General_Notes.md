## Notes

### CSS

  - display: block
      - A block level element will take up the entire space for its parent
      - (headings, div, section, footer, article paragraph, lists, nav) are all block level elements

  - display: inline-block
      -  Only take up as much space as they need
      - (anchor, em, strong, span) are all inline block elements

```css
/* A */
p.class1[attr='value']

/* B */
p.class1 { }

/* C */
p.class2 { }

/* D */
p { }

/* E */
p { property: value !important; }

/* and the following markup: */

<p style='/*F*/ property:value;' class='class1 class2' attr='value'>

```

- E has the highest precedence because of the keyword !important. It is recommended that you avoid its usage.
- F is next, because it is an inline style.
- A is next, because it is more “specific” than anything else. It has 3 specifiers: The name of the element p, its class class1, an attribute attr='value'.
- C is next, even though it has the same specificity as B. This is because it appears after B.
- B is next.
- D is the last one

- [css best practices]('https://code.tutsplus.com/tutorials/30-css-best-practices-for-beginners--net-6741')

### DOM

- he visual representation of the DOM will be just like your simple HTML. But it’s often not the same…

-  When is the DOM different than the HTML?
    - JavaScript can manipulate the DOM
    - The DOM is the lifeblood here. It’s where everything goes down in the browser. JavaScript is just the syntax, the language. It can be used totally outside the browser with no DOM APIs at all (see Node.js).
    - The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. 
    - Ajax and Templating