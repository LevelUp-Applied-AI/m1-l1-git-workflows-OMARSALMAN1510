# Hospital Admission Records Analysis

## Team Members
- Omar Salman
- Lina Haddad
- Ahmad Khalil

## Project Overview
This project analyzes hospital admission records to explore trends in patient admissions and prepare data for analysis. The goal is to create a reproducible environment so that any new contributor can clone the repository and run the project without setup issues.

## Data Sources
This project uses hospital admission records data.

Data is not tracked in this repository. See the setup instructions below
for how to obtain and place the data files before running any analysis.

Expected data location:

```
data/raw/admissions.csv
```

---

## Setup Instructions

Clone the repository:

```bash
git clone https://github.com/LevelUp-Applied-AI/m1-l1-git-workflows-OMARSALMAN1510.git
cd m1-l1-git-workflows-OMARSALMAN1510
python -m venv .venv
```

Activate the virtual environment:

**Mac / Linux**

```bash
source .venv/bin/activate
```

**Windows Git Bash**

```bash
source .venv/Scripts/activate
```

**Windows CMD**

```bash
.venv\Scripts\activate.bat
```

**Windows PowerShell**

```bash
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Verify the environment:

```bash
python test_environment.py
```

Expected output:

```
Environment OK
```

---

## Project Structure

```
m1-l1-git-workflows-OMARSALMAN1510/
├── README.md
├── CHANGELOG.md
├── AGENTS.md
├── requirements.txt
├── setup.sh
├── test_environment.py
├── .gitignore
├── tests/
├── data/
│   └── raw/
```

---

## Contributing

Branch naming convention:

- `feature/description`
- `fix/description`
- `setup/description`
- `integration/description`

Before opening a Pull Request:

1. Pull latest changes from `main`
2. Create a new branch
3. Test changes locally
4. Write clear commit messages
5. Open a Pull Request