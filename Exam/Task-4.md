# Creating a jQuery content manager
---
### HOW-TO
Create a dynamic page content depending on selected menu items

### DESCRIPTION
Implementing a jQuery content manager is easy and intuitive if you simply follow the instructions below:

### SOLUTION
*(Note: You are free to use your favorite text editor for this demo)*
1. Create a blank html document.
2. Include the jQuery library. For this demo we will use the jQuery CDN:
```
<script src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
```
3. Create an unordered list with list items that will serve as menu items and set their `id` attributes. We will need them in the next few steps:
```
<ul id="main-menu">
        <li id="home-page">Home</li>
        <li id="courses-page">Courses</li>
        <li id="about-page">About</li>
        <li id="contact-page">Contact</li>
</ul>
```
4. Add `div` elements containing the content to be dynamically changed and set `id` attributes for a more convenient DOM selection. We also set the `style` tag to `display: none' in order to hide the page content when the whole html page is initially loaded:
```
<div id="main-content">
        <div id="home-page-content" style="display: none">Home content</div>
        <div id="courses-page-content" style="display: none">Courses content</div>
        <div id="about-page-content" style="display: none">About content</div>
        <div id="contact-page-content" style="display: none">Contact content</div>
</div>
```

5. Include a script tag or create a new JavaScript file and include it, **after** the script tag including the jQuery library. There we will write the code to subscribe to a click event for each menu item. The callback function for each click event will hide all content and show only the one corresponding to the clicked menu item. We will define a function `hideAllContent()` using the jQuery function `hide()` for the first part of our event handler function to avoid unnecessary repetition of code. For simplicity, we will implement the first approach:
```
<script>
function hideAllContent() {
            $('#home-page-content').hide();
            $('#courses-page-content').hide();
            $('#about-page-content').hide();
            $('#contact-page-content').hide();
        }

        $('#home-page').on('click', function () {
            hideAllContent();
            $('#home-page-content').show();
        });

        $('#courses-page').on('click', function () {
            hideAllContent();
            $('#courses-page-content').show();
        });

        $('#about-page').on('click', function () {
            hideAllContent();
            $('#about-page-content').show();
        });

        $('#contact-page').on('click', function () {
            hideAllContent();
            $('#contact-page-content').show();
        });
</script>
```

### COMPLETE SOURCE CODE
[Click here](http://dojo.telerik.com/AjEwU)

*(Note: Basic CSS styles have been applied for a better overall look of this demo)*


### USEFUL RESOURCES
* [jQuery DOM selectors](https://api.jquery.com/category/selectors/)
* [jQuery on() function](http://api.jquery.com/on/)