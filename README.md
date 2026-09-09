# Naija Legal Rights Guide

This project helps developers build legal assistance tools for Nigerians by providing a comprehensive repository of legal rights, document explanations, and criminal justice workflows translated into multiple local languages. It takes complex Nigerian legal concepts and breaks them down into plain language so teams can easily integrate them into chatbots, websites, or educational apps. No complicated setup, just straightforward legal content that works.

## Installation

To get started with the content, simply clone the repository to your local machine:

```bash
git clone https://github.com/Ace-g-ops/legal_contents.git
```

Once cloned, you can navigate into the directory to view or integrate the markdown files into your application:

```bash
cd legal_contents
```

## Usage

Developers can use this content to build specialized legal assistants or educational platforms. The project includes a pre-configured system prompt that you can inject into your language models. Here is how you might structure your bot instructions using the provided system prompts:

```text
You are a legal rights assistant for Nigeria. Your job is to help people understand their rights when dealing with police and courts.

Rules:
- Speak simply, like explaining to a friend
- Never claim to be a lawyer
- Always remind users this is information, not legal advice
```

You can programmatically read the markdown files to serve content based on the user's language preference. Here is a simple Node.js script demonstrating how to serve the Pidgin rights file:

```javascript
const fs = require('fs');

function getLegalRights(languageCode) {
  const filePath = `./rights_${languageCode}.md`;
  return fs.readFileSync(filePath, 'utf8');
}

const pidginContent = getLegalRights('pid');
console.log(pidginContent);
```

## Features

* Local Language Support: Content is fully translated into English, Pidgin, Yoruba, Hausa, and Igbo to maximize accessibility.
* Step-by-Step Workflows: Detailed guides covering the entire Nigerian criminal justice process from the point of arrest all the way to the appeal stage.
* Legal Document Breakdowns: Plain-language explanations of confusing court documents like Charge Sheets and Bail Orders.
* Multilingual Glossary: A cross-referenced dictionary mapping core legal terminology across different regional languages.
* Built-in Disclaimers: Pre-written safety boundaries ensuring end-users understand the tool is for educational purposes and not a substitute for professional legal counsel.

## Technologies Used

| Technology | Description |
|---|---|
| [Markdown](https://daringfireball.net/projects/markdown/) | Core content structuring and documentation formatting |
| [Git](https://git-scm.com/) | Version control and collaborative content management |

## Contributing

Contributions to improve translations, add new legal topics, or refine the existing guides are highly encouraged. Please fork the repository, make your changes, and submit a pull request. Make sure your additions match the plain and accessible tone of the existing files.

## Author Info

* GitHub: [Ace-g-ops](https://github.com/Ace-g-ops)

[![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)](https://daringfireball.net/projects/markdown/)
