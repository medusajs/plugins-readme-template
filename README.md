# [Plugin Name]

_Short description of what this plugin does_

Receive payments on your Medusa commerce application using Stripe.

_Add any of your links to the following links._

[Plugin Documentation](https://docs.medusajs.com/plugins/payment/stripe) | [Medusa Website](https://medusajs.com/) | [Medusa Repository](https://github.com/medusajs/medusa)

## Features

_Either a bullet list of features or a checklist of features. The checklist is helpful if you're planning on adding more features in the future and can act as a roadmap._

- Receive payments from any sales channel.
- Capture payments from the admin dashboard.
- View payment analytics through Stripe's dashboard.

---

## Prerequisites

_A bullet list of requirements before installing and using the plugin. The requirements can be tools to be installed, accounts to be created, keys to be retrieved, or anything similar. Also, include a link that helps developers learn how to install the tool._

- [Node.js v14 or greater](https://nodejs.org/en)
- [A Medusa backend](https://docs.medusajs.com/development/backend/install)
- [Stripe account](https://stripe.com/)

---

## How to Install

_List the steps necessary to install the plugin._

1\. Run the following command in the directory of the Medusa backend:

  ```bash
  npm install medusa-payment-stripe
  ```

2\. Set the following environment variables in `.env`:

  ```bash
  STRIPE_API_KEY=sk_...
  STRIPE_WEBHOOK_SECRET=whsec_...
  ```

3\. In `medusa-config.js` add the following at the end of the `plugins` array:

  ```js
  const plugins = [
    // ...
    {
      resolve: `medusa-payment-stripe`,
      options: {
        api_key: process.env.STRIPE_API_KEY,
        webhook_secret: process.env.STRIPE_WEBHOOK_SECRET,
      },
    },
  ]
  ```

---

## Test the Plugin

_List the steps necessary to test the plugin._

1\. Run the following command in the directory of the Medusa backend to run the backend:

  ```bash
  npm start
  ```

2\. Enable Stripe in a region in the admin. You can refer to [this User Guide](https://docs.medusajs.com/user-guide/regions/providers) to learn how to do that. Alternatively, you can use the [Admin APIs](https://docs.medusajs.com/api/admin#tag/Region/operation/PostRegionsRegion).

3\. Place an order using a storefront or the [Store APIs](https://docs.medusajs.com/api/store). You should be able to use Stripe as a payment method.

---

## Additional Resources

_List here any additional resources that can be helpful in the development or usage of this plugin._

- [Stripe Plugin Documentation](https://docs.medusajs.com/plugins/payment/stripe)