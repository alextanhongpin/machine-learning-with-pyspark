
# Pyspark

## Installation

WARN: This does not work. Do the manual installation instead.
```
$ brew install spark
$ pip3 install pyspark
```

Download spark-2.4.4 [here](https://www.apache.org/dyn/closer.lua/spark/spark-2.4.4/spark-2.4.4-bin-hadoop2.7.tgz).


Unzip it and move to your opt folder. You might need sudo:
```
$ tar -xzf spark-2.4.4-bin-hadoop2.7.tgz

$ mv spark-2.4.4-bin-hadoop2.7 /opt/spark-2.4.4
```
Create a symbolic link so that you can use multiple spark versions:

```
$ ln -s /opt/spark-2.4.4 /opt/spark̀
```

Set the path in `.zshrc`:

```
export SPARK_HOME=/opt/spark
export PATH=$SPARK_HOME/bin:$PATH
```

# Pyspark configuration for Jupyter notebook.

In your `.zshrc` or `.bash_profile`:

```.zshrc
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
export PYSPARK_PYTHON=/usr/local/bin/python3
```
