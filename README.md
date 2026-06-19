# Charity Blockchain Project

### Problem Statement
- There are no platforms that can be used by charities to ensure security while providing accessibility to maximum people.
- The biggest problem faced is transparency, where people can rightly exercise their Right To Information by asking for a record of expenditure by the charity
- Even if such applications are available, they are inaccessible to smaller organisations with a good user interface for ease of access.

### Requirements of the Project
 - **Solidity Web3**
	* Solidity provides Inheritance properties in contracts including multiple level inheritance properties.
 - **Metamask**
	* To have an easy-to-use and secure wallet service, the platform connects to users' MetaMask automatically.
 - **Node.js**
	* Node.js is used a backend for our application. It records transactions communicates between the Applications and integrates frontend.
 - **Ganache**
	* Ganache provides the GUI-based local Ethereum blockchain development environment to deploy and test contracts.

### Project Working
* A metamask connection is required to run the application for any transaction.
* A ganache RPC Server is run with metamask as the wallet, using the node.js interface.
* Charity and organisation details are saved in the application, and a hash value is generated
* A transaction is carried out, between organisation and charity and transaction hash is generated for each transaction
* A block is created, when the user mines all the transactions updates.


### YouTube Video

<div align="center"> <a href="https://youtu.be/4CIUYSnVEIo"><img src="http://img.youtube.com/vi/4CIUYSnVEIo/0.jpg" width="30%"></a> <br> <a href="https://youtu.be/4CIUYSnVEIo">Demonstration Video</a></div>
<br><br>


### License

	Copyright (C) 2020 Harsh Sanjay Agrawal

	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at

	   http://www.apache.org/licenses/LICENSE-2.0

	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.

## Changelog

### 2026-06-20 — Bug fixes & dependency upgrades

- **Web3 version fix** — Changed CDN from web3@1.10.0 to web3@0.20.6 (compatible with truffle-contract@3.0.6's `toBigNumber` API)
- **Script load order fix** — Moved web3.js before truffle-contract.js to resolve `Web3 is not a constructor`
- **`ethereum.enable()` deprecation** — Replaced with `ethereum.request({ method: 'eth_requestAccounts' })`
- **Restored missing contract files** — Recovered `contracts/charity.sol`, `build/contracts/charity.json`, and `migrations/` from git history
- **Network mismatch fix** — `loadContract` now uses `.at(address)` instead of `.deployed()` to bypass network ID validation
- **Direct Ganache connection** — Frontend Web3 Provider connects directly to `http://127.0.0.1:7545`, no longer depends on MetaMask network config
- **Fixed `loadAccount`** — Uses `web3.eth.getAccounts()` asynchronously and sets `web3.eth.defaultAccount`
- **Out of gas fix** — Added `{ gas: 6721975 }` to all contract calls
- **Form default submission fix** — Added `return false;` to all `onSubmit` handlers to prevent premature page reload
- **Truffle upgrade** — `5.0.2` → `5.11.5`
- **Solidity upgrade** — `0.5.0` → `0.8.19`, updated contract syntax (`constructor()` without `public`, `if` guard → `require`)
- **Remote repository migration** — Updated git remote to `https://github.com/Mason-MSE/blockchain_charity.git`
