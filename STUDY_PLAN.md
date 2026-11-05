# Tokenizer Project: 14-Day Beginner Study Plan

This plan is based on `en.subject.pdf`. It assumes you are new to blockchain and smart-contract development and can spend **3–4 hours a day**. The goal is to finish the mandatory project first: a token on a test network, understandable source code, deployment materials, documentation, and a clear repository. The multisignature bonus is optional and should only be attempted if every mandatory requirement works.

## What you need to deliver

- A token whose name includes **42**, following the token standard for the chosen network.
- A root `README.md` explaining the choices you made.
- Readable, commented token code in a root `code/` folder.
- A separate deployment folder with the files and instructions needed to deploy.
- A root `documentation/` folder explaining what the token represents, how it works, and how to use it.
- Deployment to a **public test network**, with the network and contract address recorded in the repository. Verify/publish the contract on the network's explorer if supported.
- A short, reliable demonstration of basic token actions and any ownership/privilege controls.

## Recommended beginner route

Use **BNB Smart Chain (BSC) Testnet**, **Solidity**, **OpenZeppelin's ERC-20 implementation**, and **Remix** for the first deployment. This route matches the brief's BNB Chain context and avoids setting up a local development framework before you understand the basics. BSC uses EVM-compatible Solidity contracts and the BEP-20 token interface is compatible with ERC-20 conventions. Use test tokens only; never enter a seed phrase or private key into a website or commit one to Git.

Keep the first version deliberately small: a fixed-supply token with a clear name containing “42”, a short ticker, and no extra minting or admin features unless you can explain and demonstrate their security. Write down the token's purpose before coding. Do not add a multisig until the mandatory version is complete and checked.

## Daily rhythm

Each session is 3–4 hours. A useful pattern is: **45–60 min learning**, **90–120 min hands-on work**, **30–45 min notes and cleanup**, with a short break between blocks. If a topic takes longer, preserve the working project and move optional work later rather than skipping core deliverables.

## 14-day schedule

### Day 1 — Understand the assignment and choose a token idea (3 hours)

- Read `en.subject.pdf` once for the overall goal and again for the mandatory checklist.
- Learn the difference between a blockchain, a wallet, a smart contract, a token, and a test network.
- Decide what your token represents, who might use it, and what it explicitly does **not** promise.
- Choose a name containing “42”, ticker, and initial supply. Record the reasoning in notes.
- Create a checklist from “What you need to deliver” above.

**Done when:** you can explain your token idea and have a short list of required files and actions.

### Day 2 — Blockchain and wallet basics (3–4 hours)

- Learn accounts, addresses, transactions, blocks, gas, and confirmations at a beginner level.
- Understand the difference between a public address and a private key/seed phrase.
- Set up a development wallet and select the BSC Testnet. Follow current official faucet instructions to request test BNB.
- Confirm you can see the test network and test funds in the wallet. Do not use real funds.

**Done when:** you can describe what pays for a transaction and can distinguish testnet assets from real assets.

### Day 3 — Solidity essentials (3–4 hours)

- Learn contract structure, state variables, functions, visibility, constructors, and events.
- Read and run small examples in the Solidity documentation or Remix, without deploying a token yet.
- Learn the difference between `public`, `external`, `internal`, and `private` in simple terms.
- Write a tiny practice contract with a stored value and a function that changes it; use Remix's local VM.

**Done when:** you can locate the constructor, state, and callable functions in a small contract.

### Day 4 — Token standards and ERC-20 behavior (3 hours)

- Learn what a fungible token is and the roles of `balanceOf`, `transfer`, `approve`, `allowance`, and `transferFrom`.
- Review the ERC-20 standard overview and OpenZeppelin's ERC-20 docs.
- Understand decimals and total supply. For a simple token, use the standard 18 decimals unless you have a specific reason otherwise.
- Sketch the user actions you will demonstrate: check supply/balance, transfer tokens, and explain allowances if included in your demo.

**Done when:** you can explain the basic token functions without describing them as “coins stored in the contract.”

### Day 5 — Build and inspect the token contract (3–4 hours)

- Start with OpenZeppelin's standard ERC-20 implementation in Remix.
- Add only the constructor setup needed for your chosen token name, ticker, and fixed initial supply.
- Read every line you submit. Add comments that explain your choices, not comments that repeat the code.
- Compile in Remix and resolve compiler errors. Keep a copy of the source in `code/`.

**Done when:** the contract compiles and you can explain how initial tokens are created and assigned.

### Day 6 — Local test and security review (3–4 hours)

- Deploy the contract to Remix's local VM, not a public network yet.
- Check the initial supply and deployer's balance.
- Transfer a small amount between test accounts and confirm both balances update as expected.
- Review ownership and privileged functions. If your design has no owner/admin functions, document that. If it has them, explain who controls them and why.
- Check that you have not added an unrestricted mint function or unnecessary permissions.

**Done when:** the basic interactions work locally and you can describe the contract's permissions and limitations.

### Day 7 — Prepare the repository and deployment folder (3 hours)

- Create the required root structure: `README.md`, `code/`, `deployment/`, and `documentation/`.
- Put the Solidity source in `code/` and deployment instructions/materials in `deployment/`.
- Start the README: token purpose, chain choice, token standard, name/ticker/supply, tools, and repository map.
- Write a deployment checklist, including compiler version, network, wallet account, and explorer verification steps.

**Done when:** the repository structure matches the subject and another beginner can find the source and instructions.

### Day 8 — Write the project documentation (3–4 hours)

- In `documentation/`, explain the token's purpose, intended use, supply, decimals, and transfer behavior.
- Document how a holder can view their balance and transfer tokens.
- Explain deployment and verification at a high level; identify any risks and limitations honestly.
- Add a simple architecture/workflow diagram if it helps, but do not spend time polishing visuals.

**Done when:** a reader can understand what the token is for and what it can and cannot do.

### Day 9 — First testnet deployment (3–4 hours)

- Recheck that Remix is connected to **BSC Testnet**, your wallet shows test funds, and the compiler version/settings match.
- Deploy the contract using test BNB only. Carefully review the wallet confirmation before approving.
- Save the deployed contract address and transaction link in your notes.
- Open the address on the BSC Testnet explorer and check that the contract deployment is visible.

**Done when:** the token is deployed to the intended test network and you have the address and transaction recorded.

### Day 10 — Verify the source and test on-chain actions (3–4 hours)

- Publish/verify the source on the testnet explorer if the explorer supports verification for your deployment method.
- Use the explorer's read/write contract interface or Remix to inspect supply and balances.
- Transfer a small test amount to a second test account and check the resulting balances/transaction.
- Record the steps and outcomes so the demo is repeatable.

**Done when:** you can show a successful read and transfer on the testnet, with the source verified where supported.

### Day 11 — Make the demonstration minimal and reliable (3 hours)

- Prepare a short live demo sequence: show network, contract address, total supply, holder balance, then transfer and updated balances.
- Practice explaining gas, test BNB, and the contract's permissions in plain language.
- Update README and documentation with the actual testnet name, address, and explorer links.
- A video is optional; prioritize a working live demonstration and complete repository.

**Done when:** you can complete the demo without improvising or relying on undocumented setup.

### Day 12 — Peer-review readiness and repository cleanup (3–4 hours)

- Compare every mandatory item in the subject against your repository.
- Check filenames and folder names, remove unrelated scratch files, and ensure source comments and names are readable.
- Read the README and documentation as if you had never seen the project.
- Make sure no secret phrase, private key, or wallet export is present in the repository or Git history.

**Done when:** every mandatory requirement has a corresponding file or demonstrated action, and the repo contains no wallet secrets.

### Day 13 — Fix gaps and repeat the full walkthrough (3–4 hours)

- Fix the most important missing or unclear mandatory requirement first.
- Repeat deployment/interaction checks on the testnet, or repeat the recorded walkthrough if redeployment is unnecessary.
- Confirm the public testnet explorer links still point to the right network and address.
- If all mandatory requirements are complete and working, use remaining time to read about multisig; do not rush to add it.

**Done when:** the full workflow is repeatable and the required artifacts agree with the deployed contract.

### Day 14 — Final review and hand-in preparation (3 hours)

- Perform a final checklist pass against the subject and inspect the Git repository contents.
- Confirm README, `code/`, `deployment/`, and `documentation/` are at the root.
- Confirm the network and contract address are explicit, and documentation describes the actual deployed behavior.
- Prepare concise answers to: Why this chain? What standard? How is supply created? Who has privileges? How do you demonstrate a transfer? What are the limitations?
- Only begin a bonus if all of the above is complete and stable. The brief says the bonus is assessed only when the mandatory part is perfect.

**Done when:** the repository is submission-ready and you can explain your decisions during review.

## Learning resources

Start with the official documentation and use videos only to reinforce a topic. Web3 tools and testnet details can change, so check the official pages on the day you use them.

- [Solidity documentation: Introduction](https://docs.soliditylang.org/en/latest/introduction-to-smart-contracts.html) — contracts and EVM basics.
- [Solidity by Example](https://solidity-by-example.org/) — short, runnable examples for language concepts.
- [Remix IDE documentation](https://remix-ide.readthedocs.io/en/latest/) — compile, deploy, and interact with contracts in the browser IDE.
- [OpenZeppelin Contracts: ERC-20](https://docs.openzeppelin.com/contracts/5.x/erc20) — standard ERC-20 behavior and implementation.
- [Ethereum.org: ERC-20 token standard](https://ethereum.org/en/developers/docs/standards/tokens/erc-20/) — beginner-friendly description of the interface. The EVM token interface is relevant to BSC as well.
- [BNB Chain docs](https://docs.bnbchain.org/) — current network and developer documentation.
- [BNB Chain Testnet Faucet](https://www.bnbchain.org/en/testnet-faucet) — official source for test BNB, subject to current availability and instructions.
- YouTube search: [Solidity and Remix beginner tutorial](https://www.youtube.com/results?search_query=solidity+remix+beginner+tutorial) — choose a recent tutorial and cross-check code against current Solidity/OpenZeppelin docs.

## Final submission checklist

- [ ] Token name includes “42” and its purpose is clear.
- [ ] Token follows the chosen chain's token standard and compiles.
- [ ] `README.md` is at the repository root and explains key choices.
- [ ] Source is readable and in root `code/`.
- [ ] Deployment materials are in a separate root folder.
- [ ] Project explanation and usage instructions are in root `documentation/`.
- [ ] Contract is deployed on a public **test** network; network and address are in the repository.
- [ ] Basic token actions and privilege/ownership behavior have been demonstrated.
- [ ] Explorer source verification is done where supported, or its limitation is documented.
- [ ] No real funds or wallet secrets are used.
- [ ] Bonus work has not displaced unfinished mandatory requirements.
