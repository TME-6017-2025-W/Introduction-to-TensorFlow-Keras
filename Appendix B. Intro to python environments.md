# week-2-fundamentals-of-computer-vision

## Creating a Python Virtual Environment
1. First, make sure you have Python3 package installed on your system (3.9 or higher recommended). You can check if they are installed by running the following commands:

~~~
python3 --version
~~~

2. To create a virtual environment, navigate to the desired directory in the command line and run the following command (For this course I recommend having a venv folder at the root of the course folder). Give the virtual environment a useful name such as envwktwo or opencv-env:
~~~
python3 -m venv <myenv>
~~~

3. The command above will create a new directory called "myenv" in your current directory, which will contain all the necessary files for your virtual environment. You can replace "myenv" with any other name you prefer.

4. To activate the virtual environment, run the following command:

~~~
source myenv/bin/activate
~~~

5. Once the virtual environment is activated, you should see the name of the environment in the command line, indicating that it is currently in use.

6.To deactivate the virtual environment, simply run the command:

~~~
deactivate
~~~

7. You can also delete the virtual environment by removing the myenv folder.

8. To install packages inside the virtual environment, after activating the environment you can use pip install as usual.

~~~
pip install package_name
~~~

With these steps, you should have a working virtual environment for Python. This allows you to have different versions of packages and dependencies for different projects without interfering with each other.

## Installing Packages from a requirements.txt File
This is useful when cloning repo, as is prevents managing specific package installations.  If creating your own repo, see below for instructions on how to generate the **`requirements.txt`** file 

1. Clone the repository to your local machine using git:

~~~
git clone https://github.com/<username>/<repo_name>.git
~~~

2. Navigate to the cloned repository:

~~~
cd repo_name
~~~

3. Create a virtual environment (if you haven't already) by running the following command:

~~~
python3 -m venv <myenv>
~~~

4. Activate the virtual environment:

~~~
source myenv/bin/activate
~~~

5. Install the packages listed in the requirements.txt file by running the following command:

~~~
pip install -r requirements.txt
~~~

6. Verify that the packages have been installed by running **`pip freeze`**. You should see a list of the packages and their versions, similar to what is listed in the requirements.txt file.

7. Once you finished your work in the environment, you can deactivate it by running
~~~
deactivate
~~~

## Intstalling basic python packages & OpenCV

1. With the virtual environment activated, upgrade pip before installation

~~~
pip3 install --upgrade pip
~~~

2. Now install some basic python packages

~~~
pip install numpy
pip install pandas
pip install scipy matplotlib
pip install scikit-learn scikit-image
~~~

3. When it comes to install OpenCV there is the base package (install one or the other, not both):
~~~
pip install opencv-python
~~~
Then there is an installation with additional modules (recommended):
~~~
pip install opencv-contrib-python
~~~
See <https://pypi.org/project/opencv-contrib-python> for details


## Installing Jupyter and Jupyter lab
[Jupyter](https://jupyter.org/) is an interactive environment for python.

To install in your active virtual environment run:
~~~
pip install jupyter jupyterlab
~~~


## Generate or update `requirements.txt` file and add to repository

1. Activate the virtual environment that you want to generate a requirements.txt file for.

2. Navigate to the root of the repository

3. Run the following command to generate the requirements.txt file:

~~~
pip freeze > requirements.txt
~~~
This will add the file in the current working directory, and also overwrite it, if it already exists.

You can also use `pip freeze --local > requirements.txt` to ensure that only packages that were installed in your virtual environment are included in the file.

4. Add this file to git and commit the changes


## Set virtual env as python interpreter

1. Open PyCharm and create a new project or open an existing one.

2. In the PyCharm menu, go to `File > Settings` (or `Preferences` on macOS).

3. In the settings window, navigate to Project: `project_name > Project Interpreter`.

4. In the project interpreter section, click on the gear icon and select `Add...`

5. Select `Virtualenv Environment` and `click OK`.

6. In the `New environment` section, select the `Existing environment` option.

7. In the `Interpreter` field, click on the folder icon and navigate to the location of the virtual environment's python executable. For example, if you created the virtual environment with the command `python3 -m venv myenv`, then you should find the python executable in the myenv/bin directory.

8. Click `OK` to save the changes.

9. PyCharm will now recognize the virtual environment and use it as the Python interpreter for the project. You can confirm this by checking that the name of the virtual environment is displayed next to the project interpreter in the settings window.

By following these steps, you should have set the virtual environment as the Python interpreter in PyCharm. This will allow you to use the packages and dependencies installed in the virtual environment for your project, and it will also prevent any conflicts with other projects.

# Now we can finally get started!
## Working with Jupyter Notebooks
It's worth taking some time to get acquainted with the Jupyter environment as it makes working with python for image and data much more convenient than running python script.
This is my opinion, but is a very marketable skill to put on your CV.

[Here](https://www.youtube.com/watch?v=5pf0_bpNbkw) is a videos that you might find helpful to explain how jupyter works.  (Remember you can always speed these videos up for a faster review)

## Notebooks in this repo
All you need to do to run a notebook in Jupyterlab is make sure you virtual environment is active and that your terminal is at the root folder of the repo.
Then you can run the command:
~~~
jupyter lab
~~~
You will see that a Jupyter Server has been started with links to open the lab environment in a web browser.
Click on the local host link.

Once you are in the browser you can open up the different Jupyter Notebooks in this repo:
1. OpenCV-Mathematical Operations.ipynb
2. OpenCV-Image Annotation.ipynb
3. OpenCV-image Capture.ipynb

There is also a separate file `ASSIGNMENT WK2.md` outlining the details of this weeks assignment.
