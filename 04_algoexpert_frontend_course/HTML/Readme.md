1. HTML Introduction
   - Empty Tags ```<hr/>```

2. Tables
   - Caption
   - colgroup
      - col -> span
   - Thead
   - Tbody
   - Tfoot
   - tr
      - th
      - td

3. Forms
   - Types
      - text  
      - password 
      - date  
      - checkbox 
      - radio 
         - name
         - value
      - screen-reader (Accessibility) 
         - Use *for* in label and **id** in input
         - placeholder
      - fieldset (Create a box to contain the form elements)
         - legend
      - validation
         - min length
         - max length
         - step
         - required

4. DOM: The programming interface for interacting with HTML document represented as a tree data structure. Each element is a **node** in the DOM tree, with nested content represented as children in the tree

5. Accessibility: Building websites for everyone (People with disability)
   - Nodes: *have* name, description, role, status
   - DOM -> Accessibility Tree -> Assistive Technology
   - **How to write accessible HTML**
      - Use descriptive content, labels & alt attributes
      - Use semantic elements
      - Test keyboard controls
      - [WAI-ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques): Web Accessibility Initiative - Accessible Rich Internet Applications
         - Roles
            - Landmark Roles: banner, main, navigation
               - Major Content Areas
               - Oftentimes navigated to first
            - Structural Roles: Tooltip, list, table
               - Document Structural Information
            - Widget Roles: Tab, searchbox, button
               - Interactive Elements
            - Window Roles: dialog, alert dialog
               - sub-windows in the browser
            - Live Region Roles: Timer, Log, Alert
               - Dynamic content changes
            - Aria-live: Tell the user as per the importance of the matter
               - Dynamic content & importance: 
                  - Off: don't announce changes
                  - Polite: announce changes when idle 
                  - Assertive: announce changes as soon as possible
         - Properties
            - aria-label & aria-labelledby
            - aria-description & aria-describedby
         - States
            - aria-checked
            - aria-disabled
            - aria-expanded
            - aria-hidden
            - aria-pressed
            - aria-selected

6. MetaTags
   - Providing extra data about the webpage
     - viewport
     - author
     - description (SEO)
   - Use **name** and **content** pair