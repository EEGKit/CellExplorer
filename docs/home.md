![Cell Explorer](https://buzsakilab.com/wp/wp-content/uploads/2019/11/Cell-Explorer-example.png)

The Cell Explorer is a graphical user interface and a standardized pipeline for exploring and classifying spike sorted single units acquired using extracellular electrodes, like silicon probes or tetrodes.

Please use the right hand menu to navigate the documentation for the Cell Explorer.

### Installation
Download the repository and add it to your Matlab setpath. The pipeline uses CCGHeart.c. to calculate the CCGs. Compiled versions are included for Windows and Mac. If you are using Linux you have to compile the script. In Matlab, go to Cell-Explorer/calc_CellMetrics/CCG/ and run this line:

`mex -O CCGHeart.c`

The Cell Explorer GUI and pipeline have uses six toolboxes (four required toolboxes are included in the repository in the folder toolboxes, and two Matlab toolboxes must be installed manually).

**Toolbox dependencies**
* [GUI Layout toolbox](https://www.mathworks.com/matlabcentral/fileexchange/47982-gui-layout-toolbox) (Graphical elements in Cell Explorer)
* [JSONLab Matlab toolbox](https://www.mathworks.com/matlabcentral/fileexchange/33381-jsonlab-a-toolbox-to-encode-decode-json-files) (required for db tools)
* [UMAP Matlab toolbox](https://www.mathworks.com/matlabcentral/fileexchange/71902-uniform-manifold-approximation-and-projection-umap) (clustering in Cell Explorer)
* [IoSR Matlab Toolbox](https://github.com/IoSR-Surrey/MatlabToolbox) (lfp filtering in pipeline)
* [Curvefit Matlab toolbox](https://www.mathworks.com/help/curvefit/index.html?s_cid=doc_ftr) (ACG fit in pipeline; install manually)
* [Signal Processing Toolbox ](https://www.mathworks.com/help/signal/index.html?s_tid=CRUX_lftnav) (gausswin; install manually)

### Try the Cell Explorer with example data
There is an example dataset included in the repository. Load the mat-file ['cell_metrics_batch.mat'](https://github.com/petersenpeter/Cell-Explorer/tree/master/exampleData) into Matlab and type:

`CellExplorer('metrics',cell_metrics).`

### Tutorial for running the pipeline on your data
There is a [tutorial script: CellExplorer_Tutorial.m](https://github.com/petersenpeter/Cell-Explorer/blob/master/CellExplorer_Tutorial.m) included for running the pipeline on your data.

### Please use below DOI for citing the Cell Explorer in your research and publications:

The Cell Explorer: a graphical user interface and a standardized pipeline for exploring and classifying single cells. By Peter C. Petersen and György Buzsáki. 2019.

<a href="https://zenodo.org/badge/latestdoi/152647739"><img src="https://zenodo.org/badge/152647739.svg" alt="DOI"></a>
