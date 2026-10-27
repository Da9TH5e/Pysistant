# 🚀 Pysitant

A lightweight AI orchestration system with strict client–server separation.

Pysitant keeps the client lightweight and controlled while delegating reasoning and code generation to a VPS backend. It combines project-context building, model abstraction, and request routing to support AI-assisted codebase exploration.

## ✅ Features

- Modular model abstraction layer
- Project context builder and routing system
- CLI-based interaction
- VPS-based reasoning and code generation support
- Fast online reasoning integration
- Request-routing optimizations
- Multi-agent experimentation
- Client–server separation with API-key-based session creation

## 🔜 Coming Next

- Clearer user instructions and onboarding
- Performance and routing improvements

## 🔮 Future Plans

- Direct code modification capabilities
- Expanded project-aware assistance

## 💻 Running Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Da9TH5e/Pysistant.git
cd Pysistant
```

The server-side code is maintained separately in [Server_Pypilot](https://github.com/Da9TH5e/Server_Pypilot).

### 2. Create a Virtual Environment

**macOS / Linux**

```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows**

```powershell
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements_dev.txt
```

### 4. Configure the VPS API

Create a private `.env` file from the example configuration.

**Windows**

```powershell
copy .env.example .env
```

**macOS / Linux**

```bash
cp .env.example .env
```

Configure the following values in `.env`:

```env
PYSITANT_VPS_API_URL=https://your-domain.com/api/ask
PYSITANT_VPS_SESSION_URL=https://your-domain.com/api/session
PYSITANT_API_KEY=your-private-api-key
```

The API key is used to establish a short-lived server session. Keep your real API key private, and never commit your `.env` file or publish credentials in the client package.

### 5. Run the CLI

```bash
cd src
python -m pysitant.cli
```

## 🧠 First Usage

Start by granting consent for a project directory:

```text
consent <path-to-project>
```

If no path is provided, Pysitant uses the directory containing the relevant file.

Build the project context:

```text
build_once
```

Ask a question about the project:

```text
ask explain the project structure
```

## 🔐 Security and Architecture

Pysitant separates the client from the server-side reasoning backend. The client uses configured API endpoints and a private API key to request a short-lived session token.

Never commit real credentials, API keys, or private environment files to version control.

## 📌 Project Status

Pysitant includes a CLI, project-context tooling, model abstraction, and VPS-backed reasoning integration. Further improvements to onboarding, performance, and code modification are planned.

## 📽️ Video
https://github.com/user-attachments/assets/ce8337b1-1785-4644-a1a2-99dd43ceeb46
