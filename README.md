## Simplify Polymer Credit Card Form Element
This is a custom element that enables easy credit card payments with Simplify Commerce.

### Demo Installation

Install the bower components
```javascript
bower install
```
                    
Install grunt
```
npm install
```

Run the app
```
grunt serve
```

### Use the Element

Import the element
```
<link rel="import" href="elements/credit-card-form.html">
```

Use the element
```
<credit-card-form key="MY_PUBLIC_KEY" />
```

Handle the response
```                
<script>
    // Wait for 'polymer-ready'
    window.addEventListener('polymer-ready', function(e) {
        var ccForm = document.querySelector('credit-card-form');

            // listen to token response
        ccForm.addEventListener('token-response', function(event) {
            console.log(event.detail.token); // Extract the token value

            // Send token to the server to create the payment
        });
    });
</script>    
```