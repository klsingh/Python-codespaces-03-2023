# Installation of latest Python version in Codespaces and creation of virtual environment
## Steps to be followed (Use VSCODE ```Terminal``` in Codespaces to execute below steps). I have used Jupyter Notebook template available in Codespaces

```sudo apt-get install build-essential gdb lcov libbz2-dev libffi-dev libgdbm-dev liblzma-dev libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev lzma lzma-dev tk-dev uuid-dev zlib1g-dev ```  - Install libraries (you can install Python libararies of your choice)

```wget https://www.python.org/ftp/python/3.10.10/Python-3.10.10.tgz ``` - get the latest Python from Python.org website

```tar zxvf Python-3.10.10.tgz``` - command to un-compress tar file

```rm Python-3.10.10.tgz``` - command to remove the Python tar file imported from Python website in-order to save the space

```./configure --enable-optimizations``` - command to run the optimizations by entering into Python-3.10.10.tgz directory

```make -j 4 ``` - command to compile Python by utilizing all the 4 cores available to us. In your case number of cores may vary dpending upon your machine selection type.

```sudo make altinstall``` - command to install Python setup tools

```/usr/local/bin/python3.10``` - navigate to the dir to use our locally installed Python

```vim ~/.bashrc``` - to make Python-3.10.10 default enter in bashrc file 

```alias python="/usr/local/bin/python3.10" ``` - Once inside bashrc file enter this line which will point towards our Python-3.10.10 installation and make it default.


In bash file - the ```I``` button will enable you to edit the file, hit the ```Esc``` button to exit edit mode, then enter ```:wq ``` and press ```Enter``` button to quit and save bashrc file.


```source ~/.bashrc``` - to source the file so that Python-3.10.10 installed by us will always be loaded

```python -m venv ~/.venv``` - create virtual environment which will live in Python-3.10.10 dir

Go to  ```vim ~/.bashrc```  and enter  ```source ~/.venv/bin/activate``` - save the bash file and exit

## Once the above step is done we can see that every cell will have Python-3.10.10 version installed by us

```touch requirements.txt``` - create template for our project

```touch Makefile``` - create template for our project

## We can install ```ludwig``` AutoML tool or any other using command ```make install``` in the terminal by just entering the tool name in requirements.txt file

```git status``` - to check the current status of the working directory and the staging area

```git add " file name" ```

