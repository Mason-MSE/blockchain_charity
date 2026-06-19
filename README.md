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

- **Web3 版本修复** — CDN 从 web3@1.10.0 改为 web3@0.20.6（兼容 truffle-contract@3.0.6 的 `toBigNumber` API）
- **脚本加载顺序修复** — web3.js 移到 truffle-contract.js 之前加载，修复 `Web3 is not a constructor`
- **`ethereum.enable()` 弃用修复** — 改为 `ethereum.request({ method: 'eth_requestAccounts' })`
- **恢复缺失的合约文件** — 从 git 历史恢复了 `contracts/charity.sol`、`build/contracts/charity.json`、`migrations/` 目录
- **修复网络不匹配** — `loadContract` 改用 `.at(address)` 替代 `.deployed()`，绕过网络 ID 校验
- **直连 Ganache** — 前端 Web3 Provider 改为直连 `http://127.0.0.1:7545`，不再依赖 MetaMask 网络配置
- **修复 `loadAccount`** — 改用 `web3.eth.getAccounts()` 异步获取账户，设置 `web3.eth.defaultAccount`
- **修复 Gas 不足** — 所有合约调用加上 `{ gas: 6721975 }`
- **修复表单默认提交** — 所有 `onSubmit` 增加 `return false;` 阻止页面提前刷新
- **Truffle 升级** — `5.0.2` → `5.11.5`
- **Solidity 升级** — `0.5.0` → `0.8.19`，更新合约语法（`constructor()` 移除 `public`，`if` 守卫 → `require`）
- **远程仓库迁移** — 更新 git remote 至 `https://github.com/Mason-MSE/blockchain_charity.git`
