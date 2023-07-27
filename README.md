# RNA_labeling_fluorogenic_photoaffinity
This repo contains companion code to the paper "Imaging and tracking RNA in live mammalian cells via fluorogenic photoaffinity labeling".

Please refer to the code file [main.ipynb](main.ipynb), which contains instructions to run the code for performing the statistical analyses.

The script will generate a bunch of plots in a folder called `results`.

Data files are tab-separated text files with 1 header row and 3 columns for [position along the line, red-intensity, and green-intensity].  For example,
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
