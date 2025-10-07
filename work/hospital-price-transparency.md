---
title: Regulatory Burden to User-Centered Solution
description: I prototyped and delivered simple open source prototypes that are estimat
date: 2024-03-01
tags:
  - Public Website
layout: layouts/post.njk
logo: ../img/logo/dsac-stacked.jpg
templateClass: layout-post layout-post-portfolio

url: https://www.mathiasrechtzigel.com/work/988-suicide-and-crisis-lifeline
---
## The Challenge: When Good Policy Meets Implementation Reality

In 2021, every hospital in America was required to publish pricing information online under the Hospital Price Transparency law. The goal was simple: help patients understand healthcare costs before receiving care. The execution? Far from simple.

**The regulation was confusing**: Small hospitals were paying consultants thousands of dollars for compliance guidance that was often incorrect. Rural facilities using basic website builders like Squarespace couldn't display thousands of services effectively. Even large health systems struggled with conflicting regulatory interpretations.

Through user research with hospital administrators, billing specialists, and third-party vendors, we identified three critical barriers preventing compliance:

* **Data confusion**: The law required "machine-readable" files but provided no technical specification or validation method
* **Technical constraints**: Hospitals needed to display complex pricing data through simple website builders not designed for this purpose  
* **Validation anxiety**: No reliable way to verify compliance before potential enforcement actions

## Research & Discovery: Understanding the Ecosystem

I conducted extensive research across the healthcare compliance ecosystem and narrowed in on three personas to do further deep dive user research:

* **Hospital administrators** revealed they wanted to comply but felt abandoned by unclear guidance. Many had purchased expensive consulting services that delivered non-compliant files.
* **Billing specialists** showed me the complexity of healthcare pricing data - thousands of line items with nuanced coding requirements that didn't translate well to web formats.
* **Third-party vendors** admitted they were "figuring it out as they went" - charging hospitals for experimental solutions without validation capabilities.

**Key insight**: This wasn't just a compliance problem - it was a market failure where information asymmetry was preventing good actors from succeeding.

## Strategic Approach: Building Public Infrastructure

Rather than creating another consulting service inside of the government, I designed a comprehensive solution strategy:

### Phase 1: Eliminate Validation Uncertainty
Our team built an open-source validator that hospitals could use to instantly verify file compliance. Modeled after familiar developer tools (WebAIM, HTML5 validators, Lighthouse) to leverage existing mental models.

### Phase 2: Address Technical Constraints  
WE Created flexible metadata standards allowing hospitals to work within their existing technical infrastructure rather than requiring expensive platform changes.

### Phase 3: Scale Through Automation
Developed automated monitoring that could provide "friendly nudges" to hospitals when files became non-compliant, replacing punitive enforcement with supportive guidance.

## Design Process: Simplicity in Complexity

**Initial wireframing** focused on reducing the validation process to its essential components: upload, analyze, report. No account creation, no complex workflows.

**Usability testing** with hospital staff revealed they needed immediate, actionable feedback. The prototype evolved from technical error codes to plain-language explanations with specific remediation steps.

**Information architecture** prioritized clarity over completeness - showing critical compliance issues first, with detailed technical information available on demand.

<img src="/img/hpt/hpt-upload.png" alt="Hospital Price Transparency, Upload"/>
<img src="/img//hpt/hpt-results.png" alt="Hospital Price Transparency, Results"/>

## Technical Innovation: Open Source as Public Good

The validator became part of CMS's Open Source Program Office, demonstrating how government technology could serve as public infrastructure rather than proprietary tools.

**Technical architecture** handled multiple file formats (CSV, JSON, XML) while maintaining consistent validation logic across different data structures.

**API design** allowed integration with existing hospital systems and third-party tools, creating an ecosystem rather than a standalone solution.

**Performance optimization** ensured even large health systems could validate extensive pricing files in under 30 seconds.

## Impact: Transforming a broken ecosystem

### Quantified Outcomes
- **900,000+ hours saved annually** across U.S. hospitals
- **$millions in consulting fees** eliminated for rural hospitals
- **15 minutes** to validate instead of a month.

### Strategic Outcomes
- **Market correction**: Eliminated information asymmetry that allowed poor consulting services to charge premium prices
- **Policy success**: Enabled the Hospital Price Transparency law to achieve its intended outcomes
- **Technical precedent**: Established open-source validation as a model for future healthcare regulations

### User Outcomes
- Small rural hospitals gained the same validation capabilities as large health systems
- Billing specialists could verify third-party contractor work independently
- Hospital administrators gained confidence in their compliance status


## Lessons Learned: Product Strategy in Regulated Markets

**User research is critical in B2B government**: The stakeholders using compliance tools aren't the same as those making purchasing decisions. Understanding both audiences was essential.

**Technical simplicity enables policy success**: Complex regulations require simple implementation tools. The validator's drag-and-drop interface made compliance accessible to non-technical users.

**Open source creates trust**: In healthcare, transparency in validation logic was as important as the validation itself. Hospitals needed to understand and trust the compliance criteria.

**Automation scales impact**: Moving from reactive consultation to proactive monitoring allowed the solution to serve thousands of hospitals without proportional staffing increases.

## Looking Forward: Scaling Public Technology

This project demonstrated how government can build technology infrastructure that serves markets rather than competes with them. The validator model has since been applied to other CMS regulations, showing the broader strategic value of user-centered compliance tools.

The success metrics continue to compound as more hospitals adopt the tools and the healthcare price transparency ecosystem matures around reliable, accessible validation standards.

## More in the news

* [CMS releases tool to validate price transparency file compliance (American Hospital Association)](https://www.aha.org/news/headline/2024-03-28-cms-releases-tool-validate-price-transparency-file-compliance)
* [CMS releases tool to help hospitals with price transparency (Tech Target)](https://www.techtarget.com/revcyclemanagement/news/366600178/CMS-releases-tool-to-help-hospitals-with-price-transparency)
