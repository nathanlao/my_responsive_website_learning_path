RWD is a web development approach that creates `dynamic changes` to the appearance of a website, ensure our sites work well and optimized for various screen size and orientation of the device being used to view it. Websites should adapt and accomodate any screen, and offer a seemless experience for users based on devices 

**Absolute units**: pixels is a fixed unit, will always appear the same size no matter where we view them

**Relative units**: 
- relative to anthor value
- dynamic flexibility
- resize & scale

## Percentage unit: 
when using a percentage for a width, the percentage is based on the width of its parent element

## em unit: 
set dynamic font sizes that are relative to their parent's font sizes, a convenient way to proportionally scale font sizes, margins, paddings

- Convert a px to em (desired px / parent element in px)
- Aside: An em value can compound from one level to the other (when deal with nested element in HTML)

### em for font size (relative to parent element's font size)
- `1em` is equal to the `parent element's font-size value` (relative to 16px(default) if no ancestors has been set font size)

### em for margin and padding (relative to the element's current font size)
- `1em` is equal to the `current element's font-size value`
