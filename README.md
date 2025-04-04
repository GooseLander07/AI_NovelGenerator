This is a forked version of the "https://github.com/YILING0013/AI_NovelGenerator" translated into English.

# 📖 Automated Novel Generation Tool

>- Currently busy with school, limited time for project maintenance. Future updates may have to wait until I long vacations

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
```
novel-generator/
├── main.py # Entry file, runs GUI
├── ui.py # Graphical interface
├── novel_generator.py # Core chapter generation logic
├── consistency_checker.py # Consistency checking, prevents plot conflicts
|── chapter_directory_parser.py # Directory parsing
|── embedding_adapters.py # Embedding interface encapsulation
|── llm_adapters.py # LLM interface encapsulation
├── prompt_definitions.py # AI prompt definitions
├── utils.py # Utility functions, file operations
├── config_manager.py # Configuration management (API Key, Base URL)
├── config.json # User config file (optional)
└── vectorstore/ # (Optional) Local vector database storage
```

---

## ⚙️ Configuration Guide
### 📌 Basic Configuration (`config.json`)
```json
{
    "api_key": "sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
    "base_url": "https://api.openai.com/v1",
    "interface_format": "OpenAI",
    "model_name": "gpt-4o-mini",
    "temperature": 0.7,
    "max_tokens": 4096,
    "embedding_api_key": "sk-XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
    "embedding_interface_format": "OpenAI",
    "embedding_url": "https://api.openai.com/v1",
    "embedding_model_name": "text-embedding-ada-002",
    "embedding_retrieval_k": 4,
    "topic": "A novel about the protagonist of Honkai: Star Rail crossing over to the Teyvat continent in Genshin Impact, saving the world while entangled in love and vengeance with various characters.",
    "genre": "Fantasy",
    "num_chapters": 120,
    "word_number": 4000,
    "filepath": "D:/AI_NovelGenerator/filepath"
}
```

### 🔧 Configuration Instructions

1. **Generation Model Configuration**
   - `api_key`: API key for the large model service
   - `base_url`: API endpoint (use the local service address for Ollama, etc.)
   - `interface_format`: Interface mode
   - `model_name`: Name of the main generation model (e.g., gpt-4, claude-3, etc.)
   - `temperature`: Creativity parameter (0–1, higher means more creative)
   - `max_tokens`: Maximum response length for the model

2. **Embedding Model Configuration**
   - `embedding_model_name`: Model name (e.g., nomic-embed-text from Ollama)
   - `embedding_url`: Service address
   - `embedding_retrieval_k`: 

3. **Novel Parameter Configuration**
   - `topic`: Core story theme
   - `genre`: Type of work
   - `num_chapters`: Total number of chapters
   - `word_number`: Target word count per chapter
   - `filepath`: Path to store generated files

---

## 📘 Usage Tutorial
1. **Complete basic parameter setup after launch:**  
   - **API Key & Base URL** (e.g., `https://api.openai.com/v1`)  
   - **Model Name** (e.g., `gpt-3.5-turbo`, `gpt-4o`)  
   - **Temperature** (0~1, controls text creativity)  
   - **Topic** (e.g., "AI uprising in a post-apocalyptic world")  
   - **Genre** (e.g., "Sci-Fi"/"Fantasy"/"Urban Fantasy")  
   - **Chapter Count**, **Words per Chapter** (e.g., 10 chapters, ~3000 words each)  
   - **Save Path** (recommend creating a new output folder)

2. **Click "Step1. Generate Settings"**  
   - The system will generate based on topic, genre, chapter count etc.:  
     - `Novel_setting.txt`: Contains world-building, character info, plot points and warnings.  
   - You can review or modify settings in the generated `Novel_setting.txt`.

3. **Click "Step2. Generate Directory"**  
   - The system will generate chapter structure based on completed `Novel_setting.txt`:  
     - `Novel_directory.txt`: Includes all chapter titles and brief prompts.  
   - You can review, modify or supplement chapter titles and descriptions in the generated file.

4. **Click "Step3. Generate Chapter Draft"**  
   - Before generation, you can:  
     - **Set chapter number** (e.g., enter `1` for Chapter 1)  
     - **Provide chapter guidance** (any expectations/prompts for this chapter)  
   - After clicking, the system will:  
     - Automatically read previous settings, `Novel_directory.txt`, and finalized chapters  
     - Use vector retrieval to maintain plot continuity  
     - Generate chapter outline (`outline_X.txt`) and content (`chapter_X.txt`)  
   - After generation, you can review and edit the draft in the left text panel.
  5. **Click "Step4. Finalize Current Chapter"**  
   - The system will:  
     - **Update global summary** (write to `global_summary.txt`)  
     - **Update character states** (write to `character_state.txt`)  
     - **Update vector retrieval database** (ensure subsequent chapters access latest information)  
     - **Update key plot points** (e.g., `plot_arcs.txt`)  
   - After finalization, you'll see the polished text in `chapter_X.txt`.

  6. **Consistency Check (Optional)**  
     - Click "[Optional] Consistency Review" to detect conflicts in the latest chapter (character logic, plot contradictions, etc.)  
     - Any detected conflicts will display detailed alerts in the log area.

  7. **Repeat Steps 4-6** until all chapters are generated and finalized!

  > **Vector Retrieval Configuration Tips**  
  > 1. Embedding models require explicit interface and model name specification;
  > 2. When using **local Ollama** for **Embedding**, start the service first:  
  >    ```bash
  >    ollama serve  # Start service
  >    ollama pull nomic-embed-text  # Download/activate model
  >    ```
  > 3. After switching embedding models, clear the vectorstore directory
  > 4. Cloud-based embedding requires confirmed API access permissions

---

## ❓ Troubleshooting
### Q1: Expecting value: line 1 column 1 (char 0)

This error typically occurs when the API fails to return a proper response, possibly returning HTML or other unexpected content instead.

### Q2: HTTP/1.1 504 Gateway Timeout?
Check if your API endpoint is stable and accessible.

### Q3: How to switch between different Embedding providers?
Simply enter the new provider details in the corresponding GUI input fields.

---
For additional questions or feature requests, please submit them in the **project Issues** section.
