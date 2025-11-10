# Proof of Concept (PoC) Guidelines

This document provides detailed guidelines for creating effective Proofs of Concept for bug bounty submissions.

## What is a PoC?

A Proof of Concept (PoC) is executable code that demonstrates a security vulnerability exists and can be exploited. It serves as concrete evidence of the bug and helps the development team understand and fix the issue.

## Why PoCs Are Required

1. **Verification**: Proves the vulnerability is real and exploitable
2. **Understanding**: Helps developers understand the exact nature of the bug
3. **Reproduction**: Allows the team to reproduce the issue in their environment
4. **Severity Assessment**: Demonstrates the actual impact of the vulnerability
5. **Fix Validation**: Enables testing to confirm the fix works correctly

## PoC Requirements

### Must Have

- ✅ **Executable Code**: The PoC must be runnable
- ✅ **Clear Comments**: Explain what each part of the code does
- ✅ **Complete Setup Instructions**: Include all necessary environment setup
- ✅ **Actual Exploitation**: Show the vulnerability being exploited, not just theoretical
- ✅ **Output/Results**: Include expected output demonstrating the bug

### Should Have

- 🔶 **Minimal Code**: Only include code necessary to demonstrate the bug
- 🔶 **Test Framework Integration**: Use Hardhat, Foundry, or similar testing frameworks
- 🔶 **Realistic Scenario**: Demonstrate a realistic attack scenario
- 🔶 **Clean Code**: Well-formatted and easy to read

### Nice to Have

- ⭐ **Multiple Attack Vectors**: Show different ways to exploit the bug (if applicable)
- ⭐ **Impact Quantification**: Show exact amounts that could be stolen/lost
- ⭐ **Fix Demonstration**: Include code showing how the fix prevents the exploit

## PoC Structure

### 1. Environment Setup

Specify:
- Required dependencies (Node.js version, npm packages, etc.)
- Network configuration (mainnet fork, testnet, local)
- Required accounts/wallets
- Initial balances or states needed

### 2. Initialization

Include code to:
- Deploy necessary contracts
- Set up initial state
- Configure required parameters
- Fund accounts

### 3. Vulnerability Demonstration

Show:
- The attack being executed
- Step-by-step progression
- State changes during the attack
- Final outcome

### 4. Impact Verification

Prove:
- Funds were stolen/locked
- Protocol state was corrupted
- Expected behavior was violated
- Severity claims are accurate

## Technology-Specific Guidance

### Solidity Smart Contracts

**Using Hardhat:**

```javascript
const { expect } = require("chai");
const { ethers } = require("hardhat");

describe("Vulnerability PoC", function() {
  let contract;
  let attacker;
  
  beforeEach(async function() {
    // Setup code
    [owner, attacker] = await ethers.getSigners();
    const Contract = await ethers.getContractFactory("VulnerableContract");
    contract = await Contract.deploy();
  });
  
  it("demonstrates the vulnerability", async function() {
    // Attack code
    // Assertions to prove the vulnerability
  });
});
```

**Using Foundry:**

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "forge-std/Test.sol";
import "../src/VulnerableContract.sol";

contract VulnerabilityPoC is Test {
    VulnerableContract target;
    address attacker = address(0x1);
    
    function setUp() public {
        // Setup code
        target = new VulnerableContract();
    }
    
    function testVulnerability() public {
        // Attack code
        // Assertions
    }
}
```

### TypeScript/JavaScript

```typescript
import { expect } from "chai";
import { Contract, Signer } from "ethers";

describe("Vulnerability PoC", () => {
  let contract: Contract;
  let attacker: Signer;
  
  before(async () => {
    // Setup
  });
  
  it("exploits the vulnerability", async () => {
    // Attack demonstration
  });
});
```

## PoC Best Practices

### DO

✅ **Be Specific**: Clearly identify the vulnerable function/contract
✅ **Use Comments**: Explain each step of the attack
✅ **Include Assertions**: Prove the attack succeeded with checks
✅ **Provide Output**: Show console logs or test results
✅ **Keep It Simple**: Remove unnecessary complexity
✅ **Test Thoroughly**: Ensure the PoC works before submitting
✅ **Document Assumptions**: State any assumptions made

### DON'T

❌ **Don't Be Vague**: Avoid theoretical descriptions without code
❌ **Don't Skip Setup**: Always include complete environment setup
❌ **Don't Over-Complicate**: Keep the PoC focused on the vulnerability
❌ **Don't Submit Untested Code**: Always test your PoC first
❌ **Don't Include Exploits for Production**: Only test on testnets or forks
❌ **Don't Omit Critical Steps**: Include all necessary reproduction steps

## Example PoC Template

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "forge-std/Test.sol";
import "../src/TargetContract.sol";

/**
 * Proof of Concept for [Vulnerability Name]
 * 
 * Description: [Brief description of the vulnerability]
 * Impact: [Expected impact]
 * Severity: [Critical/High/Medium/Low]
 */
contract VulnerabilityPoC is Test {
    TargetContract public target;
    address public attacker = address(0x1337);
    address public victim = address(0x9999);
    
    function setUp() public {
        // Deploy the vulnerable contract
        target = new TargetContract();
        
        // Setup initial state
        vm.deal(victim, 100 ether);
        vm.deal(attacker, 1 ether);
        
        // Victim deposits funds
        vm.prank(victim);
        target.deposit{value: 100 ether}();
    }
    
    function testExploit() public {
        // Record initial balances
        uint256 attackerBalanceBefore = attacker.balance;
        uint256 contractBalanceBefore = address(target).balance;
        
        // Execute the attack
        vm.startPrank(attacker);
        
        // Step 1: [Explain what this does]
        target.vulnerableFunction();
        
        // Step 2: [Explain what this does]
        target.withdraw();
        
        vm.stopPrank();
        
        // Verify the attack succeeded
        uint256 attackerBalanceAfter = attacker.balance;
        uint256 contractBalanceAfter = address(target).balance;
        
        // Attacker stole all funds
        assertEq(attackerBalanceAfter - attackerBalanceBefore, 100 ether);
        assertEq(contractBalanceAfter, 0);
        
        console.log("Attacker profit:", attackerBalanceAfter - attackerBalanceBefore);
        console.log("Contract drained:", contractBalanceBefore - contractBalanceAfter);
    }
}
```

## Common PoC Pitfalls

### 1. Incomplete Setup
**Problem**: Missing deployment scripts, configuration, or initial state
**Solution**: Include complete, step-by-step setup instructions

### 2. Non-Executable Code
**Problem**: Pseudocode or code snippets that can't be run
**Solution**: Provide fully functional, tested code

### 3. Unclear Impact
**Problem**: PoC runs but doesn't clearly show the damage
**Solution**: Add assertions and logs showing the actual impact

### 4. Missing Dependencies
**Problem**: PoC requires packages or contracts not listed
**Solution**: Document all dependencies and how to install them

### 5. Environment-Specific Code
**Problem**: PoC only works on your specific machine
**Solution**: Use standard tools and document environment requirements

## Checklist Before Submission

- [ ] PoC code is complete and executable
- [ ] All dependencies are documented
- [ ] Setup instructions are clear and complete
- [ ] The vulnerability is actually demonstrated (not just described)
- [ ] Output/results are included
- [ ] Code is well-commented
- [ ] Assertions prove the attack succeeded
- [ ] The PoC has been tested in a clean environment
- [ ] All steps are reproducible
- [ ] The severity claim is backed by the PoC results

## Resources

- **Hardhat Documentation**: https://hardhat.org/docs
- **Foundry Documentation**: https://book.getfoundry.sh/
- **Ethereum Testing Best Practices**: Various community resources
- **Smart Contract Security**: OWASP, ConsenSys, Trail of Bits guides

## Questions?

If you're unsure about your PoC:
1. Review the checklist above
2. Compare against example PoCs in the repository
3. Test in a clean environment
4. Consider having a peer review it before submission

Remember: A good PoC is clear, complete, and conclusive. It should leave no doubt that the vulnerability exists and is exploitable.
