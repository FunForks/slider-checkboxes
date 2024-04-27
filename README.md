# Slider Checkboxes #

[Demo](https://funforks.github.io/slider-checkboxes)

A demonstration of how to convert a plain `input:checkbox` into an animated slider.

## Basic usage
Add the CSS from slider-checkbox.css to your project.

Wrap each checkbox input inside a label, and include three spans after the checkbox, with classes `pre`, `slot` and `post`.

```html
<label
  class="optional"
>
  <input
    type="checkbox"
  />
  <span class="pre">Text Before</span>
  <span class="slot"></span>
  <span class="post">Text After</span>
</label>
```

The `span.slot` will be used to generate a slot for a slider element. The slider element will be created by CSS as the pseudo element `span.slot::after`. The checkbox itself will be hidden.

Put text that you want to show to the left of the slider in `span.pre` and the text you want to show on the right in `span.post`.

By default, a series of checkboxes created in this way will be aligned with the slider in the centre. When the (invisible) checkbox is unchecked, the slider will appear in an "off" state at the left end of the slot. It will appear in a more active "on" state at the right end of the slot when the checkbox is checked.

## Advanced usage
You can apply different classes to the label wrapper to alter the way the slider appears and behaves.

* **label.reverse**  
  The "off" state will show the slider on the right
  
* **label.two-way**  
  The slider will retain its "on" colouration in both states, but the text at the empty end of the slot will appear in an "off" state.
  
* **label.left**
  The `span.pre` will be hidden, if present, and the slider widget will be aligned to the left.
  
* **label.right**
  The `span.post` will be hidden, if present, and the slider widget will be aligned to the right.
  
You can combine `left` or `right` with `reverse`.
  
## Customizing your slider checkboxes
You can custom the appearance of your slider checkboxes in two ways:

1. You can edit the custom CSS properties for the label rule. This will apply your changes to all checkboxes in your project.
2. You can add your own rules to override the custom CSS properties, as shown in the `custom.css` file.

> Note: In this demo, the `font-size` is set in `styles.css` so that it is proporitional to the size of the viewport. 