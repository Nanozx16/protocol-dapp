# protocol-dapp

 Installation
Prerequisites
Foundry
Node.js
Yarn
Setup
forge init \
    --template https://github.com/mitosis-org/protocol-dapp-template.git \
    ./your-project-name

cd your-project-name

# Install dependencies
yarn install
forge soldeer install -d

# Build contracts
forge build

# Run tests
forge test
🧪 Development Workflow
Building and Testing
# Build contracts
forge build

# Run all tests
forge test

# Run tests with gas reports
forge test --gas-report

# Generate coverage report
yarn coverage
Code Quality
# Format code and check style
yarn lint

# Check formatting without changes
yarn lint:check
Available Scripts
yarn build - Compile contracts
yarn lint - Format code and sort imports
yarn lint:check - Check code formatting
yarn coverage - Generate test coverage report
📁 Project Structure
protocol-dapp-template/
├── src/
│   └── Depositor.sol                # Main depositor contract
├── test/
│   ├── Depositor.t.sol              # Comprehensive tests
│   └── stub/
│       └── LibStubMitosisVault.sol  # Test utilities
├── tools/
│   └── coverage.sh                  # Coverage reporting
├── foundry.toml                     # Foundry configuration
├── package.json                     # Node.js dependencies
└── soldeer.lock                     # Solidity dependencies
🔧 Configuration
Foundry Configuration
Key settings in foundry.toml:

Solidity Version: 0.8.29
EVM Version: Prague
Dependencies: OpenZeppelin, Solady, Mitosis protocol
Dependencies & Remappings
Dependency Name	Purpose / Description	Remapping (foundry.toml)
@openzeppelin/contracts	Security and utility contracts	@oz/
@openzeppelin/contracts-upgradeable	Upgradeable contract support	@ozu/
@hyperlane-xyz/core	Cross-chain messaging	@hpl/
@mitosis-org/protocol	Mitosis vault interfaces	@mito-mainnet/
@mitosis-org/stub	Stub library for testing	@stub/
solady	Gas-optimized utilities	@solady/
forge-std	Foundry standard library	@std/
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
