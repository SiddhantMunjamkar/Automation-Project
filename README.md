# AI Automation Suite

A collection of intelligent automation workflows powered by n8n, integrated with AI agents to streamline user interactions and daily operations. This project demonstrates real-world applications of AI-powered agents processing natural language instructions.

## Overview

This automation suite provides enterprise-level workflow automation combining n8n's robust orchestration capabilities with modern AI agent frameworks. It enables users to automate complex business processes through natural language interfaces.

## Project Structure

```
AI Automation Suite/
├── AI Agent Workflows/
│   ├── 1.AI Agent Chatbot + Long Term Memory + Note Storage + Telegram.json
│   ├── 5.DeepSeek AI Agent + Telegram + Long Term Memory.json
│   └── AI_Deep_Research_agent.json
├── Content & Social Media/
│   ├── 2.Automated Social Media Content Publishing Factory + System Prompt Composition.json
│   ├── 6.Vision-Based AI Agent Scraper - Google Sheets, ScrapingBee, Gemini.json
│   ├── ai-video-factory.json
│   └── creatomate-source-editor.json
├── Lead Generation & Sales/
│   ├── 3.LinkedIn Leads Scraping & Enrichment (Main).json
│   ├── ai-b2b-email-outreach.json
│   ├── ai-recruiter-email-outreach.json
│   ├── Real Estate - Lead Qualification Workflow.json
│   └── Deepseek_R1_auto_Email_Agent.json
├── Data & Research/
│   ├── 14.Structured Data Extract, Data Mining with Bright Data & Google Gemini.json
│   ├── 7.Perplexity_Researcher.json
│   ├── AI Powered Property Recommendations.json
│   ├── bulk_property_research_by_zip_code_workflow.json
│   └── property_image_analysis_and_investment_scoring_workflow.json
├── HR & Recruitment/
│   └── 10.CV Resume Automated Screening, Sorting, Rating and Tracker System.json
├── Blockchain & Alerts/
│   └── 12.Blockchain Alert AI Powered Reporting + Gmail + Telegram.json
├── Analytics & Reporting/
│   └── 4.Google Analytics Data Report with AI sent to Email and Telegram.json
├── Chat & Communication/
│   ├── whats_app_bot.json
│   ├── whatsapp-chatbot-memory-n8n-supabase.json
│   ├── whatsapp-n8n-ai-features.json
│   └── whatsapp-n8n-basic-integration.json
├── Utilities/
│   ├── PromptAgent_Tool.json
│   ├── Calender_scheduling.json
│   ├── Make-Daily-Job-Collector.json
│   ├── BrowserAgentWorkflow.json
│   ├── mcp-n8n-local-setup-tavli-ai-workflow.json
│   └── n8n-intro-workflow-template.json
└── README.md
```

## Features

- **Natural Language Processing**: AI-powered interpretation of user instructions
- **Multi-Agent Architecture**: Support for dynamic agent instantiation and management
- **Comprehensive Integration**: Telegram, WhatsApp, Email, Google Calendar, LinkedIn, and more
- **Data Mining & Enrichment**: Web scraping, data extraction, and lead enrichment
- **Memory Management**: Long-term conversation memory and knowledge storage
- **Content Generation**: AI-powered content creation and publishing
- **Extensible Framework**: Built on n8n for easy workflow customization
- **LLM Agnostic**: Compatible with OpenAI, DeepSeek, Gemini, and other AI frameworks

## Components

### 1. AI Prompt Generator for AI Agents

#### Description

This automation enables generation of context-rich prompts for AI agents based on user instructions. It dynamically constructs well-formed system prompts that define agent behavior and capabilities.

#### Features

- Accepts natural language instructions and converts them to structured system messages
- Ready for use with OpenAI and LangChain agent frameworks
- Built on n8n's Webhook → OpenAI → Response architecture
- Supports dynamic agent instantiation in multi-agent frameworks

#### Use Cases

- Dynamic agent spawning in LangGraph, CrewAI, and Agent-LLM frameworks
- Purpose-specific AI agent behavior configuration
- System prompt composition at runtime

#### Example Input

```
"You are a software engineer that helps with Go, TypeScript, and Rust."
```

#### Example Output

```json
{
  "role": "system",
  "content": "You are an assistant developed by Siddhant Munjamkar. You are helpful, creative, and expert in Go, TypeScript, and Rust. Respond concisely and solve code-related problems efficiently."
}
```

### 2. AI Calendar Scheduler

#### Description

Implements CRUD operations for calendar events through natural language instructions interpreted by AI agents. Users can manage their schedules using plain English without technical commands.

#### Capabilities

- Create new calendar events
- Read and retrieve event details
- Update existing calendar events
- Delete calendar events

#### Supported Platforms

- Google Calendar API
- Notion API (optional)

#### Example Instructions

- "Schedule a project review call with Meera on Tuesday at 11 AM"
- "Delete the standup on Friday"
- "Reschedule the marketing sync to 4 PM tomorrow"

#### Workflow Architecture

1. **Webhook Trigger** - Receives user input via API or form
2. **AI Processing** - OpenAI node interprets user intent and extracts:
   - Action type (create/update/delete/fetch)
   - Event title
   - Date and time details
3. **Routing Logic** - Switch node routes to appropriate CRUD operation
4. **Calendar Integration** - Executes operations on target calendar service
5. **Response** - Sends confirmation or error feedback to user

#### Example Parsed Output

```json
{
  "intent": "create",
  "title": "project review call",
  "date": "2025-07-04",
  "time": "11:00",
  "platform": "Google Calendar"
}
```

## Workflow Catalog

### AI Agent Workflows

#### AI Agent Chatbot + Long Term Memory + Note Storage + Telegram
**File:** `1.AI Agent Chatbot + LONG TERM Memory + Note Storage + Telegram.json`

A sophisticated conversational AI agent with persistent memory capabilities.

**Features:**
- Chat trigger integration with Telegram
- Long-term memory retrieval from Google Docs
- Note storage and management
- Context-aware responses based on historical interactions
- Message routing to Telegram for real-time notifications

**Use Cases:**
- Interactive customer support chatbot
- Personal AI assistant with memory
- Knowledge retention and retrieval
- Multi-channel conversation management

**Integrations:** Telegram, Google Docs, LLM (OpenAI/DeepSeek), Chat Memory

---

#### DeepSeek AI Agent + Telegram + Long Term Memory
**File:** `5.DeepSeek AI Agent + Telegram + LONG TERM Memory.json`

Advanced AI agent leveraging DeepSeek models with Telegram integration.

**Features:**
- DeepSeek LLM integration for advanced reasoning
- Telegram chat interface
- Persistent long-term memory storage
- Automatic memory updates and retrieval
- Real-time message responses

**Use Cases:**
- Advanced research and reasoning tasks
- Multi-turn complex problem solving
- Telegram-based intelligent assistance
- Memory-augmented AI responses

**Integrations:** Telegram, DeepSeek AI, Chat Memory Storage

---

#### AI Deep Research Agent
**File:** `AI_Deep_Research_agent.json`

Specialized agent for conducting comprehensive research across multiple sources.

**Features:**
- Multi-source information gathering
- Deep analysis and synthesis
- Research report generation
- Source citation and verification
- Knowledge compilation

**Use Cases:**
- Market research automation
- Competitive analysis
- Technical research compilation
- Data-driven decision support

**Integrations:** Web APIs, Research Sources, LLM, Data Storage

---

### Content & Social Media Workflows

#### Automated Social Media Content Publishing Factory
**File:** `2.Automated Social Media Content Publishing Factory + System Prompt Composition.json`

End-to-end content generation and publishing automation.

**Features:**
- AI-powered content creation with system prompt composition
- Multi-platform scheduling
- Dynamic content adaptation for different channels
- Chat-based content input
- Publishing workflow automation

**Use Cases:**
- Social media content calendar automation
- Multi-channel content distribution
- Brand voice consistency
- Content scheduling at scale

**Integrations:** Social Media Platforms, OpenAI/LLM, Content Calendar, Chat Interface

---

#### Vision-Based AI Agent Scraper
**File:** `6.Vision-Based AI Agent Scraper - with Google Sheets, ScrapingBee, and Gemini.json`

Advanced web scraping with visual content analysis.

**Features:**
- Screenshot and image analysis using Gemini
- Web scraping with ScrapingBee integration
- Google Sheets data export
- Visual data extraction
- Automated data enrichment

**Use Cases:**
- Visual content aggregation
- E-commerce product data extraction
- Real estate property analysis
- Visual market monitoring

**Integrations:** ScrapingBee, Google Gemini Vision API, Google Sheets

---

#### AI Video Factory
**File:** `ai-video-factory.json`

Automated video content generation and processing.

**Features:**
- AI-powered video script generation
- Automated video creation
- Video optimization and formatting
- Multi-format export
- Content scheduling

**Use Cases:**
- Social media video automation
- Marketing video production
- Educational content creation
- Multi-platform video distribution

**Integrations:** Video Generation APIs, AI Content Tools, Storage Services

---

#### Creatomate Source Editor
**File:** `creatomate-source-editor.json`

Design and multimedia content editing workflow.

**Features:**
- Template-based content creation
- Visual design automation
- Batch content generation
- Multi-format export
- Design asset management

**Use Cases:**
- Marketing collateral generation
- Social media graphics automation
- Design template management
- Batch creative production

**Integrations:** Creatomate API, Design Assets, Cloud Storage

---

### Lead Generation & Sales Workflows

#### LinkedIn Leads Scraping & Enrichment
**File:** `3.LinkedIn Leads Scraping & Enrichment (Main).json`

Comprehensive LinkedIn lead generation and enrichment system.

**Features:**
- LinkedIn profile scraping
- Lead data enrichment
- Job title and location filtering
- Lead quality scoring
- Data validation and deduplication

**Use Cases:**
- B2B sales prospecting
- Recruitment lead sourcing
- Market analysis
- Competitive intelligence gathering

**Integrations:** LinkedIn API, Data Enrichment Services, CRM Systems

---

#### AI B2B Email Outreach
**File:** `ai-b2b-email-outreach.json`

Intelligent B2B cold email campaign automation.

**Features:**
- AI-generated personalized email content
- Lead list processing
- Email sequence automation
- Response tracking
- Campaign performance analytics

**Use Cases:**
- B2B sales prospecting
- Partnership outreach
- Enterprise sales campaigns
- Lead nurturing automation

**Integrations:** Email Services, LLM (Content Generation), CRM, Analytics

---

#### AI Recruiter Email Outreach
**File:** `ai-recruiter-email-outreach.json`

Automated recruitment outreach and candidate engagement.

**Features:**
- AI-generated recruitment emails
- Candidate database integration
- Application tracking
- Interview scheduling
- Engagement analytics

**Use Cases:**
- Talent acquisition automation
- Recruitment marketing
- Candidate pipeline management
- Hiring process acceleration

**Integrations:** Email Services, ATS (Applicant Tracking), LLM, Calendar APIs

---

#### Real Estate Lead Qualification Workflow
**File:** `Real Estate - Lead Qualification Workflow.json`

Automated real estate lead qualification and scoring.

**Features:**
- Lead data collection
- Qualification scoring
- Property matching
- Buyer intent analysis
- Follow-up automation

**Use Cases:**
- Real estate lead qualification
- Property recommendations
- Sales pipeline management
- Automated lead nurturing

**Integrations:** CRM, Property Databases, Email Services, LLM

---

#### DeepSeek R1 Auto Email Agent
**File:** `Deepseek_R1_auto_Email_Agent.json`

Advanced reasoning-based email automation agent.

**Features:**
- DeepSeek R1 reasoning model integration
- Intelligent email composition
- Context-aware responses
- Complex decision making
- Email automation workflows

**Use Cases:**
- Complex customer inquiries
- Advanced sales responses
- Technical support automation
- Strategic business communications

**Integrations:** DeepSeek API, Email Services, Knowledge Base

---

### Data & Research Workflows

#### Structured Data Extract & Data Mining with Bright Data & Gemini
**File:** `14.Structured Data Extract, Data Mining with Bright Data & Google Gemini.json`

Enterprise-grade data extraction and mining solution.

**Features:**
- Web data extraction with Bright Data
- Structured data parsing
- AI-powered data classification using Gemini
- Large-scale data mining
- Data validation and cleaning

**Use Cases:**
- E-commerce product data extraction
- Market research data collection
- Competitive pricing analysis
- Content aggregation at scale

**Integrations:** Bright Data, Google Gemini API, Data Storage, Analytics

---

#### Perplexity Researcher
**File:** `7.Perplexity_Researcher.json`

AI-powered research automation leveraging Perplexity API.

**Features:**
- Perplexity search integration
- Research query automation
- Multi-source information synthesis
- Report generation
- Citation management

**Use Cases:**
- Automated research reports
- Market analysis
- Competitive intelligence
- Industry trend analysis

**Integrations:** Perplexity API, LLM, Document Storage

---

#### AI Powered Property Recommendations
**File:** `AI Powered Property Recommendations.json`

Intelligent real estate property recommendation engine.

**Features:**
- Property data analysis
- User preference matching
- Recommendation scoring
- Market analysis integration
- Investment potential assessment

**Use Cases:**
- Real estate recommendations
- Investment property identification
- Client property matching
- Portfolio analysis

**Integrations:** Property Databases, LLM, CRM, Analytics

---

#### Bulk Property Research by Zip Code
**File:** `bulk_property_research_by_zip_code_workflow.json`

Scalable property research automation by geographic region.

**Features:**
- Batch zip code processing
- Property data aggregation
- Market analysis by region
- Bulk data export
- Comparative analysis

**Use Cases:**
- Real estate market analysis
- Investment opportunity identification
- Geographic property analysis
- Bulk data research

**Integrations:** Property APIs, Data Aggregation, Spreadsheets, Analytics

---

#### Property Image Analysis and Investment Scoring
**File:** `property_image_analysis_and_investment_scoring_workflow.json`

Visual analysis for property valuation and investment scoring.

**Features:**
- Property image analysis using vision AI
- Investment scoring algorithms
- Property condition assessment
- Market valuation estimates
- ROI predictions

**Use Cases:**
- Automated property appraisal
- Investment property screening
- Portfolio analysis
- Real estate due diligence

**Integrations:** Vision APIs (Gemini), Property Data APIs, Valuation Models, Analytics

---

### HR & Recruitment Workflows

#### CV/Resume Automated Screening, Sorting, Rating and Tracker System
**File:** `10.CV Resume Automated Screening, Sorting, Rating and Tracker System.json`

Comprehensive recruitment automation with AI-powered resume evaluation.

**Features:**
- Resume parsing and extraction
- Skill matching and analysis
- Candidate scoring and ranking
- Applicant tracking
- Bulk processing capabilities
- Report generation

**Use Cases:**
- Large-scale recruitment campaigns
- Resume screening automation
- Candidate ranking and shortlisting
- Hiring process optimization
- Compliance tracking

**Integrations:** Resume Parser, ATS, LLM (Analysis), Data Storage, Email

---

### Blockchain & Alerts Workflows

#### Blockchain Alert - AI Powered Reporting + Gmail + Telegram
**File:** `12.Blockchain_alert_AI_Powered_Reporting_+_Gmail_+_Telegram.json`

Real-time blockchain monitoring and alert system.

**Features:**
- Blockchain event monitoring
- AI-powered alert analysis
- Multi-channel notifications (Gmail, Telegram)
- Customizable alert rules
- Report generation

**Use Cases:**
- Smart contract monitoring
- Cryptocurrency transaction alerts
- DeFi risk monitoring
- Compliance tracking

**Integrations:** Blockchain APIs, Gmail, Telegram, LLM Analysis

---

### Analytics & Reporting Workflows

#### Google Analytics Data Report with AI
**File:** `4.Create a Google Analytics Data Report with AI and sent it to E-Mail and Telegram.json`

Automated analytics reporting with AI insights.

**Features:**
- Google Analytics data extraction
- AI-powered data analysis and insights
- Automated report generation
- Multi-channel delivery (Email, Telegram)
- Trend analysis and recommendations

**Use Cases:**
- Automated website analytics reporting
- Performance monitoring
- Stakeholder communication
- Data-driven insights generation

**Integrations:** Google Analytics, Gmail, Telegram, LLM (Analysis)

---

### Chat & Communication Workflows

#### WhatsApp Bot
**File:** `whats_app_bot.json`

Basic WhatsApp chatbot implementation.

**Features:**
- WhatsApp message triggering
- Automated responses
- Message routing
- Basic conversation flow

**Use Cases:**
- Customer service automation
- Information dissemination
- Lead qualification
- Support ticketing

**Integrations:** WhatsApp Business API, Message Queue

---

#### WhatsApp Chatbot + Memory + n8n + Supabase
**File:** `whatsapp-chatbot-memory-n8n-supabase.json`

Advanced WhatsApp chatbot with persistent conversation memory.

**Features:**
- WhatsApp message integration
- Supabase data persistence
- Conversation history management
- Context-aware responses
- User profiling

**Use Cases:**
- Conversational customer support
- Personalized bot experiences
- Lead nurturing via WhatsApp
- Community engagement

**Integrations:** WhatsApp API, Supabase, LLM, n8n

---

#### WhatsApp n8n AI Features
**File:** `whatsapp-n8n-ai-features.json`

WhatsApp integration with advanced AI capabilities.

**Features:**
- Natural language understanding
- Intelligent response generation
- Context awareness
- Multi-turn conversations
- Sentiment analysis

**Use Cases:**
- AI-powered customer support
- Intelligent lead qualification
- Contextual recommendations
- Advanced automation

**Integrations:** WhatsApp API, LLM, NLP Services

---

#### WhatsApp n8n Basic Integration
**File:** `whatsapp-n8n-basic-integration.json`

Foundational WhatsApp-n8n integration template.

**Features:**
- Message sending and receiving
- Webhook setup
- Basic routing
- Template responses
- Error handling

**Use Cases:**
- WhatsApp workflow foundation
- Message automation setup
- Integration starting point
- Basic notification system

**Integrations:** WhatsApp Business API, n8n Webhooks

---

### Utility Workflows

#### Prompt Agent Tool
**File:** `PromptAgent_Tool.json`

System prompt generation for dynamic agent creation.

**Features:**
- Instruction-to-prompt conversion
- Agent behavior definition
- Multi-framework compatibility
- Runtime prompt customization
- Template-based generation

**Use Cases:**
- Dynamic agent spawning
- Multi-agent system management
- Agent behavior customization
- Prompt engineering automation

**Integrations:** LLM APIs, Agent Frameworks

---

#### Make Daily Job Collector
**File:** `Make-Daily-Job-Collector.json`

Daily job aggregation and notification automation.

**Features:**
- Job posting aggregation
- Daily collection and filtering
- Notification delivery
- Source management
- Scheduling

**Use Cases:**
- Job market monitoring
- Recruitment lead generation
- Job notification distribution
- Daily briefings

**Integrations:** Job APIs, Email/Telegram, Scheduler

---

#### Browser Agent Workflow
**File:** `BrowserAgentWorkflow.json`

Automated browser-based task execution.

**Features:**
- Web automation
- Form submission
- Data extraction
- Click automation
- Screenshot capture

**Use Cases:**
- Web scraping
- Automated form filling
- Website monitoring
- Browser task automation

**Integrations:** Browser Automation APIs, Puppeteer, Web Services

---

#### MCP n8n Local Setup - Tavli AI Workflow
**File:** `mcp-n8n-local-setup-tavli-ai-workflow.json`

Local development setup for Model Context Protocol with n8n.

**Features:**
- Local MCP server configuration
- Tavli AI integration
- Development environment setup
- Testing workflows
- Debug capabilities

**Use Cases:**
- Local AI agent development
- Model experimentation
- Workflow testing
- Development setup

**Integrations:** MCP Protocol, Tavli AI, Local Development

---

#### n8n Intro Workflow Template
**File:** `n8n-intro-workflow-template.json`

Introductory template for n8n workflow creation.

**Features:**
- Basic workflow structure
- Common node patterns
- Documentation
- Example configurations
- Best practices

**Use Cases:**
- Learning n8n
- Workflow template starting point
- Onboarding new team members
- Architecture reference

**Integrations:** n8n Core, Basic Node Types

---

## Getting Started

### Prerequisites

- n8n instance (self-hosted or n8n cloud)
- API credentials for integrated services:
  - OpenAI or DeepSeek API key
  - Google APIs (Analytics, Sheets, Calendar)
  - LinkedIn API access (for scraping workflows)
  - Telegram bot token (for bot workflows)
  - WhatsApp Business API (for WhatsApp workflows)
  - Email service credentials (Gmail, SendGrid)
  - Database access (Supabase for chat memory workflows)

### Installation

1. Clone or download this repository
2. Import workflow JSON files into n8n
3. Configure API credentials in n8n environment variables
4. Set up required integrations and connections
5. Test individual workflows before deployment

### Configuration

Each workflow requires specific configuration:

1. **API Credentials**: Update authentication credentials in node settings
2. **Webhook URLs**: Configure callback URLs for external services
3. **Schedule Settings**: Adjust cron triggers for scheduled workflows
4. **LLM Settings**: Configure model selection and parameters
5. **Storage Configuration**: Set up database connections for persistent data

## Best Practices

- **Security**: Store API keys in n8n's credentials manager, never commit them
- **Logging**: Enable detailed logging for debugging workflow issues
- **Testing**: Test workflows in a development environment first
- **Monitoring**: Set up alerts for workflow failures
- **Documentation**: Maintain clear documentation for custom configurations
- **Versioning**: Version control your workflow modifications

## Troubleshooting

### Common Issues

- **API Connection Failures**: Verify API credentials and network connectivity
- **Memory Issues**: Large workflows may require increased n8n instance memory
- **Rate Limiting**: Implement delays and retry logic for external API calls
- **Data Loss**: Enable database backups and implement error handling
- **Performance**: Optimize large data processing with batch operations

### Support

For issues and feature requests:
1. Review workflow documentation and comments
2. Check n8n community forums
3. Review API documentation for integrated services
4. Enable debug logging for detailed error information



## Contributing

Contributions are welcome. Please ensure workflows include:
- Clear documentation and comments
- Error handling and fallback logic
- Proper credential management
- Testing and validation

---

