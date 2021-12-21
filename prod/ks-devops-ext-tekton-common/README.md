# Tekton common manifests

Why do we host those manifests? Because they are common enough, they need to be placed in a public place for others to reuse.

## Common tasks

Below are some common tasks that can be reused by others.

| Manifest             | Description                                                                                                                                                                                                                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| git-clone            | Copied from [here](https://github.com/tektoncd/catalog/blob/main/task/git-clone/0.5/git-clone.yaml).                                                                                                                                                                                         |
| github-set-status    | Copied from [here](https://github.com/tektoncd/catalog/blob/main/task/github-set-status/0.3/github-set-status.yaml).                                                                                                                                                                         |
| goreleaser           | Mainly copied from [here](https://github.com/tektoncd/catalog/blob/main/task/goreleaser/0.2/goreleaser.yaml). But we have changed it for providing `docker` support.                                                                                                                         |
| goreleaser-and-trivy | Mainly copied from [here](https://github.com/tektoncd/catalog/blob/main/task/goreleaser/0.2/goreleaser.yaml) and [here](https://github.com/tektoncd/catalog/blob/main/task/trivy-scanner/0.1/trivy-scanner.yaml). But we have changed it for providing `docker` and `trivy-scanner` support. |
