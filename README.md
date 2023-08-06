# RNA_labeling_fluorogenic_photoaffinity
This repo contains companion code to the paper "Imaging and tracking RNA in live mammalian cells via fluorogenic photoaffinity labeling".

The script will generate red/green intensity plots, as well as analysis of areas under both curves and curve overlap/similarity.

### Data File Format
Input data files should be tab-separated text files with 1 header row and 3 columns for [position along the line, green-intensity, and red-intensity].  For example,
```
distance (um)	coilin-GFP	1x MGA-U6 : MGD2
0	29	80
0.2877	9.6154	62.1953
0.5754	48.1183	9.0454
0.8632	34.9704	8.1124
...
10.6457	36.4221	20.3886
10.9335	54.1203	81.0966
11.2212	94	90
```

## Usage Instructions

### Running on Google Colab [Recommended]
1. Click here: <a href="https://colab.research.google.com/github/gchenfc/RNA_labeling_fluorogenic_photoaffinity/blob/main/main.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
2. On the left-toolbar, click the "folder" icon to bring up the Files menu.
3. In the file-browser, `right click` anywhere -> `New Folder`.  Name it "data"
4. Mouse over "data" folder -> click the 3-dots on the right -> "Upload" -> Select all the files you want to upload (click-shift-click)
5. Edit the OPTIONS below as desired
6. On the top toolbar (File, Edit, View, Insert, ...) Click "Runtime -> Run all"
7. Download "results.zip" (you may need to click the "Refresh" icon in the "Files" left-toolbar)

### Running on your own computer

1. [Click here](https://github.com/gchenfc/RNA_labeling_fluorogenic_photoaffinity/archive/refs/heads/main.zip) to download this repository and unzip it.
2. Set up a python environment if you don't already have one.  [Anaconda](https://www.anaconda.com/download) is highly recommended.  See [Setting Up Jupyter Notebook using Anaconda](#setting-up-jupyter-notebook-using-anaconda) for a crash-course if you aren't familiar with Python environments or Jupyter notebooks.
3. Install dependencies:
     ```bash
     conda install numpy pandas scipy matplotlib jupyter
     ```

     - `numpy`: For working with numbers.
     - `pandas`: For working with tables.
     - `scipy`: For statistics (`f_oneway` is ANOVA).
     - `matplotlib`: For plotting.
     - `jupyter`: For the Jupyter Notebook interface.
4. Launch Jupyter Notebook:
     ```bash
     cd /path/to/github/repo/
     jupyter notebook main.ipynb
     ```
5. Create a folder in the same directory as main.ipynb called "data" and put all your data files in there.
6. Run through all the cells in the notebook.  You can do this by clicking the "Run" button on the top toolbar, or by pressing `Shift+Enter` on your keyboard.  The resulting plots will be saved in a folder called `results`.

---

## Setting Up Jupyter Notebook using Anaconda

### 1. Installing Anaconda:

1. **Download Anaconda:** Go to the official [Anaconda download page](https://www.anaconda.com/products/distribution#download-section).
   - For Windows and macOS users, you'll find graphical installers. Download the installer for Python 3.x.
   - For Linux users, you'll see a command to run in your terminal. Copy and run that command.

2. **Install Anaconda:**
   - **Windows:** Open the downloaded `.exe` file and follow the installation instructions.
   - **macOS:** Open the downloaded `.pkg` file and follow the installation instructions.
   - **Linux:** In your terminal, `cd` to the directory where you've downloaded Anaconda, then run `bash <downloaded_file_name>.sh` and follow the prompts.

3. **Verify Installation:** Open your terminal or command prompt and type `conda --version`. You should see the version of `conda` displayed.

### 2. Setting up an Anaconda Environment:

For command line users, type these into your terminal.  For graphical users, open the Anaconda application and use the command prompt inside there or use the equivalent buttons for creating and activating an environment.

1. **Create a new environment:** This is a good practice to keep your projects separate. You can name the environment whatever you want. For this guide, we'll name it `rna_labeling`.

```bash
conda create --name rna_labeling python=3.9
```

2. **Activate the environment:** Before installing packages or running Jupyter, you need to activate the environment.

```bash
# For Windows:
conda activate rna_labeling

# For macOS and Linux:
source activate rna_labeling
```

### 3. Installing Dependencies:

Once the environment is activated, install the necessary Python packages using `conda`:

```bash
conda install numpy pandas scipy matplotlib jupyter
```

- `numpy`: For working with numbers.
- `pandas`: For working with tables (optional).
- `scipy`: For statistics (`f_oneway` is ANOVA).
- `matplotlib`: For plotting.
- `jupyter`: For the Jupyter Notebook interface.

### 4. Launching Jupyter Notebook:

After installing the necessary packages, you can launch Jupyter Notebook:

```bash
cd /path/to/github/repo/
jupyter notebook main.ipynb
```

This should open a new tab in your default web browser with the Jupyter interface.  If it doesn't open automatically, look for a URL in your terminal that looks like `http://localhost:8888/?token=...` and paste it into your browser.

### 5. Running the Notebook:

Continue with the instructions [above](#running-on-your-own-computer).
