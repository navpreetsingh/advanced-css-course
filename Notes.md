1. 3 pillars to write good code and build good websites
  - Responsive Design
    - Fluid layouts
    - Media queries
    - Responsive images
    - Correct units
    - Desktop-first vs mobile-first
  - Maintainable and scalable code
    - Clean
    - Easy to understand
    - Growth
    - Reusable
    - How to organize files
    - How to name classes
    - How to structure HTML
  - Web Performance
    - Less HTTP requests
    - Less code
    - Compress code
    - Use a CSS preprocessor
    - Less images
    - Compress images

2. Use of inheritance
  - Use of **REM**
  - use of **percentage**
  - this helps to modify design as user changes the zoom setting of the page
  - use of **inherit**

3. BEM: block element modifier
  - .block
  - .block__element
  - .block__element--modifier

4. CSS folder structure
  - base: put the basic product definitions
  - components: have one file for each component
  - layout: define overall layout of the project
  - pages: have styles for specific pages of the project
  - themes: want to implement different themes
  - abstracts: put code that doesn't output any CSS (variables or mixins)
  - vendors: all 3rd party css goes

5. Basic Responsive Design Principles
  - Fluid Layouts
    - allow webpage to adapt to current viewport width or height
    - use % (or vh/vw) unit instead of px of elements (Adapt to viewport)
    - use max-width instead of width
    - 3 ways
      - Float Layouts
        - old way of building layouts (Outdated)
      - Flexbox
        - 1-dimensional row
        - perfect for component layouts
      - CSS Grid
        - 2 dimensional grid
        - perfect for page layouts and complex components
  - Responsive Units
    - Use **rem** instead of px for most lengths
    - to make it easy to scale the entire layout down (or up) automatically
  - Flexible Images
    - by default, images don't scale automatically as we change the viewport, so we need to fix that
    - always use % for image dimensions, together with the max-width property
  - Media Queries
    - change css styles on certain viewport widths (called breakpoints)
  
6. Use of **codingheroes.io** 