***Note*** - *My Agentic network location is under registries/generated/jira_tickets_router.hocon*

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/cognizant-ai-lab/neuro-san-studio.git
```

### 2. Navigate to the Project Directory

```bash
cd neuro-san-studio
```

### 3. Verify Python Version

Ensure you are using **Python 3.12** or **Python 3.13**.

```bash
python --version
```

### 4. Create a Virtual Environment

```bash
python -m venv venv
```

###  5. Activate the Virtual Environment (Windows PowerShell)

```powershell
.\venv\Scripts\Activate.ps1
$env:PYTHONPATH = (Get-Location).Path
```

### 6. Install Dependencies

```bash
pip install -r requirements.txt
```

### 7. Configure the Mistral API Key

Since this project uses **Mistral AI**, set your API key in PowerShell:

```powershell
$env:MISTRAL_API_KEY="YOUR_MISTRAL_API_KEY"
```

> Replace `YOUR_MISTRAL_API_KEY` with your actual Mistral API key.

### 8. Run the Application

From the project root directory, start the server and client:

```bash
python -m neuro_san_studio run
```

### 9. Open the Application

Open your browser and navigate to:

```
http://localhost:4173/
```

### 10. View Logs (Optional)

The following log files are generated during execution:

* **Server Logs:** `logs/server.log`
* **Client Logs:** `logs/nsflow.log`
* **Agent Logs:** `logs/thinking_dir/`

### 11. Additional Help

To view all available runtime options:

```bash
python -m neuro_san_studio run --help
```

