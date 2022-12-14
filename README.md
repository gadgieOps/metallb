Ansible Role: Deploy metallb
=========

Deploys metallb on a kubernetes control plane node. Based on installation documentation as per: https://metallb.universe.tf/installation/


Role Variables
--------------

~~~
version: "0.13.7"
~~~
Version of metallb to deploy

~~~
ipvs: true
~~~
Set if ipvs is enabled in kube-proxy. (This will set strictArp: true)

~~~
remove: false
~~~
Will remove metallb rather than deploy it when set to true

Example Playbook
----------------
~~~
- name: Deploy metallb
  hosts: control-plane-node
  become: true
  roles:
  - role: gadgieOps.metallb
~~~

License
-------

MIT

Author Information
------------------

Authored by gadgieOps
