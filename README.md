# Prometheus — AI-Native Code Editor & Off-Grid Intelligence Engine

Prometheus is a high-performance, local-first workbench built with C++20, Qt 6 / QML, and native inference engines (`llama.cpp` CUDA/CPU backends, with AMD ROCm/HIP and Intel SYCL/OpenVINO support planned). Designed around a **Vulkan 1.3 & DirectX 12_1** graphics rendering architecture, Prometheus delivers offline autonomy, privacy, and deep developer productivity across twelve unified modules.

---

## ⚡ Core Subsystems & Status Matrix

| Subsystem | Features & Capabilities | Status / Roadmap |
|---|---|---|
| **Graphics Engine** | **Vulkan 1.3 & DirectX 12_1** QML rendering viewport | Active |
| **Code Editor** | Multi-buffer editing, syntax highlighting, line decorations, tree navigation | Active |
| **LSP & AI Completion** | Language Server Protocol integration, inline code completion, semantic diffing | Roadmap |
| **Local LLM Engine** | Native `llama.cpp` C++ engine with streaming tokens, GGUF model loading, system prompts | Active |
| **Model Registry** | GGUF discovery, metadata inspection, automatic VRAM/RAM fit calculator | Active / Expanding |
| **AI Lab Runtime** | Embedded Python 3.15 environment, GGUF/Safetensors manipulation, script execution | Active |
| **Model Fine-Tuning** | LoRA/QLoRA training wizard, dataset preparation, automated perplexity benchmark | Roadmap |
| **Binary & Hex Inspector** | Fast byte viewer, ImHex-style full-type Data Inspector, patch editing, entropy & struct fields | Active / Expanding |
| **Document Suite** | Markdown renderer, note manager, rich text editor, offline knowledge graph | Active / Expanding |
| **Web & Network Tools** | External browser bookmarks + native FTP, IRC, SSH, and RDP clients (zero embedded Chromium) | Active / Expanding |
| **System & Hardware Monitor** | Real-time CPU, RAM, VRAM, and GPU sensor tracking; multi-adapter selector | Active |
| **Security & Audit** | Static code security scanner, license checker, secret leak detector | Active |

---

## 🌟 Key Features & Core Modules

### 📝 Code Editor & IDE (`editor`)
- **Current**: Full-featured code editor with syntax highlighting, line decorations, tree navigation, and multi-buffer workspace support.
- **Planned / Roadmap**: Advanced LSP (Language Server Protocol) integration, inline AI code completions, real-time semantic diffing, and multi-cursor refactoring.

### 🔍 Hex & Binary Inspection (`hex`)
- **Current**: Fast binary viewer and patch editor with ImHex-style full-type Data Inspector (`Binary`, `uint8`–`int64`, `float`/`double`, `char`), async large-file search, bookmarks, checksum repair, struct field dock, and entropy visualization.
- **Planned / Roadmap**: Custom binary pattern scripting, diff comparison, and multi-file binary workspaces.

### 💬 Local AI Chat & Assistance (`chat`)
- **Current**: Multi-turn local LLM chat interface powered by native `llama.cpp` integration with streaming tokens, custom system prompts, and context management.
- **Planned / Roadmap**: Multi-model routing, prompt template library, RAG (Retrieval-Augmented Generation) document indexing, and agentic function calling.

### 🎨 Media Studio (`studio`)
- **Current**: All 19 sub-modules wired — image generation & editing, video, audio/TTS, 3D mesh generation, CAD/PCB, palette, plus interactive pixel/animation, SVG vector, isometric voxel, font inspector, upscaler, SRT subtitles, translation, narration, and roleplay tools.
- **Planned / Roadmap**: Deeper authoring tools across pixel/vector/voxel, Whisper auto-transcription, local LLM/TTS wiring for text tools, and Hunyuan3D 2.1 single-safetensors pipeline.

### 📄 Document & Office Suite (`office`)
- **Current**: Structured document editing, Markdown rendering, and note management.
- **Planned / Roadmap**: Rich text / Office document processing, slide presentation generator, and collaborative offline knowledge graph.

### 🤖 Model Manager & Registry (`models`)
- **Current**: GGUF model file discovery, metadata parsing, and quantization profile inspector.
- **Planned / Roadmap**: One-click Hugging Face / model hub downloader, automatic VRAM/RAM fit calculator, and dynamic GPU layer offloading controls.

### 🌐 Hub (`hub`)
- **Current**: Centralized task launcher, activity log viewer, and workspace configuration manager.
- **Planned / Roadmap**: Plugin ecosystem manager, remote workspace synchronization, and automated project templates.

### 🧪 AI Lab (`lab`)
- **Current**: Python stage runner integration for offline AI experiments, script execution, and GGUF/Safetensors manipulation.
- **Planned / Roadmap**: Model fine-tuning interface (LoRA/QLoRA), dataset preparation wizard, and automated benchmark runner.

### 🌐 Web & Network Tools (`web`)
- **Current**: Zero-Chromium external browser bookmark launcher plus native FTP, live TCP IRC, SSH, and RDP profile & probe tools.
- **Planned / Roadmap**: In-app Python/toolchain package & environment manager, SSH sessions inside the native ConPTY terminal, and full SFTP file transfers.

### ⚙️ System Monitor & Settings (`system`)
- **Current**: Hardware resource tracker (CPU, VRAM, RAM, GPU utilization) and application preference engine.
- **Planned / Roadmap**: Multi-GPU adapter selector, power consumption profiler, and detailed thread scheduler metrics.

### 🖥️ OS & Virtual Workspace (`os`)
- **Current**: Integrated shell terminal host and workspace layout builder.
- **Planned / Roadmap**: Multi-window tiling manager, virtual desk environments, and isolated execution containers.

### 🛡️ Compliance & Security Audit (`audit`)
- **Current**: Static security scanner, license dependency checker, and file integrity verifier.
- **Planned / Roadmap**: Automated policy compliance reporter, permission boundary auditor, and secret leak detector.

---

## 🏗️ Architecture & Technology Stack

- **Graphics APIs**: Vulkan 1.3 & DirectX 12_1.
- **UI & Workbench**: Qt 6.12, QML, custom 12-theme desktop palette system (`system` + 11 curated light/dark themes).
- **Native Engine**: C++20 engine DLL (`core/native`) with direct hardware bindings.
- **Inference Engine**: Native `llama.cpp` C++ library with CUDA, Vulkan, and CPU backends (AMD ROCm/HIP and Intel oneAPI SYCL / OpenVINO planned).
- **Lab Runtime**: Embedded Python 3.15 virtual environment for specialized AI tools and pipelines.
- **Internationalization**: Native JSON i18n localization engine (35 locale catalogs supported).

---

## 🛠️ Building & Running

### Prerequisites
- **Visual Studio 2022** (C++20 MSVC compiler)
- **Qt 6.12** (`msvc2022_64`)
- **Vulkan SDK 1.3+**
- **Python 3.15**

### Build Commands

```bat
:: Build Release binary (Prometheus.exe)
build.bat Release

:: Build Debug binary
build.bat Debug

:: Run the application
run.bat
```

---

## 📜 License

Prometheus is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
