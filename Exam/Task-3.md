Dear User,

jQuery uses different means of subscribing to events. After you have selected the DOM element you wish to manipulate, you have several options of subscribing to an event:
* Using the `on()` function which takes as first parameter the type of the event and as a second - the function to be executed when the event is fired. Consider the following code snippet:
```
$('#home-page').on('click', function () {
            hideAllContent();
            $('#home-page-content').show();
        });
```

* Using the syntactic sugar provided by jQuery - the `click()` function which requires as parameter only the callback function. The same code as above in this scenario would look like this:
```
$('#home-page').click(function () {
            hideAllContent();
            $('#home-page-content').show();
        });
```

For further information on these jQuery functions, please visit the following links:
* https://api.jquery.com/click/
* https://api.jquery.com/on/

Feel free to contact us for feedback or if you have any further questions.

Best regards