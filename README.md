# BountyX - Bug Bounty Research & Submission Framework

A comprehensive framework for conducting security research and submitting bug bounty reports for the Beanstalk protocol on Immunefi.

## Overview

This repository provides structured guidance, templates, and workflows for security researchers participating in the Beanstalk bug bounty program. It helps you:

- Conduct systematic security research
- Create high-quality Proof of Concepts (PoCs)
- Submit professional bug reports
- Maximize your chances of finding valid vulnerabilities

## Quick Start

1. **Understand the Program**: Read [Beanstalk Scope](docs/BEANSTALK_SCOPE.md) to understand what's in scope and severity levels
2. **Follow the Process**: Review [Bounty Process](docs/BOUNTY_PROCESS.md) for the complete workflow
3. **Plan Your Research**: Use [Research Workflow](docs/RESEARCH_WORKFLOW.md) to guide your investigation
4. **Create PoCs**: Follow [PoC Guidelines](docs/POC_GUIDELINES.md) for creating executable proofs
5. **Submit**: Use the [Bug Submission Template](templates/bug_submission_template.md) for your report

## Repository Structure

```
bountyx/
├── docs/
│   ├── BEANSTALK_SCOPE.md      # Scope, severity levels, and focus areas
│   ├── BOUNTY_PROCESS.md        # Complete submission process
│   ├── POC_GUIDELINES.md        # How to create effective PoCs
│   └── RESEARCH_WORKFLOW.md     # Step-by-step research methodology
├── templates/
│   └── bug_submission_template.md  # Structured submission template
└── README.md
```

## Documentation

### Core Guides

- **[Beanstalk Scope](docs/BEANSTALK_SCOPE.md)**: Understand the bug bounty program scope, severity classifications, and research priorities for the Beanstalk protocol
- **[Bounty Process](docs/BOUNTY_PROCESS.md)**: Complete guide to the bug bounty submission process, from research to submission
- **[Research Workflow](docs/RESEARCH_WORKFLOW.md)**: Detailed workflow for conducting systematic security research
- **[PoC Guidelines](docs/POC_GUIDELINES.md)**: Best practices for creating executable Proof of Concepts

### Templates

- **[Bug Submission Template](templates/bug_submission_template.md)**: Structured template for submitting bug reports

## Severity Levels

### Critical
- Direct theft of user funds
- Permanent freezing of funds
- Protocol insolvency

### High
- Theft of unclaimed yield
- Permanent freezing of unclaimed yield
- Temporary freezing of funds (24+ hours)

### Medium
- Smart contract unable to operate due to lack of funds
- Block stuffing for profit
- Griefing attacks

### Low
- Contract fails to deliver promised returns

## Key Features

✅ **Systematic Approach**: Step-by-step workflow for thorough research
✅ **PoC Framework**: Guidelines for creating working exploits
✅ **Quality Templates**: Professional submission templates
✅ **Best Practices**: Industry-standard security research methods
✅ **Focus Areas**: Prioritized research targets
✅ **Tools & Resources**: Recommended tools and references

## Requirements for Valid Submissions

1. **Within Scope**: Must target in-scope components
2. **Original**: Not previously reported or audited
3. **Executable PoC**: Working code that demonstrates the vulnerability
4. **Clear Documentation**: Detailed description and reproduction steps
5. **Impact Assessment**: Accurate severity classification
6. **Professional**: Well-formatted and complete submission

## Research Focus Areas

### High Priority
- Fund security and withdrawal mechanisms
- Protocol solvency and collateralization
- Access control and permissions
- Economic attacks and flash loans

### Medium Priority
- Yield calculation and distribution
- State management and consistency
- External integrations and oracles

## Getting Started

### 1. Preparation
- Review all documentation in `docs/`
- Set up your development environment
- Study previous audit reports
- Understand the protocol architecture

### 2. Research
- Follow the [Research Workflow](docs/RESEARCH_WORKFLOW.md)
- Use static analysis tools
- Focus on high-priority areas
- Document your findings

### 3. PoC Development
- Create executable proof of concept
- Follow [PoC Guidelines](docs/POC_GUIDELINES.md)
- Test thoroughly before submission
- Include clear comments and output

### 4. Submission
- Use the [Bug Submission Template](templates/bug_submission_template.md)
- Include all required information
- Submit through Immunefi platform
- Be available for follow-up questions

## Best Practices

### Do's ✅
- Focus on critical and high-severity vulnerabilities
- Create working, executable PoCs
- Document everything thoroughly
- Test on testnets or forks only
- Follow responsible disclosure
- Be professional and responsive

### Don'ts ❌
- Don't test on production/mainnet
- Don't submit theoretical vulnerabilities
- Don't rush the submission
- Don't ignore previous audit findings
- Don't submit duplicate reports
- Don't be vague or incomplete

## Tools Recommended

### Static Analysis
- Slither
- Mythril
- Securify

### Testing Frameworks
- Hardhat
- Foundry
- Truffle

### Debugging
- Tenderly
- Hardhat Network
- Ganache

## Resources

- [Immunefi Platform](https://immunefi.com/)
- Beanstalk Protocol Documentation
- Smart Contract Security Best Practices
- DeFi Security Resources

## Contributing

This framework is designed to help security researchers conduct effective bug bounty research. If you have suggestions for improvements:

1. Focus on making the process clearer
2. Add helpful examples or templates
3. Share best practices (without revealing specific vulnerabilities)
4. Improve documentation clarity

## Ethical Guidelines

- Only test on designated testnet environments or local forks
- Never exploit vulnerabilities on production
- Follow responsible disclosure practices
- Submit only valid, in-scope vulnerabilities
- Be professional in all communications
- Help protect user funds and the protocol

## Success Tips

1. **Be Thorough**: Don't rush the research process
2. **Be Clear**: Write clear, professional reports
3. **Be Complete**: Include all required information and PoC
4. **Be First**: Check for duplicates before submitting
5. **Be Professional**: Maintain professional communication
6. **Be Patient**: Allow time for review and validation

## License

This framework is provided for educational and research purposes to support bug bounty hunters in the Beanstalk program.

## Disclaimer

This repository provides guidance only. Actual bug bounty rewards are determined by the Beanstalk team and Immunefi based on the validity and severity of submitted vulnerabilities. Always follow the official program rules and guidelines.

---

**Good luck with your security research! Help make Beanstalk more secure.**