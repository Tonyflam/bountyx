# Quick Reference Guide

A quick reference for bug bounty hunters working on the Beanstalk program.

## 🚀 Quick Start (5 minutes)

1. Read [README.md](../README.md) for overview
2. Review [BEANSTALK_SCOPE.md](../docs/BEANSTALK_SCOPE.md) for program details
3. Start with [RESEARCH_WORKFLOW.md](../docs/RESEARCH_WORKFLOW.md)

## 📋 Essential Documents

| Document | Purpose | When to Use |
|----------|---------|-------------|
| [README.md](../README.md) | Framework overview | First read |
| [BEANSTALK_SCOPE.md](../docs/BEANSTALK_SCOPE.md) | Program scope & severity | Before research |
| [RESEARCH_WORKFLOW.md](../docs/RESEARCH_WORKFLOW.md) | Step-by-step process | During research |
| [POC_GUIDELINES.md](../docs/POC_GUIDELINES.md) | PoC best practices | When creating PoC |
| [BOUNTY_PROCESS.md](../docs/BOUNTY_PROCESS.md) | Complete process guide | Throughout |

## 📝 Templates

| Template | Use For |
|----------|---------|
| [bug_submission_template.md](../templates/bug_submission_template.md) | Final bug report |
| [SUBMISSION_CHECKLIST.md](../templates/SUBMISSION_CHECKLIST.md) | Pre-submission review |
| [POC_EXAMPLE.md](../templates/POC_EXAMPLE.md) | PoC code reference |

## ⚡ Severity Quick Reference

| Level | Examples | Reward |
|-------|----------|--------|
| **Critical** | Direct theft, permanent freeze, insolvency | Highest |
| **High** | Unclaimed yield theft, 24h+ freeze | High |
| **Medium** | DoS, griefing, block stuffing | Medium |
| **Low** | Failed returns (no value loss) | Low |

## ✅ Submission Requirements

**Must Have:**
- ✅ Within scope
- ✅ Not previously reported
- ✅ Executable PoC
- ✅ Clear documentation
- ✅ Impact assessment
- ✅ Reproduction steps

## 🎯 High Priority Research Areas

1. **Fund Security** - Deposits, withdrawals, transfers
2. **Protocol Solvency** - Collateralization, debt management
3. **Access Control** - Permissions, privileged functions
4. **Economic Attacks** - Flash loans, price manipulation

## 🛠️ Recommended Tools

**Static Analysis:** Slither, Mythril, Securify
**Testing:** Hardhat, Foundry
**Debugging:** Tenderly, Hardhat Network

## 📊 Research Timeline

| Phase | Duration | Focus |
|-------|----------|-------|
| Preparation | 1-2 days | Setup & learning |
| Reconnaissance | 2-3 days | Finding vulnerabilities |
| Deep Dive | 3-5 days | Analysis & validation |
| PoC Development | 2-4 days | Creating proof |
| Documentation | 1-2 days | Writing report |
| Review & Submit | 1 day | Final checks |

**Total:** ~10-15 days for thorough research

## ⚠️ Common Mistakes to Avoid

❌ Testing on production
❌ Submitting without PoC
❌ Theoretical vulnerabilities only
❌ Duplicate submissions
❌ Out of scope items
❌ Poor documentation

## 🎓 Best Practices

✅ Focus on critical/high severity
✅ Create working PoCs
✅ Document thoroughly
✅ Test on testnets/forks only
✅ Follow responsible disclosure
✅ Be professional

## 🔍 Research Process (Simplified)

```
1. Read docs & audits
   ↓
2. Set up environment
   ↓
3. Static analysis
   ↓
4. Manual review
   ↓
5. Find vulnerability
   ↓
6. Create PoC
   ↓
7. Write report
   ↓
8. Review & submit
```

## 📞 Getting Help

**Documentation Issues:** Review the specific guide again
**Technical Questions:** Refer to tool documentation
**Process Questions:** Check [BOUNTY_PROCESS.md](../docs/BOUNTY_PROCESS.md)
**PoC Help:** See [POC_EXAMPLE.md](../templates/POC_EXAMPLE.md)

## 🔄 Typical Workflow

### Day 1-2: Setup
- Install tools
- Clone repositories
- Read documentation
- Review audits

### Day 3-5: Research
- Run static analysis
- Review contracts
- Identify targets
- Test hypotheses

### Day 6-10: Development
- Confirm vulnerabilities
- Create PoCs
- Test thoroughly
- Document findings

### Day 11-12: Finalization
- Write report
- Review submission
- Final testing
- Submit

## 💡 Pro Tips

1. **Start early** - Set up environment before you need it
2. **Take notes** - Document everything as you go
3. **Test incrementally** - Don't wait to test PoC
4. **Focus on impact** - Prioritize high-severity bugs
5. **Be thorough** - Quality over quantity
6. **Stay ethical** - Never test on production

## 📈 Success Indicators

Your research is going well if:
- ✅ You understand the protocol deeply
- ✅ You've identified specific attack surfaces
- ✅ Your PoCs work consistently
- ✅ Your documentation is clear
- ✅ You can explain the bug simply

## 🚨 Red Flags

Stop and reconsider if:
- 🚩 Can't create working PoC
- 🚩 Impact seems theoretical
- 🚩 Very similar to known bugs
- 🚩 Can't explain clearly
- 🚩 Requires many assumptions

## 📚 Learning Path

**Beginner:**
1. Read all documentation
2. Review example PoCs
3. Start with static analysis
4. Focus on clear patterns

**Intermediate:**
1. Manual code review
2. Create simple PoCs
3. Understand attack vectors
4. Analyze previous exploits

**Advanced:**
1. Complex vulnerability chains
2. Economic attack vectors
3. Novel exploit techniques
4. Multiple attack scenarios

## ⏰ Time Management

Allocate your time wisely:
- 10% - Preparation
- 20% - Reconnaissance  
- 30% - Deep dive
- 20% - PoC development
- 15% - Documentation
- 5% - Review & submission

## 🎯 Daily Goals

Set achievable daily goals:
- **Day 1:** Setup complete
- **Day 3:** First contract reviewed
- **Day 5:** Potential bug identified
- **Day 7:** PoC working
- **Day 10:** Documentation started
- **Day 12:** Submission ready

## 📖 Before You Start

Read in this order:
1. [README.md](../README.md) - Overview
2. [BEANSTALK_SCOPE.md](../docs/BEANSTALK_SCOPE.md) - Scope
3. [RESEARCH_WORKFLOW.md](../docs/RESEARCH_WORKFLOW.md) - Process
4. [POC_GUIDELINES.md](../docs/POC_GUIDELINES.md) - PoC creation

## 📋 Before You Submit

Check these:
1. [SUBMISSION_CHECKLIST.md](../templates/SUBMISSION_CHECKLIST.md) - Complete checklist
2. [bug_submission_template.md](../templates/bug_submission_template.md) - Format report
3. [POC_EXAMPLE.md](../templates/POC_EXAMPLE.md) - Verify PoC quality

## 🎉 Ready to Start?

1. Set up your environment
2. Read [RESEARCH_WORKFLOW.md](../docs/RESEARCH_WORKFLOW.md)
3. Begin with reconnaissance
4. Good luck!

---

**Remember:** The goal is to help secure Beanstalk and protect user funds. Take your time, be thorough, and maintain the highest ethical standards.
