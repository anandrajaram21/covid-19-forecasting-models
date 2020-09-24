# COVID-19 Forecasting Models

## Steps to run on a local machine (using Docker) (recommended)

**Step 1** - Pull the Docker image using the following command

```
docker pull anandrajaram21/covid-19:latest
```

**Step 2** - Run the following commands to start the container, and run Jupyter Lab from inside of it.

```
docker run -it --name covid -v path/to/folder/you/want/to/mount:/home/jovyan/work -p 8888:8888 anandrajaram21/covid-19:latest bash
```

This command will open up a shell in the Docker container. Now run the command `jupyter lab` to start a Jupyter Lab server in the container, and click on the link shown in the terminal.

After you are done, run the following command to stop the Docker container

```
docker stop covid
```

If you want to access the container again in the future, just run the following commands in the terminal

```
docker start covid
docker exec -it covid bash
```

## Alternative (Using python venv)

**Step 1** - Run the following command to create a python3 venv

```
python3 -m venv covid_env
```

**Step 2** - Activate the venv, and run the following command to install all dependencies

```
pip install -r requirements.txt
```

**Step 3** - Run the command `jupyter lab` in the terminal to fire up a jupyter lab server.

Please make sure that you have statsmodels version 0.12.0 or greater installed, as the code will not run without it. (The docker image and requirements.txt file already has the right dependencies, so if you are following the instructions here to set up your environment, you can ignore this warning)
