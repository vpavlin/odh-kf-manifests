# odh-kf-manifests
Experimental repo for additional components originally available in Open Data Hub added on top of Kubeflow

## Usage

Download kfctl 1.0 RC (kfctl 0.7 has a problem with downloading the manifests - https://github.com/kubeflow/kubeflow/issues/4642)

```
curl -O -L https://github.com/kubeflow/kfctl/releases/download/v1.0-rc.1/kfctl_v1.0-rc.1-0-g963c787_linux.tar.gz
# Unpack and copy to bin/ location
```

Full Kubeflow:

Deploys most of the 

```
kfctl build -f kfdef/kfdef_opendatahub.yaml
kfctl apply -f kfdef/kfdef_opendatahub.yaml
```

Only Spark Operator

```
kfctl build -f kfdef/kfdef_opendatahub_spark_only.yaml
kfctl apply -f kfdef/kfdef_opendatahub_spark_only.yaml
```
