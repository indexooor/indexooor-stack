# 🤖 Indexooor Stack
📚 indexooor stack: the next gen dev tool for indexing smart contract data 🫶

### 📄 Repository Setup 

To fetch all modules use `git submodule update --init --recursive`. If you want to use modules seperately, use the equivivalent git command.

To update submodules to remote use `git submodule update --remote`

## 😃 About

Welcome to the Indexooor Stack, an open-source project for indexing and querying smart contract data. Our unique database schema allows for complex join queries and fetching full arrays and mappings from smart contracts, without the need for smart contracts to emit events.

The stack is composed of several submodules, each serving a specific purpose:

🚀 Core: Our core indexing service, written in Go, indexes smart contract slot data using a lightweight algorithm that detects slot changes for a contract in each block. All slot data is stored in a PostgreSQL database.
🔍 Queriooor: Our querying service, written in Python using FastAPI, allows developers to upload a storage layout for their contract address and query variables by their name. The service finds the slot and data type of the variable, fetches data, and decodes it before returning it to the user.
🖥️ Goooi-queriooor: Our UI web-app, built using Vite, simplifies querying by allowing developers to query in the browser instead of calling a REST API.
🎮 Simulatooor: Our simulator service, written in Go, simulates all our services and demonstrates the workings of the Indexooor Stack.
🐘 Op-geth: Our version of the Optimism Go Ethereum, which has the Indexooor Core integrated into the node for indexing smart contract data. This makes things easier for developers, who can then run an extra querier connecting their database with it for users to query data!
Our stack is lightweight and easy to run, making it accessible for developers of all levels. In this README, we'll explain how to set up and use each submodule of the stack. Let's get started!

## 🛠️ Setup

### Core

To set up the Core submodule, follow these steps:

- Install Go and PostgreSQL on your machine.
- Clone the Indexooor Stack repository and navigate to the core directory.

Once this is done refer [core-setup](https://github.com/indexooor/core/blob/main/README.md)

### Queriooor

To setup the Queriooor submodel, follow there steps:

- Have `python3` and PostgreSQL installed on your machine

Once this is done refer [queriooor-setup](https://github.com/indexooor/queriooor)

### Goooi-querioor

This is a vanilla vite project, follow the instruction for the same or use our [deployment](https://goooi-queriooor.vercel.app/)

### Simulatooor
 
Add instructions

### Op-geth

Refer [Op-Geth Readme](https://github.com/indexooor/op-geth/blob/optimism/README.md)


