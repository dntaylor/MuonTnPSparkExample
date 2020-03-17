# MuonTnPSparkExample
An example repository showing the usage of Muon POG tag-and-probe fits using Apache Spark

## Interactive notebook

Follow the instructions in [MuonTnP.ipynb](MuonTnP.ipynb).
This notebook uses [swan.cern.ch](swan.cern.ch) to connect to the Apache Spark clusters at CERN.

More details on CERN's Apache Spark can be found [here](https://hadoop-user-guide.web.cern.ch/hadoop-user-guide/spark/Using_Spark_on_Hadoop.html).

## Commandline

Connect to the hadoop edge node:

```bash
ssh it-hadoop-client
```

Setup the environment:

```bash
source /cvmfs/sft.cern.ch/lcg/views/LCG_96python3/x86_64-centos7-gcc8-opt/setup.sh
source hadoop-setconf.sh analytix
```

Run the flattening step:

```bash
python tnp_spark_parquet.py
```
