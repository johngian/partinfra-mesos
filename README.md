# Participation infrastructure
## Mesos cluster

This ansible role tracks our effort to build a Mesos cluster in order to facililate [**Participation Infrastructure
team's**](https://wiki.mozilla.org/Participation/Infrastructure) needs for computing resources.

## Vagrant local provisioning
### Requirements
In order to test this setup locally you need to install ``ansible`` and ``vagrant`` to your host system:

* [Ansible installation docs](http://docs.ansible.com/intro_installation.html)
* [Vagrant installation docs](https://docs.vagrantup.com/v2/installation/)

Our ``Vagrantfile`` launches 6 ``ubuntu/trusty64`` dev instances:

* ``mesos-master[1..3]``
* ``mesos-slave[1..3]``

We also provide ``hosts-dev.dist`` inventory file targeting the VMs described above.

### Provision

To test this cluster locally follow these steps:

* ``$ cd partinfra-mesos``
* ``$ vagrant box add ubuntu/trusty64``
* ``$ vagrant up``
* ``$ ansible-playbook playbook.yml -i hosts-dev.dist``

If all tasks are completed succesfully you can visit the following web services:
* master[1..3]
  * **Local IPs**: 192.168.60.4, 192.168.60.5, 192.168.60.6
  * **Port 5050**: Mesos web interface
  * **Port 8080**: Marathon web interface
