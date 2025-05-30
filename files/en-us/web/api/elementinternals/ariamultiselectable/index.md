---
title: "ElementInternals: ariaMultiSelectable property"
short-title: ariaMultiSelectable
slug: Web/API/ElementInternals/ariaMultiSelectable
page-type: web-api-instance-property
browser-compat: api.ElementInternals.ariaMultiSelectable
---

{{APIRef("Web Components")}}

The **`ariaMultiSelectable`** property of the {{domxref("ElementInternals")}} interface reflects the value of the [`aria-multiselectable`](/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-multiselectable) attribute, which indicates that the user may select more than one item from the current selectable descendants.

> [!NOTE]
> Setting aria attributes on `ElementInternals` allows default semantics to be defined on a custom element. These may be overwritten by author-defined attributes, but ensure that default semantics are retained should the author delete those attributes, or fail to add them at all. For more information see the [Accessibility Object Model explainer](https://wicg.github.io/aom/explainer.html#default-semantics-for-custom-elements-via-the-elementinternals-object).

## Value

A string with one of the following values:

- `"true"`
  - : More than one item may be selected at a time.
- `"false"`
  - : Only one item may be selected.

## Examples

In this example the value of `ariaMultiSelectable` is set to "true".

```js
class CustomControl extends HTMLElement {
  constructor() {
    super();
    this.internals_ = this.attachInternals();
    this.internals_.ariaMultiSelectable = "true";
  }
  // …
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [ARIA: listbox role](/en-US/docs/Web/Accessibility/ARIA/Reference/Roles/listbox_role)
