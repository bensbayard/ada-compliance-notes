# ADA Compliance Notes

* Refs: https://snippets.cacher.io/snippet/96f4b3a76774fa16176c

### Background Images

Background images behaving as standard images should be tagged and described
* Search: ```background-image: url(```
* Add in element: ```role="img" aria-label="Supporting Image"```
* Exclude: .css, .scss

### Include Hidden Link(s) That Allow Skipping Blocks - Main Content
Every page should include hidden links that by clicking on them (either using keyboard navigation or a screen-reader), the user will "skip" certain blocks directly to main landmarks such as main content, menu or footer.

* Add in opening body element ```<a href='#main-content' class='sr-only'>Skip to main content</a>```
* Search: Find the first component on the page with text or video with audio
* Add in element: ```id="main-content"```

### Links That Open in a New Tab
Links that open in a new tab or a new window should either have an aria-label attribute or a screen-reader only element explaining to screen-readers that this opens in a new tab.

* ```aria-label="(opens in a new tab)"```

### Menus should be tagged for assistive technology

Menus should either be built using the HTML5 "nav" element or include a "role" attribute that equals to "menu" or "navigation" to indicate a navigation landmark for screen-readers.

* Search: for a unique element attribute. 
* Added in element: ```role="navigation"```

### Interactive elements should be navigable using the keyboard
Interactive elements such as links, buttons and form fields should all be navigable using the keyboard by either using a focusable element (a, button, input, etc.) or including the "tabindex" attribute that equals to "0".

* Search: for a unique element attribute. 
* Add in element ```"tabindex"=0```

### Titles built as text tags should be labeled as headings for assistive technology
Elements that visually appear as titles but are coded with a non-heading HTML Tag should include a "role" attribute that equals to "heading" or have their tags fixed.

* Search: for a unique element attribute. 
* Add in element ```"role="heading"```

### Required form fields should be tagged for assistive technology
Required form fields should include an "aria-required" attribute that equals to "true" so blind users using screen-readers know their validation.

* Search: for relevant form. 
* Add in input element ```aria-required="true"```
