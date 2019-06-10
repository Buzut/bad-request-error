# bad-request-error
BadRequestError is a custom error constructor for HTTP errors (bad parameters, forbidden, unauthorized…).

It takes an error message as first parameter and optionally a [HTTP error code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_errors) as second parameter (defaults to `400`).

## Installation
As it uses JavaScript classes it requires at least Node V6.

```
npm install --save bad-request-error
```

## Usage
```js
const BadRequestError = require('bad-request-error');

async function addComment(req, res) {
    await const isCorrectPasswd = checkPasswd(req);
    if (!isCorrectPasswd) return throw new BadRequestError('Your password looks wrong', 401);

    // whatever you have to do if password is correct
}
```

## Contributing
There's sure room for improvement, so feel free to hack around and submit PRs!
Please just follow the style of the existing code, which is [Airbnb's style](http://airbnb.io/javascript/) with [minor modifications](.eslintrc).

To maintain things clear and visual, please follow the [git commit template](https://github.com/Buzut/git-emojis-hook).
