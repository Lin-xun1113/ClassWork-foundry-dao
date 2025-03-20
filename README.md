# Foundry DAO Governance System

## Overview

This project implements a complete on-chain DAO governance system using Solidity and the OpenZeppelin governance contracts. The system allows token holders to propose, vote on, and execute changes to the protocol through a democratic process.

## Components

- **GovToken**: ERC20 token with voting capabilities that serves as the governance token for the DAO.
- **MyGovernor**: The main governance contract that handles proposals, voting, and execution.
- **TimeLock**: A timelock controller that adds a delay between proposal approval and execution for security.
- **Box**: A simple contract that demonstrates how governance can control protocol parameters.

## Governance Process

1. **Proposal**: Token holders can propose changes to the protocol.
2. **Voting**: After a delay period, token holders can vote on proposals.
3. **Queue**: Successful proposals are queued in the timelock.
4. **Execution**: After the timelock delay, proposals can be executed.

## Technical Details

- Voting delay: 7200 blocks (approximately 1 day at 12 second block times)
- Voting period: 50400 blocks (approximately 1 week)
- Minimum delay for execution: 3600 seconds (1 hour)
- Quorum: 4% of total token supply must vote for a proposal to pass

## Getting Started

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd foundry-dao

# Install dependencies
forge install
```

### Build

```bash
forge build
```

### Test

```bash
forge test
```

## License

This project is licensed under the MIT License.

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
