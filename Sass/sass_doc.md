What I have learned Today:
1. SCSS Basics
SCSS is an extension of CSS, allowing us to use extra features like variables, loops, and functions to make our stylesheets easier to manage.

2. Variables
Variables let us store values (like colors, font sizes, or spacing) so that we can reuse them throughout the stylesheet. For example, instead of writing a color code multiple times, I can store it in a variable and use it whenever needed.
Example:
scss
Copy
$primary-color: #3498db;  // Blue color
3. Importing SCSS Files
SCSS lets us break down our styles into smaller files. We can then combine them using the @import command.
For example, I created a global.module.scss file for all my variables and settings and imported it into my main SCSS file.
4. Math Functions
SCSS allows us to use basic math operations (like adding, subtracting, etc.) directly in the stylesheet. For example, I used a function to darken a color when hovering over a button.
Example:
scss
Copy
$button-hover-color: darken($primary-color, 10%);  // Darkens the blue color by 10%
5. Maps
A map is like an object in JavaScript. It lets us store key-value pairs, which can be helpful for organizing things like button colors or spacing values.
Example:
scss
Copy
$button-colors: (green: #2ecc71, red: red, yellow: yellow);
6. Loops
SCSS has @each and @for loops to make repetitive styles easier to write.
Example (using @each loop):
scss
Copy
@each $color, $value in $button-colors {
  .button-#{$color} {
    background-color: $value;
  }
}
This creates button styles for each color in the $button-colors map without repeating the code.
7. Conditional Statements (if-else)
SCSS also lets us use @if, @else, and @else if to apply styles based on conditions.
Example:
scss
Copy
@if $button-color == red {
  background-color: red;
} @else {
  background-color: yellow;
}
8. Mixins
Mixins allow us to group styles into reusable blocks that can be included in multiple places. Mixins can also take arguments to make them more flexible.
Example:
scss
Copy
@mixin button-styles($bg-color, $color) {
  padding: 10px 20px;
  background-color: $bg-color;
  color: $color;
}
9. Parent Selector (&)
The & symbol in SCSS refers to the parent selector. This allows us to apply styles to elements that are nested inside others.
Example:
scss
Copy
.button {
  background-color: $primary-color;
  
  &:hover {
    background-color: darken($primary-color, 10%);
  }
}
