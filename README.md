## Experimenting with Luigi
[Luigi](https://github.com/spotify/luigi) is a Python module that helps you build complex pipelines of batch jobs, handle dependency resolution, and create visualizations to help manage multiple workflows.

This code was initially based on [a tutorial on luigi](https://towardsdatascience.com/a-tutorial-on-luigi-spotifys-pipeline-5c694fb4113e) and [how to build a data processing pipeline using Luigi](https://www.digitalocean.com/community/tutorials/how-to-build-a-data-processing-pipeline-using-luigi-in-python-on-ubuntu-20-04).

The goal of this work is build a pipeline that
* can extract Premier League Fantasy Football data from an API and write it to BigQuery
* ran a data validation check on the raw data
* transform it to the desired output

## Installation instructions

```commandline
python -m virtualenv env
. env/bin/activate
```

Please note the name of the virtual environment is referenced later and if you use a name other than `env` the command to run the Luigi scheduler will need to be updated.

## Run hello world example

```commandline
cd
python -m luigi --module main HelloLuigi --local-scheduler
```
**TODO break down cli args and add documentation

## Run the Luigi Scheduler

```commandline
sudo sh -c ". env/bin/activate ;luigid --port 8082"
```

```
# Run as background task
sudo sh -c ". env/bin/activate ;luigid --background --port 8082"
```

## Notes for future me

* [Luigi Config](https://www.promptworks.com/blog/configuring-complex-luigi-pipelines/)