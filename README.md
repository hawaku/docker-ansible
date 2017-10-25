# Ansible Docker Container

## Usage

```shell
docker run -it --rm -v ${PWD}:/playbooks -w /playbooks hawaku/ansible
```

You can also get a specific version of Ansible.

```shell
docker run -it --rm -v ${PWD}:/playbooks -w /playbooks hawaku/ansible:<version>
```

See our [Docker tags](https://hub.docker.com/r/hawaku/ansible/tags/) for available versions.

For example: ping all your nodes

```shell
docker run -it --rm -v ${HOME}/.ssh:/root/.ssh:ro -v ${PWD}:/playbooks -w /playbooks hawaku/ansible ansible -i hosts all -m ping
```

Or to run from a bash session

```shell
docker run -it --rm -v ${HOME}/.ssh:/root/.ssh:ro -v ${PWD}:/playbooks -w /playbooks hawaku/ansible bash
root@29867ac2540f:/playbooks# ansible -i hosts all -m ping
```
