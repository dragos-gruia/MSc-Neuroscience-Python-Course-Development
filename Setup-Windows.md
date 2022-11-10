# Installing software on a Windows

## Step 1: Install Python

1. Check if you have Python installed by opening the `Command Line`. Then, type `Python` and press enter. If you get error it probably means that Python is not installed.
2. If that is the case, go to https://www.python.org/downloads/ and click on `Download Python`.
3. Go back to command line after Python is installed and type `Python` to check that the installation was done successfully.

## Step 2: Install Pip
Pip is a useful package manager which allows us to download all of the extra modules that we need to work with Python. 
1. Check if you have pip installed by typing `pip help` in the command line. If you get a message saying does not exist, it means you need to install pip.
2. To do this, go to this webpage and follow the steps https://phoenixnap.com/kb/install-pip-windows
3. DO NOT DOWNGRADE YOUR PIP VERSION

## Step 3: Install Jupyter Notebook
1. Now that you have pip, we can use that to install jupyter notebook. This is the place where will write and execute all the Python code. We chose this as it provides a very nice interface and it is easy to use if you are a beginner.
2. Open a terminal by selecting the `Command Line` app from the Windows Menu
2. Once the terminal (or command line) is open, write `pip install jupyter` and press `Enter`
3. To Open `Jupyter` simply type `jupyter notebook` and `Enter`, in `Command Line`
4. To create a new Notebook, click on New (upper right side of the screen) and select Python3 (ipykernel). You can now use this to write your own code. Type `print('Hello World')` and click the `Run` button. If you don't get any errors it means you are all set up and ready to go.
5. to install the packages you need, you have to write the following commands in one cell (or chunk of code) of the jupyer:

    `%%cmd`
    
    `pip install numpy pandas matplotlib`
  

## Step 4: Open the Lecture Materials
1. Open a terminal by selecting the `Command Line` app from the Windows Menu
2. Copy the following commands and press  `Enter ` at the end of each command

     `cd ~`

     `cd Desktop/`

     `git clone https://github.com/dragos-gruia/MSc-Neuroscience-Python-Course-Development.git`

     `cd MSc-Neuroscience-Python-Course-Development`
3. Once it is done downloading, type `jupyter notebook` and `Enter`. This should open a Jupyter interface.
4. If everything worked well, you should now be able to see and open the programming materials we created. To do so, press on the file called `Lecture1.ipnb` and start with the lectures.


## Extra resources

If you have never used Jupyter Notebook before, it might be useful going through this tutorial. This will teach you about its functionalities, and it will be of great help as you progress through the course.

https://www.dataquest.io/blog/jupyter-notebook-tutorial/


If you have any installation issue, write an email to Valentina Giunchiglia (v.giunchiglia20@imperial.ac.uk) AND Dragos Gruia (dragos-cristian.gruia19@imperial.ac.uk)

**IMPORTANT: There will be a 1 hour drop-in session on Thursday 6th October - 4.30PM to 5.30PM to help with any installation issues**
