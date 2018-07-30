# Development

This repository serves as a Helm chart repository, set up using this guide:
https://github.com/helm/helm/blob/master/docs/chart_repository.md.

## Generate package index file

1. Build your package tgz (`helm package`).
2. Copy that tgz to the charts/ directory in this project.
3. `cd charts/`
4. Run `helm repo index --merge .`
5. Commit and push your changes.
