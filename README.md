# stanford-music-364
Guest lecture for Music 364, CCRMA, Stanford University, with Blair Kaneshiro.

**Title: Feature Extraction and Classification of Musical Signals**

Date: 2017 January 27, 12:30-2:20 pm

[Music 364 Course Website](https://ccrma.stanford.edu/courses/364/)

## Goals

1.  Address the broad question: how do we teach computers to understand music?
2.  Inspect some specific tasks in music information retrieval (MIR):
    -   genre classification
    -   song structure and form
3.  Write basic systems in Python to accomplish these MIR tasks.

## Outline

1.  Audio Representation
    -   Time Domain
    -   Frequency Domain
2.  Segmentation
3.  Feature Extraction
    -   zero-crossing rate
    -   spectral moments (centroid, etc.)
4.  Feature Analysis with Pandas
    -   reading a DataFrame
    -   feature correlation
    -   visualization
5.  Genre Classification
    -   brief literature review of existing approaches
    -   K-NN using scikit-learn
6.  Song Structure/Form
    -   brief literature review of existing approaches
    -   relevant features, e.g. chroma, MFCCs
    -   K-means clustering using scikit-learn

## Software Prerequisites

Git is *not* required for this lecture and assignment. However, those who *do* know Git may find it convenient to clone this repository onto their computers.

### IPython, scikit-learn, pandas

Install Python 2 and relevant libraries. Your system may already have Python 2.

If you’re totally new, the simplest solution is to download and install [Anaconda for Python 2 (2.7)](https://www.continuum.io/downloads), not Python 3. If you can do the following without errors, then you’re set:

- Run the IPython shell. 
    -   For Mac, at the Terminal: `ipython`. 
    -   For Windows, open the application "IPython".
    Type `exit` to exit.
- Run the IPython/Jupyter notebook. 
    -   For Mac, at the Terminal: `jupyter notebook`.
    -   For Windows, open the application "Jupyter Notebook". Alternatively for Windows: open the application "Anaconda Prompt" and type in `jupyter notebook`.
- In the IPython shell, run `import scipy, sklearn, pandas`. If that runs without error, congratulations, you are set.

Immediately after installing, if something doesn’t work, try closing the terminal or restarting the OS. Sometimes that can reset the necessary configurations.

### Librosa

Librosa is a Python library for audio and music analysis.

1.  [Install Librosa.](https://github.com/librosa/librosa#installation) In short:

        pip install librosa

    Mac users will enter this command in the Terminal; Windows users will enter this command from the Anaconda Prompt. If that doesn't work, try:

        conda install -c conda-forge librosa

2.  Follow the [tutorial quickstart](http://librosa.github.io/librosa/tutorial.html#quickstart). If you can execute these lines in particular:

        import librosa
        filename = librosa.util.example_audio_file()
        x, fs = librosa.load(filename)

    then you are in good shape.

More information:
-   [Documentation](http://librosa.github.io/librosa/)
-   [GitHub](https://github.com/librosa/librosa)
-   [Tutorials](https://github.com/librosa/tutorial)

