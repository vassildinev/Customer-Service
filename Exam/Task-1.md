Dear User,

With the current state of the code this behavior is expected. Please make sure you are not missing the hash symbol (#) when selecting the DOM elements with jQuery.
Your function should look like this:

```
function hideAllContent() {
            $('#home-page-content').hide();
            $('#courses-page-content').hide();
            $('#about-page-content').hide();
            $('#contact-page-content').hide();
}
```

Feel free to contact us for feedback or if you have further questions regarding our product.

Best regards