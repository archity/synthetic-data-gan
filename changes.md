# Changes from original Colab Notebook

## Essential changes

* For installing ydata-synthetic lib
    * `!pip install ydata-synthetic` rather than `! pip install pip install git+https://github.com/ydataai/ydata-synthetic.git`
    * Previous GitHub repo link for installing lib throwing error in Google Colab as well as local notebook

* Saving the trained generator
    * Corrected path parameter to correctly save the model in pkl format
  
* In the final graph, the xlabel for the 'GAN' plot should also be V17 (more generally `col1`) rather than V1 (`data_cols[0]` -> `'V1'`).

## Non-essential changes

* Minor spelling/grammar changes
* More detailed comments added wherever necessary
* The final plot now plots according to the number of models in the list, and hence utilizes the figure space optimally.
  * `columns = 1 + len(models)` instead of hard-defining it as constant