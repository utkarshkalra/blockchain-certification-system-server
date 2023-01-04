# Certificate Generation and Validation Using Blockchain

> Built using Ethereum on local blockchain setup

## Steps to set up local development environment

### Setting local blockchain

1. We need to install CLI version of Ganache.

   ```bash
   npm install -g ganache-cli
   ```

   > Ganache provides us our personal local blockchain network which we can use to develop our blockchain application. It also gives temporary test accounts with fake ethereum which we can use to run our apps. We need to start the RPC server before running our application.

1. To start the RPC server run the command

   ```bash
   npm run ganache
   ```

   > Windows user will need to run this command in separate command prompt or terminal.

1. Deploy the smart contract to the local blockchain.

   ```bash
   npm run contract-deploy
   ```

> The above 2 steps need to be run everytime you are running the project.

### Setting local database

> MongoDB server should be running as a background Process

1. Open mongo in terminal using command `mongo`

1. Then change the db using command

   ```bash
   use certification
   ```

1. Then set DB user and password with the following command

   ```javascript
   db.createUser({
     user: "<YOUR USER NAME>",
     pwd: "<YOUR USER PASSWORD>",
     roles: [{ role: "dbOwner", db: "certification" }],
   });
   ```

1. Include these username and password in the `.env` file.

### Now we can start the server

```bash
npm start
```
