# Install openscenegraph

## Install the latest Python and setup a new Python virtualenv

```bash
pkcon install -y git
pkcon install -y python3
pkcon install -y python3-pip
pkcon install -y python3-virtualenv
virtualenv-3 ~/python
source ~/python/bin/activate
echo "source ~/python/bin/activate" | tee -a ~/.bashrc
```

## Install the latest Ansible

```bash
pip install setuptools_rust wheel
pip install --upgrade pip
pip install ansible
```

## Install openscenegraph as a prerequisite

Follow these instructions to install a recent version of openscenegraph using Ansible automation: 

https://github.com/computate-org/computate_openscenegraph

## Install the openscenegraph ansible role

### Create a directory for the ansible role. 

```bash
install -d ~/.ansible/roles/computate.computate_openscenegraph
```

### Clone the openscenegraph ansible role. 

```bash
git clone git@github.com:computate-org/computate_openscenegraph.git ~/.ansible/roles/computate.computate_openscenegraph
```

## Run the openscenegraph ansible playbook to install the application locally. 

```bash
cd ~/.ansible/roles/computate.computate_openscenegraph
ansible-playbook install.yml
```

