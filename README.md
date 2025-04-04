This is a forked version of the "https://github.com/YILING0013/AI_NovelGenerator" translated into English.

# 📖 Automated Novel Generation Tool

>- Currently busy with school, limited time for project maintenance. Future updates may have to wait until long vacations

<div align="center">
  
✨ **Core Features** ✨

| Feature Module         | Key Capabilities                          |
|-----------------------|------------------------------------------|
| 🎨 Novel Setting Workshop | World-building / Character Design / Plot Blueprinting |
| 📖 Intelligent Chapter Generation | Multi-stage generation for plot coherence |
| 🧠 State Tracking System | Character development tracking / Foreshadowing management |
| 🔍 Semantic Search Engine | Vector-based long-range context consistency |
| 📚 Knowledge Base Integration | Supports local document references |
| ✅ Auto-Proofreading Mechanism | Detects plot contradictions & logical conflicts |
| 🖥 Visual Workbench | Full-process GUI operation - configure/generate/review integration |

</div>

> A multifunctional novel generator based on large language models, helping you efficiently create long stories with rigorous logic and consistent settings

2025-03-05 Added character library feature

2025-03-09 Added word count display

2025-03-13 
1. Added Xianyun modifications;
2. Changed "chapter guidance" to "content guidance";
3. Added guiding prompts to: 
   - 2. Character Dynamics (Character Arc Model) 
   - 3. World-Building Matrix (Three-Dimensional Interweaving Method) 
   - 4. Plot Structure (Three-Act Suspense) 
   in the generation framework, and to: 
   - 5. Chapter Directory Generation (Suspense Rhythm Curve) 
   in the directory generation, to prevent generated content from deviating from actual needs when only core seeds are used.
4. Restored deleted LLM prompts and LLM response displays in the terminal for review and prompt modification reference.
---

## 📑 Navigation
1. [Environment Setup](#-environment-setup)  
2. [Project Structure](#-project-structure)  
3. [Configuration Guide](#⚙️-configuration-guide)  
4. [Running Instructions](#🚀-running-instructions)  
5. [Usage Tutorial](#📘-usage-tutorial)  
6. [Troubleshooting](#❓-troubleshooting)  

---

## 🛠 Environment Setup
Ensure the following requirements are met:
- **Python 3.9+** runtime (recommended 3.10-3.12)
- **pip** package manager
- Valid API keys:
  - Cloud services: OpenAI / DeepSeek etc.
  - Local services: Ollama or other OpenAI-compatible interfaces

---


## 📥 Installation Guide
1. **Download Project**  
   - Download project ZIP from [GitHub](https://github.com), or clone with:
     ```bash
     git clone https://github.com/YILING0013/AI_NovelGenerator
     ```

2. **Install Build Tools (Optional)**  
   - If certain packages fail to install, download [Visual Studio Build Tools](https://visualstudio.microsoft.com/zh-hans/visual-cpp-build-tools/) and install C++ build tools;
   - During installation, only MSBuild tools are included by default - manually check the **C++ Desktop Development** option in the top-left list.

3. **Install Dependencies & Run**  
   - Open terminal, navigate to project directory:
     ```bash
     cd AI_NovelGenerator
     ```
   - Install dependencies:
     ```bash
     pip install -r requirements.txt
     ```
   - Run main program:
     ```bash
     python main.py
     ```

>If missing dependencies, manually execute:
>```bash
>pip install XXX
>```

## 🗂 Project Structure
