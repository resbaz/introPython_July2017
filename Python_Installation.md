# Installing Python

This is guide for those trying to install Python for the first time, or who already have Python installed and want to install the required packages for the July 2017 Beginner's Python Workshop

The options are:
- Installing through Anaconda - for those people who aren't concerned about space/memory requirements on their computers. Installs base Python along with a number of useful packages.
- Miniconda - installs base Python, and allows the user to control which packages to install. Good for people with limited space.
- Package specific - for those who use pip to install Python

## Installing Python with Anaconda

Anaconda is a Python distribution platform which allows you to install and manage up to 720 different Python packages through the Anaconda installer, `conda`. If you have at least 400MB of free space on your laptop, then I would recommend using this, as it will automatically install many of the packages that you will find useful for your research and future coding. 

Just navigate to the [Anaconda home page](https://www.continuum.io/downloads) and follow the instructions to download Python version 3.6 for your Windows, Mac or Linux device. 

For windows devices - if you are not sure and are using windows 7, 8, 9 or 10, then download the 64-bit exe installer.

Please ensure that you allow Anaconda to set the default Python `path` on your device. This means that, if you already have Python installed (as MacOS does natively), you are allowing Anaconda to use it's own version of Python - and the associated packages - when you are coding. If you change this option you will run into errors when trying to use your packages, and in particular, when trying to run the jupyter notebook required for this workshop.


## Installing Python Through Miniconda

This is the better option for people with limited memory left on their device. This option will install base Python onto your device, and allows you to install specific packages according to your requirements.  

### Windows Installation

1) Download the `python 3 exe installer` from https://conda.io/miniconda.html (If you are not sure and you are using windows 7, 8, 9 or 10, then download the 64-bit exe installer)

2) Run the exe installer and install using default choices.  By clicking next.  (The installation might take a few minutes if the computer is slow, you can click "Show Details" to see the installation progress.

3) When installation is complete, find and open a program called `Select Anaconda Prompt` from the Windows Start Menu. 

This will open a new window with a black background (it might keep blinking if the computer is slow).  Wait until you can start typing

4) Type `conda install jupyter numpy matplotlib` and hit `ENTER` key.  When asked do you want to proceed, type `y` and hit `ENTER`.

   This will take a few minutes to download the jupyter, numpy and matplotlib packages. 
   
    If you wish to install more packages in the future, you just need to use the `conda install <package name>` from your command line.

5) To view a list of packages and versions installed, or to confirm that a package has been added or removed, type `conda list`. Confirm that jupyter, numpy and matplotlib packages have been installed

6) The workshop will be using jupyter notebooks. When you open Jupyter, the directory in which you are currently located becomes the "home directory" for Jupyter. To change this home directory (preferably to C:/ drive, or your user folder), in your command line you enter  `cd C:\Users\myUsername`, or `cd <file path to navigate to>`

7) Once you have navigated to your preferred file location, type `jupyter-notebook` and press `ENTER` key. This will start jupyter notebook in the default browser.  It might open in Internet Explorer.  If you prefer to use Chrome or Firefox, then you need to change the windows settings to use Chrome or Firefox as the default browser. If this does not open automatically, you can copy the "local host" URL on your command line to a new browser tab.

This instance of jupyter notebooks is running through your command line, and closing your command terminal will also terminate your Jupyter session. Alternatively, if you wish to exit Jupyter through the command line, use `ctrl-C`.

8) If you need to uninstall miniconda for any reason, you can do this through "Add or remove Program" in the control panel, by removing "Python 3.6(Miniconda)"


### OS X Setup

1) In your browser download the Python 3.6 Miniconda installer for OS X from https://conda.io/miniconda.html, then in your terminal window type the following:

`bash Miniconda3-latest-MacOSX-x86_64.sh`

2) Follow the prompts on the installer screens. If unsure about any setting, simply accept the defaults as they all can be changed later. After installation is complete, close your terminal window.

3) Re-open your terminal window, and type `conda --version` into the command terminal to test that miniconda has been installed. Conda should respond with the version number that you have installed, like: conda 3.11.0

NOTE: If you see an error message, check to see that you are logged into the same user account that you used to install Anaconda or Miniconda, and that you have closed and re-opened the terminal window after installing it.

4) Type `conda install jupyter numpy matplotlib` and hit `ENTER` key.  When asked do you want to proceed, type `y` and hit `ENTER`. If you wish to install more packages in the future, you just need to use this `conda install <package name>` from your command line.

5) To view a list of packages and versions installed, or to confirm that a package has been added or removed, type `conda list`. Confirm that jupyter, numpy and matplotlib have been installed

6) The workshop will be using jupyter notebooks. When you open Jupyter, the directory in which you are currently located becomes the "home directory" for Jupyter. To change this home directory (preferably to C:/ drive, or your user folder), in your command line you enter  `cd C:\Users\myUsername`, or `cd <file path to navigate to>`

7) Once you have navigated to your preferred file location, type `jupyter-notebook` and press `ENTER` key. This will start jupyter notebook in the default browser.  It might open in Safari.  If you prefer to use Chrome or Firefox, then you need to change the settings to use Chrome or Firefox as the default browser. If this does not open automatically, you can copy the "local host" URL on your command line to a new browser tab. 

This instance of Jupyter Notebooks is running through your command line, and closing your command terminal will also terminate your Jupyter session. Alternatively, if you wish to exit Jupyter through the terminal, use `command-C`.

8) If you need to uninstall miniconda for any reason, open a terminal window and remove the entire miniconda install directory by typing: `rm -rf ~/miniconda` 

You may also edit ~/.bash_profile and remove the miniconda directory from your PATH environment variable, and remove the hidden .condarc file and .conda and .continuum directories which may have been created in the home directory with: `rm -rf ~/.condarc ~/.conda ~/.continuum`

### Linux Installation

1) In your browser download the Python 3.6 Miniconda installer for OS X from https://conda.io/miniconda.html, then in your terminal window type the following:

`bash Miniconda3-latest-Linux-x86_64.sh`

2) Follow the prompts on the installer screens. If unsure about any setting, simply accept the defaults as they all can be changed later. After installation is complete, close your terminal window.

3) Close and re-open your terminal window. Type `conda --version` into the command terminal to test that miniconda has been installed. Conda should respond with the version number that you have installed, like: conda 3.11.0

4) Type `conda install jupyter numpy matplotlib` and hit `ENTER` key.  When asked do you want to proceed, type `y` and hit `ENTER`. If you wish to install more packages in the future, you just need to use this `conda install <package name>` from your command line.

5) To view a list of packages and versions installed, or to confirm that a package has been added or removed, type `conda list`. Confirm that jupyter, numpy and matplotlib have been installed

6) The workshop will be using jupyter notebooks. When you open Jupyter, the directory in which you are currently located becomes the "home directory" for Jupyter. To change this home directory (preferably to C:/ drive, or your user folder), in your command line you enter  `cd C:\Users\myUsername`, or `cd <file path to navigate to>`

7) Once you have navigated to your preferred file location, type `jupyter-notebook` and press `ENTER` key. This will start jupyter notebook in the default browser.  It might open in Safari.  If you prefer to use Chrome or Firefox, then you need to change the settings to use Chrome or Firefox as the default browser. If this does not open automatically, you can copy the "local host" URL on your command line to a new browser tab. 

This instance of Jupyter Notebooks is running through your command line, and closing your command terminal will also terminate your Jupyter session. Alternatively, if you wish to exit Jupyter through the terminal, use `command-C`.

8) If you need to uninstall miniconda for any reason, open a terminal window and remove the entire miniconda install directory: `rm -rf ~/miniconda`. 

You may also edit `~/.bash_profile` and remove the miniconda directory from your PATH environment variable, and remove the hidden .condarc file and .conda and .continuum directories which may have been created in the home directory with `rm -rf ~/.condarc ~/.conda ~/.continuum`.


## pip Installation for Advanced Users

As an existing Python user, you may wish to install Jupyter using Python’s package manager, pip, instead of Anaconda.

Jupyter installation requires Python 3.3 or greater, or Python 2.7. Please ensure you have these installed first before proceeding. 

1) Ensure that you have the latest pip; older versions may have trouble with some dependencies: `pip3 install --upgrade pip`
(Use `pip` instead of `pip3` if using legacy Python 2.)

2) Install the Jupyter Notebook using: `pip3 install jupyter numpy matplotlib` (Use `pip` instead of `pip3` if using legacy Python 2). Close and re-open your terminal window.

3) The workshop will be using jupyter notebooks. When you open Jupyter, the directory in which you are currently located becomes the "home directory" for Jupyter. To change this home directory (preferably to C:\ drive, or your user folder), in your command line you enter  `cd C:\Users\myUsername`, or `cd <file path to navigate to>`

4) Once you have navigated to your preferred file location, type `jupyter-notebook` and press `ENTER` key. This will start jupyter notebook in the default browser.  If you prefer to use a different internet rowser, such as Firefox, then you need to change the default settings to use this as the default browser. If this does not open automatically, you can copy the "local host" URL on your command line to a new browser tab.
