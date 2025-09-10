# 🤖 AI Development Agent

> **Autonomous AI Agent that builds complete websites from natural language prompts**

[![Gemini API](https://img.shields.io/badge/Powered%20by-Gemini%20API-blue?style=for-the-badge&logo=google)](https://ai.google.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://javascript.com)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org)

## 🌟 What Makes This Special?

This isn't just another code generator. It's an **autonomous AI agent** that:

- 🧠 **Thinks step-by-step** using multi-turn conversations
- ⚡ **Executes shell commands** automatically
- 🔄 **Learns from feedback** and adjusts its approach
- 🎯 **Creates complete projects** from a single prompt

## 🚀 Demo

```bash
$ node agent.js
🤖 I am a cursor: let's create a website
Ask me anything--> Build me a calculator website

🔥 Creating project structure...
📁 mkdir calculator
📄 touch calculator/index.html
🎨 touch calculator/style.css
⚙️  touch calculator/script.js
✨ Writing HTML code...
🎉 Website ready! Check your VS Code
```

## 🛠️ Tech Stack

| Technology           | Purpose                         |
| -------------------- | ------------------------------- |
| **Gemini 2.5 Flash** | AI reasoning & function calling |
| **Node.js**          | Runtime environment             |
| **Child Process**    | Shell command execution         |
| **Readline-sync**    | Interactive CLI interface       |

## 🧠 How It Works

### Architecture Overview

```
User Input → Gemini API → Function Calling → Shell Execution → File Creation → Live Website
```

### Key Features

- **🎯 Function Calling**: Uses Gemini's function calling to execute terminal commands
- **🔄 Conversation Memory**: Maintains context across multiple interactions
- **🖥️ Cross-Platform**: Automatically detects OS and adapts commands
- **⚡ Real-time Execution**: Watch as files get created in your VS Code
- **🎨 Complete Websites**: Generates HTML, CSS, and JavaScript

## 📦 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Sh1va84/AI-Development-Agent.git
   cd AI-Development-Agent
   ```

2. **Install dependencies**

   ```bash
   npm install @google/genai readline-sync
   ```

3. **Set up Gemini API Key**

   - Get your API key from [Google AI Studio](https://aistudio.google.com/)
   - Replace `YOUR_API_KEY` in the code with your actual key

4. **Run the agent**
   ```bash
   node agent.js
   ```

## 💡 Usage Examples

### Simple Website

```
Input: "Create a portfolio website"
Output: Complete portfolio with HTML, CSS, JS
```

### Complex Applications

```
Input: "Build a todo app with local storage"
Output: Full todo app with CRUD operations
```

### Games & Interactive Content

```
Input: "Make a tic-tac-toe game"
Output: Interactive game with win detection
```

## 🎯 Core Code Highlights

### Function Calling Setup

```javascript
const executeCommandDeclaration = {
  name: "executeCommand",
  description: "Execute terminal/shell commands",
  parameters: {
    type: "OBJECT",
    properties: {
      command: {
        type: "STRING",
        description: "Terminal command to execute",
      },
    },
    required: ["command"],
  },
};
```

### AI Agent Loop

```javascript
while (true) {
  const response = await ai.models.generateContent({
    model: "gemini-2.5-flash",
    contents: History,
    tools: [{ functionDeclarations: [executeCommandDeclaration] }],
  });

  if (response.functionCalls) {
    // Execute the command autonomously
    const result = await executeCommand(args);
  } else {
    // Agent finished the task
    break;
  }
}
```

## 🔥 What Sets This Apart

| Feature          | Traditional Tools     | This AI Agent             |
| ---------------- | --------------------- | ------------------------- |
| **Intelligence** | Pre-defined templates | Contextual understanding  |
| **Flexibility**  | Fixed structures      | Adapts to any request     |
| **Automation**   | Manual file creation  | Full autonomous execution |
| **Learning**     | Static behavior       | Learns from interaction   |

## 🚀 Future Enhancements

- [ ] **Multi-language Support** - Python, React, Vue projects
- [ ] **Git Integration** - Auto-commit and deploy
- [ ] **Package Management** - Install dependencies automatically
- [ ] **Testing Generation** - Create unit tests for generated code
- [ ] **Deployment** - Deploy to Vercel/Netlify automatically

## 🤝 Contributing

Want to make this agent even smarter?

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Google Gemini** for the incredible function calling capabilities
- **OpenAI** for pioneering AI agent concepts
- **The Dev Community** for inspiration and feedback

---

<div align="center">

**Made with ❤️ by [Shiva](https://github.com/Sh1va84)**

_If this project helped you, give it a ⭐!_

[![GitHub followers](https://img.shields.io/github/followers/Sh1va84?style=social)](https://github.com/Sh1va84)
[![GitHub stars](https://img.shields.io/github/stars/Sh1va84/AI-Development-Agent?style=social)](https://github.com/Sh1va84/AI-Development-Agent)

</div>
