# Express Conditional Middleware

This module provides a conditional middleware for express. Use as follows:

```javascript
var conditional = require('express-conditional');

// Simple boolean method.
app.use(conditional(true, function (req, res, next) {
  // ...
});

// Function method.
app.use(conditional(
  function (req, res, next) {
    return req.get('accept') === 'application/json';
  },
  function (req, res, next) {
    // ...
  }
));
```
