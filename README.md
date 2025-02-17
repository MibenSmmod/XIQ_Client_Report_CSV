# HistoricalClient_csvtoexcel.py


## Requirements

This script was written to work with python version 2.7 that comes installed default with mac os as well as the new version of python 3.9 if installed manually. To preform the needed tasks to read the csv and and export to excel a couple modules will need to be installed.  
These modules are needed in order to run this script. Please see the Setup Section at the bottom for instructions on installing the needed module. 

When running the script, two arguments need to be give

1. The name of the site the report will be generated for. The name of the site should be added within quotes. ```"Retail Store 1234"```
2. The name of the csv file that is located in the same directory as the HistoricalClient_csvtoexcel.py script.


## How to run the script

### MAC OS
To run the script use terminal and go to the directory the script is in. Make sure the downloaded csv file is in the same directory, then run the script with the needed arguements.
```
python HistoricalClient_csvtoexcel.py "<site name>" <csv file>
```
### Windows 10
To run the script use PowerShell and go to the directory the script is in. Make sure the downloaded csv file is in the same directory, then run the script with the needed arguements.
```
python.exe .\HistoricalClient_csvtoexcel.py "<site name>" .\<csv file>
```
## Setup

### MAC OS
pip can be used to install modules but that will need to be installed on the mac if it currently is not. 

To check if pip is currently installed, in Terminal run ```pip --version```. If pip is installed a version number will be in the response. If pip is not installed it can be installed by running ```curl https://bootstrap.pypa.io/pip/2.7/get-pip.py -o get-pip.py``` followed by ```sudo python get-pip.py```

> credit [blog](https://ahmadawais.com/install-pip-macos-os-x-python/) - can view for more detailed instructions

Once pip is installed, you can install the needed modules located in the requirements.txt file. Navigate in the termial to the folder containing the script and requirements.txt file. To install these modules from the requirements.txt file enter:
```
pip install -r requirements.txt
``` 

### Windows 10
Install python from the Microsoft Store (tested with python 3.9). This will also install pip
Open Windows PowerShell and navigate to the to the folder containing the script and requirements.txt file. To install these modules from the requirements.txt file enter:
```
pip install -r .\requirements.txt
```

# Running an EXE to make this process more simple
### Option 1
Download the EXE to your Windows machine and put the CSV file in the same folder and follow the prompts

### Option 2
Run the EXE on a Mac utilizing an application called CrossOver: https://www.codeweavers.com/crossover
1) Download the EXE to your downloads folder
2) Open CrossOver app
3) Press:  Install - bottom left corner
4) Click "Install an unlisted application" since this is not a native supported EXE we're trying to run
5) Press Edit: "You will need to provide the installer file or disk in order to install this software using CrossOver"
    - Browse and select:  XIQHistoricalReport.exe
    - Press: Choose Installer
6) Press Edit:  "You will need to select the bottle to install this software into"
    - This will be in a New Bottle...
    - New Bottle Name:  XIQ Client Report
    - Choose New Bottle Type:  Windows 10 64-bit
    - Press:  DONE
7) Press:  Install

A application window will popup and run the script...
8) Press X to close the application window and CrossOver will complete the install
9) Your new XIQ Client Report bottle is listed on the left column; it should be selected
10) Press:  Open C: Drive
11) Copy your EXE into the root of the C: drive of your bottle
12) Rename the file to XIQ.exe for simplicity
13) Copy your XIQ Report into the root of the C: drive and rename to XIQ.csv
Both the EXE and CVS should be in the root of the C: drive in your XIQ Client Report Bottle

14) Go back to CrossOver app > press:  Run Command
15) Type:  c:\XIQ.exe
16) Press:  Save Command as a Launcher
17) Press X to close Run Command window
18) Double left click XIQ icon to launch script
Prompts:
- Please enter Location name:  My Library
- Please enter the name of the Statistics Summary file:  XIQ.csv  <- This file can't be touched by Excel or it will error
- Window should close after it completes
19) Go back to the drive_c Finder window and find your XIQ.xlsx

Copy that file out of the bottle and you're complete
