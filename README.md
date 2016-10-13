##<span style="color:cyan">Simple Ansible Vagrant Docker & Web Provisioner</span>

###<span style="color:darkcyan">What is it for?</span>

This simple test is for use with a vagrant instance. This is a simpler version
of the [Vagrant__docker_web_selector](https://github.com/twistedgitbox/Vagrant_docker_web_selector.git)

This program loads a vagrant guest, and using ansible, git clones the
appropriate repos to `/web` and `/docker` on `/vagrant` directory of the
Vagrant guest.

###<span style="color:darkcyan">Instructions</span>

**To run**:
- cd into folder
- type 'vagrant up'
- select the bridge for your network (usually `eth01`)
- After installation concludes, go to `localhost:8000` or the IP address of your
  Vagrant guest at port 8000.

**To change repositories to load and install:**
- cd into folder
- edit `playbook.yml`
- find the section `vars:`

**For repositories to place on *web* folder**:
the repository is downloaded into the
`/vagrant/web` folder on the Vagrant guest.

**For repositories to load your *Docker* container**:
Replace the github URL with the URL of your project after `gitWebRepo`.
The repository will be cloned into the `/vagrant/docker` folder on the Vagrant guest. The docker-container is then started using the `docker-compose.yml` file in the folder.

(*note: this does require a docker-compose folder to exist and to be in the root
directory of the repository*)







