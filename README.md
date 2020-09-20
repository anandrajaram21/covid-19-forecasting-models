# COVID-19 Forecasting Models

## Steps to run on a local machine (using Docker)

**Step 1** - Pull the Docker image using the following command

```
docker pull anandrajaram21/jupyter-environments:deep-learning
```

**Step 2** - Run the following commands to start the container, and run Jupyter Lab from inside of it.

```
docker run -it --name deep-learning -v path/to/folder/you/want/to/mount:/home/jovyan/work -p 8888:8888 anandrajaram21/jupyter-environments:deep-learning bash
```

This command will open up a shell in the Docker container. Now run the command `jupyter lab` to start a Jupyter Lab server in the container, and click on the link shown in the terminal.

After you are done, run the following command to stop the Docker container

```
docker stop deep-learning
```

If you want to access the container again in the future, just run the following commands in the terminal

```
docker start deep-learning
docker exec -it deep-learning bash
```

