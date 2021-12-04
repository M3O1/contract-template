# Solidity Template

### Objective 

> 프로젝트 템플릿 리파짓토리로, 프로젝트 폴더을 보다 간단히 진행하도록 도와줍니다.

### How To SetUp

깃헙에서 `Use this Template`을 누르면, 이 리파짓토리를 기준으로 새로운 리파짓토리가 만들어집니다.

![](https://imgur.com/vjlEBIr.png)

해당 리파짓토리에서 `.env.example`을 `.env`로 바꾸고, 파일에 있는 apiKey들을 필요한 것들로 바꾸면 됩니다. 

````shell
MNEMONIC=test test test test test test test test test test test test
REPORT_GAS=true
INFURA_API_KEY=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
ETHERSCAN_API_KEY=YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY
````

### 템플릿 프로젝트들

- [Hardhat](https://github.com/nomiclabs/hardhat): compile and run the smart contracts on a local development network
- [TypeChain](https://github.com/ethereum-ts/TypeChain): generate TypeScript types for smart contracts
- [Ethers](https://github.com/ethers-io/ethers.js/): renowned Ethereum library and wallet implementation
- [Waffle](https://github.com/EthWorks/Waffle): tooling for writing comprehensive smart contract tests
- [Solhint](https://github.com/protofire/solhint): linter
- [Prettier Plugin Solidity](https://github.com/prettier-solidity/prettier-plugin-solidity): code formatter

## Usage

### 의존성 설치하기


```sh
$ yarn install
```

### 스마트 컨트랙트 컴파일 하기 (with HardHat)

```sh
$ yarn compile
```

### 스마트 컨트랙트 테스트 하기 (with Mocha)

```sh
$ yarn test
```

### 네트워크에 배포하기 (requires Mnemonic and infura API key)

```
npx hardhat run --network <NETWORK> ./scripts/deploy.ts
```

### 이더스캔으로 스마트컨트랙트 검증하기 (requires API key)

```
npx hardhat verify --network <NETWORK> <DEPLOYED_CONTRACT_ADDRESS> "Constructor argument 1"
```

### Added plugins

- Gas reporter [hardhat-gas-reporter](https://hardhat.org/plugins/hardhat-gas-reporter.html)
- Etherscan [hardhat-etherscan](https://hardhat.org/plugins/nomiclabs-hardhat-etherscan.html)

