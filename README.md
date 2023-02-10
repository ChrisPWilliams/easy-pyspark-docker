# Easy setup for Pyspark using docker

Requirements:
- Docker
- IDE of your choice
- Recommend attempting to pip install or conda install pyspark on your local machine, so that your IDE will be able to lint correctly - you don't need environment variables or hadoop set up to do this

To set up, open your IDE from Anaconda and run 'conda install -c conda-forge pyspark' - this will allow your IDE to highlight properly when you use pyspark.

Then run 'docker compose run --rm pyspark' - this will set up a container with pyspark, bind the local directory from your machine to the working directory of the container, and then open a bash terminal in the container.

Store python scripts in the scripts folder, and data in the data folder.

When you want to run a script, just navigate into the scripts folder with 'cd scripts' and then run them as normal e.g. 'python3 mypysparktest.py'.

You will also have access to the pyspark shell with the 'pyspark' command.

If you want to open additional terminals into the container, just open a new terminal window, find the container id in docker desktop, and run 'docker exec -it <your_container_id> /bin/bash'.

When you have exited all terminals, the container will automatically shut down