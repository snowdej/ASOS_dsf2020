# Data Science Festival X ASOS
## Data Science Festival Workshop 7 November 2020 – Building a fashion recommender using Tensorflow/Keras with ASOS.

SEE THE /notebooks/README for the Demo notes

DSF_ASOS_Build_and_Deploy_a_Recommender_in_3_Hours_docker.ipynb file 
This is a docker version of the same ASOS DSF2020 repo - with a (hopefully) correct bit of typing during the demo.

You can save a new version of the recommender and it will be automatically served by tensorflow

The model output from TF serving can be seen via the same notebook - no need for command line on the host

You can switch between versions by using tags or version numbers, again see the notebook for details

To create a new version with different learning parameters or so on then amend the "model_path" to have a new number

Have a look at the models.config to see how this could work

The tf/server refreshes the config file every 15seconds (this can be changed in the docker-compose to be less frequent etc)

To use this you will at least need docker desktop and probably wsl2 containers for it

You can use vscode to clone the repo locally and right click the docker-compose file and choose UP

Visit http://localhost:8888

go to the notebook folder and open the DOCKER version of the notebook

password is hard coded to dsf2020 - see docker file for how this is done

The server runs on port 8501 - but you don't need to worry about that - you can get to the results from the notebook.

To get a different model and serve it - change the path parameter text model_path = "models/recommender/2"  to 3/4/5 etc as you play with the epochs/learning rates etc in the model 

You can just run every cell in the notebook and it will spit out a model that is on the same path as that being used by the server.

The server checks for new models every 15 seconds

look at notebooks\models\models.config to see how versions work

look at .buildfiles\docker-compose.yml to see how the model file is used in docker startup 

The last few cells on the notebook show how to access the latest version, a named version or a version number

