# 🚨 Mission 06: Create a Custom Agent Using Natural Language with Copilot

## 🕵️‍♂️ CODENAME: `OPERATION NATURAL LANGUAGE`

> **⏱️ Operation Time Window:** `~60 minutes`

## 🎯 Mission Brief

Welcome, Agent Maker. This mission teaches you how to build a custom agent in Microsoft Copilot Studio by describing your needs in plain language rather than coding. The focus is on creating an IT helpdesk agent that can access and reference enterprise knowledge sources.

## 🔎 Objectives

In this mission, you'll learn:

1. What custom agents are and how they differ from pre-built agents
2. How to use natural language prompts to define agent behavior
3. Understanding different knowledge source types available in Copilot Studio
4. How to ground your agent with enterprise data from multiple sources
5. Testing and refining your agent's responses with citations

## 🤔 What are Custom Agents?

**Custom Agents** are chatbots you design where "you decide the purpose" and "you ground it with your own data" through supported knowledge resources. Unlike pre-built agents that come with predefined capabilities, custom agents give you full control over:

- The agent's personality and tone
- What knowledge sources it can access
- How it responds to specific queries
- Which tools and actions it can perform

## 📝 Understanding Prompts

A **prompt** is the message or instruction you give to an AI agent to tell it what you want it to do. Effective prompts are:

- **Specific** - Clearly describe what you want
- **User-focused** - Consider how users will interact with the agent
- **Example-rich** - Include examples when possible to guide behavior

## 🔌 Generative Orchestration

**Generative Orchestration** refers to how the agent uses AI to dynamically decide how to answer a question by combining its built-in language skills with information from your added knowledge sources. This enables your agent to:

- Understand user intent even with varied phrasing
- Search multiple knowledge sources simultaneously
- Synthesize information from different sources
- Provide contextual, relevant responses

## 📚 Knowledge Source Types

Copilot Studio supports six categories of knowledge sources:

| Source Type | Description | Best For |
|-------------|-------------|----------|
| **Public websites** | Searched via Bing | General information, documentation sites |
| **Uploaded documents** | Stored in Dataverse | Internal policies, procedures, guides |
| **SharePoint connections** | Direct integration | Enterprise content, team documents |
| **Dataverse tables** | Structured data | Customer records, inventory, tickets |
| **Real-time connectors** | Salesforce, ServiceNow, etc. | Live external system data |
| **Azure AI Search** | Advanced search capabilities | Large document collections |

## 🧪 Lab 06: Create an IT Helpdesk Agent

In this hands-on lab, you'll create an IT helpdesk agent named "Contoso Helpdesk Agent" that:

- Uses natural language prompts to define behavior
- Accesses Microsoft support website content
- References a SharePoint site for internal documentation
- Incorporates an uploaded guidance document
- Provides step-by-step responses with citations

### Prerequisites

- Access to Microsoft Copilot Studio
- SharePoint site with IT documentation (from Course Setup)
- Sample IT guidance documents

### 6.1 Create the Agent Using Natural Language

1. Navigate to [https://copilotstudio.microsoft.com](https://copilotstudio.microsoft.com)

2. Select **+ Create** and choose **New agent**

3. In the conversational creation experience, describe your agent:

    ```text
    I want to create an IT helpdesk agent that helps employees troubleshoot common technical issues. It should be friendly, professional, and provide step-by-step guidance. The agent should be able to answer questions about software, hardware, and network problems.
    ```

4. Follow the prompts to refine your agent's capabilities

5. Name your agent:

    ```text
    Contoso Helpdesk Agent
    ```

### 6.2 Add Knowledge Sources

1. Navigate to the **Knowledge** section of your agent

2. Add a **Public website** knowledge source:
   - URL: `https://support.microsoft.com`
   - This enables the agent to reference Microsoft's official support documentation

3. Add a **SharePoint** knowledge source:
   - Connect to your Contoso IT SharePoint site
   - This gives access to internal documentation

4. Upload a **Document**:
   - Upload your IT guidance document
   - This provides specific organizational policies

### 6.3 Test Your Agent

1. Open the **Test** pane

2. Try various queries:
   - "How do I reset my password?"
   - "My computer is running slowly, what should I do?"
   - "How do I connect to the VPN?"

3. Observe how the agent:
   - Searches multiple knowledge sources
   - Provides citations for its answers
   - Offers step-by-step guidance

## ✅ Mission Complete

Congratulations! 👏🏻 You've created a custom agent using natural language that can access multiple knowledge sources and provide helpful, cited responses to user queries.

⏭️ [Move to **Add new topic with trigger and nodes** lesson](../Lab%207/index.md)

## 📚 Tactical Resources

🔗 [Create agents with natural language](https://learn.microsoft.com/microsoft-copilot-studio/authoring-first-bot)

🔗 [Add knowledge sources](https://learn.microsoft.com/microsoft-copilot-studio/knowledge-add-existing-copilot)

🔗 [Test your agent](https://learn.microsoft.com/microsoft-copilot-studio/authoring-test-bot)
