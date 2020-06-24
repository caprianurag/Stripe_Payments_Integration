## Submitted by Anurag Juneja

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app). 

## Assumptions

1. The instructions for this README assume that the project would be run on an Apple Macbook.
2. It is assumed that the tester of this application has a stripe account.
3. It is also assumed that the tester of this application knows how to get their API and secret keys from their Stripe account.
4. The instructions for verifying payments in the Stripe account are not part of this README and it is assumed that the tester of this application knows how to do that.


## Project files

1. Download the project folder `Stripe_Payments_Integration` to your local machine. 
2. Get your secret API key from your Stripe account and use in file server.js in the project.
3. Get your publishable API key from your Stripe account and use in file src/App.js.

## Install Stripe
Install the required Stripe libraries on your machine. 

1. Open a terminal window.
2. Install the Stripe Node library
`npm install --save stripe`
3. Add Stripe to your React app
`npm install --save @stripe/react-stripe-js @stripe/stripe-js`

## Install Stripe CLI

1. Download the latest mac-os tar.gz file from [Stripe-CLI](https://github.com/stripe/stripe-cli/releases/latest).
2. Open a terminical window.
3. Unzip the file: `tar -xvf stripe_X.X.X_mac-os_x86_64.tar.gz` to a folder of your choice. This would install the Stripe CLI on your machine. Optionally, you can also put it in `/usr/local/bin` folder so you can execute it globally.
3. Once you have the Stripe CLI installed, run `stripe login` in the command line to generate a pairing code to link to your Stripe account. Press Enter to launch your browser and log in to your Stripe account to allow access. The generated API key is valid for 90 days. You can modify or delete the key under API Keys in the Dashboard.


## Log to file

1. Open another terminal window.
2. Navigate to the folder where you installed the Stripe CLI. Skip this step if you installed Stripe CLI to `/usr/local/bin`
3. Run `./stripe listen > output.txt`. This would log the payment logs to the output.log file in the current folder.

## Run the application

1. Open a terminal window.
2. Use the commad `cd` to navigate to the `Stripe_Payments_Integration` folder.
3. Run `npm start`. If you don't have `yarn` installed, please install it and ensure that its in your profile so you can run it
4. This will open a browser window with the payments field, ready to accept paymenTest paymentIntents

## Make a test payment
Use a test card number to try your integration. These card numbers work in test mode with any CVC, postal code, and future expiry date. Stripe also has a set of international test cards to test specific postal code formats (e.g. only allow numerical values for U.S. zip codes).

Payment succeeds `4242 4242 4242 4242`<br>
Payment requires authentication `4000 0025 0000 3155`<br>
Payment is declined `4000 0000 0000 9995`

## Check Payments
You can check the payment attempst two ways:
1. Check your Stripe Dashboard `https://dashboard.stripe.com/test/payments`
2. Check the log file output.log



