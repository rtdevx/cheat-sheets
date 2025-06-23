# Cheat Sheets

## [Ansible](./DevOps/ansible.md)

Command | Explanation
--------|-------------
`ansible all -m gather_facts --limit ux-vm1` | Gather facts for a single machine.

## [Kubernetes](./DevOps/kubernetes.md)

Command | Explanation
--------|-------------
`k config set-context --current --namespace=<desired-namespace>` | Switch namespace.
`k get kustomizations` | Get Flux reconciliation status.
`k describe kustomizations NAME` | See the reconciliation status conditions and events. https://fluxcd.io/flux/components/kustomize/kustomizations/
`k get customresourcedefinitions.apiextensions.k8s.io` | Get Custom Resource Definitions.
`k get customresourcedefinitions.apiextensions.k8s.io kustomizations.kustomize.toolkit.fluxcd.io -o yaml` | Specification of the Kustomization custom resource in yaml.

## [Windows Terminal](./Windows/windows-terminal-panes.md)

Command | Explanation
--------|-------------
`ALT-SHIFT-+` | Split pane vertically.
`ALT-SHIFT--` | Split pane horizontally.
`CTRL-SHIFT-w` | Close pane.