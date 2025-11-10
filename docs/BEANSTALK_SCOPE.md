# Beanstalk Bug Bounty Program - Scope and Context

This document provides essential context about the Beanstalk bug bounty program to guide vulnerability research.

## Program Overview

**Platform**: Immunefi
**Protocol**: Beanstalk - A permissionless fiat stablecoin protocol
**Focus**: Smart contract vulnerabilities

## Severity Classification

### Critical (Highest Priority)

**Reward**: Up to maximum payout as defined by Immunefi

**Vulnerabilities Include**:
- Direct theft of any user funds, whether at-rest or in-motion, other than unclaimed yield
- Permanent freezing of funds
- Protocol insolvency

**Research Focus**:
- Fund handling mechanisms
- Withdrawal and deposit functions
- Protocol solvency calculations
- Access control for critical functions

### High Severity

**Vulnerabilities Include**:
- Theft of unclaimed yield
- Permanent freezing of unclaimed yield
- Temporary freezing of funds for at least 24 hours

**Research Focus**:
- Yield calculation and distribution
- Time-locked functions
- Emergency pause mechanisms
- Yield claiming processes

### Medium Severity

**Vulnerabilities Include**:
- Smart contract unable to operate due to lack of token funds
- Block stuffing for profit
- Griefing (e.g. no profit motive for an attacker, but damage to the users or the protocol)

**Research Focus**:
- Gas optimization issues
- DoS attack vectors
- Economic griefing opportunities
- Resource exhaustion

### Low Severity

**Vulnerabilities Include**:
- Contract fails to deliver promised returns, but doesn't lose value

**Research Focus**:
- Return calculation errors
- Minor accounting issues
- Display/reporting bugs

## Out of Scope

The following are explicitly NOT in scope:
- Attacks requiring access to privileged addresses (governance, admin)
- Theoretical vulnerabilities without proof of exploitability
- Bugs in third-party dependencies (unless they directly impact Beanstalk)
- Social engineering attacks
- UI/UX bugs that don't affect contract security
- Issues already covered in previous audits

## Research Priorities

### High Priority Areas

1. **Fund Security**
   - User deposit safety
   - Withdrawal mechanisms
   - Transfer functions
   - Balance tracking

2. **Protocol Solvency**
   - Collateralization ratios
   - Debt management
   - Reserve mechanisms
   - Price oracle manipulation

3. **Access Control**
   - Permission systems
   - Role-based access
   - Ownership transfers
   - Critical function protection

4. **Economic Attacks**
   - Flash loan exploits
   - MEV opportunities
   - Price manipulation
   - Liquidity attacks

### Medium Priority Areas

1. **Yield Distribution**
   - Calculation accuracy
   - Fair distribution
   - Claiming mechanisms
   - Rounding errors

2. **State Management**
   - State transitions
   - Consistency checks
   - Recovery mechanisms
   - Upgrade processes

3. **Integration Points**
   - External protocol interactions
   - Oracle dependencies
   - Token transfers
   - Cross-contract calls

## Common Vulnerability Patterns to Investigate

### 1. Reentrancy
- Check all external calls
- Verify state updates happen before external calls
- Look for checks-effects-interactions violations

### 2. Access Control
- Review all privileged functions
- Check for missing access modifiers
- Look for signature replay vulnerabilities

### 3. Integer Issues
- Overflow/underflow possibilities
- Rounding errors in calculations
- Precision loss in conversions

### 4. Logic Errors
- Incorrect conditional statements
- Off-by-one errors
- Edge case handling
- Unhandled return values

### 5. Economic Exploits
- Flash loan attack vectors
- Price oracle manipulation
- Front-running opportunities
- Sandwich attacks

### 6. DoS Attacks
- Unbounded loops
- Block gas limit issues
- Resource exhaustion
- Griefing vectors

## Research Methodology

### Phase 1: Reconnaissance
1. Review protocol documentation
2. Study smart contract architecture
3. Map critical functions and data flows
4. Identify attack surfaces
5. Review previous audit reports

### Phase 2: Analysis
1. Static code analysis
2. Identify potential vulnerability patterns
3. Trace fund flows
4. Analyze access control mechanisms
5. Review state management

### Phase 3: Exploitation
1. Develop attack scenarios
2. Create proof of concept
3. Test on fork/testnet
4. Measure impact
5. Document findings

### Phase 4: Documentation
1. Write clear vulnerability description
2. Create executable PoC
3. Assess severity
4. Suggest remediation
5. Prepare submission

## Tools and Resources

### Recommended Tools

**Static Analysis**:
- Slither
- Mythril
- Securify

**Testing Frameworks**:
- Hardhat
- Foundry
- Truffle

**Debugging**:
- Tenderly
- Hardhat Network
- Ganache

**Fuzzing**:
- Echidna
- Harvey
- Foundry Fuzz

### Learning Resources

- Smart Contract Security Best Practices
- Ethereum Smart Contract Security
- DeFi Security Summit talks
- Immunefi blog posts
- Past vulnerability disclosures

## Responsible Disclosure

### Timeline

1. **Initial Submission**: Submit through Immunefi platform
2. **Acknowledgment**: Team acknowledges receipt (typically 24-48 hours)
3. **Validation**: Team validates the vulnerability
4. **Remediation**: Team develops and tests fix
5. **Reward**: Bounty paid according to severity
6. **Disclosure**: Coordinated public disclosure (if appropriate)

### Best Practices

- Submit only one vulnerability per report
- Wait for confirmation before public disclosure
- Be responsive to team questions
- Provide additional details if requested
- Don't exploit vulnerabilities on mainnet

## Submission Tips

### Maximize Your Chances

1. **Be First**: Check if the bug has been reported before submitting
2. **Be Clear**: Write clear, concise descriptions
3. **Be Complete**: Include all necessary information and PoC
4. **Be Professional**: Maintain professional communication
5. **Be Patient**: Allow time for review and validation

### Common Rejection Reasons

- Duplicate submission
- Out of scope
- Insufficient proof
- Theoretical without demonstration
- Already known/documented
- Severity mismatch

## Example Research Questions

When analyzing Beanstalk contracts, ask:

- Can user funds be stolen or frozen?
- Can the protocol become insolvent?
- Can yield calculations be manipulated?
- Are there reentrancy vulnerabilities?
- Can external calls be exploited?
- Are access controls properly implemented?
- Can price oracles be manipulated?
- Are there integer overflow/underflow risks?
- Can transactions be front-run for profit?
- Are there DoS attack vectors?

## Success Metrics

A successful vulnerability submission should:
- Fall within the defined scope
- Be original (not previously reported)
- Include a working PoC
- Accurately assess severity
- Provide clear reproduction steps
- Suggest potential fixes (optional but valued)

## Next Steps

1. Review the [Bounty Process](BOUNTY_PROCESS.md) document
2. Study the [PoC Guidelines](POC_GUIDELINES.md)
3. Use the [Bug Submission Template](../templates/bug_submission_template.md)
4. Begin your research with the highest priority areas
5. Document findings as you go
6. Prepare your submission carefully

## Important Reminders

- **Never test on production/mainnet** - Use testnets or local forks only
- **Focus on unaudited areas** - Maximize your chances of finding new bugs
- **Quality over quantity** - One well-documented critical bug is better than many low-quality reports
- **Stay ethical** - Follow responsible disclosure practices
- **Be thorough** - A complete submission is more likely to be accepted and rewarded

Good luck with your research! Remember, the goal is to help secure the Beanstalk protocol and protect user funds.
