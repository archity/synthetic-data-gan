## Essential changes

* [x] For installing ydata-synthetic lib
    * `!pip install ydata-synthetic` rather than `! pip install pip install git+https://github.com/ydataai/ydata-synthetic.git`
    * Previous GitHub repo link for installing lib throwing error in Google Colab as well as local notebook

* [x] Saving the trained generator
    * Modify `path` parameter to correctly save the model in pkl format
        * `synthesizer.save('./saved/gan', 'generator_fraud')` -> `synthesizer.save(path="./saved/gan/generator_fraud.pkl")`
  
* [x] For the final graph: 
  * the xlabel for the 'GAN' plot should also be V17 (more generally `col1`) rather than V1
    * `data_cols[0]` -> `col1`
  * Training went upto 200 steps, and step size (`log_step`) is 100, so there should be 0, 100, 200 step instances
    * `model_steps = [ 0, 200, 300]` -> `model_steps = [ 0, 100, 200]`

## Non-essential changes

* [x] Minor spelling/grammar changes
* [x] More detailed comments added wherever necessary
* [x] The final plot now plots according to the number of models in the list, and hence utilizes the figure space optimally.
  * `columns = 1 + len(models)` instead of hard-defining it as constant