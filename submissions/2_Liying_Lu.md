# Assignment 2

## A. Working with Conda
1. Make a conda environment called python2 that's identical to your python3 environment except it uses Python 2.  
`conda -n python2 -c conda-forge python=2 jupyter`  

2. Practice activating and deactivating conda environments.  
    ```
    conda activate python2
    conda deactivate
    ```

3. Use conda install and pip install to install additional packages to your environment.
    ```
    conda install -c conda-forge scikit-learn

    # python2 env did not have the correct encoding, run the following lines before pip install
    set PYTHONIOENCODING=UTF-8
    pip install requests
    ```

4. List your conda environments.  
`conda env list` 

5. List the packages installed in one of your environments.  
`conda list`

6. Optional: If you are familiar with R, create an environment and install the R kernel using the instructions here.  
I installed R kernel.
    ```
    # step 1: install r package in a R console via CRAN
    install.packages('IRkernel')

    # step 2: Making the kernel available to Jupyter
    ## Open Anaconda Prompt, look up the executable of R (C:\Program Files\R\R-3.5.1\bin). Start R by typing R. Then type one of the following command. 
    ## The kernel spec can be installed for the current user with the following line from R:
    IRkernel::installspec()

    ## To install system-wide, set user to False in the installspec command:
    IRkernel::installspec(user = FALSE)

    # step 3: Make useful shortcuts available
    ## Install nodejs if the environment does not already have it:
    # conda install -c conda-forge nodejs
    # install shortcut below:
    jupyter labextension install @techrah/text-shortcuts
    ```

7. Optional: If you are familiar with QIIME, create an environment and install QIIME using the instructions here.  
I did not install QIIME.

## B. IPython command-line interpreter and Python basics  

1. Activate your python2 conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and `print('Hello, world')`. Do they both work?
    ```
    D:\liying\!working\GitHub\python-for-data-analysis>conda activate python2

    (python2) D:\liying\!working\GitHub\python-for-data-analysis>python
    Python 2.7.15 (default, Mar  5 2020, 14:56:45) [MSC v.1500 64 bit (AMD64)] on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>> print 'Hello world'
    Hello world
    >>> print('Hello, world')
    Hello, world
    ```
2. Activate your python3 conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and `print('Hello, world')`. Do they both work?
    ```
    (python3) D:\liying\!working\GitHub\python-for-data-analysis>python
    Python 3.8.12 (default, Oct 12 2021, 03:01:40) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>> print 'Hello, world'
    File "<stdin>", line 1
        print 'Hello, world'
            ^
    SyntaxError: Missing parentheses in call to 'print'. Did you mean print('Hello, world')?
    >>> print('Hello, world')
    Hello, world
    ```

3. Pick 3 of the 8 sections in Data Types we covered in Lesson 4: booleans, numbers, strings, lists, tuples, arrays, sets, and dictionaries. Using the IPython interpreter in your python3 environment, type and run the commands we used in those sections of Lesson 4.

    ```
    >>> # strings
    >>> s = 'Hello, world'
    >>> type(s)
    <class 'str'>
    >>> s[0:4]
    'Hell'
    >>> s + '!'
    'Hello, world!'
    >>> s
    'Hello, world'
    >>> s = s + '!'
    >>> s
    'Hello, world!'
    >>> # arrays (NumPy)
    >>> import math
    >>> import numpy as np
    >>> mylist = [0, 2, 4]
    >>> np.array(mylist)
    array([0, 2, 4])
    >>> np.zeros(5)
    array([0., 0., 0., 0., 0.])
    >>> np.arange(5)
    array([0, 1, 2, 3, 4])
    >>> np.arange(4, 10)
    array([4, 5, 6, 7, 8, 9])
    >>> np.arange(0, 10, 2)
    array([0, 2, 4, 6, 8])
    >>> np.linspace(0, 10, 20)
    array([ 0.        ,  0.52631579,  1.05263158,  1.57894737,  2.10526316,
            2.63157895,  3.15789474,  3.68421053,  4.21052632,  4.73684211,
            5.26315789,  5.78947368,  6.31578947,  6.84210526,  7.36842105,
            7.89473684,  8.42105263,  8.94736842,  9.47368421, 10.        ])
    >>> np.random.rand()
    0.3259804923138211
    >>> np.random.rand(5)
    array([0.29023713, 0.81485877, 0.32639741, 0.47124626, 0.02579474])
    >>> # sets
    >>> s1 = {'a', 'b', 'c'}
    >>> s2 = {'a', 'd', 'e'}
    >>> s1 & s2
    {'a'}
    >>> s1 | s2
    {'a', 'e', 'd', 'c', 'b'}
    >>> l = [0, 1, 1, 2, 3, 5, 8]
    >>> m = [5, 2, 'a', 'xxx', True, [0, 1]]
    >>> s3 = set(l)
    >>> s4 = set(m[0:2])
    >>> s3
    {0, 1, 2, 3, 5, 8}
    >>> s4
    {2, 5}
    >>> s3 & s4
    {2, 5}
    >>> s3 | s4
    {0, 1, 2, 3, 5, 8}
    >>> s3 - s4
    {0, 1, 3, 8}
    ```

## C. Working with Jupyter notebooks

1. Activate your python2 conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?  
I can create a Python 2 or R Notebook. `python --verion` shows that my Python version is 2.7.15

2. Activate your python3 conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?  
Python 3.8.12

3. Pick 1 of the 4 sections in Loops and Control Structures we covered in Lesson 4: boolean and comparison operations, if tests, while loops, and for loops. Using a Jupyter notebook in your python3 environment, type the code from that section in one or more cells, then run those cells. Put a header above the code cell using a Markdown cell. Practice creating, deleting, and moving cells using the keyboard shortcuts.
I did not install QIIME.
