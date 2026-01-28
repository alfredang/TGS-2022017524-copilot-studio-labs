---
prev:
  text: 'Add an agent flow to your Topic for automation'
  link: '/recruit/09-add-an-agent-flow'
next:
  text: 'Publish your agent'
  link: '/recruit/11-publish-your-agent'
---

# 🚨 Mission 10: Add Event Triggers - Enable autonomous agent capabilities

## 🕵️‍♂️ CODENAME: `OPERATION GHOST ROUTINE`

> **⏱️ Operation Time Window:** `~45 minutes`

🎥 **Watch the Walkthrough**

[![Event triggers video thumbnail](./assets/video-thumbnail.jpg)](https://www.youtube.com/watch?v=ZgwHL8PQ1nY "Watch the walkthrough on YouTube")

## 🎯 Mission Brief

It's time to elevate your agent from conversational assistant to autonomous operative. Your mission is to enable your agent to act without being summoned - responding to signals from across your digital domain with precision and speed.

With Event Triggers, you'll train your agent to monitor external systems and execute intelligent actions the moment a signal is received.

## 🔎 Objectives

In this mission, you'll learn:

1. Understanding Event Triggers and how they enable autonomous behavior
2. Learning the difference between event triggers and topic triggers
3. Exploring common Event Trigger scenarios
4. Understanding authentication and security considerations
5. Building an autonomous agent that responds to SharePoint events

## 🤔 What is an Event Trigger?

An **Event Trigger** allows your agent to act autonomously in response to external events, without requiring direct user input. Examples include:

- When a new file is created in SharePoint
- When a record is created in Dataverse
- When a task is completed in Planner
- When a new Form response is submitted
- Based on a recurring schedule

### Event vs Topic Triggers

| Event Triggers | Topic Triggers |
|----------------|----------------|
| Activated by external system events | Activated by user input/phrases |
| Enable autonomous agent behavior | Enable conversational responses |
| Use maker's authentication | Option for user's authentication |
| Run without user interaction | Require user to start conversation |

## 📦 Understanding Trigger Payloads

When an event occurs, the trigger sends a **payload** containing:

- **Default payload** - Basic event information
- **Custom payload** - Specific instructions and data formatting

## 🎯 Common Event Trigger Scenarios

| Scenario | Trigger | Action |
|----------|---------|--------|
| IT Help Desk | New SharePoint item | Categorize, assign priority, notify team |
| Employee Onboarding | New Dataverse user | Send welcome, create tasks, provision access |
| Project Management | Task completed in Planner | Update dashboard, notify stakeholders |
| Document Management | File uploaded to SharePoint | Extract metadata, apply tags |

## 🧪 Lab 10 - Add Event Triggers for autonomous behavior

### 🎯 Use case

Enhance your IT Help Desk agent to automatically respond to new support requests in SharePoint.

### Prerequisites

- Completed previous labs (especially Lab 6-8)
- SharePoint site with IT support tickets list
- Generative orchestration enabled on your agent

### 10.1 Enable Generative AI and create trigger

1. Open your IT Help Desk agent
2. Enable **Generative orchestration** in Settings
3. Navigate to **Triggers** section and click **+ Add trigger**
4. Select **When an item is created** (SharePoint)
5. Configure:
   - **Trigger name**: New Support Ticket Created in SharePoint
   - **Site Address**: Your Contoso IT site
   - **List Name**: Tickets list
   - **Instructions**:
     ```text
     New Support Ticket Created: {Body}
     Use the 'Acknowledge SharePoint Ticket' tool to respond.
     IMPORTANT: Work completely autonomously.
     ```

### 10.2 Edit the Trigger in Power Automate

1. Select **Edit in Power Automate**
2. Update the Body/message with an expression containing ticket details:
   ```text
   concat('Submitted By: ', triggerOutputs()?['body/Author/DisplayName'],
          '\nTitle: ', triggerOutputs()?['body/Title'],
          '\nDescription: ', triggerOutputs()?['body/Description'])
   ```
3. **Publish** the flow

### 10.3 Create email acknowledgment tool

1. Navigate to **Tools** tab
2. Add **Send an email (V2)** connector
3. Configure:
   - **Name**: Acknowledge SharePoint ticket
   - **Description**: Sends email acknowledgement that ticket was received

### 10.4 Test the trigger

1. Click **Test Trigger** in the Overview tab
2. Create a new item in your SharePoint Tickets list
3. Monitor the test panel for trigger activation
4. Verify the acknowledgment email is sent

## ✅ Mission Complete

🎉 Congratulations! You've implemented event triggers that enable your agent to operate autonomously, automatically processing support tickets without user intervention.

⏭️ [Move to **Publish your agent** lesson](../Lab%2011/index.md)

## 📚 Tactical Resources

🔗 [Make your agent autonomous](https://learn.microsoft.com/training/modules/autonomous-agents-online-workshop/)
🔗 [Add an event trigger](https://learn.microsoft.com/microsoft-copilot-studio/authoring-trigger-event)
🔗 [Power Automate triggers introduction](https://learn.microsoft.com/power-automate/triggers-introduction)
