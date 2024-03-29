## What is responsive design?
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

## rem unit: `Root em`
- A rem unit is always relative to the `root <html> element`
- By default, rem value will be relative a multiple of 16px

## When to use px, em, rem?
1. font sizes: use `rem`, no compounding effect, more predictoble
2. margin & padding: use `em`, proportional scaling, based on current element's font size
3. line-height: use `unitless` number values
4. width: use `%`, flexible containers, flexible images
5. max-width: use `px`, easier to manage, ensures consistency

### Media Queries
Be able to create different layouts depending on the size of the browser viewport

### Mobile-first CSS
1. Write the base CSS with mobile devices in mind first
2. Use media queries to adjust the layout and design for wider screens

## Commom Breakpoints:
- 480px for mobile devices
- 768px for tablets
- 1024px for labtop screens
- 1280px for desktops

## Viewport Unit:
- Always relative to the size of the `user's viewport` (the area within browswer window)
- `vh`: viewport height -> 1vh is equal to 1% of the viewport height
- `vw`: viewport width -> 1vw is equal to 1% of the viewport width

## Flexbox vs. Grid
Flexbox only deals with 1-dimension at a time:
- `flex-direction: row`, we get columns (horizontal)
- `flex-direction: column`, we get rows (vertical)

Grid deals with both vertical and horizontal axis at a time:
- Allow us to simplify our markup
- Don't have to think too hard about how content to be grouped

### Grid:
- `Margins` no longer collapse and the `direct children` of the element become grid items
- Grid items `stretch` by default
- `grid-gap` or `gap` to create gap in between rows or cols

1. `display: gird` 
2. `grid-template-columns`: specify the **width** for # of columns
3. `grid-template-rows`: specify the **height** for # of rows
4. `grid-template` to specify grid layout (shorthand)
5. `minmax()`: setting a min-width and max-width to template columns and rows
6. `repeat()`: use it when we have `mulpitle columns` that are the same width, 1st param: how many `times` to be repeated, 2nd param: `size`
    - `auto-fit` will fit the columns we have defined into the available space
    - `auto-fill` will keep adding in new columns, even if they are empty

### The 'fr' unit
- Used to distribute a `fraction` of the available space
- Using `fr` for the size of a grid item makes it a flexible item
- Cannot use `fr` as the minimum size in `minmax()`

### Implicit vs. Explicit rows and cols:
- When we set up `grid-template-columons` or `grid-template-rows`, we are **explicitly** stating how big they should be
- If not the case, cols and rows are **implicitly** created. Using `grid-auto-rows` or `grid-auto-columns` to state how big they are

### Grid areas:
- `grid-template-areas` and `grid-area`
- Keeping track of row and column by assigning grid areas, effectively giving `names` to different parts of our grid and assign items to those areas
