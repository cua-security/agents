## Installation Guide

Follow the steps below to get started.

### Step 1: Set Up Python Environment

We recommend using [Anaconda](https://www.anaconda.com/products/distribution) to manage the environment.

Create and activate the conda environment:

```bash
conda create -n webui python=3.11
conda activate webui
```

### Step 2: Install Dependencies
Install Python packages:
```bash
pip install -r requirements.txt
```

Install Playwright:
```bash
playwright install
```

### Step 3: Configure Environment
1. Create a copy of the example environment file:
- Windows (Command Prompt):
```bash
copy .env.example .env
```
- macOS/Linux/Windows (PowerShell):
```bash
cp .env.example .env
```
2. Open `.env` in your preferred text editor and add your API keys for the models you want to run. `OPENROUNTER_API_KEY` is general and can be used for many models.

###  Step 4: Browser Setup
- Set `CHROME_PATH` to the executable path of your browser and `CHROME_USER_DATA` to the user data directory of your browser. 
  - Windows
    ```env
      CHROME_PATH="C:\Program Files\Google\Chrome\Application\chrome.exe"
      CHROME_USER_DATA="C:\Users\YourUsername\AppData\Local\Google\Chrome\User Data"
    ```
    > Note: Replace `YourUsername` with your actual Windows username for Windows systems.
  - Mac
    ```env
      CHROME_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
      CHROME_USER_DATA="/Users/YourUsername/Library/Application Support/Google/Chrome"
    ```

## Evaluation using LLM Judge
To run LLM Judge, simply specify the model's log directory and the folder containing the test cases in `llms_judge.py`. Then run:
```bash
python llms_judge.py
```
## Result Calculation
Just need to specify the path of the judgement. Then run:
```bash
python calculate_result.py
```
