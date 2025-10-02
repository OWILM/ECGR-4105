# HW2 — How to run Problem 1, 2 and 3

This README explains how to run the scripts in this folder (`Problem 1`, `Problem 2`, `Problem 3`).

Prerequisites
- Python 3.8+ installed and available as `python` on the PATH.
- It's recommended to use a virtual environment so dependencies don't affect your system Python.

Recommended quick steps (PowerShell)

1. Open PowerShell in the project root (where `requirements.txt` lives) or run from anywhere but use absolute paths below.

2. Create and activate a virtual environment (recommended):

```powershell
cd "C:\Users\drag0\ECGR 4105\ECGR-4105"
python -m venv .venv
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

3. Install dependencies (numpy, pandas, matplotlib, scikit-learn):

```powershell
python -m pip install --upgrade pip
python -m pip install -r .\requirements.txt
```

Running the problems

- Problem 1

	Run the script `Problem 1` (it's a plain Python file inside this folder). From the workspace root or from the `HW2` folder you can run:

	```powershell
	python .\HW2\"Problem 1"
	```

	Notes:
	- The script expects `Housing.csv` to be in the same folder (`HW2\Housing.csv`).
	- It will run gradient descent for two feature sets and display compact loss plots. If figures do not appear, ensure you activated the virtual environment and installed `matplotlib`.

- Problem 2

	Run `Problem 2` similarly:

	```powershell
	python .\HW2\"Problem 2"
	```

	(Follow any prompts or check the top of the file for dataset requirements.)

- Problem 3

	Run `Problem 3`:

	```powershell
	python .\HW2\"Problem 3"
	```

Troubleshooting
- If you get `FileNotFoundError` for `Housing.csv`, confirm the file exists at `HW2\Housing.csv` and that you're running the script from the project root or using the full path to the script.
- If `import numpy` fails, make sure the virtual environment is activated and `pip install -r requirements.txt` completed successfully.
- If plots are empty or have weird axes limits, try a fresh Python session (close the interactive window) or add `plt.close('all')` before creating new figures in the scripts.

Further tweaks
- If you'd like a command-line flag to control plotting (compact vs full) or to save plots instead of showing them, I can add argparse options to each Problem script.

Contact
- If anything above fails, paste the full error message here and I will help debug.


