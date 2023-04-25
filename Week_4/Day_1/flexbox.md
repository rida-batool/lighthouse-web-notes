## html display

1. display: block

A block level element will take up the entire space of its parent element. It can contain other block elements or inline elements.

Other block elements include:

```
* headings (<h1>, <h2>, <h3>,<h4>,<h5>,<h6>)
* div (<div>)
* section (<section>)
* footer (<footer>)
* article (<article>)
* paragraph (<p>)
* lists (<ul>, <ol>)
* nav (<nav>)
```

2. display: inline

Inline elements do not start a new line when they are rendered in the browser. They only take up as much space as the content needs. A span tag is an example of an inline element.
Other inline elements include:

```
anchor (<a>)
em (<em>)
strong (<strong>)
span (<span>)
```

3. display: flex

Flexbox (also known as CSS Flexible Box) is a layout module in CSS. It allows us to specify how elements on our page should appear. It is great for layouts that need to adapt to different screen sizes and display devices.

To start using Flexbox, we add the display: flex property to the parent element.

```css
.parent {
  display: flex;
}
```

We can add more properties of flex display to the class.

i)  justify-content : .....
```
flex-start: Items align to the left side of the container.

flex-end: Items align to the right side of the container.

center: Items align at the center of the container.

space-between: Items display with equal spacing between them.

space-around: Items display with equal spacing around them.
```

2) align-items: ...

This CSS property aligns items vertically and accepts the following values:

```
flex-start: Items align to the top of the container.

flex-end: Items align to the bottom of the container.

center: Items align at the vertical center of the container.

baseline: Items display at the baseline of the container.

stretch: Items are stretched to fit the container.
```

3)  flex-direction: ...

This CSS property defines the direction items are placed in the container, and accepts the following values:

```
row: Items are placed the same as the text direction.

row-reverse: Items are placed opposite to the text direction.

column: Items are placed top to bottom.

column-reverse: Items are placed bottom to top.
```