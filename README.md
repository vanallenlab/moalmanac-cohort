# Standard cohort analyses for samples profiled with the Molecular Oncology Almanac
This repository includes a Jupyter notebook to execute a set of standard questions and figures that provide a descriptive summary of the clinical interpretation landscape for a given cohort, given that each profile has been processed with the [Molecular Oncology Almanac](https://github.com/vanallenlab/moalmanac).  

You can open `moalmanac-cohort.ipynb` and configure it to run with your own data by following the instructions to edit variables under the `Load data` and `Configuration` sections.

Currently, the notebook uses the [actionable.txt](https://github.com/vanallenlab/moalmanac/blob/main/docs/description-of-outputs.md#actionable) and [somatic.scored.txt](https://github.com/vanallenlab/moalmanac/blob/main/docs/description-of-outputs.md#somatic-scored) outputs from the Molecular Oncology Almanac.

The notebook currently addresses the following questions,
- How many patients are contained within this cohort?
- How many patients have genomic alterations?
- How many alterations does each patient have, by feature type?
- How many patients have at least one alteration assocaited with therapeutic sensitivity? resistance? disease prognosis?
- What percentage of patients have an association for therapeutic sensitivity per evidence type? What about cumulatively?
- What are the most common observed alterations, by feature type?
- What are the most common observed clinically relevant alterations, by feature type?
- What are the most common observed biologically relevant alterations, by feature type?
- What therapies are most commonly highlighted for therapeutic sensitivity? For resistance?
- Which alteration and therapy pairs are most commonly highlighted for therapeutic sensitivity? For resistance?

And the notebook also generates seven figures, 
- Patients with clinically relevant alterations, by feature type
- Associations by evidence for therapeutic sensitivity, resistance, and disease prognosis
- Counts of patients by evidence with at least one alteration associated with therapeutic sensitivity, resistance, and disease prognosis


# Installation
To use this repository, please follow these instructions to [download this repository from GitHub](#download-this-repository-from-github) and [install python dependencies](#install-python-dependencies) by setting up a virtual environment. 

## Download this repository from GitHub
This package can be downloaded through Github on the website or by using terminal. To download on the website, navigate to the top of this page, click the green `Clone or download` button, and select `Download ZIP`. This will download this repository in a compressed format. To install using Github on terminal, type 

```bash
git clone https://github.com/vanallenlab/moalmanac-cohort.git
cd moalmanac-cohort
```


## Install Python dependencies 
Code in this repository uses Python 3.10 and we recommend using a [virtual environment](https://docs.python.org/3/tutorial/venv.html) and running Python with either [Anaconda](https://www.anaconda.com/download/) or  [Miniconda](https://conda.io/miniconda.html). After installing Anaconda or Miniconda, you can set up by running

```bash
conda create -y -n moalmanac-cohort python=3.10
conda activate moalmanac-cohort
pip install -r requirements.txt
ipython kernel install --user --name=moalmanac-cohort
```

If you are using base Python, you can create a virtual environment and install dependencies by running:
```bash
virtualenv moalmanac-cohort
source activate moalmanac-cohort/bin/activate
pip install -r requirements.txt
```
