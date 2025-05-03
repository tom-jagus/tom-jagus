# 🧰 My Working Stack

## 🖥️ Programming & Query Languages

These are the core languages I use to build, automate, and model solutions — from semantic layers to scripting to interface design.

- **Python** — scripting, automation, data analysis, scraping, and integration
- **SQL** — querying, transformation, and modeling across BI and backend systems
- **DAX** — advanced measure creation and expression logic for Power BI models
- **Power Query (M)** — data transformation and shaping inside Power BI
- **TMDL** — semantic modeling and deployment for enterprise-scale tabular models
- **Lua** — daily use for customizing and extending my Neovim configuration (via LazyVim)
- **C#** — scripting in Tabular Editor for DAX automation and metadata handling
- **JavaScript** — used for scripting in workflow automation and custom widgets
- **HTML/CSS** — used for styling and customizing visual elements in web-based reports and dashboards

## 📊 Data Tools & BI Platforms

These are the primary platforms and tools I use to design, deploy, and maintain enterprise-ready BI and reporting solutions.

- **Power BI** — my core platform for report development, modeling, and insight delivery

  - **Power BI Desktop** — for model design, data transformation (Power Query), and report layout
  - **Power BI Service** — for dataset publishing, dataflows, pipelines, row-level security, and workspace management

- **Microsoft Fabric** — early adopter of Fabric as a unified analytics platform

  - Working with **Lakehouses**, **Warehouses**, **Pipelines**, and **Semantic Models** (via TMDL)

- **Tabular Editor** — used for advanced semantic modeling, automation, and deployment

  - Authoring and editing TMDL or Tabular Object Model (TOM)
  - Scripting with C# for model manipulation and optimization
  - Managing calculation groups, translations, metadata, and source control

- **DAX Studio** — essential for performance tuning, diagnostics, and query inspection

  - Evaluating DAX query plans and storage engine behavior
  - Measuring performance with Server Timings and Query Plan
  - Testing and refining DAX expressions in isolation

- **Excel** — often used for rapid validation, ad hoc data profiling, and business-oriented modeling
  - Verifying model output via pivot tables connected to datasets
  - Creating sanity checks and reconciliation reports
  - Supporting hybrid workflows with non-technical users

## 🤖 AI, LLMs & Automation

I actively integrate AI tooling into my workflows — both to accelerate development and to create intelligent, adaptable systems for clients and internal use.

- **Prompt Engineering** — designing modular, context-aware prompts for analysis, content creation, automation, and structured logic chains

- **LLM Tooling** — working across multiple platforms for prototyping, insight generation, and workflow integration:

  - **OpenAI** — for structured prompt systems, content extraction, and assistant-style interfaces
  - **Microsoft Copilot** — for productivity acceleration across documentation and reporting tools
  - **Ollama** — experimenting with lightweight, private LLMs for offline and local-enhanced tasks

- **Generative AI** — using LLMs for interface sketching, documentation scaffolding, semantic tagging, and rapid knowledge transfer

- **AI-Augmented Workflows** — supporting tasks like data profiling, column descriptions, metric definitions, text-to-query translation, and QA/testing scenarios

- **RAG and Vector Search (Exploratory)** — experimenting with semantic search, FAISS/Qdrant vector stores, and structured context injection

- **Automation Integration** — embedding LLMs into terminal workflows, scripts, and custom tools to reduce boilerplate, lookup effort, and repetitive coding

I focus on using AI to support **human-led problem solving** — not to replace thinking, but to reduce friction, amplify insights, and enable faster, more confident execution.

## ⚙️ Developer Tooling

I maintain a lean, fast, and fully version-controlled development environment across Linux and Windows. My setup is built around consistency, automation, and low-friction navigation — designed to scale from quick scripting to full data workflows.

- **Neovim (LazyVim)** — my primary editor, extended with Lua plugins for LSP, AI assistance, markdown tools, and customized workflows

  - Includes tools like:
    - `mason` — LSP installer/manager
    - `conform.nvim` — formatter management
    - `nvim-treesitter` — syntax-aware parsing and highlighting
    - `nvim-cmp` stack — fast, intelligent autocompletion

- **Git & GitHub** — used for everything from project and config management to automation and CI/CD

  - I follow a GitHub Flow strategy, extended with personal aliases for feature branches, PRs, and safe merges

- **lazygit** — terminal-based Git UI used for staging, reviewing, resolving, and committing changes efficiently

- **ripgrep, fzf, yazi** — my go-to stack for fuzzy finding, recursive search, and file navigation in terminal environments

- **Python environment tools** — I use [`uv`](https://github.com/astral-sh/uv) for fast dependency management and environment isolation, and [`ruff`](https://github.com/astral-sh/ruff) for linting and formatting

- **Shell automation** — portable setup scripts (Bash + PowerShell) to bootstrap Neovim, clone dotfiles, configure Git, and prep new machines

- **GitHub CLI & Actions** — used to automate PRs, repo ops, and site/blog deployments in personal and client-facing projects

I treat my tooling like any production system — composable, documented, and continuously improved.

## 🧪 Scripting & Integration

I rely heavily on scripting to automate data flows, integrate systems, and reduce manual effort across recurring tasks. My scripting environment spans multiple languages and platforms — all focused on portability, clarity, and real-world output.

- **Python** — my primary language for scripting data pipelines, API connectors, web scraping, and file processing

  - Often used in automation flows to extract data, reshape files, upload results, or trigger downstream tools

- **Shell scripting (Bash & PowerShell)** — used for bootstrapping environments, managing config, orchestrating setup flows across Linux and Windows

- **C# scripting (Tabular Editor)** — used for automating model changes, managing calculation groups, mass-editing metadata, and generating reusable DAX patterns

- **REST API integration** — experience working with JSON, token-based authentication, and platform-specific APIs (e.g., ServiceNow, GitHub, OpenAI)

  - Scripting API calls for data extraction, automation triggers, or status/reporting updates

- **ServiceNow scripting & reporting** — building export flows, extracting reporting data, and automating performance analytics exports using the platform's scripting layer

- **Data flow automation** — scripting ETL/ELT-like tasks across file systems, Excel, APIs, and databases — often bridging structured tools like Power BI with external logic

My scripting focus is always on clarity, reuse, and versionability — not throwaway scripts, but modular tools that can scale or adapt as needed.

## 📦 Data Modeling & Semantics

Designing clean, scalable, and understandable semantic models is central to my work — whether for one-off reporting or enterprise-wide datasets. I treat the model layer as a critical interface between raw data and business value.

- **Tabular Modeling** — experienced in building and maintaining semantic models using Power BI, Microsoft Fabric, and Tabular Editor

  - Creating reusable measures, hierarchies, calculation groups, and KPI structures
  - Managing relationships, normalization, and performance-optimized schema design
  - Applying role-level security (RLS), perspectives, and documentation standards

- **TMDL (Tabular Model Definition Language)** — used for versioning, deploying, and managing semantic models in source control

  - Enabling clean diffing, rollbacks, collaboration, and CI/CD-style deployments
  - Working with TMDL in both Tabular Editor and Microsoft Fabric environments

- **Metadata & Governance** — I take a disciplined approach to model metadata

  - Using consistent naming conventions, foldering, and descriptions
  - Supporting documentation via scripting, metadata extraction, and alignment with stakeholders

- **Measure Logic & Performance** — I build DAX that balances readability and performance
  - Avoiding unnecessary dependencies or filters
  - Using `CALCULATE`, `REMOVEFILTERS`, `VAR`, and iterator patterns effectively
  - Validating assumptions with tools like DAX Studio and server timings

For me, modeling isn’t just technical — it’s where context, logic, and usability come together. I build semantic layers that clarify, not complicate.
