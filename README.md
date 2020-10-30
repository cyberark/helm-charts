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

### Helm 3+

```sh-session
$ helm search repo cyberark
NAME                    CHART VERSION   APP VERSION     DESCRIPTION                     
cyberark/conjur-oss     2.0.1                           A Helm chart for CyberArk Conjur

$ helm search repo -l cyberark/conjur-oss
NAME                    CHART VERSION   APP VERSION     DESCRIPTION                     
cyberark/conjur-oss     2.0.1                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     2.0.0                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     1.3.8                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     1.3.7                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     1.3.6                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     1.3.5                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     1.3.4                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     0.2.1                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     0.2.0                           A Helm chart for CyberArk Conjur
cyberark/conjur-oss     0.1.0                           A Helm chart for CyberArk Conjur
```

### Helm 2
```sh-session
$ helm search -r 'cyberark/*'
NAME                CHART VERSION	APP VERSION DESCRIPTION
cyberark/conjur-oss 2.0.1                      A Helm chart for CyberArk Conjur
```

## Inspect and install a chart

### Helm 3+
```sh-session
$ helm inspect chart cyberark/conjur-oss
apiVersion: v1
description: A Helm chart for CyberArk Conjur
home: https://www.conjur.org
...
$ helm install conjur-oss \
  --set dataKey="$(docker run --rm cyberark/conjur data-key generate)" \
  cyberark/conjur-oss
NAME: conjur-oss
LAST DEPLOYED: Mon Dec 23 11:40:04 2019
NAMESPACE: default
STATUS: deployed
REVISION: 1
...
```

### Helm 2
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

## Contributing

We welcome contributions of all kinds to this repository. For instructions on
how to get started and descriptions of our development workflows, please see our
[contributing guide](CONTRIBUTING.md).

## License

This repository is licensed under Apache License 2.0 - see [`LICENSE`](LICENSE) for more details.
