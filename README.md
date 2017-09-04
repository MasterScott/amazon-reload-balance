# Work in progress

--------

# Amazon Reload Balance

Reload your Amazon's account balance with your credit/debit cards.

## Usage

```js
import {AmazonReloadBalance} from 'amazon-reload-balance';

const amazonReloadBalance = new AmazonReloadBalance();
await amazonReloadBalance.signIn('username', 'password');

// The credit card you would like to use should be already registered on your Amazon account.
// Minimum amount is 0.50
await amazonReloadBalance.reload(20.00, 'last 4 digits of your card number');
await amazonReloadBalance.reload(15.75, 'last 4 digits of your card number');

await amazonReloadBalance.signOut();
```

For running the example:

1. create `/config/local.json` and fill out values like this:

```json
{
  "email": "your email on Amazon",
  "password": "your password"
}
```

## Requirements

Intended to be run on Node 4.x or higher as a requirement of Nightmare.

## Why did you build this?

Sometimes you just want to automate reloading Amazon balance, right? :)

I've been optimizing my micro management of my life and one of them is periodically
using ~20 of my unused credit cards to prevent them from being closed. Otherwise, it would negatively affect my credit score.
One option is to pay one item with each of them, such as utilities and cellphone bill.
But I wanted to optimize more to collect more credit card points.
I found that you can reload your Amazon balance as low as 50 cents,
so I've been reloading the balance with all of my unused credit cards.

In addition, I wanted to try out Nightmare, Vue, Jest, and no semicolons in this module, and AWS lambda with scheduled events for periodically reloading my Amazon balance.

## License

[WTFPL](http://www.wtfpl.net)
