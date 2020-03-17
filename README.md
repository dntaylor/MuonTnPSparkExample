# MuonTnPSparkExample
An example repository showing the usage of Muon POG tag-and-probe fits using Apache Spark

## Interactive notebook

Follow the instructions in [MuonTnP.ipynb](MuonTnP.ipynb).
This notebook uses [swan.cern.ch](swan.cern.ch) to connect to the Apache Spark clusters at CERN.

More details on CERN's Apache Spark can be found [here](https://hadoop-user-guide.web.cern.ch/hadoop-user-guide/spark/Using_Spark_on_Hadoop.html).

## Commandline

There are a couple of ways you can run. Either connect to the edge node or directly on lxplus.

### Edge node
Connect to the hadoop edge node:

```bash
ssh it-hadoop-client
```

Setup the environment:

```bash
source /cvmfs/sft.cern.ch/lcg/views/LCG_96bpython3/x86_64-centos7-gcc8-opt/setup.sh
source hadoop-setconf.sh analytix
```

### Lxplus

Setup the environment:

```bash
source /cvmfs/sft.cern.ch/lcg/views/LCG_96bpython3/x86_64-centos7-gcc8-opt/setup.sh
source /cvmfs/sft.cern.ch/lcg/etc/hadoop-confext/hadoop-swan-setconf.sh analytix
```

### Lxplus (k8s)

In case you do not have permission to submit to the analytix cluster, you can use `k8s`.

```bash
source /cvmfs/sft.cern.ch/lcg/views/LCG_96bpython3/x86_64-centos7-gcc8-opt/setup.sh
source /cvmfs/sft.cern.ch/lcg/etc/hadoop-confext/k8s-swan-setconf.sh k8s analytix
```

### Flatten

Run the flattening step:

```bash
python tnp_spark_parquet.py
```
