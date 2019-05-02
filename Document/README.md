# IST718 Project

### The following below is so important and you could not want to miss.

**How to run these code and models on `notebook.acuna.io`?

Because there are too many files, you need 

- First, zip/compress "IST718_project" folder to "IST718_project.zip"
- Second, upload the zip file to notebook.acuna.io, and wait
- Third, find the file "unzip_file.ipynb" in "IST718_project" folder and upload it to notebook.acuna.io, as well
- Fourth, keep this two file you upload in same directory.
- Fifth, run "unzip_file.ipynb" on notebook.acuna.io, and wait
- Sixth, you already have these awesome code and models online, enjoy.

This notebook contains 6 parts.

- A little cleaning.
- Change some columns to percentage, split data to training, validation, test.
- Create dummy variable
- Logistic Regression, Random Forest, Gradient Boosted Trees.
- Inference
- Cluster

** Because we use grid search to tune our models, **it will need too much time to fitting these 3 models.** You may get stuck into this long time fitting. You could try Logistic Regression, which is relative faster.

So we have saved all the models we already fitted, and the same for all best models. They are saved in `models` directory.

In the fitting process in this code, the models are saved in `temp/models` directory, just for playing. You can also loaded the models we already fitted from `models/lr`, `models/rf`, `models/gbt`, if you want to check all the accuracies.

In the evaluate process, the models are loaded from `models/best_models`, which could save you much time.

** So, you may skip the fitting process, directly run the evaluate process for different model types.

It's like:

> lr_best_model = PipelineModel.load("models/best_models/lr_best_model")

> evaluator.evaluate(lr_best_model.transform(testing_df))

** Because it loads models we already trained, **the performance may have some difference.**

The Inference and cluster process is fast, it is suggested to run it.

### Explanation for `temp` directory.

It is like a playground.

No need to worry the important data and models used in other notebook will be re-write, appended, or changed by some running error.

- The **raw data** are saved in `raw_data` directory.

- The **cleaned data** are saved in `data` directory, which will be used by other .ipynb files.

- The **fitted models** are saved in `models` directory.

- The **dataset and models created in this notebook** are saved in `temp/data` directory. Because we assumed you run this code only for checking the code, It is a temp directory, saving temporary data and models.
