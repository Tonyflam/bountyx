# Example Proof of Concept Template

This is an example PoC template using Foundry (Forge). Adapt this template for your specific vulnerability.

## File: ExampleVulnerabilityPoC.t.sol

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "forge-std/Test.sol";
import "forge-std/console.sol";

/**
 * Proof of Concept for [VULNERABILITY_NAME]
 * 
 * Severity: [Critical/High/Medium/Low]
 * 
 * Description:
 * [Brief description of what this PoC demonstrates]
 * 
 * Impact:
 * [Brief description of the impact]
 * 
 * Date: [Submission date]
 * Researcher: [Your name/handle]
 */
contract ExampleVulnerabilityPoC is Test {
    // ============================================
    // Contract Instances
    // ============================================
    
    // TODO: Add the vulnerable contract instance
    // VulnerableContract public targetContract;
    
    // ============================================
    // Test Actors
    // ============================================
    
    address public attacker = address(0x1337);
    address public victim = address(0x9999);
    address public protocolOwner = address(0xABCD);
    
    // ============================================
    // Setup
    // ============================================
    
    function setUp() public {
        // Label addresses for better trace output
        vm.label(attacker, "Attacker");
        vm.label(victim, "Victim");
        vm.label(protocolOwner, "Protocol Owner");
        
        // TODO: Deploy contracts
        // vm.prank(protocolOwner);
        // targetContract = new VulnerableContract();
        
        // TODO: Set up initial state
        // Give victim some funds
        vm.deal(victim, 100 ether);
        
        // Give attacker minimal funds for gas
        vm.deal(attacker, 1 ether);
        
        // TODO: Victim interacts with protocol (deposits, etc.)
        // vm.startPrank(victim);
        // targetContract.deposit{value: 100 ether}();
        // vm.stopPrank();
    }
    
    // ============================================
    // Vulnerability Test
    // ============================================
    
    function testVulnerabilityExploit() public {
        console.log("=== Vulnerability PoC Execution ===");
        console.log("");
        
        // ----------------------------------------
        // Step 1: Record Initial State
        // ----------------------------------------
        console.log("--- Initial State ---");
        
        uint256 attackerBalanceBefore = attacker.balance;
        uint256 victimBalanceBefore = victim.balance;
        // uint256 contractBalanceBefore = address(targetContract).balance;
        
        console.log("Attacker balance:", attackerBalanceBefore);
        console.log("Victim balance:", victimBalanceBefore);
        // console.log("Contract balance:", contractBalanceBefore);
        console.log("");
        
        // ----------------------------------------
        // Step 2: Execute the Attack
        // ----------------------------------------
        console.log("--- Executing Attack ---");
        
        vm.startPrank(attacker);
        
        // TODO: Implement attack steps
        // Example:
        // Step 1: Call vulnerable function
        // console.log("Step 1: Calling vulnerable function...");
        // targetContract.vulnerableFunction(maliciousInput);
        
        // Step 2: Exploit the vulnerability
        // console.log("Step 2: Exploiting...");
        // targetContract.exploit();
        
        // Step 3: Extract gains
        // console.log("Step 3: Withdrawing stolen funds...");
        // targetContract.withdraw();
        
        vm.stopPrank();
        
        console.log("");
        
        // ----------------------------------------
        // Step 3: Verify Attack Success
        // ----------------------------------------
        console.log("--- Final State ---");
        
        uint256 attackerBalanceAfter = attacker.balance;
        uint256 victimBalanceAfter = victim.balance;
        // uint256 contractBalanceAfter = address(targetContract).balance;
        
        console.log("Attacker balance:", attackerBalanceAfter);
        console.log("Victim balance:", victimBalanceAfter);
        // console.log("Contract balance:", contractBalanceAfter);
        console.log("");
        
        // ----------------------------------------
        // Step 4: Calculate Impact
        // ----------------------------------------
        console.log("--- Impact Analysis ---");
        
        uint256 attackerProfit = attackerBalanceAfter - attackerBalanceBefore;
        uint256 victimLoss = victimBalanceBefore - victimBalanceAfter;
        // uint256 contractLoss = contractBalanceBefore - contractBalanceAfter;
        
        console.log("Attacker profit:", attackerProfit);
        console.log("Victim loss:", victimLoss);
        // console.log("Contract drained:", contractLoss);
        console.log("");
        
        // ----------------------------------------
        // Step 5: Assertions
        // ----------------------------------------
        console.log("--- Verification ---");
        
        // TODO: Add assertions to prove the exploit
        // Example assertions:
        
        // Verify attacker gained funds
        // assertGt(attackerProfit, 0, "Attacker should have profited");
        
        // Verify victim lost funds
        // assertGt(victimLoss, 0, "Victim should have lost funds");
        
        // Verify contract was drained
        // assertEq(contractBalanceAfter, 0, "Contract should be drained");
        
        // Verify the stolen amount matches
        // assertEq(attackerProfit, victimLoss, "Stolen amount should match victim loss");
        
        console.log("All assertions passed - Vulnerability confirmed!");
    }
    
    // ============================================
    // Helper Functions (Optional)
    // ============================================
    
    /**
     * Helper function to check contract state
     */
    function _checkContractState() internal view {
        // TODO: Add state checks if needed
        // Example:
        // uint256 totalDeposits = targetContract.totalDeposits();
        // uint256 totalWithdrawals = targetContract.totalWithdrawals();
        // console.log("Total deposits:", totalDeposits);
        // console.log("Total withdrawals:", totalWithdrawals);
    }
    
    /**
     * Helper function to setup complex attack scenario
     */
    function _setupAttackScenario() internal {
        // TODO: Add complex setup if needed
    }
}
```

## Running the PoC

### Prerequisites

```bash
# Install Foundry if not already installed
curl -L https://foundry.paradigm.xyz | bash
foundryup

# Clone the target repository
git clone [BEANSTALK_REPO_URL]
cd beanstalk

# Install dependencies
forge install
```

### Execution

```bash
# Run the specific test
forge test --match-test testVulnerabilityExploit -vvvv

# Run with gas reporting
forge test --match-test testVulnerabilityExploit --gas-report

# Run on a forked network (if needed)
forge test --match-test testVulnerabilityExploit -vvvv --fork-url [RPC_URL]
```

### Expected Output

```
[⠊] Compiling...
[⠒] Compiling 1 files with 0.8.19
[⠢] Solc 0.8.19 finished in 1.23s
Compiler run successful!

Running 1 test for test/ExampleVulnerabilityPoC.t.sol:ExampleVulnerabilityPoC
[PASS] testVulnerabilityExploit() (gas: 123456)
Logs:
  === Vulnerability PoC Execution ===
  
  --- Initial State ---
  Attacker balance: 1000000000000000000
  Victim balance: 100000000000000000000
  Contract balance: 100000000000000000000
  
  --- Executing Attack ---
  Step 1: Calling vulnerable function...
  Step 2: Exploiting...
  Step 3: Withdrawing stolen funds...
  
  --- Final State ---
  Attacker balance: 101000000000000000000
  Victim balance: 100000000000000000000
  Contract balance: 0
  
  --- Impact Analysis ---
  Attacker profit: 100000000000000000000
  Victim loss: 0
  Contract drained: 100000000000000000000
  
  --- Verification ---
  All assertions passed - Vulnerability confirmed!

Test result: ok. 1 passed; 0 failed; finished in 2.34s
```

## Alternative: Hardhat Example

```javascript
// File: test/vulnerability-poc.js

const { expect } = require("chai");
const { ethers } = require("hardhat");

describe("Vulnerability PoC", function () {
  let targetContract;
  let attacker;
  let victim;
  let owner;

  beforeEach(async function () {
    // Get signers
    [owner, attacker, victim] = await ethers.getSigners();

    // Deploy vulnerable contract
    // const VulnerableContract = await ethers.getContractFactory("VulnerableContract");
    // targetContract = await VulnerableContract.deploy();
    // await targetContract.deployed();

    // Setup initial state
    // await victim.sendTransaction({
    //   to: targetContract.address,
    //   value: ethers.utils.parseEther("100")
    // });
  });

  it("should demonstrate the vulnerability", async function () {
    console.log("=== Vulnerability PoC Execution ===\n");

    // Record initial state
    console.log("--- Initial State ---");
    const attackerBalanceBefore = await attacker.getBalance();
    const contractBalanceBefore = await ethers.provider.getBalance(
      targetContract.address
    );
    console.log(
      `Attacker balance: ${ethers.utils.formatEther(attackerBalanceBefore)} ETH`
    );
    console.log(
      `Contract balance: ${ethers.utils.formatEther(contractBalanceBefore)} ETH\n`
    );

    // Execute attack
    console.log("--- Executing Attack ---");
    // await targetContract.connect(attacker).vulnerableFunction();
    console.log("");

    // Record final state
    console.log("--- Final State ---");
    const attackerBalanceAfter = await attacker.getBalance();
    const contractBalanceAfter = await ethers.provider.getBalance(
      targetContract.address
    );
    console.log(
      `Attacker balance: ${ethers.utils.formatEther(attackerBalanceAfter)} ETH`
    );
    console.log(
      `Contract balance: ${ethers.utils.formatEther(contractBalanceAfter)} ETH\n`
    );

    // Calculate impact
    console.log("--- Impact Analysis ---");
    const profit = attackerBalanceAfter.sub(attackerBalanceBefore);
    console.log(`Attacker profit: ${ethers.utils.formatEther(profit)} ETH\n`);

    // Assertions
    console.log("--- Verification ---");
    expect(contractBalanceAfter).to.equal(0);
    expect(profit).to.be.gt(0);
    console.log("All assertions passed - Vulnerability confirmed!");
  });
});
```

## Running Hardhat PoC

```bash
# Install dependencies
npm install --save-dev hardhat @nomiclabs/hardhat-ethers ethers chai

# Run the test
npx hardhat test test/vulnerability-poc.js

# Run with verbose output
npx hardhat test test/vulnerability-poc.js --verbose

# Run on a forked network
npx hardhat test test/vulnerability-poc.js --network hardhat --fork [RPC_URL]
```

## Customization Tips

1. **Replace placeholders**: Change `TODO` comments with actual code
2. **Add contracts**: Import the vulnerable contracts you're testing
3. **Adjust actors**: Modify test accounts based on your scenario
4. **Update assertions**: Add specific checks for your vulnerability
5. **Enhance logging**: Add more console logs for clarity
6. **Include comments**: Explain complex attack steps

## Best Practices

- ✅ Keep the PoC minimal and focused
- ✅ Use descriptive variable names
- ✅ Add clear console output
- ✅ Include comprehensive comments
- ✅ Verify all assertions
- ✅ Test in a clean environment
- ✅ Document expected vs actual behavior

## Common Patterns

### Reentrancy Attack
```solidity
contract AttackerContract {
    VulnerableContract target;
    
    function attack() external {
        target.deposit{value: 1 ether}();
        target.withdraw();
    }
    
    receive() external payable {
        if (address(target).balance >= 1 ether) {
            target.withdraw();
        }
    }
}
```

### Flash Loan Attack
```solidity
function executeFlashLoan() external {
    // 1. Borrow large amount
    // 2. Manipulate protocol state
    // 3. Profit from manipulation
    // 4. Repay flash loan
}
```

### Access Control Bypass
```solidity
function testUnauthorizedAccess() public {
    vm.prank(attacker);
    // Should revert but doesn't
    targetContract.adminFunction();
}
```

Remember: The PoC should clearly demonstrate the vulnerability and its impact!
