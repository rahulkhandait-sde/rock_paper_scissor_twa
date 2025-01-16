# Rock Paper Scissors TWA

A decentralized, blockchain-powered version of the classic rock-paper-scissors game, built with TypeScript, React, and Flow blockchain integration.

## Features

- **Blockchain Integration**: Utilizes Flow Testnet for transparent and secure game logic.
- **User Authentication**: Authenticates users via thirdweb's Sign-In with Ethereum (SIWE) for seamless access.
- **Smart Contract**: Interacts with a smart contract deployed on the Flow Testnet.
- **Responsive Design**: Optimized for both desktop and mobile platforms.

## Prerequisites

1. **Accounts and Credentials**:
   - [Vercel](https://vercel.com) account for deployment.
   - [thirdweb](https://thirdweb.com) dashboard account.
   - [Flow Wallet](https://wallet.flow.com) Testnet account.

## Environment Setup

1. **Create a `.env` File**:
   - Add your thirdweb client ID:
     ```
     NEXT_PUBLIC_THIRDWEB_CLIENT_ID=your_thirdweb_client_id
     ```

2. **Set Up Flow Credentials**:
   - Create a `testnet-account.pkey` file with your Flow private key.
   - Update `flow.json` with your Testnet account address:
     ```json
     {
       "accounts": {
         "testnet-account": {
           "address": "<YOUR_FLOW_ADDRESS>",
           "key": {
             "type": "file",
             "location": "testnet-account.pkey"
           }
         }
       }
     }
     ```

## Smart Contract Deployment

1. **Install Flow CLI**:
   - Run the following command to install Flow CLI:
     ```sh
     sh -ci "$(curl -fsSL https://raw.githubusercontent.com/onflow/flow-cli/master/install.sh)"
     ```

2. **Deploy Contract to Testnet**:
   - Deploy your contract using Flow CLI:
     ```sh
     flow project deploy --network testnet
     ```

## Frontend Deployment

1. **Install Dependencies**:
   - Install project dependencies:
     ```sh
     npm install
     ```

2. **Build the Project**:
   - Build the project for production:
     ```sh
     npm run build
     ```

3. **Deploy to Vercel**:
   - Deploy your application to Vercel:
     ```sh
     vercel --prod
     ```

## Security Notes

- **Private Key**: Keep your `testnet-account.pkey` secure and never commit it to version control.
- **thirdweb Client ID**: Your thirdweb client ID (`NEXT_PUBLIC_THIRDWEB_CLIENT_ID`) is safe to commit.
- **Environment Variables**: Add `.env` to your `.gitignore` file if it's not already there.

## Team

- **Rahul Khandait**: [@rahulkhandait](https://twitter.com/rahulkhandait)

Feel free to contribute or reach out to the team for any queries!

**Note**: Since the project is on the Flow Testnet, users can acquire test FLOW tokens from the [Flow Testnet Faucet](https://testnet-faucet.onflow.org/fund-account) to interact with the application.

For more information on integrating thirdweb's Sign-In with Ethereum, refer to their [documentation](https://portal.thirdweb.com/connect/auth). 


[<img src="https://api.gitsponsors.com/api/badge/img?id=909485127" height="20">](https://api.gitsponsors.com/api/badge/link?p=lgtuiOSs+TTeesHNGnzI0urR+h2yYJWGKQHD3Bq8woFI0J1tBQ10XHC2AEH9mKPNdurFKTv0F7O/2NDGIf6YizYH+/N3FGZjqPphuxqz7AMytmkTqZaUDz/7mPgMWYhP85P7si4s10CHromHzHrHfc2KrJk0KT4CeizJUCl9hrY=)
