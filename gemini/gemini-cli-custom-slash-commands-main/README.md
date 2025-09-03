# Gemini CLI Custom Slash Commands - Daily Workflow Automation

This repository contains 10 practical workflow commands for Gemini CLI that help with both general productivity tasks and essential development work, inspired by the [Google Cloud blog post](https://cloud.google.com/blog/topics/developers-practitioners/gemini-cli-custom-slash-commands).

## 🎯 Available Commands

### 📸 General Workflow Commands

**`/photo-rename`** - Smart Photo Organization  
Organizes and renames photos based on visual content, dates, and metadata.  
_Usage:_ `/photo-rename ~/Photos/vacation-2024`

**`/report-gen`** - Data Analysis & Reporting  
Generates comprehensive reports from data files with insights and visualizations.  
_Usage:_ `/report-gen ./sales-data`

**`/email-draft`** - Professional Email Writer  
Drafts professional emails with proper tone, structure, and templates.  
_Usage:_ `/email-draft "Schedule meeting with marketing team for Q4 planning"`

**`/meeting-summary`** - Meeting Notes Analyzer  
Converts meeting notes into actionable summaries with clear follow-ups.  
_Usage:_ `/meeting-summary ./meeting-notes.txt`

**`/file-organizer`** - Smart File Organization  
Intelligently organizes directories by content type, date, and purpose.  
_Usage:_ `/file-organizer ~/Downloads`

**`/task-prioritizer`** - Task Management  
Analyzes and prioritizes tasks with time estimates and urgency levels.  
_Usage:_ `/task-prioritizer "Write presentation, call dentist, review budget"`

### 💻 Developer Commands

**`/test-gen`** - Test Case Generator  
Automatically generates comprehensive test cases with edge cases and best practices.  
_Usage:_ `/test-gen UserAuthService`

**`/debug-assistant`** - Debugging Helper  
Analyzes errors and provides systematic debugging strategies and solutions.  
_Usage:_ `/debug-assistant "TypeError: Cannot read property 'id' of undefined"`

**`/security-audit`** - Security Scanner  
Performs security audits of code changes, dependencies, and vulnerabilities.  
_Usage:_ `/security-audit ./src`

**`/cleanup`** - Codebase Cleaner  
Identifies cleanup opportunities including unused code and optimization suggestions.  
_Usage:_ `/cleanup ./project`

## 🚀 Quick Start

1. **Install/Update Gemini CLI:**

   ```bash
   npm install -g @google/gemini-cli@latest
   ```

2. **Copy commands to your project:**

   ```bash
   # Project-scoped (recommended for teams)
   cp -r .gemini /path/to/your/project/

   # Or user-scoped (available everywhere)
   cp -r .gemini/commands ~/.gemini/commands/
   ```

3. **Use the commands:**

   ```bash
   # Organize vacation photos
   /photo-rename ~/Photos/summer-trip-2024

   # Draft a professional email
   /email-draft "Request time off for next week"

   # Analyze sales data
   /report-gen ./quarterly-sales.csv

   # Generate tests for a function
   /test-gen calculateTotal

   # Debug an error
   /debug-assistant "Connection timeout error"
   ```

## 💡 Why These Commands?

- **⚡ Save Time:** Automate repetitive tasks like photo organization and email drafting
- **📊 Data Insights:** Turn raw data into actionable reports instantly
- **🔧 Code Quality:** Generate tests, debug issues, and maintain clean codebases
- **📝 Communication:** Create professional emails and meeting summaries
- **🗂️ Organization:** Keep files and tasks systematically organized

## 🔧 Customization

Each `.toml` file can be customized:

- Modify shell commands for your environment
- Adjust prompts for your specific needs
- Add project-specific rules
- Include your preferred tools and formats

## 📚 Learn More

- [Google Cloud Blog Post](https://cloud.google.com/blog/topics/developers-practitioners/gemini-cli-custom-slash-commands) - Original inspiration
- [Gemini CLI Documentation](https://cloud.google.com/sdk/gcloud/reference/alpha/ai/custom-jobs) - Official docs
- [TOML Format](https://toml.io/) - Configuration file format

---

_Transform your daily workflow with intelligent automation. From organizing family photos to debugging code, these commands handle the routine tasks so you can focus on what matters most._
