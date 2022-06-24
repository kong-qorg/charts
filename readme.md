 Qualys Helm charts

A collection of Helm charts for deploying Qualys product in Kubernetes.

## Installing charts

### Helm Charts

This repository contains these Helm charts.
Chart | Description
----- | -----------
cssensor | Deploy Qualys container security sensor. [chart](charts/cssensor)

### Adding chart repo

```console
$ helm repo add qualys https://TBD.github.io/qualys-helm/
$ helm search repo qualys/cssensor
```

### Versioning

Helm charts for officially released product are published from the release branch of the repository.
The main branch is used for the charts of the product in the development. 
Typically the charts in the main branch are published with the alpha, beta or rc tag. They can be discovered with --devel option.

```console
$ helm search qualys qualys/cssensor -l
NAME          	CHART VERSION	APP VERSION	DESCRIPTION
qualys/cssensor	1.0.2        	1.15   	  Helm chart for CS Sensor services
qualys/cssensor	1.0.1        	1.14      	Helm chart for CS Sensor services
qualys/cssensor	1.0.0        	1.13      	Helm chart for CS Sensor services

...
...

$ helm search repo qualys/cssensor --devel
NAME            	CHART VERSION	APP VERSION	DESCRIPTION
qualys/cssensor
1.0.2-b1     	1.15-b1   	Helm chart for CS Sensor services
...
...
```

### Deploy in Kubernetes

- Create the qualys namespace.
```console
$ kubectl create namespace qualys
```


## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ helm delete my-release
```
