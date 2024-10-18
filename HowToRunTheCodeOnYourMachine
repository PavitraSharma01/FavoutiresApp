# Favourites Program: Local Setup Guide

This guide will walk you through the process of setting up and running the **Favourites program** locally using Anchor.

---

## **Prerequisites**

1. **Install Anchor**  
   Follow the instructions on the official Anchor GitHub repository:  
   [Anchor Installation Guide](https://book.anchor-lang.com/chapter_2/installation.html)  

2. **Install Solana CLI**  
   Install the Solana CLI and configure it to use the local cluster:

   ```bash
   sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
   solana config set --url localhost
   ```

---

## **Steps to Run the Project Locally**

### **1. Clone and Extract the Project**

1. Extract the project zip file in your desired directory.
2. Navigate into the project directory:

   ```bash
   cd favourites-project
   ```

---

### **2. Install Dependencies**

Make sure **Yarn** is installed. If not, install it with:

```bash
npm install -g yarn
```

Now, install the dependencies by running:

```bash
yarn
```

---

### **3. Build the Program**

Use the following command to compile your Anchor program:

```bash
anchor build
```

If the build is successful, it will generate a `.so` file in the `target/deploy/` directory.

---

### **4. Test the Program**

Run the tests to ensure everything is working correctly:

```bash
anchor test
```

If everything passes, the program is correctly set up!

---

### **5. Run the Client**

Use the following command to run the client-side application:

```bash
anchor run client
```

---

## **Note**

If you are using **Playground-exclusive features** (like `pg.wallets.myWallet`), you will need to manually load each keypair when running locally.  
Example for manually loading a keypair:

```javascript
const fs = require('fs');
const anchor = require('@project-serum/anchor');

// Load the wallet keypair
const keypair = anchor.web3.Keypair.fromSecretKey(
    Uint8Array.from(JSON.parse(fs.readFileSync('./path/to/keypair.json')))
);
```

---

### **Troubleshooting**

1. **Anchor Build Fails:**  
   Ensure Solana CLI and Anchor are properly installed. Run:
   ```bash
   solana --version
   anchor --version
   ```

2. **Cannot Connect to Local Validator:**  
   Start a local validator with:
   ```bash
   solana-test-validator
   ```

---

This guide should help you get your project up and running locally. If you encounter any issues, refer to the Anchor documentation or reach out for support.
