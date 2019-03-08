# Using Neural Networks to Identify Bird Species from Birdsong Samples

The files in this repository support the book chapter "Using Neural Networks to Identify Bird Species from Birdsong Samples" by Russell Houpt, Mark Pearson, Paul Pearson, Taylor Rink, Sarah Seckler, Darin Stephenson, and Allison VanderStoep. This work was done at Hope College between 2016 and 2018.

## Getting Started

- Sample code for creating scalograms from WAV files is in the Jupyter notebook `Making_Scalograms.ipynb`.

	- The inputs are a group of WAV files and a CSV file which lists the WAV files and some of their attributes.
	
	- The outputs are HDF5 files containing scalograms and snippets, and a few CSV files that list the WAV files in the training, validation, and testing sets.

- Sample code for creating convolutional neural networks is in the Jupyter notebook `CNN_Training.ipynb`.

	- The inputs are HDF5 files and CSV (which describe the original WAV files).
	
	- The outputs are HDF5 files that contain the neural network that was trained.

- Fgures in the book chapter are in the directory `Figures` together with a Jupyter notebook that generates most of them.  The source code for all figures is included.

### Installing

We outline how to install Ubuntu, ffmpeg, Anaconda Python, TensorFlow, and Keras.

- Install Ubuntu 18.04.2 LTS (Long Term Support)
	- [https://www.ubuntu.com/download/desktop](https://www.ubuntu.com/download/desktop)

- Install ffmpeg for converting MP3 files to WAV files
	- Open a terminal window `Ctrl-Alt-T`
	- In the terminal: `sudo apt-get install ffmpeg`

- Install Anaconda Python
	- Use a web browser to download Anaconda Python 3
		- [https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86_64.sh](https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86_64.sh)
	- In the terminal: `cd ~/Downloads`
	- In the terminal: `bash Anaconda3-2018.12-Linux-x86_64.sh`
	- When prompted by the installer, hit `Enter` to accept all of the defaults

- Install TensorFlow in a virtual environment named tf-cpu-conda
	- In the terminal: `conda create --name tf-cpu-conda tensorflow`
	- In the terminal: `conda activate tf-cpu-conda`

- Install Keras in the tf-cpu-conda virtual environment
	- In the terminal: `conda activate tf-cpu-conda`
	- In the terminal: `conda install keras`

- Install MatplotLib in the tf-cpu-conda virtual environment
	- In the terminal: `conda activate tf-cpu-conda`
	- In the terminal: `conda install matplotlib`

- Install a package in the tf-cpu-conda virtual environment that will make conda work well with Jupyter notebook 
	- In the terminal: `conda activate tf-cpu-conda`
	- In the terminal: `conda install nb_conda`

- Run Jupyter notebook
	- In the terminal: `conda activate tf-cpu-conda`
	- In the terminal: `jupyter notebook`
	- A web browser should open running Jupyter notebook
	- Create a new Jupyter notebook file
	- Check that everything is working properly by entering this in a Jupyter notebook cell
	
```
import sys
print(sys.version) # should say Anaconda
print(sys.executable) # should have ~/anaconda3/...
import tensorflow as tf # should not throw errors
import keras # should report that it's using the tensorflow backend
```

- Execute the contents of the Jupyter notebook cell by pressing `Ctrl-Enter` while the cursor is in the cell


## Running the Jupyter notebooks

Download the Jupyter notebooks from this github repository, follow the commands to Run Jupyter notebook (above), open a Jupyter notebook, and select `Kernel -> Restart & Run All` from the menu.

## Authors

* Russell Houpt, Mark Pearson, Paul Pearson, Taylor Rink, Sarah Seckler, Darin Stephenson, Allison VanderStoep

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Copyright

Copyright 2019 Russell Houpt, Mark Pearson, Paul Pearson, Taylor Rink, Sarah Seckler, Darin Stephenson, Allison VanderStoep.  All rights reserved.