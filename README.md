# Divvy bike share data analysis, January - May 2019

### Installation
Analysis was done with Python 3 and the following tools:
* Pandas
* Scipy
* Seaborn
* Matplotlib
* Jupyter Notebook
* Docker

**Step 1:**
Pull a Docker image of Anaconda 3, maintained by Continuum [here](https://hub.docker.com/r/continuumio/anaconda3).


```
$ docker pull continuumio/anaconda3
```

**Step 2:**
Run a Docker container and specify a local folder on your hard-drive as a volume by includin `C:\projects\some-project:/opt/notebooks` when executing `docker run`.


```
$ docker run -i -t -v C:\projects\some-project:/opt/notebooks -p 8888:8888 continuumio/anaconda3 /bin/bash -c  "/opt/conda/bin/conda install jupyter -y --quiet && mkdir -p /opt/notebooks && /opt/conda/bin/jupyter notebook --notebook-dir=/opt/notebooks --ip='*' --port=8888 --no-browser --allow-root"
```

The container can be shutdown and restarted with `docker start gallant_haslett`. Replace `gallant_haslett` with the name of the container.

### Dataset
This dataset contains anonymized trips data of Lyft bike sharing system(Bay Wheels), in the Bay Area from January 2019 to May 2019.

https://www.kaggle.com/jolasa/bay-area-bike-sharing-trips


#### Acknowledgements
This data was created with information obtained from Lift Bike Sharing Site: https://www.lyft.com/bikes/bay-wheels