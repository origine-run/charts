# Origine Charts

## Introduction
This is a collection of charts for Origine. They are used internally and also publicly available

## Usage
- [Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

- Once Helm has been set up correctly, add the repo as follows:
```
$ helm repo add origine-run https://origine-run.github.io/charts
```

- If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. 

- You can then run `helm search repo origine-run` to see the charts.

- To install a chart called `sample`, use:
```
$ helm install my-sample-chart origine-run/sample
```

- To uninstall the chart:
```
$ helm delete my-sample-chart
```

## Contribution
- This repository is set up as a GitHub Page, Github page point to the `docs` folder.

- Init a new chart
```
$ helm create my-chart
```
- Work on the chart

- Package the chart
```
$ helm package my-chart
```

- Move chart to `docs` 
```
$ mv my-chart-x.y.z.tgz docs
```

- Update repository index
```
$ helm repo index docs --url https://origine-run.github.io/charts
```

- Commit and Push
```
$ git add -i
$ git commit -av
$ git push origin master
```

