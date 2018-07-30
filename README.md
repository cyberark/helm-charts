# helm-charts

CyberArk [Helm](https://github.com/helm/helm) charts repository.

## Download charts from this repository

To use charts from this repository, add the repository to Helm:

```sh-session
$ helm repo add cyberark https://cyberark.github.io/helm-charts
"cyberark" has been added to your repositories

$ helm repo update
Hang tight while we grab the latest from your chart repositories...
...Skip local chart repository
...Successfully got an update from the "cyberark" chart repository
...Successfully got an update from the "stable" chart repository
Update Complete. ⎈ Happy Helming!⎈
```

## View all CyberArk charts

```sh-session
$ helm search -r 'cyberark/*'
NAME                CHART VERSION	APP VERSION DESCRIPTION
cyberark/conjur-oss 0.1.0                      A Helm chart for CyberArk Conjur
```

## Inspect and install a chart

```sh-session
$ helm inspect cyberark/conjur-oss
apiVersion: v1
description: A Helm chart for CyberArk Conjur
home: https://www.conjur.org
...

$ helm install \
  --set dataKey="$(docker run --rm cyberark/conjur data-key generate)" \
  cyberark/conjur-oss
NAME:   full-swan
LAST DEPLOYED: Mon Jul 30 17:40:28 2018
NAMESPACE: conjur
STATUS: DEPLOYED
...
```
