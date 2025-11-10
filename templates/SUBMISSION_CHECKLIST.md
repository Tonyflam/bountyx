# Bug Bounty Submission Checklist

Use this checklist before submitting your bug report to ensure completeness and quality.

## Pre-Submission Verification

### Scope Validation
- [ ] The vulnerability is within the defined scope of the Beanstalk bug bounty program
- [ ] The affected component is explicitly listed as in-scope
- [ ] The vulnerability type is covered by the program
- [ ] The bug is not in the exclusions list

### Originality Check
- [ ] Searched previous audit reports for this vulnerability
- [ ] Checked Immunefi submissions (if publicly available)
- [ ] Verified this is not a known issue
- [ ] Confirmed the bug has not been previously disclosed
- [ ] The vulnerability is in unaudited code or a new finding

### Severity Assessment
- [ ] Severity level is accurately classified (Critical/High/Medium/Low)
- [ ] Impact assessment matches program guidelines
- [ ] Severity is justified by the PoC results
- [ ] Potential damage is clearly quantified

## Documentation Completeness

### Bug Report
- [ ] Clear, descriptive title
- [ ] Comprehensive vulnerability description
- [ ] Technical details of the flaw
- [ ] Attack scenario walkthrough
- [ ] Impact analysis with real-world implications
- [ ] List of affected components
- [ ] Preconditions for exploitation

### Proof of Concept
- [ ] PoC code is included
- [ ] PoC is executable (not pseudocode)
- [ ] Setup instructions are complete
- [ ] All dependencies are documented
- [ ] Step-by-step reproduction guide
- [ ] Expected vs actual results shown
- [ ] Output/logs included
- [ ] Code is well-commented

### Testing Verification
- [ ] PoC tested in clean environment
- [ ] Results are reproducible
- [ ] All steps verified
- [ ] Edge cases considered
- [ ] Impact confirmed by PoC execution

## Code Quality

### PoC Code Standards
- [ ] Code is clean and readable
- [ ] Proper formatting applied
- [ ] Comments explain each step
- [ ] Variable names are descriptive
- [ ] No unnecessary complexity
- [ ] Follows best practices for the language
- [ ] Includes assertions to prove impact

### Technical Accuracy
- [ ] All technical claims are accurate
- [ ] Code execution path is correct
- [ ] Function names and addresses are correct
- [ ] No errors in the PoC code
- [ ] Results match the claims made

## Submission Content

### Required Sections
- [ ] Vulnerability Information (title, severity, type, component)
- [ ] Summary (2-3 sentence overview)
- [ ] Detailed Description
- [ ] Impact Assessment
- [ ] Attack Scenario
- [ ] Preconditions
- [ ] Proof of Concept (with code)
- [ ] Reproduction Steps
- [ ] Expected vs Actual Results
- [ ] Execution Output

### Optional but Recommended
- [ ] Recommended fix
- [ ] Example fix code
- [ ] References to similar vulnerabilities
- [ ] Additional context or notes
- [ ] Diagrams or visual aids (if helpful)

## Professional Standards

### Presentation
- [ ] Report is well-formatted
- [ ] No spelling or grammar errors
- [ ] Professional tone throughout
- [ ] Clear and concise writing
- [ ] Logical organization
- [ ] Easy to follow

### Communication
- [ ] Contact information included
- [ ] Preferred communication method stated
- [ ] Available for follow-up questions
- [ ] Response time expectations set (optional)

## Ethical Compliance

### Testing Ethics
- [ ] Only tested on testnet or local fork
- [ ] No exploitation on mainnet
- [ ] No actual user funds at risk during testing
- [ ] Followed responsible disclosure practices
- [ ] Did not share vulnerability publicly before submission

### Submission Ethics
- [ ] Submitted through official Immunefi channel
- [ ] Not submitted to multiple platforms simultaneously
- [ ] No attempts to leverage for personal gain before disclosure
- [ ] Honest and accurate reporting

## Final Review

### Self-Review
- [ ] Read through entire submission
- [ ] Verified all information is accurate
- [ ] Checked all links work (if any)
- [ ] Ensured PoC works as described
- [ ] Reviewed against submission template

### Peer Review (Optional)
- [ ] Had colleague review (if possible)
- [ ] Incorporated feedback
- [ ] Verified clarity with fresh eyes
- [ ] Tested PoC with someone else

### Material Preparation
- [ ] All files organized
- [ ] Supporting materials ready
- [ ] Screenshots/diagrams prepared (if needed)
- [ ] Backup copies saved locally

## Submission Process

### Platform Submission
- [ ] Logged into Immunefi platform
- [ ] Selected correct program (Beanstalk)
- [ ] Filled all required fields
- [ ] Attached all necessary files
- [ ] Reviewed submission before sending
- [ ] Saved submission confirmation

### Post-Submission
- [ ] Saved submission reference number
- [ ] Noted submission date and time
- [ ] Available to answer questions
- [ ] Prepared to provide additional information if needed
- [ ] Set expectations for response time

## Common Mistakes to Avoid

### Before Submission
- ❌ Submitting without a PoC
- ❌ Theoretical vulnerabilities only
- ❌ Incomplete reproduction steps
- ❌ Missing severity justification
- ❌ Vague or unclear descriptions
- ❌ Untested PoC code
- ❌ Out-of-scope submissions

### During Testing
- ❌ Testing on production
- ❌ Risking actual funds
- ❌ Incomplete environment setup
- ❌ Not verifying reproducibility
- ❌ Skipping edge cases

### In Documentation
- ❌ Poor formatting
- ❌ Missing critical information
- ❌ Unclear writing
- ❌ Inaccurate technical details
- ❌ Exaggerated claims
- ❌ Insufficient detail

## Quality Indicators

Your submission is likely high quality if:
- ✅ PoC works on first try
- ✅ All information is present
- ✅ Severity is well-justified
- ✅ Documentation is professional
- ✅ Technical details are accurate
- ✅ Impact is clearly demonstrated
- ✅ Reproduction is straightforward

## Red Flags to Address

Review if you notice:
- 🚩 PoC requires many attempts to work
- 🚩 Unclear how to reproduce
- 🚩 Severity seems arbitrary
- 🚩 Missing key information
- 🚩 Vague impact description
- 🚩 Theoretical exploitation only
- 🚩 Similar to reported bugs

## Time Estimates

Plan for these review times:
- Self-review: 1-2 hours
- PoC testing in clean environment: 2-4 hours
- Documentation polish: 1-2 hours
- Final checks: 30 minutes
- Submission process: 30 minutes

**Total**: ~5-9 hours for thorough review and submission

## Success Criteria

Before submitting, confirm:
1. ✅ You can explain the vulnerability in 30 seconds
2. ✅ Someone else could reproduce it from your docs
3. ✅ The PoC clearly shows the impact
4. ✅ All claims are backed by evidence
5. ✅ The submission is professional
6. ✅ You're proud of the quality

## If You Answer "No" to Any Item

**Don't submit yet!** Instead:
1. Identify what's missing or incomplete
2. Address the gap
3. Re-test if needed
4. Update documentation
5. Run through checklist again

## Final Confidence Check

Ask yourself:
- Would I be confident presenting this to the development team?
- Is this the quality I would expect to receive?
- Have I provided everything needed to validate the bug?
- Am I proud of this submission?

If yes to all: **You're ready to submit!**

If no to any: **Take more time to improve.**

---

## Post-Submission

After submitting:
- [ ] Monitor for acknowledgment
- [ ] Be ready to answer questions
- [ ] Prepare additional details if requested
- [ ] Be patient during validation
- [ ] Maintain professional communication

Remember: A well-prepared submission is more likely to be accepted and rewarded. Take the time to ensure quality!

## Notes Section

Use this space for final notes or reminders:

```
[Your notes here]
```

---

**Good luck with your submission!**
