[README.md](https://github.com/user-attachments/files/33150888/README.md)
# Travel Assistant AI

> 🟠 Experimental project — not completed

A conversational AI travel assistant prototype built with BuilderBot.

The project was designed to simulate a travel agency assistant capable of understanding customer requirements, recommending travel packages from a controlled catalog, generating estimated budgets, structuring customer data, and sending the final information to an external automation workflow.

## Project Goal

The intended workflow was:

Customer conversation  
↓  
Requirement collection  
↓  
Controlled catalog lookup  
↓  
Travel recommendation  
↓  
Estimated budget  
↓  
Customer confirmation  
↓  
Structured data  
↓  
HTTP request  
↓  
n8n  
↓  
Google Sheets

The entire project was developed in a controlled test environment using simulated travel packages and data.

## What Was Built

The prototype successfully demonstrated several components of the intended system:

- Conversational travel assistant
- Natural-language requirement extraction
- Interpretation of destination, duration, number of travelers and budget
- Controlled travel package catalog
- Travel recommendations
- Budget calculation based on catalog data
- Structured data model with 11 fields
- Text, Number and Boolean data types
- Structured Output configuration
- Custom variables
- HTTP request configuration
- Variable references
- Separation of responsibilities using different Flows
- BuilderBot Web SDK integration

## Architecture

The conceptual architecture was:

```text
Customer
   ↓
BuilderBot AI Agent
   ↓
Requirement Collection
   ↓
Controlled Travel Catalog
   ↓
Recommendation & Budget
   ↓
Customer Confirmation
   ↓
Structured Output
   ↓
HTTP
   ↓
n8n
   ↓
Google Sheets

What Worked
The conversational part of the system was successfully developed and tested.
The assistant was able to:
1. Understand travel requirements expressed in natural language.
2. Extract relevant information from the conversation.
3. Interpret destination, duration, travelers and budget.
4. Work with a controlled catalog of travel packages.
5. Generate coherent recommendations.
6. Calculate budgets based on catalog information.
7. Work with structured output and typed fields.
8. Integrate the chatbot into a web page using the BuilderBot SDK.
What Was Not Completed
The complete end-to-end automation was not successfully validated.
The critical sequence was:
Customer Confirmation
        ↓
Intent Detection
        ↓
Registration Flow
        ↓
Structured Output
        ↓
HTTP
        ↓
n8n
        ↓
Google Sheets

This sequence remained incomplete.
The final web test also revealed conversational inconsistencies, including difficulties maintaining the correct flow after customer confirmation.
Therefore, the project should not be considered a completed production-ready solution.
Technical Learning
This project introduced several new concepts:
- Conversational AI agents
- Structured Output
- JSON-oriented data structures
- Variables and typed fields
- HTTP integrations
- Flow-based conversational architecture
- Web chatbot integration
- Separation of conversational and technical responsibilities
- End-to-end testing of conversational workflows
One of the most important lessons was understanding the difference between testing an individual component and testing the complete conversational system.
A block may work correctly in isolation while the complete workflow fails because of interactions between:
- prompts
- variables
- intent detection
- Flow transitions
- structured output
- external integrations
Tool Evaluation
BuilderBot
BuilderBot was used as the main conversational platform.
During the project, significant friction was encountered around:
- Flow management
- Triggers
- Variable references
- Flow transitions
- Debugging conversational behavior
Based on the experience of this specific project, the decision was made not to continue developing this solution with BuilderBot.
This is an implementation-specific evaluation and not a general assessment of BuilderBot.
Key Professional Lesson
A tool should not be evaluated only by the features it provides on paper. It should also be evaluated by how clearly and reliably it allows a solution to be built, tested, debugged and maintained.

The project also highlighted the importance of validating critical architecture before investing significant development time.
The critical mechanism in this project was:
AI Agent
   ↓
Customer Confirmation
   ↓
Flow Transition
   ↓
Technical Execution

This mechanism should have been validated as a small Proof of Concept before building the rest of the assistant.
Reusable Development Pattern
The main process learned from this project is:
Business Problem
       ↓
Proposed Architecture
       ↓
Identify Critical Components
       ↓
Minimal PoC
       ↓
Validate
       ↓
Build

If the PoC fails, the architecture or tool should be reconsidered before expanding the solution.
Project Status
🟠 Experimental / Not Completed
The project did not achieve the complete functional objective, but it provided valuable practical experience in conversational AI, structured data, integrations, workflow architecture and tool evaluation.
The prototype has been intentionally preserved as a learning artifact.
Project Context
This is the third project in my practical AI learning portfolio.
The project represents a progression from:
Project 01 — Business impact analysis
to:
Project 02 — AI-powered workflow automation
to:
Project 03 — Conversational AI + structured data + external integrations
The main outcome of this project was not only technical implementation, but learning when to validate, redesign or abandon a technical approach.
