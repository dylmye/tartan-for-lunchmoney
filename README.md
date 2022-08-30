# Tartan for Lunchmoney
## Sync any Plaid Link compatible bank account to Lunch Money

---

Lunchmoney recently announced that they were unable to continue syncing some foreign (aka UK) bank accounts in their pilot programme. This script enables you to continue syncing transactions to Lunchmoney, by utilising both Lunchmoney's API and Plaid's generous development provisions + API. Lunchmoney previously provided UK bank account sync via Plaid so the selection of accounts should be the same.

This Amplify template includes a backend that processes [Plaid transaction webhook](https://plaid.com/docs/transactions/webhooks/) events to create/update/delete transactions in Lunchmoney using their [API](https://lunchmoney.dev/#transactions). You can sync up to 100 of your bank accounts to Lunchmoney.

You can deploy this template by clicking this button:

[![amplifybutton](https://oneclick.amplifyapp.com/button.svg)](https://console.aws.amazon.com/amplify/home#/deploy?repo=https://github.com/dylmye/tartan-for-lunchmoney)

Alternatively, if you have the [AWS CLI](https://awscli.amazonaws.com/v2/documentation/api/latest/reference/amplify/create-app.html) installed, you can run this command:

```
aws amplify create-app --name WHATEVER_NAME_HERE --repository https://console.aws.amazon.com/amplify/home#/deploy?repo=https://github.com/dylmye/tartan-for-lunchmoney --access-token MY_TOKEN
```

## Test locally

0. Clone this repo locally: `git clone https://github.com/dylmye/tartan-for-lunchmoney && cd tartan-for-lunchmoney && yarn`
1. Import the backend environment deployed by the Amplify Console to your repo (the `amplify/team-provider.json` file contains information on all backend environments in your AWS account). The GIF below shows how you to copy the amplify env import command from the Amplify Console.

<img src="https://github.com/aws-samples/create-react-app-auth-amplify/blob/master/src/images/import-backend.gif" width="800"/>

2. Run `amplify pull`. You should see the `amplify/team-provider.json` updated with a backend named `amplify`.
3. Run locally with `yarn start`.

---

Parts of this Readme are shamelessly stolen from [here](https://github.com/aws-samples/create-react-app-auth-amplify), thanks to the AWS team including [Nikhil Swaminathan](https://github.com/swaminator) + [Henri Yandell](https://github.com/hyandell).
