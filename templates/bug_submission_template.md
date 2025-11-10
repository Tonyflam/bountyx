# Bug Submission Template

Use this template when submitting a bug to the Beanstalk bug bounty program.

---

## Vulnerability Information

**Title:** [Concise, descriptive title of the vulnerability]

**Severity:** [Critical / High / Medium / Low]

**Vulnerability Type:** [e.g., Reentrancy, Access Control, Logic Error, etc.]

**Affected Component:** [Contract name(s) and function(s)]

---

## Summary

[Provide a brief, high-level summary of the vulnerability in 2-3 sentences]

---

## Description

[Detailed description of the vulnerability, including:
- What the vulnerability is
- Why it exists
- How it can be exploited
- Technical details of the flaw]

---

## Impact

[Describe the potential impact of this vulnerability:
- What assets are at risk?
- How many users could be affected?
- What is the worst-case scenario?
- Financial implications]

**Severity Justification:**
[Explain why you classified this as Critical/High/Medium/Low based on the bug bounty program guidelines]

---

## Attack Scenario

[Describe a realistic attack scenario step-by-step:
1. Attacker does X
2. This causes Y
3. Resulting in Z]

---

## Preconditions

[List any preconditions required for the vulnerability to be exploitable:
- Specific contract states
- Required permissions
- Market conditions
- Other dependencies]

---

## Proof of Concept

### Environment Setup

[Describe the environment needed to reproduce:
- Network (mainnet fork, testnet, etc.)
- Required tools (Hardhat, Foundry, etc.)
- Dependencies]

### Reproduction Steps

1. [First step]
2. [Second step]
3. [Third step]
...

### Code

```solidity
// Paste your PoC code here
// This should be executable and demonstrate the vulnerability

```

### Expected vs Actual Results

**Expected Behavior:**
[What should happen in a secure system]

**Actual Behavior:**
[What actually happens due to the vulnerability]

### Execution Output

```
[Paste the output from running your PoC]
```

---

## Recommended Fix

[Provide suggestions for fixing the vulnerability:
- Code changes needed
- Alternative approaches
- Security considerations]

### Example Fix (Optional)

```solidity
// Example of how the vulnerability could be fixed
```

---

## References

[List any relevant references:
- Similar vulnerabilities in other projects
- Security best practices documentation
- Relevant EIPs or standards]

---

## Additional Information

[Any other relevant information:
- Related vulnerabilities discovered
- Impact on other parts of the system
- Notes for the development team]

---

## Contact Information

**Researcher:** [Your name or handle]

**Contact Method:** [How the team can reach you for clarification]

**Date Submitted:** [Date]

---

## Appendix

[Include any additional supporting materials:
- Screenshots
- Diagrams
- Extended code samples
- Test results]
