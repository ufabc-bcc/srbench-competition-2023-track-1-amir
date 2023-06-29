# Symbolic Regression GECCO Competition - 2023 - Track 1 - Performance

Installation and execution instructions:
To run the code, you need to follow the installation and setup steps outlined below:  

Based on windows 10 version, Download anaconda, Julia and python 3.10.9 version

pip  
 1. Install anaconda, Julia, and python packages, and necessary libraries
   - Type "jupyter notebook" from anaconda prompt,
   - Connect Julia package from anaconda command prompt using Pkg, Pkg.add("IJulia") command to jupyter notebook. 
   - To install Julia dependencies, run: python -m pysr install    
   - Now from Jupyter notebook terminal, open ("file name").ipynb file
   - Install scikit-learn: pip install -U scikit-learn
   - Install numpy, pandas, matplotlib through pip command
   - Then install pysr library from jupyter notebook, for that run: pip install -U pysr  
   - import all the dependencies and libraries to run the (file name).ipynb file
   - now run the code and find R-Scquared score as well as find the best model with equation
  
 

Conda
The PySR build in conda includes all required dependencies, 
so you can install it by simply running: conda install -c conda-forge pysr
From within your target conda environment. However, note that the conda install does not support precompilation of Julia libraries, so the start time may be slightly slower as the JIT-compilation will be running. (Once the compilation finishes, there will not be a performance difference though)

Docker build 
1. Clone this repo.
2. In the repo, run the build command with: docker build -t pysr 
3. You can then start the container with an IPython execution with:
     docker run -it --rm pysr ipython

Common issues
	Common issues tend to be related to Python not finding Julia. To debug this, try running python3 -c 'import os; print(os.environ["PATH"])'. If none of these folders contain your Julia binary, then you need to add Julia's bin folder to your PATH environment variable.

Running PySR on macOS with an M1 processor: 
	you should use the pip version, and make sure to get the Julia binary for ARM/M-series processors.
