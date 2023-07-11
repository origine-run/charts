# Origine Charts

This is an example charts repository.

### How It Works

I set up GitHub Pages to point to the `docs` folder. From there, I can
create and publish docs like this:

```console
$ helm create mychart
$ helm package mychart
$ mv mychart-0.1.0.tgz docs
$ helm repo index docs --url https://technosophos.github.com/tscharts
$ git add -i
$ git commit -av
$ git push origin master
```

From there, I can do a `helm repo add tscharts
https://technosophos.github.com/tscharts`

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

helm repo add origine-run https://origine-run.github.io/charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo
origine-run` to see the charts.

To install the `sample` chart:

    helm install my-sample origine-run/sample

To uninstall the chart:

    helm delete my-sample
