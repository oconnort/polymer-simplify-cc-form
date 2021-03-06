## Simplify Polymer Credit Card Form Element
This is a custom element that enables easy credit card payments with Simplify Commerce.

Ref: http://www.simplify.com/commerce/docs
Demo: http://oconnort.github.io/

#### Demo Installation

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

#### Use the Element

Import the element
```html
<link rel="import" href="elements/credit-card-form.html">
```

Use the element
```html
<credit-card-form key="MY_PUBLIC_KEY" />
```

Handle the response
```html                
<script>
    // Wait for 'polymer-ready'
    window.addEventListener('polymer-ready', function(e) {
        var ccForm = document.querySelector('credit-card-form');

            // listen to token response
        ccForm.addEventListener('token-response', function(event) {
            console.log(event.detail.token); // Extract the token value

            // Send token to the server to create the payment
            // https://www.simplify.com/commerce/docs/apidoc/payment
        });
    });
</script>    
```