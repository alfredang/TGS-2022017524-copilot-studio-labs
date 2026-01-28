---
prev:
  text: 'Add new topic with trigger and nodes'
  link: '/recruit/07-add-new-topic-with-trigger'
next:
  text: 'Add an agent flow to your Topic for automation'
  link: '/recruit/09-add-an-agent-flow'
---

# 🚨 Mission 08: Enhance user interactions in Topics with Adaptive Cards

## 🕵️‍♂️ CODENAME: `OPERATION INTERFACE UPLIFT`

> **⏱️ Operation Time Window:** `~45 minutes`

🎥 **Watch the Walkthrough**

[![Adaptive cards video thumbnail](./assets/video-thumbnail.jpg)](https://www.youtube.com/watch?v=RhIlzYHPCXo "Watch the walkthrough on YouTube")

## 🎯 Mission Brief

Agents, your mission is to infiltrate the static user experience and replace it with rich, dynamic, and actionable Adaptive Cards. You'll deploy JSON payloads and Power Fx formulas to transform Copilot Studio conversations from basic Q&A into fully interactive engagements.

## 🔎 Objectives

In this mission, you'll learn:

1. Understanding what Adaptive Cards are and how they enhance user interactions
2. Learning to build interactive cards using JSON and Power Fx formulas
3. Exploring the Adaptive Card Designer and its key components
4. Creating rich, interactive forms and data collection experiences
5. Implementing best practices for designing responsive adaptive cards

## 🤔 What is an Adaptive Card?

An **Adaptive Card** is a way to create interactive, visually rich UI elements that can be embedded in apps like Microsoft Teams, Outlook, or agents. It's a structured JSON object that defines:

- What elements appear on the card (text, images, buttons)
- How those elements are arranged
- What actions users can take (submitting forms, opening links)

### Why Adaptive Cards matter in Copilot Studio

1. **Makes conversations interactive** - show buttons, forms, images instead of just text
2. **Look great everywhere** - automatically match the style of the host app
3. **Easy to build with JSON** - define cards using JSON code
4. **Collect and use data** - gather user input and use it in conversation flow
5. **Boost user experience** - clean, clickable, user-friendly interface

## 🎨 Adaptive Card Designer

The **Adaptive Card Designer** is a visual tool that lets you build interactive cards using drag-and-drop elements.

### Key Components

- **Card Elements** - TextBlock, Image, FactSet, Input fields, Actions
- **Card Viewer** - Preview area showing real-time changes
- **Card Structure** - Hierarchy and layout of your card
- **Element Properties** - Customize settings for each element
- **Card Payload Editor** - Raw JSON code behind your card

## 🌵 Common Use Cases

1. **Forms and data collection** - Leave requests, feedback forms, contact info
2. **Displaying dynamic information** - Order summaries, ticket status
3. **Interactive choices** - Product categories, confirmations
4. **Triggering actions** - Submit buttons, view details links

## 🧪 Lab 08 - Add adaptive cards and enhance topic capabilities

### ✨ Use case

**As an** employee
**I want to** request a device
**So that I** can request a device from the list of available devices

### Prerequisites

1. SharePoint Devices list (from Course Setup)
2. Contoso Helpdesk Agent with Available devices topic (from Lab 07)

### 8.1 Create a new topic with an adaptive card

1. Create a new topic named `Request device`
2. Add trigger description:
   ```text
   This topic helps users request a device when they answer yes to requesting one.
   ```

3. Add an **Ask with adaptive card** node
4. Design the card to display available devices and collect user selection

### 8.2 Use Power Fx formula for dynamic content

Switch from JSON to Formula mode and use Power Fx to loop through devices:

```text
ForAll(Global.VarDevices.value, {title: ThisRecord.Model, value: Text(ThisRecord.ID)})
```

### 8.3 Update agent instructions

Add instruction to invoke the Request device topic:
```text
- If the user answers yes to requesting a device, trigger [Request device].
```

### 8.4 Test the flow

1. Enter: `I need a laptop`
2. Answer `Yes` to the device request question
3. Verify the adaptive card displays with device options

## ✅ Mission Complete

Congratulations! 👏🏻 You've learned how to add adaptive cards using Power Fx formulas to display dynamic data and redirect between topics.

⏭️ [Move to **Add an agent flow for automation** lesson](../Lab%209/index.md)

## 📚 Tactical Resources

🔗 [Using Adaptive Cards in Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/guidance/adaptive-cards-overview)
🔗 [Add an adaptive card in Send a message node](https://learn.microsoft.com/microsoft-copilot-studio/authoring-send-message)
🔗 [Create expressions using Power Fx](https://learn.microsoft.com/microsoft-copilot-studio/advanced-power-fx)
