# Content Creation Tool for Marketing Teams

Build a GUI-based content creation tool with chat interface that helps content teams automate blog writing from idea capture to Medium publishing using local filesystem operations.

## Requirements

### Setup

- Configure MCP Filesystem server for local file operations
- Get OpenAI and Medium API keys
- Create local workspace: `content-workspace/ideas/`, `generated/`, `published/`, `templates/`

## Core Features

### 1. Chat-Based Idea Capture

- **GUI chat interface**: "I want to write about MCP for developers"
- AI assistant captures structured ideas and saves to local `ideas/` folder
- Use `write_file` to create idea templates with metadata
- **Local file naming**: `YYYY-MM-DD-idea-title.md`

### 2. AI Content Generation via Chat

- **Chat command**: "Generate article from my MCP idea"
- Use `read_file` to load idea from local filesystem
- Call OpenAI API with structured prompts for content generation
- Use `write_file` to save generated drafts to local `generated/` folder
- Show content preview in chat interface

### 3. Content Review Dashboard

- GUI interface showing local file directory structure
- Use `list_directory` to display generated content
- In-app editor for content refinement using `edit_file`
- **Approval workflow**: move files from `generated/` to `published/` using `move_file`
- Real-time file status updates in GUI

### 4. One-Click Medium Publishing

- **GUI button**: "Publish to Medium"
- Use `read_file` to load approved content from local filesystem
- Post to Medium API with proper formatting
- Use `edit_file` to update local file with Medium URL and publication date
- Success notification in chat interface

## GUI Requirements

- **Chat Interface**: Natural language interaction for all operations
- **File Browser**: Visual representation of local content workspace
- **Content Editor**: In-app editing of generated content
- **Status Dashboard**: Track content pipeline progress
- **Local Filesystem Integration**: All operations save/read from local files

## Deliverables

- GUI application with chat interface
- MCP filesystem integration for local file operations
- Working content pipeline (idea → generated → published → Medium)
