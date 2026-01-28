---
prev:
  text: 'Create a custom agent using natural language with Copilot'
  link: '/recruit/06-create-agent-from-conversation'
next:
  text: 'Enhance user interactions in Topics with Adaptive Cards'
  link: '/recruit/08-add-adaptive-card'
---

# 🚨 Mission 07: Add new topic with trigger and nodes

## 🕵️‍♂️ CODENAME: `OPERATION STAY ON TOPIC`

> **⏱️ Operation Time Window:** `~60 minutes`

🎥 **Watch the Walkthrough**

[![Trigger video thumbnail](./assets/video-thumbnail.jpg)](https://www.youtube.com/watch?v=7iPAZaA8nJs "Watch the walkthrough on YouTube")

## 🎯 Mission Brief

You've built an agent. It listens, learns, and answers questions - but now it's time to get more tactical. In this mission, you'll go deep under the hood and teach your agent how to respond to specific prompts with precision.

With Topics and Triggers, your agent can:

- Recognize intent
- Route conversations with logic
- Gather and store variables
- Trigger flows and take action

You're not just building dialogue, you're wiring up its decision making cortex. Welcome to the Neural Nexus.

## 🔎 Objectives

In this mission, you'll learn:

1. Understanding what topics are and their role in creating structured conversations for your agent
2. Learning the anatomy of topics including trigger phrases and conversation nodes
3. Exploring different types of conversation nodes and how to use Power Fx for dynamic logic
4. Creating custom topics from scratch to handle specific user requests and tasks
5. Building a functional topic that connects to SharePoint data using connectors and tools

## 🤔 What is a Topic?

A topic is a structured conversation that helps your agent respond to specific user questions or tasks. Think of a topic as a mini-conversation or task that your agent can handle. Each topic is designed to respond to a specific user question or request.

### 🌌 Purpose of a topic

There are three common purposes for topics based on what users need:

**Informational** - answers questions such as:
- `What is …?`
- `When will …?`
- `Why …?`

**Task completion** - helps users _do_ something:
- `"I want to …"`
- `"How do I …?"`

**Troubleshooting** - solves problems:
- `Something isn't working …`
- `I'm encountering an error message …`

## 🪺 Types of topics

1. **System topics** - built-in topics that handle common events (starting/ending conversations, errors, escalation)

2. **Custom topics** - topics you create to handle specific tasks or questions

## 🧬 Anatomy of a topic

### 🗣️ Trigger phrases

Words or sentences users might say to start the topic.

### 💬 Conversation nodes

Steps the agent follows once the topic is triggered:

- **Send a message** - sends a message to the user
- **Ask a question** - asks the user a question and waits for their answer
- **Ask with adaptive card** - send a rich, interactive card using JSON
- **Add a condition** - add logic to check something and decide what to do next
- **Variable management** - stores or clears information during the conversation
- **Topic management** - moves the conversation to another topic
- **Add a tool** - connects to connectors, agent flows, prompts
- **Generative answers node** - uses AI to generate natural responses
- **HTTP request node** - connect to external systems via API calls

## 🏋🏻‍♀️ Using Power Fx in your nodes

Power Fx is a low-code programming language used to add logic and dynamic behavior to your agent. It's similar to Excel formulas.

### What Power Fx can do in topics

- Set and manipulate variables: `Set(userName, "Adele Vance")`
- Create conditions: `If(score > 80, "Pass", "Fail")`
- Format and transform data: `Text(DateValue, "dd/mm/yyyy")`

## 🧪 Lab 07 - Add a new topic with conversation nodes

### ✨ Use case

**As an** employee
**I want to** know what devices are available
**So that I** have a list of available devices

### Prerequisites

1. SharePoint list with Devices (from Course Setup)
2. Contoso Helpdesk Agent from Lab 06

### 7.1 Add a new topic from blank

1. Select the **Topics tab** in your agent
2. Select **+ Add a topic** and select **From blank**
3. Name the topic: `Available devices`
4. Enter trigger description:
   ```text
   This topic helps users find devices that are available from our SharePoint Devices list.
   ```

### 7.2 Define the trigger inputs and outputs

1. Open **Topic details** and create input variable `VarDeviceType`
2. Create output variable `VarAvailableDevices` (Table type)

### 7.3 Add a tool using a connector

1. Add a **Get items** SharePoint connector action
2. Configure the connection and select your Devices list
3. Add a filter query using Power Fx:
   ```text
   Concatenate("Status eq 'Available' and AssetType eq '", Topic.VarDeviceType, "'")
   ```

4. Update agent instructions to invoke the topic:
   ```text
   - Help find available devices using [Available devices]. Always extract the VarDeviceType from the inputs.
   ```

5. Test with: `I need a laptop`

## ✅ Mission Complete

Congratulations! 👏🏻 You've learned how to add topics with triggers, use SharePoint connectors, and apply Power Fx filters.

⏭️ [Move to **Enhance user interactions with Adaptive Cards** lesson](../Lab%208/index.md)

## 📚 Tactical Resources

🔗 [Use system topics](https://learn.microsoft.com/microsoft-copilot-studio/authoring-system-topics)
🔗 [Topics in Microsoft Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/guidance/topics-overview)
🔗 [Create expressions using Power Fx](https://learn.microsoft.com/microsoft-copilot-studio/advanced-power-fx)
