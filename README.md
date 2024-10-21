# capabilities (gitops hub and workers template)
TODO

## Testing

### Option 1: ansible-navigator
Recommended way of running tests.

#### prerequisites
* ansible-navigator >=24.2.0

#### run
```bash
ansible-navigator --eei ee-kube-hub-init-tools:latest run tests/test-all-kustomization-builds-playbook.yaml -m stdout
```

### Option 2: ansible-playbook
Based on experience getting all of these dependencies correct can be a pain. Option 1 is recommended.

#### prerequisites
* Python >=3.9.6
* ansible >=2.15.12
* [helm](https://github.com/helm/helm) >=3.16
* [kustomize](https://github.com/kubernetes-sigs/kustomize) >=5.50
* [Open Cluster Management PolicyGenerator kustomize plugin](https://github.com/open-cluster-management-io/policy-generator-plugin) >=1.15.0

#### run
```bash
ansible-playbook tests/test-all-kustomization-builds-playbook.yaml
```
