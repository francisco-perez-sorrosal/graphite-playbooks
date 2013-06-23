Usage
=====

To deploy a graphite server you must create an inventory file with this format:

[graphiteservers]
myserver1
myserver2
...

A sample file called `openhouse` is provided.

Then, invoke the playbook site.xml for creating the graphite server installation and setup:

`ansible-playbook -i inventory-file --extra-vars "remote_user=XXX" -v -K site.yml`

You have to substitute XXX by the remote user with permissions to install stuff in the remote host.

There are also playbooks to stop and start the graphite server if necessary:

`ansible-playbook -i inventory-file -v -K stop-graphite.yml`

`ansible-playbook -i inventory-file -v -K start-graphite.yml`

NOTE: It has been tested with Fedora Linux and with an OpenStack-based VM framework



