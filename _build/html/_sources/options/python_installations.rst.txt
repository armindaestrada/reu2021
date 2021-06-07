Python Installation
+++++++++++++++++++++
.. warning:: Before installing Python make sure to find the correct operating sytem you will be installing it in. 

Ubuntu 20.04
---------------
Ubuntu 20.04 has Python 3 pre-installed. We need to make sure that the version is up to date. 
First let’s update and upgrade the system 
::
    sudo apt update
    sudo apt -y upgrade

Check the pre-installed version 
::
    python3 -V

To manage software packages for python install pip. 
::
    sudo apt install -y python3-pip

Using pip commands you are able to install python packages. Such as: 
::
    pip3 install numpy


Windows 10
------------
1. Download through the `Official Python Website. <https://www.python.org/downloads/>`_
    You will need to select the operating system and download the installation. 
    Go through the interactive installation. 
2. Select "Install launcher for all users (recommended)" and "Add Python to path" 
3. Click on "Customize Installation". 
4. Make sure all the optional features are selected and click next. 
5. Make sure all advanced options are selected and click next. 
6. Once you get the setup successful screen click done. 
7. Verify installation by opening the ``command prompt`` and typing ``python --version``. 


MacOS
---------
1. Download through the `Official Python Website. <https://www.python.org/downloads/>`_
    You will need to select the operating system and download the installation. 
    Go through the interactive installation. 
2. Click next on the screen and authorize the installation until the "Congratulations!" screen appears. (You may chose to move the python installer to trash once prompted). 
3. Open a ``terminal`` window and check it has been installed using ``python --version``. 