# Research Workflow for Bug Bounty Hunters

This guide provides a step-by-step workflow for conducting effective security research on the Beanstalk protocol.

## Overview

Effective bug bounty hunting requires a systematic approach. This workflow is designed to help you:
- Maximize your chances of finding valid bugs
- Avoid duplicate work
- Create high-quality submissions
- Work efficiently

## Workflow Stages

### Stage 1: Preparation (1-2 days)

**Goal**: Understand the protocol and set up your environment

#### Tasks:
1. **Read Documentation**
   - [ ] Review Beanstalk protocol documentation
   - [ ] Understand the protocol's core mechanisms
   - [ ] Identify key contracts and functions
   - [ ] Study the economic model

2. **Review Previous Work**
   - [ ] Read all previous audit reports
   - [ ] Check disclosed vulnerabilities
   - [ ] Review Immunefi submissions (if public)
   - [ ] Study similar protocol exploits

3. **Set Up Environment**
   - [ ] Install necessary tools (Hardhat/Foundry)
   - [ ] Clone the Beanstalk repository
   - [ ] Set up local testing environment
   - [ ] Configure mainnet fork for testing

4. **Initial Reconnaissance**
   - [ ] Map out contract architecture
   - [ ] Identify critical functions
   - [ ] Document fund flows
   - [ ] Note access control patterns

**Deliverable**: Research notes and environment setup complete

---

### Stage 2: Reconnaissance (2-3 days)

**Goal**: Identify potential attack surfaces and vulnerability patterns

#### Tasks:
1. **Static Analysis**
   - [ ] Run Slither on all contracts
   - [ ] Run Mythril for automated detection
   - [ ] Review compiler warnings
   - [ ] Check for known vulnerability patterns

2. **Manual Code Review**
   - [ ] Read through each contract carefully
   - [ ] Focus on critical functions first
   - [ ] Note suspicious patterns
   - [ ] Document questions and concerns

3. **Attack Surface Mapping**
   - [ ] List all external functions
   - [ ] Identify state-changing operations
   - [ ] Map trust boundaries
   - [ ] Document integration points

4. **Priority Ranking**
   - [ ] Rank potential vulnerabilities by severity
   - [ ] Identify most promising areas
   - [ ] Focus on unaudited code
   - [ ] Note edge cases

**Deliverable**: Prioritized list of potential vulnerabilities to investigate

---

### Stage 3: Deep Dive (3-5 days)

**Goal**: Thoroughly investigate promising vulnerability candidates

#### For Each Potential Vulnerability:

1. **Hypothesis Formation**
   - What is the suspected vulnerability?
   - What would be the impact?
   - What are the preconditions?
   - Is it theoretically exploitable?

2. **Initial Testing**
   - Write quick test to check if vulnerability exists
   - Verify the bug is reproducible
   - Check if it's already known
   - Assess initial severity

3. **Deep Analysis**
   - Trace execution flow
   - Identify all conditions required
   - Check for mitigations in place
   - Explore alternative attack vectors

4. **Impact Assessment**
   - How much could be stolen/lost?
   - How many users affected?
   - What are the real-world implications?
   - Does severity match initial assessment?

**Deliverable**: Confirmed vulnerabilities with initial impact assessment

---

### Stage 4: Proof of Concept Development (2-4 days)

**Goal**: Create robust, executable PoCs for confirmed vulnerabilities

#### Tasks:
1. **PoC Design**
   - [ ] Plan the PoC structure
   - [ ] Identify minimal code needed
   - [ ] Choose testing framework
   - [ ] Design test scenarios

2. **Implementation**
   - [ ] Write setup code
   - [ ] Implement attack scenario
   - [ ] Add verification checks
   - [ ] Include comprehensive comments

3. **Testing**
   - [ ] Test on local fork
   - [ ] Verify reproducibility
   - [ ] Test edge cases
   - [ ] Validate impact claims

4. **Refinement**
   - [ ] Optimize code clarity
   - [ ] Remove unnecessary complexity
   - [ ] Add detailed output/logging
   - [ ] Document all steps

**Deliverable**: Working, well-documented PoC

---

### Stage 5: Documentation (1-2 days)

**Goal**: Create comprehensive bug report

#### Tasks:
1. **Write Description**
   - [ ] Clear, concise vulnerability description
   - [ ] Technical details of the flaw
   - [ ] Why it exists
   - [ ] How it can be exploited

2. **Impact Analysis**
   - [ ] Detailed impact assessment
   - [ ] Severity justification
   - [ ] Affected components
   - [ ] Real-world scenarios

3. **PoC Documentation**
   - [ ] Complete setup instructions
   - [ ] Step-by-step reproduction
   - [ ] Expected vs actual results
   - [ ] Sample output

4. **Recommendations**
   - [ ] Suggested fixes
   - [ ] Alternative solutions
   - [ ] Security best practices
   - [ ] Additional considerations

**Deliverable**: Complete bug report following the submission template

---

### Stage 6: Review and Submission (1 day)

**Goal**: Ensure submission quality and submit through proper channels

#### Tasks:
1. **Self Review**
   - [ ] Check submission against checklist
   - [ ] Verify PoC works in clean environment
   - [ ] Ensure all information is accurate
   - [ ] Proofread for clarity

2. **Peer Review (Optional)**
   - [ ] Have colleague review (if possible)
   - [ ] Get feedback on clarity
   - [ ] Verify PoC works for others
   - [ ] Address any questions

3. **Final Preparation**
   - [ ] Organize all materials
   - [ ] Prepare supporting documents
   - [ ] Format submission properly
   - [ ] Double-check severity assessment

4. **Submission**
   - [ ] Submit through Immunefi platform
   - [ ] Include all required information
   - [ ] Save confirmation/receipt
   - [ ] Note submission date

**Deliverable**: Submitted bug report with confirmation

---

## Daily Research Routine

### Morning (2-3 hours)
- Review previous day's findings
- Plan today's investigation targets
- Set specific goals for the day
- Begin deep analysis work

### Afternoon (3-4 hours)
- Continue investigation
- Test hypotheses
- Document findings
- Review and refine code

### Evening (1-2 hours)
- Review day's progress
- Update research notes
- Plan next day's work
- Read relevant security research

## Research Tips

### Do's ✅
- Take detailed notes as you work
- Test hypotheses quickly
- Focus on high-severity vulnerabilities
- Document everything
- Stay organized
- Take breaks to maintain focus
- Cross-reference with known vulnerabilities
- Think like an attacker

### Don'ts ❌
- Don't spend too long on low-severity issues
- Don't ignore your intuition
- Don't skip documentation
- Don't test on production
- Don't submit untested PoCs
- Don't rush the process
- Don't ignore edge cases
- Don't give up too easily

## Time Management

**Total Time Estimate**: 10-15 days for thorough research

**Breakdown**:
- Preparation: 10%
- Reconnaissance: 20%
- Deep Dive: 30%
- PoC Development: 20%
- Documentation: 15%
- Review & Submission: 5%

**Note**: These are estimates. Adjust based on:
- Protocol complexity
- Your experience level
- Availability of documentation
- Number of vulnerabilities found

## Success Metrics

Track your progress with these metrics:

- **Coverage**: % of contracts reviewed
- **Depth**: Number of functions analyzed in detail
- **Quality**: Bugs confirmed vs. false positives
- **Documentation**: Completeness of research notes
- **PoC Quality**: Working vs. non-working PoCs

## Common Pitfalls to Avoid

1. **Analysis Paralysis**: Don't spend weeks in preparation
2. **Tunnel Vision**: Don't focus only on one vulnerability type
3. **Incomplete PoCs**: Don't submit theoretical vulnerabilities
4. **Poor Documentation**: Don't submit unclear reports
5. **Duplicate Work**: Always check previous audits
6. **Scope Creep**: Stay focused on in-scope items
7. **Rushing**: Don't sacrifice quality for speed

## When to Move On

Move on from a potential vulnerability if:
- Can't create a working PoC after reasonable effort
- Discover it's already been reported
- Find it's mitigated in the code
- Realize it's out of scope
- Determine impact is lower than initially thought

## When to Dig Deeper

Dig deeper if:
- Initial tests show promise
- Impact could be critical
- Pattern matches known exploits
- Intuition says something is wrong
- Could affect many users
- Involves fund handling

## Research Checklist

Before moving to next stage, ensure:
- [ ] All tasks for current stage completed
- [ ] Deliverables are ready
- [ ] Documentation is up to date
- [ ] No obvious gaps in analysis
- [ ] Ready to proceed to next stage

## Resources for Each Stage

### Preparation
- Protocol documentation
- Audit reports
- Similar protocol architectures

### Reconnaissance
- Slither, Mythril tools
- Vulnerability pattern databases
- Smart contract security guides

### Deep Dive
- Debuggers (Tenderly, Hardhat)
- Code analysis tools
- Execution tracers

### PoC Development
- Testing frameworks docs
- Example exploits
- PoC templates

### Documentation
- Bug report templates
- Technical writing guides
- Previous submissions (if public)

## Getting Unstuck

If you're stuck:
1. Review your notes from the beginning
2. Take a break and come back fresh
3. Try a different approach
4. Consult security resources
5. Move to a different area temporarily
6. Review similar vulnerabilities
7. Discuss with peers (without revealing specifics)

## Final Checks Before Submission

- [ ] PoC tested in clean environment
- [ ] All documentation complete
- [ ] Severity assessment justified
- [ ] No duplicate submissions
- [ ] Within scope
- [ ] Professional presentation
- [ ] Contact information included
- [ ] Ready to answer questions

---

Remember: Quality over quantity. One well-researched, thoroughly documented critical vulnerability is worth more than multiple low-quality submissions.

Good luck with your research!
