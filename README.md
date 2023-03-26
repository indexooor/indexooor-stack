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

# 🚀 Getting Started

Now that you've set up each submodule of the Indexooor Stack, let's learn how to use them.

## Indexing with Core

1. Start the indexer giving `rpc`, `contractAddresses` and `startBlock`, where `rpc` is the rpc url of your node, `contractAddresses` is `,` delimited list of your contracts and `startBlock` is the block number where you want to start indexing from.

### Querying with Qeuriooor

To query a variable in a smart contract using the Queriooor submodule, follow these steps:

1. Upload the storage layout for the smart contract you want to query by making a POST request to `/queriooor/setStorageLayout` with the contract's address and the storage layout as the body of the request.
2. To query a variable, make a POST request to ``/queriooor/getVariable` with the contract's address, the variable name, and key/deep key information.
3. Other API calls can be viewed in the swagger doc at `/docs`

Queriooor will find the slot and data type of the variable, fetch its data from the PostgreSQL database, and return the decoded value.


### Querying with Goooi-queriooor

To query a variable in a smart contract using the Goooi-queriooor web-app, follow these steps:

1. Start the Queriooor service 
2. Start the Goooi-Queriooor after doing the setup using `npm run dev` or visit our [hosted webapp](https://goooi-queriooor.vercel.app/).
3. Add queriooor url, contract address, variable name and key information.

### Running Indexooor with OP-Geth Node

Add instructions

## 📚 Documentation 

If you're looking for more detailed information on how to use the Indexooor Stack, check out our documentation. We have comprehensive guides on each submodule as well as a glossary of terms.


- [Indexooor Core documentation](https://github.com/indexooor/core/blob/main/README.md)
- [Queriooor documentation](https://github.com/indexooor/queriooor)
- [Goooi-queriooor documentation]()
- [Simulatooor documentation]()
- [Indexooor Stack glossary]()

If you have any questions or issues while using the Indexooor Stack, feel free to open an issue on our GitHub repository. We're happy to help!

## 🤝 Contributing

We welcome contributions from the community! If you'd like to contribute to the Indexooor Stack, please take a look at our [contributing guidelines](https://github.com/indexooor/indexooor-stack/blob/main/README.md#-contributing-guidelines) to get started.

We use GitHub issues and pull requests for all contributions. If you'd like to report a bug or suggest a feature, please open an issue on our GitHub repository. If you'd like to submit a code change, please fork our repository and submit a pull request.

All contributions are appreciated, no matter how small. We're grateful for any help in making the Indexooor Stack even better!

## 📞 Contact

If you have any questions or feedback about the Indexooor Stack, you can reach us through the following channels:

- Email: kaushalpatil10@gmail.com
- Twitter: Coming Soon
- Discord: Coming Soon

We'd love to hear from you and answer any questions you may have about the Indexooor Stack. Don't hesitate to reach out!

## 🙏 Acknowledgements

We would like to thank the following people and organizations for their contributions to the Indexooor Stack:

- The developers of [Solc](https://github.com/ethereum/solidity), [Geth](https://github.com/ethereum/go-ethereum), [PostgreSQL](https://www.postgresql.org/), [FastAPI](https://fastapi.tiangolo.com/), and [Vite](https://vitejs.dev/) for creating and maintaining the tools we use in our stack.
- Special thanks to developers of projects such as [slither](https://github.com/crytic/slither) and [heimdall-rs](https://github.com/Jon-Becker/heimdall-rs) which were refered heavily during this build.
- The contributors to the open source community for providing valuable feedback and contributions to the projects we depend on.
- Our users for providing feedback and support as we continue to develop and improve the Indexooor Stack.
- The entire Ethereum community for advancing the state of the art in blockchain technology and inspiring us to build better tools.

Thank you all for your support and contributions!

## 📢 Spread the Word

If you find the Indexooor Stack useful, we encourage you to share it with others in the blockchain development community. Here are some ways you can help spread the word:

- Star our [GitHub repository](https://github.com/indexooor/indexooor-stack) and [follow us](https://github.com/orgs/indexooor/people) on GitHub.
- Tweet about the Indexooor Stack and mention us `@kau5hal10`, `@manav24_`, `@MeetModi_`, `PARAMS704`, `nisarg1499`
- Share the Indexooor Stack with your friends and colleagues who are interested in blockchain development.
- Write a blog post or tutorial about how you've used the Indexooor Stack in your own projects.

By helping us spread the word, you'll be helping us reach more developers and grow the Indexooor Stack community. Thank you for your support!

## 🚀 Contributing Guidelines

We welcome contributions to the Indexooor Stack! If you're interested in contributing, please follow these guidelines:

1. Fork the repository and create a new branch for your contribution.
1. Make your changes and write tests to ensure that they work as expected.
1. Run the existing tests to make sure you didn't break anything.
1. Commit your changes and push them to your fork.
1. Open a pull request to our repository with a clear description of your changes.
1. We'll review your changes and work with you to get them merged into the main repository. By contributing to the Indexooor Stack, you'll be helping to make blockchain development easier and more accessible for everyone.

Thank you for your interest in contributing to the Indexooor Stack!
