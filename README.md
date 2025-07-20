# Cheat Sheets - often used.

## [Ansible](./DevOps/ansible.md)

Command | Explanation
--------|-------------
`ansible all -m gather_facts --limit ux-vm1` | Gather facts for a single machine.
`ansible all -m ping`<br>`ansible "app*" -m ping`<br>`ansible 'prod:!db' -m ping`<br>`ansible all -i inventory -m ping`<br>`ansible 'prod:!db' -a uptime`<br>`ansible 'prod' -a 'uname -a'` | Ping all hosts in the inventory.<br>-m = MODULE_NAME<br> -a =  MODULE_ARGS<br>https://docs.ansible.com/ansible/2.9/user_guide/modules.html
`ansible all -m apt`<br>`ansible all -m apt -a update_cache=true --become`<br>`ansible all -m apt -a update_cache=true  --ask-become-pass`<br>`ansible all -m apt -a update_cache=true --become --ask-become-pass`<br>`ansible prod -m -s -a "free \| grep -i swap"`<br>`ansible prod -m command -a "free" \| grep -i swap`<br>`ansible prod -m shell -a "free \| grep -i swap"` | Run commands on the remote nodes.
`ansible-playbook systems.yml --syntax-check`<br>`ansible-playbook systems.yml --list-hosts`<br>`ansible-playbook systems.yml --list-tasks`<br>`ansible-playbook systems.yml --list-tags`<br>`ansible-playbook systems.yml --check`<br>`ansible-playbook systems.yml --step` | Syntax check.

## [Git](./DevOps/ansible.md)

Command | Explanation
--------|-------------
`git branch -d <branch>` | Delete a branch locally.
`git push origin --delete <branch>` | Delete a remote branch.
`git pull --rebase origin <branch>` | Fetch and reapply commits from a remote repository.

## [Kubernetes](./DevOps/git.md)

| Command                                                                                                   | Explanation                                                                                                      |
| --------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `k config set-context --current --namespace=<desired-namespace>`                                          | Switch namespace.                                                                                                |
| `k get all`                                                                                               | All that is running in a current namespace (PODS, Services, Deployments, etc.)                                   |
| `k get kustomizations`                                                                                    | Get Flux reconciliation status.                                                                                  |
| `k describe kustomizations NAME`                                                                          | See the reconciliation status conditions and events. https://fluxcd.io/flux/components/kustomize/kustomizations/ |
| `flux get kustomizations`                                                                                 | Get applied kustomizations.                                                                                      |
| `flux reconcile kustomization apps`                                                                       | Enforce reconciliation.                                                                                          |
| `k get customresourcedefinitions.apiextensions.k8s.io`                                                    | Get Custom Resource Definitions.                                                                                 |
| `k get customresourcedefinitions.apiextensions.k8s.io kustomizations.kustomize.toolkit.fluxcd.io -o yaml` | Specification of the Kustomization custom resource in yaml.                                                      |
| `k kubectl get events --sort-by=.metadata.creationTimestamp`                                              | Check Kubernetes events for detailed logs.                                                                       |

## [Windows Terminal](./Windows/windows-terminal-panes.md)

Command | Explanation
--------|-------------
`ALT-SHIFT-+` | Split pane vertically.
`ALT-SHIFT--` | Split pane horizontally.
`CTRL-SHIFT-w` | Close pane.