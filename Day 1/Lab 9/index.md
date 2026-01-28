---
prev:
  text: 'Enhance user interactions in Topics with Adaptive Cards'
  link: '/recruit/08-add-adaptive-card'
next:
  text: 'Add Event Triggers'
  link: '/recruit/10-add-event-triggers'
---

# 🚨 Mission 09: Add an agent flow to your Topic for automation

## 🕵️‍♂️ CODENAME: `OPERATION AUTOMATION POWERHOUSE`

> **⏱️ Operation Time Window:** `~30 minutes`

🎥 **Watch the Walkthrough**

[![Agent flow video thumbnail](./assets/video-thumbnail.jpg)](https://www.youtube.com/watch?v=vtLZJT3eBXg "Watch the walkthrough on YouTube")

## 🎯 Mission Brief

Your agent can now converse with users and provide information, but true operational excellence requires your agent to take action. This mission will transform your conversational agent into an automation powerhouse by equipping it with agent flows.

## 🔎 Objectives

In this mission, you'll learn:

1. Understanding what agent flows are and how they differ from Power Automate cloud flows
2. Learning the key features including AI actions and natural language authoring
3. Exploring the agent flow designer and expressions for dynamic data handling
4. Creating a complete device request automation with SharePoint and email notifications

## 🤔 What is an agent flow?

Agent flows are structured, step-by-step workflows that your agent can execute to automate tasks or connect with other applications. They are **deterministic workflows** - following the same path every time for consistent, reliable results.

### Agent flows vs Power Automate cloud flows

| Agent Flows | Power Automate Cloud Flows |
|-------------|---------------------------|
| Built for conversational agents in Copilot Studio | General-purpose automation |
| Easy to build directly in Copilot Studio | Wide range of connectors |
| No separate license needed | Requires Power Automate license |
| Only visible in Copilot Studio | Can be shared and reused |

## 🔌 Key Features

1. **Natural language authoring** - Describe what you want in plain English
2. **AI actions** - Read documents, summarize content, make recommendations
3. **Generative actions** - Adapt in real time based on changing information
4. **Integration actions** - Connect to 1400+ built-in connectors
5. **Human in the loop** - Add approval steps for review

## 🔤 Understanding Expressions

Expressions are formulas that help your agent flow work with data:

- **Text functions**: `concat()`, `toLower()`, `substring()`, `trim()`
- **Math functions**: `add()`, `sub()`, `mul()`, `div()`
- **Date functions**: `utcNow()`, `addDays()`, `formatDateTime()`
- **Logical functions**: `if()`, `equals()`, `and()`, `or()`

## 🧪 Lab 09 - Add an agent flow for automation

### ✨ Use case

**As a** manager
**I want to** receive device requests
**So that I** can review devices requested by employees

### Prerequisites

1. SharePoint Devices list (from Course Setup)
2. Contoso Helpdesk Agent with Request device topic (from Lab 08)

### 9.1 Create an agent flow

1. In the Request device topic, add a new node
2. Select **Add a tool** → **New Agent flow**

3. Configure the trigger with inputs:
   - `DeviceSharePointId` (Text) - The SharePoint item ID
   - `User` (Text) - The user's name
   - `AdditionalComments` (Text, optional) - User comments

4. Add **Get item** SharePoint action to retrieve device details

5. Add **Send an email (V2)** action to notify the manager

6. Configure the **Respond to agent** action to return the device model

7. **Save** and **Publish** the agent flow

### 9.2 Add agent flow to topic

1. Add the agent flow as a tool in the Request device topic
2. Map the input variables from the adaptive card outputs
3. Add a confirmation message using the returned model value
4. Redirect to End of Conversation topic

### 9.3 Test the complete flow

1. Test with: `I need a laptop`
2. Answer `Yes` to request a device
3. Select a device and optionally add comments
4. Verify the email is received with device details

## ✅ Mission Complete

Congratulations! 👏🏻 You've built an agent flow that retrieves SharePoint data and sends email notifications, creating a complete device request automation.

⏭️ [Move to **Add Event Triggers** lesson](../Lab%2010/index.md)

## 📚 Tactical Resources

🔗 [Agent flows overview](https://learn.microsoft.com/microsoft-copilot-studio/flows-overview)
🔗 [Use agent flows with your agent](https://learn.microsoft.com/microsoft-copilot-studio/advanced-flow)
🔗 [List of functions reference](https://learn.microsoft.com/azure/logic-apps/workflow-definition-language-functions-reference)
