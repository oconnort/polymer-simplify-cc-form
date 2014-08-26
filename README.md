# Simplify Polymer Credit Card Form Element
This is a custom element that enables easy credit card payments with Simplify Commerce.

### Install the Demo

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
&lt;link rel="import" href="elements/credit-card-form.html"&gt;
```

Use the element
```
&lt;credit-card-form key="MY_PUBLIC_KEY" /&gt;
```

Handle the response
```                
    &lt;script&gt;<br/>
        // Wait for 'polymer-ready'
        window.addEventListener('polymer-ready', function(e) {
            var ccForm = document.querySelector('credit-card-form');

            // listen to token response
            ccForm.addEventListener('token-response', function(event) {
                console.log(event.detail.token); // Extract the token value

                // Send token to the server to create the payment
            });
        });
    &lt;/script&gt;    
```