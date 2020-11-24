# Data Science Festival X ASOS
## Data Science Festival Workshop 7 November 2020 – Building a fashion recommender using Tensorflow/Keras with ASOS.

First we will build a recommender model together in Google Colab. Then we will deploy the model into production.


DSF_ASOS_Build_and_Deploy_a_Recommender_in_3_Hours_docker.ipynb file 
This is a docker version of the same ASOS DSF2020 repo - with a (hopefully) correct bit of typing during the demo.

You can save a new version of the recommender and it will be automatically served by tensorflow

The model output from TF serving can be seen via the same notebook - no need for command line on the host

You can switch between versions by using tags or version numbers, again see the notebook for details

To create a new version with different learning parameters or so on then amend the "model_path" to have a new number

Have a look at the models.config to see how this could work

The tf/server refreshes the config file every 15seconds (this can be changed in the docker-compose to be less frequent etc)




