# Rancher Update

This action helps by updating a service in the Rancher 2 environment with kubernetes. 

# Examples

## Update service

```yaml
on:
push:
  branches:
  - master

jobs:
  release:
    runs-on: ubuntu-latest
    steps:
    - uses: yurisouza/rancher-2x-actions@2.0.2
      with:
        rancher_url: https://rancher.test.de
        rancher_token: ${{ secrets.RANCHER_BEARER_TOKEN }}
        cluster_id: ${{ secrets.CLUSTER_ID }}
        namespace: ${{ secrets.NAMESPACE }}
        deployment: ${{ secrets.DEPLOYMENT }}
        docker_image: nginx:latest
```
