---
title: border-bottom-color
slug: Web/CSS/border-bottom-color
page-type: css-property
browser-compat: css.properties.border-bottom-color
sidebar: cssref
---

The **`border-bottom-color`** [CSS](/en-US/docs/Web/CSS) property sets the color of an element's bottom [border](/en-US/docs/Web/CSS/border). It can also be set with the shorthand CSS properties {{cssxref("border-color")}} or {{cssxref("border-bottom")}}.

{{InteractiveExample("CSS Demo: border-bottom-color")}}

```css interactive-example-choice
border-bottom-color: red;
```

```css interactive-example-choice
border-bottom-color: #32a1ce;
```

```css interactive-example-choice
border-bottom-color: rgb(170 50 220 / 0.6);
```

```css interactive-example-choice
border-bottom-color: hsl(60 90% 50% / 0.8);
```

```css interactive-example-choice
border-bottom-color: transparent;
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="transition-all" id="example-element">
    This is a box with a border around it.
  </div>
</section>
```

```css interactive-example
#example-element {
  background-color: #eee;
  color: #000;
  border: 0.75em solid;
  padding: 0.75em;
  width: 80%;
  height: 100px;
}
```

## Syntax

```css
/* <color> values */
border-bottom-color: red;
border-bottom-color: #ffbb00;
border-bottom-color: rgb(255 0 0);
border-bottom-color: hsl(100deg 50% 25% / 75%);
border-bottom-color: currentcolor;
border-bottom-color: transparent;

/* Global values */
border-bottom-color: inherit;
border-bottom-color: initial;
border-bottom-color: revert;
border-bottom-color: revert-layer;
border-bottom-color: unset;
```

The `border-bottom-color` property is specified as a single value.

### Values

- {{cssxref("&lt;color&gt;")}}
  - : The color of the bottom border.

## Formal definition

{{CSSInfo}}

## Formal syntax

{{csssyntax}}

## Examples

### A div with a border

#### HTML

```html
<div class="my-box">
  <p>
    This is a box with a border around it. Note which side of the box is
    <span class="red-text">red</span>.
  </p>
</div>
```

#### CSS

```css
.my-box {
  border: solid 0.3em gold;
  border-bottom-color: red;
  width: auto;
}

.red-text {
  color: red;
}
```

#### Result

{{EmbedLiveSample('A_div_with_a_border')}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The border-related CSS shorthand properties: {{Cssxref("border")}}, {{Cssxref("border-bottom")}}, and {{Cssxref("border-color")}}.
- The color-related CSS properties for the other borders: {{Cssxref("border-right-color")}}, {{Cssxref("border-top-color")}}, and {{Cssxref("border-left-color")}}.
- The other border-related CSS properties applying to the same border: {{cssxref("border-bottom-style")}} and {{cssxref("border-bottom-width")}}.
- The default [`currentcolor`](/en-US/docs/Web/CSS/color_value#currentcolor_keyword) color value.
