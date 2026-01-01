# machine_learning

Anaconda, Python Environment & VS Code Setup (macOS)

This guide explains how to install Anaconda, set up a Python 3.10 virtual environment, install dependencies, and configure Visual Studio Code for development on macOS.

1. Install Anaconda

Download and install Anaconda for macOS from the official website.

After installation, verify that Conda is available:

conda --version


If the command returns a version number, Conda is installed correctly.

2. Fix Conda PATH (If conda Is Not Found)

If conda --version does not work, follow these steps.

Check that Conda exists in the expected location:

ls /opt/anaconda3/bin/conda


Initialize Conda for zsh:

/opt/anaconda3/bin/conda init zsh


This will:

Modify ~/.zshrc

Enable conda activate automatically in zsh

Add Conda to your PATH

Reload the shell configuration:

source ~/.zshrc


Verify that Conda has been added to the PATH:

echo $PATH

3. Create and Activate a Virtual Environment

Create a Conda virtual environment with Python 3.10:

conda create -p venv python=3.10


Activate the environment:

conda activate ./venv


Install IPython kernel support (useful for notebooks and IDEs):

pip install ipykernel

4. Install Project Dependencies

Create a file named requirements.txt and add the libraries you need.

Example requirements.txt
scikit-learn


Install all dependencies listed in the file:

pip install -r requirements.txt

5. Install and Configure Visual Studio Code

Install Visual Studio Code.

Enable the code . command so you can open projects from the terminal:

Open VS Code

Press Cmd + Shift + P to open the Command Palette

Select:

Shell Command: Install 'code' command in PATH


Restart your terminal after completing this step.

6. Open the Project in VS Code

From your project directory, run:

code .


This will open the current folder in Visual Studio Code.

Notes

Make sure the Conda environment is activated before installing packages.

Always verify the Python version using:

python --version


