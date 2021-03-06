# recognizerAI


[![](http://www.bu.edu/asllrp/SignStream/screenshots/ss2-screen.gif)](http://www-i6.informatik.rwth-aachen.de/~dreuw/download/021.avi)

Another [AIND](https://www.udacity.com/course/artificial-intelligence-nanodegree--nd889) project, that uses American Sign Language data from Boston University to a **Hidden Markov Machine (HMM)**, leveraging our understanding of **Probabilistic Models**, **Bayesian Networks**, and **Statistics**:  


## Data 

The data in the `data/` directory was derived from 
the [RWTH-BOSTON-104 Database](http://www-i6.informatik.rwth-aachen.de/~dreuw/database-rwth-boston-104.php). 
The handpositions (`hand_condensed.csv`) are pulled directly from 
the database [boston104.handpositions.rybach-forster-dreuw-2009-09-25.full.xml](boston104.handpositions.rybach-forster-dreuw-2009-09-25.full.xml)

The three markers are:

*   0  speaker's left hand
*   1  speaker's right hand
*   2  speaker's nose
*   X and Y values of the video frame increase left to right and top to bottom.

Take a look at the sample [ASL recognizer video](http://www-i6.informatik.rwth-aachen.de/~dreuw/download/021.avi)
to see how the hand locations are tracked.

The videos are sentences with translations provided in the database.  
For purposes of this project, the sentences have been pre-segmented into words 
based on slow motion examination of the files. These segments are provided in the `train_words.csv` and `test_words.csv` files in the form of start and end frames (inclusive)

The videos in the corpus include recordings from three different ASL speakers.
The mappings for the three speakers to video are included in the `speaker.csv` 
file.


## Setup

This project requires **Python 3** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [SciPy](https://www.scipy.org/)
- [scikit-learn](http://scikit-learn.org/0.17/install.html)
- [pandas](http://pandas.pydata.org/)
- [matplotlib](http://matplotlib.org/)
- [jupyter](http://ipython.org/notebook.html)
- [hmmlearn](http://hmmlearn.readthedocs.io/en/latest/)

It is highly recommended that you install the [Anaconda](http://continuum.io/downloads) distribution of Python, which includes most of these packages. There have been issues with using the default `hmmlearn` package, so do install the development version from Github if you have any probelms. 

```sh
pip install git+https://github.com/hmmlearn/hmmlearn.git
```

## Model

They entire approach is explored in the notebook `asl_recognizer.ipynb`, with additional support from other modules in the directory (especially `my_model_selectors.py`).

From a terminal or command window, please run the following command from the top level directory to get started:
    `jupyter notebook asl_recognizer.ipynb`
