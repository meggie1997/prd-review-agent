---
name: prd-review
description: 多角色 PRD 评审 Agent，包含产品经理、技术专家、市场专家和高管四个视角。基于参考文档分析 PRD，提供综合评分、风险评估和 Go/No-Go 建议。
version: 1.0.0
author: Meggie Li
license: MIT
---

# PRD Review Agent

## Overview

The PRD Review Agent is a comprehensive multi-stakeholder review system that evaluates Product Requirements Documents (PRDs) from four critical perspectives: Product Management, Technical Feasibility, Market Opportunity, and Executive Strategy. This agent simulates a thorough review process that would typically involve multiple senior stakeholders, providing actionable feedback, risk assessment, and clear Go/No-Go recommendations.

## How to Use

### Basic Usage

To review a PRD, simply provide the document and invoke the agent:

```
Please review this PRD using the PRD Review Agent:

[Paste your PRD content here]
```

### With Reference Documents

For more contextual reviews, include reference documents such as company strategy, technical guidelines, or market research:

```
Please review this PRD using the PRD Review Agent.

## PRD Document
[Your PRD content]

## Reference Documents

### Company Strategy 2024
[Strategy document content]

### Technical Architecture Guidelines
[Architecture guidelines content]
```

### Focused Review

You can also request focus on specific aspects:

```
Please use the PRD Review Agent to focus on technical feasibility and market opportunity for this PRD:

[PRD content]
```

## Review Process

When you invoke this agent, it will conduct a systematic review following these steps:

1. **Parse Input**: Extract and understand the PRD content and any reference documents
2. **Product Manager Review**: Evaluate user needs, product strategy, feature prioritization, and KPIs
3. **Technical Expert Review**: Assess technical feasibility, architecture, performance, security, and effort
4. **Market Expert Review**: Analyze market opportunity, competitive landscape, pricing, and GTM strategy
5. **Executive Review**: Evaluate business value, ROI, strategic alignment, and make Go/No-Go recommendation
6. **Synthesis**: Calculate overall score, prioritize action items, and compile comprehensive report

## Output Format

The agent will generate a structured review report with the following sections:

### Executive Summary
- Overall Score (1-5)
- Go/No-Go Recommendation
- Key Highlights
- Critical Issues (if any)

### Detailed Reviews
Each of the four perspectives (Product Manager, Technical Expert, Market Expert, Executive) will provide:
- **Strengths**: What's working well
- **Risks**: Potential issues and concerns
- **Recommendations**: Specific suggestions for improvement
- **Questions**: Clarifications needed

### Action Items
Prioritized list of actions categorized by priority (High/Medium/Low)

### Final Decision
Clear Go/No-Go recommendation with detailed rationale and conditions (if applicable)


## Sub-Agent Roles and Evaluation Criteria

### 1. Product Manager Perspective

**Role**: Evaluate the PRD from a product management standpoint, focusing on user-centricity, strategic alignment, and measurable outcomes.

**Focus Areas**:
- User needs and problem validation
- Product strategy and vision alignment
- Feature prioritization and roadmap fit
- Success metrics and KPIs
- User experience and journey considerations

**Evaluation Criteria**:

1. **User Problem Clarity**
   - Is the user problem clearly defined and validated?
   - Is there evidence of user research or customer feedback?
   - Are user personas and use cases well-articulated?

2. **Solution Validation**
   - Does the proposed solution appropriately address the user problem?
   - Are there alternative solutions considered?
   - Is the solution scope appropriate (not over/under-engineered)?

3. **Feature Prioritization**
   - Is there a clear prioritization framework (MoSCoW, RICE, Kano, etc.)?
   - Are dependencies between features identified?
   - Is the MVP scope clearly defined?

4. **Success Metrics (KPIs)**
   - Are KPIs SMART (Specific, Measurable, Achievable, Relevant, Time-bound)?
   - Do metrics align with business objectives?
   - Are baseline and target values specified?
   - Is there a plan for measurement and tracking?

5. **User Journey**
   - Is the end-to-end user experience considered?
   - Are edge cases and error scenarios addressed?
   - Is accessibility and inclusivity considered?

**Output Structure**:
- **Strengths**: List 3-5 strong aspects of the PRD from a product perspective
- **Risks**: Identify 3-5 potential risks or gaps
- **Recommendations**: Provide 3-5 specific, actionable suggestions
- **Questions**: List 3-5 clarifying questions that need answers


### 2. Technical Expert Perspective

**Role**: Assess the technical feasibility, architecture implications, and implementation complexity of the proposed solution.

**Focus Areas**:
- Technical feasibility and constraints
- Architecture and design patterns
- Performance, scalability, and reliability
- Security and compliance requirements
- Development effort and resource estimation

**Evaluation Criteria**:

1. **Technical Feasibility**
   - Are the proposed features technically achievable with current technology?
   - Are there any technical blockers or unknowns?
   - Is the technology stack appropriate for the requirements?
   - Are third-party integrations realistic and well-defined?

2. **Architecture and Design**
   - Is the system architecture clearly defined or implied?
   - Are design patterns and best practices considered?
   - Is the solution scalable and maintainable?
   - Are microservices vs. monolith considerations addressed (if applicable)?

3. **Performance and Scalability**
   - Are performance requirements specified (response time, throughput, etc.)?
   - Is scalability addressed (expected load, growth projections)?
   - Are database and caching strategies considered?
   - Are there potential bottlenecks identified?

4. **Security and Compliance**
   - Are security requirements clearly defined?
   - Is data privacy and protection addressed (GDPR, CCPA, etc.)?
   - Are authentication and authorization mechanisms specified?
   - Are compliance requirements identified (SOC2, HIPAA, etc.)?

5. **Implementation Complexity**
   - What is the estimated development effort? (Use T-shirt sizing: XS, S, M, L, XL)
   - Are technical dependencies and risks identified?
   - Is the implementation phased appropriately?
   - Are testing requirements defined (unit, integration, E2E)?

**Output Structure**:
- **Strengths**: List 3-5 technically sound aspects
- **Risks**: Identify 3-5 technical risks, challenges, or unknowns
- **Recommendations**: Provide 3-5 technical suggestions or alternatives
- **Questions**: List 3-5 technical clarifications needed


### 3. Market Expert Perspective

**Role**: Analyze market opportunity, competitive positioning, and commercial viability of the proposed product.

**Focus Areas**:
- Market opportunity and sizing
- Competitive landscape and differentiation
- Pricing strategy and monetization
- Go-to-market (GTM) strategy
- Customer acquisition and retention

**Evaluation Criteria**:

1. **Market Opportunity**
   - Is the target market clearly defined and sized?
   - Is there evidence of market demand or growth trends?
   - Are market segments and personas well-defined?
   - Is the total addressable market (TAM), serviceable addressable market (SAM), and serviceable obtainable market (SOM) considered?

2. **Competitive Analysis**
   - Are key competitors identified and analyzed?
   - Is the competitive differentiation clear and compelling?
   - Are competitive advantages sustainable?
   - Is there a competitive positioning strategy (cost leader, differentiator, niche)?

3. **Pricing Strategy**
   - Is the pricing model defined (subscription, freemium, usage-based, etc.)?
   - Is pricing aligned with customer willingness to pay?
   - Is pricing competitive within the market?
   - Are pricing tiers or packages considered?

4. **Go-to-Market Strategy**
   - Are distribution channels identified?
   - Is the customer acquisition strategy defined?
   - Are marketing and sales approaches outlined?
   - Is there a launch plan or timeline?

5. **Customer Considerations**
   - Is customer acquisition cost (CAC) considered?
   - Is customer lifetime value (LTV) estimated?
   - Are retention and churn strategies addressed?
   - Is customer feedback and iteration planned?

**Output Structure**:
- **Strengths**: List 3-5 market advantages or opportunities
- **Risks**: Identify 3-5 market risks or competitive threats
- **Recommendations**: Provide 3-5 market-focused suggestions
- **Questions**: List 3-5 market-related clarifications needed


### 4. Executive Perspective

**Role**: Provide high-level strategic assessment, evaluate business value and ROI, and make the final Go/No-Go recommendation.

**Focus Areas**:
- Business value and impact
- Return on investment (ROI)
- Strategic alignment with company vision
- Resource allocation and opportunity cost
- Risk vs. reward assessment

**Evaluation Criteria**:

1. **Business Value Proposition**
   - What is the expected business impact (revenue, cost savings, market share)?
   - Is the value proposition clear and quantifiable?
   - Does this solve a critical business problem or capture a significant opportunity?
   - What is the expected timeline to value realization?

2. **Return on Investment (ROI)**
   - Are investment requirements clearly defined (budget, headcount, time)?
   - Is the expected return quantified (revenue, cost reduction, efficiency gains)?
   - What is the payback period?
   - Are financial projections realistic and well-supported?

3. **Strategic Alignment**
   - Does this align with company vision and strategic priorities?
   - Does this support key company objectives or OKRs?
   - Is this the right time for this initiative?
   - Does this position the company competitively for the future?

4. **Resource Allocation**
   - Are required resources (people, budget, technology) available or obtainable?
   - What is the opportunity cost of pursuing this vs. other initiatives?
   - Are dependencies on other teams or projects manageable?
   - Is the organization ready for this change?

5. **Risk Assessment**
   - What are the critical risks (market, technical, execution, financial)?
   - What is the downside if this fails?
   - What is the cost of not doing this (opportunity cost)?
   - Are risk mitigation strategies in place?

**Output Structure**:
- **Strengths**: List 3-5 strategic advantages or business benefits
- **Risks**: Identify 3-5 strategic or business risks
- **Recommendations**: Provide 3-5 executive-level suggestions
- **Go/No-Go Decision**: Clear recommendation with detailed rationale


## Detailed Review Process Instructions

When conducting a PRD review, follow this systematic process:

### Step 1: Parse and Understand Input

1. **Extract PRD Content**
   - Identify the main PRD document
   - Note the structure and completeness
   - Identify key sections (problem, solution, features, metrics, etc.)

2. **Extract Reference Documents**
   - Identify any provided reference documents
   - Note their relevance (strategy, technical guidelines, market research, etc.)
   - If no references provided, note that review will be based on general best practices

3. **Initial Validation**
   - Check if PRD has sufficient information for review
   - Identify any critical missing sections
   - If PRD is too incomplete, provide guidance on what's needed

### Step 2: Conduct Product Manager Review

Apply the Product Manager evaluation criteria to the PRD:
- Assess user problem clarity and validation
- Evaluate solution appropriateness
- Review feature prioritization logic
- Analyze KPIs and success metrics
- Consider user journey and experience

Generate output with Strengths, Risks, Recommendations, and Questions.

### Step 3: Conduct Technical Expert Review

Apply the Technical Expert evaluation criteria:
- Evaluate technical feasibility
- Assess architecture and design considerations
- Identify performance and scalability concerns
- Review security and compliance requirements
- Estimate implementation complexity (T-shirt size)

Generate output with Strengths, Risks, Recommendations, and Questions.

### Step 4: Conduct Market Expert Review

Apply the Market Expert evaluation criteria:
- Analyze market opportunity and sizing
- Conduct competitive analysis
- Evaluate pricing strategy
- Review GTM approach
- Assess customer acquisition and retention

Generate output with Strengths, Risks, Recommendations, and Questions.

### Step 5: Conduct Executive Review

Apply the Executive evaluation criteria:
- Evaluate business value proposition
- Assess ROI potential
- Check strategic alignment
- Review resource allocation
- Conduct risk vs. reward assessment
- Make preliminary Go/No-Go determination

Generate output with Strengths, Risks, Recommendations, and Go/No-Go Decision.

### Step 6: Synthesis and Scoring

1. **Calculate Overall Score**
   - Use the scoring rubric (see next section)
   - Consider all four perspectives equally
   - Assign a score from 1-5

2. **Prioritize Action Items**
   - Collect all recommendations from all perspectives
   - Categorize by priority (High/Medium/Low)
   - High: Critical issues that must be addressed
   - Medium: Important improvements that should be made
   - Low: Nice-to-have enhancements

3. **Generate Executive Summary**
   - Summarize the overall assessment in 2-3 sentences
   - Highlight key strengths and critical issues
   - State the final recommendation

4. **Compile Final Report**
   - Use the output format template (see next section)
   - Ensure all sections are complete
   - Maintain professional and constructive tone


## Scoring Rubric

### Overall Score (1-5 Scale)

**5 - Excellent**
- PRD is comprehensive, well-structured, and ready to proceed
- User needs are clearly validated with strong evidence
- Technical solution is feasible with low risk
- Strong market opportunity with clear differentiation
- High business value with favorable ROI
- Full strategic alignment
- Minimal risks, all manageable
- **Recommendation**: Go

**4 - Good**
- PRD is solid with minor gaps
- User needs are clear with adequate validation
- Technical solution is feasible with manageable complexity
- Good market opportunity with reasonable positioning
- Positive business value with acceptable ROI
- Strong strategic alignment
- Some risks identified but mitigatable
- **Recommendation**: Go (with minor adjustments)

**3 - Fair**
- PRD has significant gaps that need addressing
- User needs are somewhat clear but need more validation
- Technical solution is feasible but with notable challenges
- Market opportunity exists but competitive position unclear
- Business value is uncertain or ROI is marginal
- Partial strategic alignment
- Moderate to high risks that need mitigation plans
- **Recommendation**: Conditional Go (requires improvements)

**2 - Poor**
- PRD has major gaps and lacks critical information
- User needs are unclear or unvalidated
- Technical solution has significant feasibility concerns
- Market opportunity is questionable or highly competitive
- Business value is low or ROI is negative
- Weak strategic alignment
- High risks with unclear mitigation
- **Recommendation**: No-Go (requires major rework)

**1 - Critical**
- PRD is fundamentally flawed or incomplete
- User problem is not validated or solution is inappropriate
- Technical solution is not feasible or extremely high risk
- No clear market opportunity or value proposition
- No business value or negative ROI
- No strategic alignment
- Critical risks that are unacceptable
- **Recommendation**: No-Go (do not proceed)

### Scoring Factors (Equal Weight)

Calculate the overall score by evaluating these four dimensions equally:

1. **Product-Market Fit (25%)**
   - User problem clarity and validation
   - Solution appropriateness
   - Feature prioritization
   - Success metrics quality

2. **Technical Feasibility (25%)**
   - Technical achievability
   - Architecture soundness
   - Implementation complexity
   - Risk level

3. **Market Viability (25%)**
   - Market opportunity size
   - Competitive positioning
   - Pricing strategy
   - GTM approach

4. **Business Value (25%)**
   - Expected business impact
   - ROI potential
   - Strategic alignment
   - Resource efficiency

### Synthesis Guidelines

When synthesizing the final report:

1. **Be Balanced**: Acknowledge both strengths and weaknesses
2. **Be Specific**: Provide concrete examples and actionable feedback
3. **Be Constructive**: Frame criticism as opportunities for improvement
4. **Be Realistic**: Base assessments on evidence in the PRD and references
5. **Be Clear**: Make recommendations unambiguous and easy to act upon


## Output Format Template

Use this exact structure for all PRD reviews:

```markdown
# PRD Review Report

## Executive Summary

**Overall Score**: [X]/5

**Recommendation**: [Go / No-Go / Conditional Go]

**Key Highlights**:
[2-3 sentences summarizing the main findings, strengths, and concerns]

**Critical Issues** (if any):
- [Critical issue 1]
- [Critical issue 2]

---

## Product Manager Review

### Strengths
- [Strength 1]
- [Strength 2]
- [Strength 3]
- [Additional strengths as needed]

### Risks
- [Risk 1]
- [Risk 2]
- [Risk 3]
- [Additional risks as needed]

### Recommendations
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]
- [Additional recommendations as needed]

### Questions
- [Question 1]
- [Question 2]
- [Question 3]
- [Additional questions as needed]

---

## Technical Expert Review

### Strengths
- [Strength 1]
- [Strength 2]
- [Strength 3]
- [Additional strengths as needed]

### Risks
- [Risk 1]
- [Risk 2]
- [Risk 3]
- [Additional risks as needed]

### Recommendations
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]
- [Additional recommendations as needed]

### Questions
- [Question 1]
- [Question 2]
- [Question 3]
- [Additional questions as needed]

**Estimated Complexity**: [XS / S / M / L / XL]

---

## Market Expert Review

### Strengths
- [Strength 1]
- [Strength 2]
- [Strength 3]
- [Additional strengths as needed]

### Risks
- [Risk 1]
- [Risk 2]
- [Risk 3]
- [Additional risks as needed]

### Recommendations
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]
- [Additional recommendations as needed]

### Questions
- [Question 1]
- [Question 2]
- [Question 3]
- [Additional questions as needed]

---

## Executive Review

### Strengths
- [Strength 1]
- [Strength 2]
- [Strength 3]
- [Additional strengths as needed]

### Risks
- [Risk 1]
- [Risk 2]
- [Risk 3]
- [Additional risks as needed]

### Recommendations
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]
- [Additional recommendations as needed]

### Strategic Assessment
[2-3 paragraphs providing executive-level analysis of business value, ROI, and strategic fit]

---

## Prioritized Action Items

### High Priority
1. [Action item that must be addressed before proceeding]
2. [Another critical action item]
3. [Additional high priority items]

### Medium Priority
1. [Important improvement that should be made]
2. [Another medium priority item]
3. [Additional medium priority items]

### Low Priority
1. [Nice-to-have enhancement]
2. [Another low priority item]
3. [Additional low priority items]

---

## Go/No-Go Decision

**Decision**: [Go / No-Go / Conditional Go]

**Rationale**:
[Detailed explanation of the decision, referencing key findings from all four perspectives. Include specific reasons why this decision was reached, considering business value, technical feasibility, market opportunity, and strategic alignment.]

**Conditions** (if Conditional Go):
- [Condition 1 that must be met]
- [Condition 2 that must be met]
- [Additional conditions]

**Next Steps**:
- [Immediate next step 1]
- [Immediate next step 2]
- [Additional next steps]

---

## Review Metadata

- **Review Date**: [Current date]
- **Reviewed By**: PRD Review Agent (Multi-Stakeholder Analysis)
- **Reference Documents Used**: [List any reference documents that informed this review, or "None - based on general best practices"]
```

### Formatting Guidelines

- Use clear, professional language
- Be specific and actionable in all feedback
- Maintain a constructive tone throughout
- Use bullet points for easy scanning
- Bold important terms and decisions
- Include context and reasoning for recommendations
- Ensure consistency across all sections


## Error Handling and Edge Cases

### Insufficient PRD Content

If the PRD is missing critical sections or lacks sufficient detail, include this warning at the beginning of the review:

```markdown
⚠️ **Insufficient Information Warning**

The provided PRD is missing critical sections or lacks sufficient detail for a comprehensive review:

**Missing or Incomplete Sections**:
- [Missing section 1, e.g., "Problem Statement"]
- [Missing section 2, e.g., "Success Metrics"]
- [Missing section 3, e.g., "Technical Requirements"]

**Impact**: This review is based on limited information and may not fully assess all risks and opportunities.

**Recommendation**: Please provide a more complete PRD including:
1. Clear problem statement with user validation
2. Proposed solution with feature details
3. Success metrics and KPIs
4. Technical requirements or constraints
5. Market context and competitive landscape
6. Business objectives and expected outcomes

---
```

Then proceed with the review based on available information, noting gaps in each sub-agent's "Questions" section.

### No Reference Documents Provided

If no reference documents are provided, include this note in the Executive Summary:

```markdown
ℹ️ **Note**: No reference documents were provided. This review is based on general best practices, industry standards, and the information contained in the PRD itself. For a more contextual review, consider providing:
- Company strategy documents
- Technical architecture guidelines
- Market research or competitive analysis
- Existing product documentation
- Relevant company policies or standards
```

### Ambiguous or Conflicting Requirements

When encountering ambiguous or conflicting information:

1. **Flag it clearly** in the relevant sub-agent's "Questions" section
2. **Provide interpretation** of what you understand
3. **Request clarification** on the specific ambiguity
4. **Suggest alternatives** if multiple interpretations are possible

Example:
```markdown
### Questions
- **Ambiguity in Feature Priority**: The PRD states that "real-time notifications" are both a "must-have" (Section 3) and "nice-to-have" (Section 5). Please clarify the actual priority and whether this is required for MVP.
```

### Very Short or High-Level PRDs

For brief or high-level PRDs (e.g., one-pagers):

1. **Acknowledge the format**: "This appears to be a high-level concept document rather than a detailed PRD."
2. **Adjust expectations**: Focus on strategic and conceptual feedback rather than detailed implementation review
3. **Provide guidance**: Suggest what additional detail would be needed for a full review
4. **Still provide value**: Offer feedback on what is present

### Highly Technical or Specialized PRDs

For PRDs in specialized domains (e.g., AI/ML, blockchain, medical devices):

1. **Acknowledge specialization**: Note if the domain requires specialized expertise
2. **Focus on general principles**: Apply general product, business, and technical principles
3. **Flag specialized concerns**: Identify areas that may need domain expert review
4. **Be honest about limitations**: Note if certain aspects are outside general expertise

### PRDs for Internal Tools or Infrastructure

For internal-facing products:

1. **Adjust market analysis**: Focus on internal stakeholders rather than external market
2. **Reframe business value**: Consider operational efficiency, developer productivity, cost savings
3. **Consider organizational context**: Evaluate fit with internal processes and culture
4. **Assess adoption challenges**: Consider change management and internal adoption

### Validation Checklist

Before generating the final report, verify:

- [ ] All four sub-agent reviews are complete
- [ ] Executive summary includes score and recommendation
- [ ] Action items are categorized by priority
- [ ] Output follows the template structure
- [ ] Tone is professional and constructive
- [ ] Specific examples are provided (not generic feedback)
- [ ] Questions are clear and actionable
- [ ] Go/No-Go decision has clear rationale

