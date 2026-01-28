---
prev:
  text: 'Publish your agent'
  link: '/recruit/11-publish-your-agent'
---

# 🚨 Mission 12: Understanding Licensing

## 🕵️‍♂️ CODENAME: `OPERATION KNOW WHAT YOU OWE`

> **⏱️ Operation Time Window:** `~15 minutes – intel only, no fieldwork required`

## 🎯 Mission Brief

Welcome, Recruit. Before you deploy agents into production, you need a clear understanding of how those agents are measured and billed. This mission exists to help prevent licensing surprises after an agent goes live.

## 🔎 Objectives

In this mission, you'll learn:

1. How Copilot Studio licensing works using Copilot Credits
2. How credits are acquired through pay-as-you-go, capacity packs, and prepaid commitments
3. What Microsoft 365 Copilot user licenses include — and where credits are still required
4. How different agent scenarios affect credit consumption
5. How to plan, estimate, and monitor usage

## 🔎 What are Copilot Credits?

Copilot Credits are the **currency used to measure usage** in Copilot Studio.

Credits are consumed whenever an agent:
- Looks up information
- Answers a question
- Runs workflows and actions

Every topic invocation, tool call, grounding operation, and custom skill consumes credits. More complex behavior uses more credits.

## 💳 How Licensing Works

### 1. Pay-As-You-Go (PAYGO)

- No upfront commitment
- **$0.01 per Copilot Credit** via Azure
- Flexible, scalable usage
- Ideal for development or unpredictable workloads

### 2. Copilot Studio License (Capacity Pack)

- Monthly subscription: **25,000 Copilot Credits per pack**
- Credits pooled at tenant level
- Can buy multiple packs
- Unused credits **do not roll over**
- Best for predictable usage

### 3. Copilot Credit Pre-Purchase Plan

- Annual, prepaid option for large volumes
- Credits purchased as **Copilot Credit Commit Units (CCCUs)**
- Each CCCU = **100 Copilot Credits**
- Cost advantage at scale

## 📌 User Licenses

- **Copilot Studio Tenant License** enables Copilot Studio in your tenant
- **Copilot Studio User License** ($0) must be assigned to anyone creating or managing agents

## 🧠 Microsoft 365 Copilot Licenses

Microsoft 365 Copilot licenses include:
- Copilot access in Word, Teams, Outlook, Excel
- Ability to create and interact with agents

### When Copilot Studio Credits Still Apply

Credits are consumed when agents:
- Run agent flows
- Use connectors or external services
- Publish outside of internal M365 experiences
- Execute topics with actions beyond simple responses

**Simple rule:**
- **Internal M365 interaction + basic responses** → Covered by M365 Copilot license
- **Automation, integrations, external publishing** → Consume Copilot Studio credits

## 📊 Capacity Planning Tips

Before launching an agent:

1. **Estimate consumption** using the [Copilot Studio Agent Usage Estimator](https://aka.ms/copilotstudioestimator)
2. **Disable unused tools** to avoid extra costs
3. **Mix capacity packs + pay-as-you-go** to prevent service interruptions
4. **Assign User Licenses** to all builders
5. **Monitor consumption** in Power Platform admin center

## 🧠 Real-World Scenarios

| Scenario | Licensing |
|----------|-----------|
| Internal Teams agent with default knowledge | Covered by user license (basic); actions use credits |
| Agent with Power Automate/connector actions | Uses Copilot Credits |
| Autonomous agents | Uses Copilot Credits |
| Published on external web | Uses Copilot Credits |
| Maker building agents | Requires Copilot Studio User License |

## 🏁 Mission Complete

You now understand:
- How **Copilot Credits** work
- What Microsoft 365 Copilot licenses include and don't
- How to plan with capacity packs, pay-as-you-go, and prepaid plans

With this knowledge, you're ready to manage agent usage cost-effectively as you scale!

## 📚 Tactical Resources

🔗 [Copilot Studio Licensing & Message Rates](https://learn.microsoft.com/microsoft-copilot-studio/billing-licensing)
🔗 [Power Platform Licensing Guide](https://aka.ms/PowerPlatformLicensing)
🔗 [Message Management & Capacity Monitoring](https://learn.microsoft.com/power-platform/admin/manage-copilot-studio-messages-capacity)
