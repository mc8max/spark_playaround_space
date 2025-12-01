## Setup
Before you start, please install dependencies through uv.

```sh
uv sync
```

If you would like to test with a local spark build, perform the following:
```sh
export SPARK_HOME=/Users/mc8max/tutorials/spark/spark           
export PYSPARK_PYTHON=$(which python)
export PY4J_ZIP=$(ls "$SPARK_HOME"/python/lib/py4j-*.zip | head -n1)
export PYTHONPATH="$SPARK_HOME/python:$PY4J_ZIP:$PYTHONPATH"
```

## Notebook: issue_partitioning.ipynb
The notebook shows performance issue when select data from latest partition of a table.