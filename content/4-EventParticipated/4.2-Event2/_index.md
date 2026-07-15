---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Summary Report: "AWS Knowledge Quiz Final Round and Technical Presentations on AWS Security Agent & Amazon CloudWatch"

## General Event Information

- **Event Name:** Not yet determined (to be filled in)
- **Time:** To be filled in
- **Location:** To be filled in
- **Role:** Attendee

## Presentations & Key Highlights

### 1. Final Round: AWS Services Knowledge Quiz Competition

**Host:** Mr. Long

**Details:** The session opened with the final round of a quiz competition testing participants' knowledge of AWS services. Contestants who had advanced from earlier rounds competed head-to-head, answering questions covering core AWS concepts, service use cases, and best practices. The competitive format encouraged active engagement from the audience and reinforced practical, applied knowledge of the AWS ecosystem rather than rote memorization, with the host guiding the flow of questions and clarifying key concepts as they came up.

### 2. Introduction and Demo of AWS Security Agent

**Speaker:** Mr. Thinh

**Details:** This presentation introduced AWS Security Agent, an AI-driven security service designed to help teams find and fix vulnerabilities faster than traditional tooling. The speaker explained how the service moves beyond simple pattern-matching static analysis: instead, it reasons about an application's architecture, trust boundaries, and data flows to uncover systemic vulnerabilities that conventional scanners tend to miss.

The demo walked through the core capabilities of the service, including:
- **Full repository code review**, which scans an entire codebase (connected via GitHub, GitLab, or Bitbucket) and produces findings tied to specific files and lines of code, along with calibrated severity and confidence ratings.
- **Automated remediation**, where the agent generates concrete code fixes for identified issues â€” opening pull requests directly for private repositories, or providing a downloadable diff for public repositories so the vulnerability isn't disclosed before it's patched.
- **Threat modeling**, which analyzes design documents or source code to identify threats and recommend mitigations using the STRIDE framework.
- **Penetration testing**, allowing teams to validate findings and generate working exploits on demand from the CLI before deploying to production.
- **IDE and workflow integration**, showing how developers can trigger scans and remediation directly from their development environment via Kiro, a Claude Code plugin, or an open MCP integration â€” without needing to switch context.

The speaker emphasized that the tool is meant to complement, not replace, existing security practices â€” surfacing the obvious and semi-obvious issues so that human security teams can focus their limited time on deeper, design-level judgment calls.

### 3. Overview of Amazon CloudWatch

**Details:** The final presentation introduced Amazon CloudWatch, AWS's monitoring and observability service. The speaker covered how CloudWatch collects metrics, logs, and events from AWS resources and applications, enabling teams to visualize system health on dashboards, set alarms for abnormal behavior, and troubleshoot issues in near real time. Emphasis was placed on how CloudWatch supports both infrastructure-level monitoring (compute, storage, networking) and application-level observability, including tracking Service Level Objectives (SLOs) to help teams define, monitor, and get alerted on reliability goals across distributed systems. The presentation highlighted CloudWatch's role as a foundational tool for maintaining operational visibility and proactively catching problems before they affect end users.

## Key Takeaways and Action Plan

### New Knowledge and Mindset:

- **Applied AWS knowledge through competition:** The quiz format reinforced practical understanding of AWS services in an engaging, memorable way, highlighting areas of AWS knowledge worth reviewing further.
- **AI-driven application security:** Gained a clearer picture of how AI agents like AWS Security Agent can automate vulnerability discovery and remediation at the repository level, going beyond traditional static analysis by reasoning about architecture and data flow.
- **Security workflow integration:** Learned how modern security tooling can be embedded directly into developer workflows (IDE, CLI, CI/CD) to reduce context switching and speed up the fix cycle.
- **Observability fundamentals:** Strengthened understanding of how Amazon CloudWatch supports monitoring, alerting, and reliability tracking (SLOs) across cloud infrastructure and applications.

### Action Plan:

- Review the AWS service areas that came up during the quiz to reinforce and fill gaps in foundational AWS knowledge.
- Explore AWS Security Agent on a personal or sandbox repository to understand its scanning and remediation workflow firsthand.
- Set up a basic Amazon CloudWatch dashboard and alarm for a personal or test project to practice monitoring and alerting concepts.
- Look into how security scanning and observability tools can be integrated into a typical CI/CD pipeline for future projects.

## Event Photos

![Event photo 1](/images/4-event-participated/event2-1.jpg)
![Event photo 2](/images/4-event-participated/event2-2.jpg)
![Event photo 3](/images/4-event-participated/event2-3.jpg)


