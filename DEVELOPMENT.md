# Development

This repository serves as a Helm chart repository, set up using this guide:
https://github.com/helm/helm/blob/master/docs/chart_repository.md.

## Generate package index file

1. Build your package tgz (`helm package`).
2. Copy that tgz to the docs/ directory in this project.
3. Run `helm repo index docs --url https://cyberark.github.com/helm-charts`
4. Commit and push your changes.
