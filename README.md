# Sup Wallet

## Vision

Sup Wallet is the next-gen consumer wallet aimed at onboarding 3 billion WhatsApp users to the Algorand Blockchain. Our vision is to allow any user to create a wallet with their phone number using WhatsApp and to send, receive, or swap Algorand cryptocurrency just by chatting on WhatsApp.

## Description

### Problem

The user experience (UX) of existing wallets makes it very difficult for people to interact with cryptocurrency for the first time.

### Solution

Sup Wallet allows anyone to use WhatsApp as a wallet to send, receive, or swap algorand cryptocurrency by chatting with a WhatsApp bot. We have replicated how Account Abstraction works but in Algorand through the Algo Kit. Users only need to interact with a WhatsApp bot. Sup Wallet will create a smart contract to store the relationship between the phone number and the Algorand wallet. We are using Smart Signatures to authorize transactions without the need to access the wallet's private key associated with the phone number.

## How It Works

1. **User Interaction with WhatsApp Bot**: Users interact with the Sup Wallet bot on WhatsApp to create a wallet, send, receive, or swap algorand cryptocurrency.

2. **Backend - API**:
    - **Save Phone Number**: The phone number is saved using the Algo SDK.
    - **Create Wallet**: A wallet is created using the API.
    - **Create Transactions**: Transactions are managed using the API.

3. **Algorand Integration**:
    - **Smart Contract**: A smart contract is created to store the relationship between the phone number and the Algorand wallet.
    - **Smart Signatures**: Smart signatures are used to authorize transactions without accessing the wallet's private key.

## Components

- **WhatsApp Bot**: The interface for users to interact with their wallet.
- **API**: Backend service to handle requests from the WhatsApp bot.
- **Algo SDK**: Used to interact with the Algorand blockchain.
- **Smart Contracts**: Used to store user information and manage transactions on the Algorand blockchain.

## Architecture


## Testing Instructions - Configuration

To configure the database connection, you will need to create a file named `orm.config.json` at the root of the project with the following structure:

```json
{
    "type": "your database type",
    "host": "your database host",
    "port": "your database port",
    "username": "your database username",
    "password": "your database password",
    "database": "your database name",
    "entities": ["src/**/*.entity.ts"],
    "migrations": ["src/database/migrations/*.ts"],
    "cli": {
        "migrationsDir": "src/database/migrations"
    }
}
```

For development and production, it's recommended to use separate environment files. Create a file named .env.development for development and a file named .env.production for production. These files should be located at the root of the project.

# .env.development or .env.production
```js
# Application environment variables.
NODE_ENV=your_environment
PORT=0000

# Database environment variables.
DB_PORT=0000
DB_HOST=https://example.com
DB_NAME=example
DB_USER=username
DB_PASSWORD=password
```

## Installation

```bash
$ yarn install
```

## Running the app

```bash
# development
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```

## Test

```bash
# unit tests
$ yarn run test

# e2e tests
$ yarn run test:e2e

# test coverage
$ yarn run test:cov
```
