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